---
header_img: assets/images/folium_map.webp
header_title: "Data Enrichment"
header_type: hero
layout: default
title: "Data Enrichment"
---

# Data Enrichment
To get an estimate of the species' **maximal dispersal distance**, we implemented a streamlined approach inspired by **retrieval-augmented generation**, though without the use of embedding-based similarity search, as the queries were predefined and not user-generated.  
Each query targeted a particular species, and the corresponding context was extracted from species-specific documents.  
Relevant sections of text were identified and isolated using natural language processing techniques.  
The query and its extracted context were then jointly submitted to the LLM, from which we retrieved the desired output.