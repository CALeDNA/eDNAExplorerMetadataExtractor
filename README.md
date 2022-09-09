# eDNAExplorerMetadataExtractor
Script to extract environmental and social data at locations near eDNA sampling locations, and within specified temporal ranges of sampling.

To run this script please upload a copy to your Google Drive and run it using:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/CALeDNA/eDNAExplorerMetadataExtractor/blob/main/eDNAExplorerMetadataExtractor.ipynb)

# What does this script do?
Extracts the values of a wide variety of map layers, for variables covering a wide variety of environmental and social values, for a given set of locations and times. This allows the user to add information about natural, and human-dominated, conditions to locations and times where biodiversity measurements were collected.

# Getting started
## Preparing field data.
Your field data contains information on when and where you made biodiversity measurements, along with any field observations you may have made of the environment.
Your field data needs to consist of a CSV file with one row for each sample. At minimum it must have the following columns: sample_id, latitude, longitude, sample_date, spatial_uncertainty. The format for these columns need to be as follows: sample_id (string labeling your environmental DNA sample), latitude (degrees, with north being positive), longitude (degrees with east being positive), sample_date (yyyy-mm-dd), spatial_uncertainty (meters).
## What layers are being extracted?
We have selected a number of environmental and social layers which can potentially influence biodiversity patterns. These include data describing the natural environment, such as terrain and climate, human activities, such as land use and light pollution, as well as socioeconomic values such as access to health care and demography.
### Map layers describing the natural environment
#### Climate
The following data sets are used to describe climatic conditions:
1. BioClim.  The [BioClim dataset](https://developers.google.com/earth-engine/datasets/catalog/WORLDCLIM_V1_BIO) has 19 bands representing different measures of temperature and precipitation to a resolution of 30 arc seconds (1 kilometer).
2. Global SRTM CHILI (Continuous Heat-Insolation Load Index). The [CHILI](https://developers.google.com/earth-engine/datasets/catalog/CSP_ERGo_1_0_Global_SRTM_CHILI) factors in the effects of solar heating and shading, due to the topography of the landscape, on evapotranspiration. These calculations are done using models of early afternoon sunlight as experienced during the equinox.
