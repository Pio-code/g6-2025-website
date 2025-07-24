---
header_img: assets/images/folium_map.webp
header_title: "Data"
header_type: hero
layout: default
title: "Data"
---

### Species Distribution Modeling Workflow using Maxent

In this report, we describe the complete workflow we have developed for building and projecting species distribution models (SDM) based on Maxent. Maxent is a machine learning algorithm that creates a fitness map for a species. It assumes that the species could be found anywhere and then uses the locations to understand the environmental constraints that limit its distribution, contrasting the conditions with the background environment (represented by pseudo absence points).


### Study Area Definition

Our first step involved precisely defining our study area, which corresponds to "core" Europe. Starting from a global shapefile, we selected all national polygons of the European Union and then applied a bounding box to exclude the easternmost portions of Russia. Subsequently, we merged all polygons into a single continuous geometry and transformed them into the Lambert Azimuthal Equal Area (LAEA) system. This step is crucial because in LAEA projection, each raster cell represents the same surface area on the ground, eliminating areal distortions that would otherwise compromise the spatial comparability of our analyses.


### Pre-processing Current Environmental Variables

With the study area defined, we proceeded to pre-process the current environmental variables. Each raster is cropped to the European extent, masked to eliminate pixels outside the exact boundaries, and finally projected to LAEA with 1 km resolution, using interpolation for continuous data and nearest neighbor for categorical data (such as land use). At this point, we calculate the Variance Inflation Factor (VIF) for all covariates. This approach minimizes multicollinearity and provides us with a final stack of predictors. In total, we obtained 11 bioclimatic variables, 1 variable representing elevation, and one categorical variable for land cover.


### Future Data Preparation

The next step concerns the preparation of future data. For each socio-economic scenario (SSP2 and SSP3) and for the three time horizons (2050, 2070, 2100), we apply exactly the same "recipe" of cropping, masking, projection, and resampling already used for current data.


### Modeling and Prediction with Maxent

For training, we use the ENMeval package in combination with dismo, setting up a grid search across various feature classes (L, LQ...) and different regularization multiplier values. The optimal configuration is selected through cross-validation, balancing model complexity and predictive capacity. We leverage the native terra::predict() function, which automatically handles tiling and parallelism.


### Managing Presence and Pseudo-absence (Background) Points

In parallel, we carefully manage presence and pseudo-absence (background) points. From the original occurrences extracted from GBIF, we take only those that fall reduce them the EU mask, reproject to LAEA, eliminate points that fall in cells with missing values, and reduce to one point per cell to mitigate potential sampling bias. For the background, we define a circular buffer for each species whose radius corresponds to the maximum dispersal distance known in the literature. Within this buffer, we sample up to 10,000 points, ensuring we have at least 5,000 available points for statistical stability.


### Thresholds and Binarization

After obtaining the continuous suitability raster, we manually calculate the MaxTSS threshold to define a suitability threshold. 
Habitat Mask Application
We also apply a habitat mask to our predictions. through an association of each species for the preference of the habitats present in the land cover, i.e. cropland, forest, grassland, urban area, infertile land and water, was multiplied by each value of continuous suitability, 1, for the suitable and preferred habitats, 0.8 for the mostly unsuitable habitats, and 0.01 for the absolutely unsuitable ones.


### MESS Mask Integration

Finally, we integrate the MESS (Multivariate Environmental Similarity Surface) mask to exclude from predictions areas that are ecologically too dissimilar from the training dataset. This additional environmental filter allows us to obtain even more robust models by applying two levels of filtering habitat and environmental analogy to our projections.

