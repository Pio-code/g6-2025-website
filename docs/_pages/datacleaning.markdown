---
layout: default
title: "Data Cleaning"
---

# Data Cleaning
The species occurrence records obtained from GBIF were consolidated into a single CSV file and subjected to a data cleaning process.  
The cleaning process included the following steps:
+ removal of data fields not relevant to the analysis;
+ validation of date fields;
+ removal of records with a coordinate uncertainty greater than 5.000 meters;
+ application of a geographic bounding box encompassing the European continent, and removal of any occurrences falling outside this defined spatial extent;
+ removal of species represented by fewer than 20 occurrence records.