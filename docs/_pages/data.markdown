---
header_img: assets/images/folium_map.webp
header_title: "Data"
header_type: hero
layout: default
title: "Data"
---

# Collection

### Species Occurrences
The **species occurrence data**, including **geographic coordinates** of individual observations, were obtained from the [Global Biodiversity Information Facility (GBIF)](https://www.gbif.org/).  
As GBIF enforces a delay between successive download requests (each corresponding to a single species) we implemented a **polling mechanism** to automate the process.  
This approach enabled continuous querying and data retrieval without manual intervention, effectively eliminating idle time and improving the overall efficiency of the data acquisition workflow.

### Habitat
Information on species' **conservation status** and **habitat preferences** was obtained from [International Union for Conservation of Nature (IUCN) Red List](https://www.iucnredlist.org/), where the relevant data are provided in individual documents.  
To facilitate large-scale data collection and avoid the need for manual downloading, we developed a custom **web scraper** tailored to the structure of the IUCN website.  
This automation significantly streamlined the process, enabling efficient and systematic retrieval of multiple files.

### Climate
**Climatic data** were obtained from [WorldClim](https://www.worldclim.org/), which provides high-resolution global climate layers.  
As the data are readily accessible through the platform, they were downloaded directly via standard web access.

# Cleaning

The species occurrence records obtained from GBIF were consolidated into a single file and subjected to a **data cleaning** process.  
The cleaning process included the following steps:
+ removal of data fields not relevant to the analysis;
+ validation of date fields;
+ removal of records with a coordinate uncertainty greater than 5.000 meters;
+ application of a geographic bounding box encompassing the European continent, and removal of any occurrences falling outside this defined spatial extent;
+ removal of species represented by fewer than 20 occurrence records.

# Enrichment

To get an estimate of the species' **maximum dispersal distance**, we implemented a streamlined approach inspired by **retrieval-augmented generation**, though without the use of embedding-based similarity search, as the queries were predefined and not user-generated.  
Each query targeted a particular species, and the corresponding context was extracted from species-specific documents.  
Relevant sections of text were identified and isolated using natural language processing techniques.  
The query and its extracted context were then jointly submitted to a **LLM**, from which we retrieved the desired output.