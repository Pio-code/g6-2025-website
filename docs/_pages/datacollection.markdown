# Data Collection

## Species Occurrences
The species occurrence data, including geographic coordinates of individual observations, were obtained from the [Global Biodiversity Information Facility (GBIF)](https://www.gbif.org/).  
As GBIF enforces a delay between successive download requests (each corresponding to a single species) we implemented a polling mechanism to automate the process.  
This approach enabled continuous querying and data retrieval without manual intervention, effectively eliminating idle time and improving the overall efficiency of the data acquisition workflow.

## Habitat
Information on species' conservation status and habitat preferences was obtained from [International Union for Conservation of Nature (IUCN) Red List](https://www.iucnredlist.org/), where the relevant data are provided in individual PDF documents.  
To facilitate large-scale data collection and avoid the need for manual downloading, we developed a custom web scraper tailored to the structure of the IUCN website.  
This automation significantly streamlined the process, enabling efficient and systematic retrieval of multiple PDF files.

## Climate
Climatic data were obtained from [WorldClim](https://www.worldclim.org/), which provides high-resolution global climate layers.  
As the data are readily accessible through the platform, they were downloaded directly via standard web access.