# Analyzing Bikeability and Bicycle Infrastructure in Moscow
In this project, I'm evaluating the bikeability of Moscow and analyzing the distribution and quality of bicycle infrastructure. The goal of the project is to provide insights into the city's bike-friendliness and identify areas where improvements can be made to encourage cycling as a sustainable mode of transportation.

## This repository contains the following files:
1. **mos_bikeability_main.ipynb** - main notebook with the following data:
   1.1. maps with all Moscow municipalities and population by municipalities
   1.2. the code for scraping data from mos.ru using API
   1.3. bike roads, parkings and rentals maps
   1.4. a new proposed metric Bikeability Index (BI) used for analysis and a full analysis itself (with calculations)
   1.5. code snippets for creating an interactive map using Folium library
2. **create_csv_population.ipynb** - a notebook for creating csv file with municipalities, their OKATOs, OKTMOs, etc. and their population based on the existing file mo-shape.zip with municipalities. Population data in year 2023 is taken from Rosstat: https://rosstat.gov.ru/storage/mediabank/chisl_MO_Site_01-01-2023.xlsx
3. **population_by_municipalities_2023.ipynb** - a notebook with the code to create maps of Moscow using GeoPandas: a map showing municipalities (colour is chosen based on population count) and an interactive map with names and population count of municipalities
4. **mo-shape.zip** - geodata on the current administrative-territorial division of Moscow with classifier codes tken from https://gis-lab.info/qa/moscow-atd.html
5. **bike_parkings.geojson**, **bike_roads.geojson**, **rental.geojson** - datasets scraped for this project from mos.ru
6. **moscow_municipal_population_2023.csv** - a csv file with municipalities, their OKATOs, OKTMOs, etc. and their population created by running **create_csv_population.ipynb**
7. **moscow_municipal_population_2023.html** - an interactive map of Moscow showing municipalities and their population count
8. **map_bike_infrastructure_with_pop.html** - an interactive map of Moscow showing municipalities coloured based on their Bikeability Index; bike roads (the lines and markers), parkings and rentals with names and addresses. All the markers are grouped into clusters for for better visibility of the map. A user can also choose tiles (2 preset ones and one custom taken from http://leaflet-extras.github.io/leaflet-providers/preview/ and switch on/off the population layer, markers with roads, parkings and rentals.
