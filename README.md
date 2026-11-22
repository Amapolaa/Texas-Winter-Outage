# Homework 4: Identifying the impacts of extreme weathers

* **Author:** Amapola Garcia
* **Date:** November 15,2026
* **Course Name:** Geospatial Analysis and Remote Sensing
* **Term:** Fall 2026

## About
In February 2021, a major winter storm swept across the U.S. central plains, setting nationwide records for low temperatures. One of the storm's biggest impacts hit Texas, where people across the state suffered extended outages of electricity and water. It was one of the worst winter weather events in history, causing loss of life and economic impacts that will unfold over years. When disaster strikes, the flurry of political positioning and finger-pointing can make it difficult to understand what really happened.

## Purpose:
In this assignment we will be identifying the impacts of these series of extreme winter storms by estimating the number of homes in the Houston metropolitan area that lost power and investigating whether or not these impacts were disproportionatley felt.

My Analysis will bases on remotely-sensed night lights data, acquired from *Visible infrared Imaging  Radio Suite (VIIRS)* onboard the Suomi satellite. In particular, I will use the VNP46A1 to detect differences in night lights before and after the storm to identify areas that lost electric power.To determine the number of homes that lost power, I will  link (spatially join) these areas with OpenStreetMap data on buildings and roads.

This assignment will reinforce key concepts in geospatial analysis by practicing the following:
* load vector/raster data
* simple raster operations
* simple vector operations
* spatial joins


## Instructions & Workflow:

 For this assignment, you must produce the following:
* A set of maps comparing night light intensities before and after the first two storms
* A map of the homes in Houston that lost power
* An estimate of the number of homes in Houston that lost power
* A brief reflection (approx. 100 words) summarizing your results and discussing any limitations to this study

To complete complete the tasks of this assignment, I will break my analysis into the following key steps:
* Find locations that experienced a blackout by creating a mask
* Exclude highways from analysis
* Identify homes that experienced blackouts by combining the locations of homes and blackouts


# Data Files:
With R code we will be working with three different datafiles from VIIRS data :

*  VNP46A1.A2021038.h08v05.001.2021039064328.tif: tile h08v05, collected on 2021-02-072. gis_osm_roads_free_1.gpkg

* VNP46A1.A2021038.h08v06.001.2021039064329.tif: tile h08v06, collected on 2021-02-07

*  VNP46A1.A2021047.h08v05.001.2021048091106.tif: tile h08v05, collected on 2021-02-16

* VNP46A1.A2021047.h08v06.001.2021048091105.tif: tile h08v06, collected on 2021-02-16

## Data sets
1. Roads: gis_osm_roads_free_1.gpkg
3. Houses: gis_osm_buildings_a_free_1.gpkg


# Repository Structure
```bash
Texas-Winter-Outage
└───README.md
└───Rmd/Proj files    
└─── texas_outage.qmd 
└───.gitignore
    └───data
        └───gis_osm_buildings_a_free_1.gpkg
        └───gis_osm_roads_free_1.gpkg
        └───VNP46A1
            └───VIIRS data files
```

## References and Acknowledgement

Wikipedia. 2021. “2021 Texas power crisis.” Last modified October 2, 2021. https://en.wikipedia.org/wiki/2021_Texas_power_crisis.↩︎

