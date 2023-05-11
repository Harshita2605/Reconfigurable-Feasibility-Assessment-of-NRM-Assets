### Reconfigurable-Feasibility-Assessment-of-NRM-Assets

This repo contains all the preprocessing scripts for the Feasiblity Assessment Tool. <br>
Tool on Earth Engine [Link](https://code.earthengine.google.com/07e6cd6895a336b34de9b84d84731cdc) <br>
GEE User Manual [Link](https://docs.google.com/document/d/1yWilmX4YBwFBbxF6BKFlPdxAyHhDO3uSpU2nLYXz3JI/edit?usp=sharing) <br> 
Relevant datasets [Link](https://drive.google.com/drive/folders/1CnqiY4um1tkURohksRH-DqeiupelRZVL?usp=sharing) <br>

The tool uses weighted multi-criteria analysis on Geology, Drainage, Lineament, Slope and Land use and Land Cover (LULC) layers. Depending on how these layers affect the classification under consideration, these layers can be assigned different weights to result in a composite map. The description of the files in this repo are-

lineaments.ipynb - fetches lineaments as png files statewise using API calls to Bhuvan. Each state's png has a different resolution depending on its length and width. The pngs are converted to a mask where pixels with lineaments are given value 1 and others 0. This binary mask is generated and stored.

lithology.ipynb - uses statewise lithology shapefiles (present in the dataset folder above). 10 different soil types - Alluvium (1), Granite (2), Schist (3), Gneiss (4), Phyllite (5), Quartz (6), Basalt (7), Sandstone (8), Shale (9) and Laterite (10) are extracted as individual rasters and recombined to get final rasters with all soil types. The value in brackets correspond to the pixel values in the output raster.

recharge_potential & feasibility_score.ipynb - combines all preprocessed layers and generates output. This script has been replaced by the GEE App.
