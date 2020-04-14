# ENV872_Project
Repository for final project of ENV872 Environmental Data Analytics for Spring 2020

# ENV872_Project

Repository for the final project of Thomas Hancock for ENV 872 Environmental Data Analytics at Duke University, spring semester, 2020.


## Summary

This repository contains data on COVID-19 cases in all of the US Counties, collected from the Johns Hopkins University Center for Systems Science and Engineering. It also contains TIGER census data for each county from the US Government, and a shapefile containing geographic information on all of the active coal mines in the US from the US Department of Energy. Accompanying this raw data is R code to perform a geospatial analysis exlporing whether counties with coal mines experience different COVID-19 case rates and death rates than other similar counties. Of particular interest are counties in Pennsylavania (where mines ceased operation due to COVID-19) and West Virginia (where mine operation has continued).


## Investigators

Thomas Hancock, Nicholas School of the Environment, Duke University
Email: tnh23@duke.edu

## Keywords
COVID, COVID-19, coronavirus, cases, deaths, coal, mining, mines, mine, counties, GIS

## Database Information

COVID-19 cases and deaths information at a county level come from the Center for Systems Science and Engineering (CSSE) at Johns Hopkins University. Currently, the data being used is from April 2, 2020. However, this data may be updated closer to the project completion date, and capability to pull live data from the database might be added to the code.
https://systems.jhu.edu/research/public-health/ncov/

GIS information for the operating surface and underground coal mines in the United States comes from the US Energy Information Administration. This data was published January 18, 2019 and accessed April 2, 2020.
https://catalog.data.gov/dataset/coal-mines-surface-and-underground

US State GIS files (e.g., shapefiles) are from the US Census Bureau. Accessed April 2, 2020.
https://www.census.gov/cgi-bin/geo/shapefiles/index.php

US County GIS files (e.g., shapefiles) are from the US Census Bureau, released August 9, 2019. These files were accessed April 2, 2020.
https://www.census.gov/cgi-bin/geo/shapefiles/index.php

US County population data is from the US Census Bureau for July 1, 2019. This data was accessed April 13, 2020.
https://www.census.gov/data/datasets/time-series/demo/popest/2010s-counties-total.html


## Folder structure, file formats, and naming conventions 

Folders:
/Code: RMarkdown scripts used to assemble report and analyze data

/Data
  /Raw: contains the raw data downloaded from the sites listed above
    /Spatial: contains raw spatial/shapefile files
  /Processed: contains processed data outputs from analysis scripts
    /Spatial: contains processed spatial/shapefile files
  /Metadata: contains any metadata documents describing the data in other folders
  
/Ouputs
  /Images: Graphical outputs (e.g., maps)
  /Tables: Formatted tables produced in script

/Report: Final compiled report

Files:
- Numerical data (e.g., Populations, COVID19 rates): these files are .csv comma-separated files

- Geospatial (e.g., county boundaries, mine locations): these files are .shp shapefiles, which include support files with the following extensions: .cpg, .dbf, .prj, .sbn., .sbx., .shx.

- R Markdown (e.g., report): these files are .rmd files that can be run in R Studio using R Markdown

File Naming Convention: File names will contain a descriptive title at the beginning, with words separated by underscores or abutted with capital letters. For files produced during analysis, this descriptor will be followed by an underscore and the process that was performed on it (for example, Example_File_cleaned.csv or ExampleFile_map.pdf).


## Metadata

US Census Bureau Population Estimates (co-est2019-annres.csv)
*Geographic Area: County in the United States
*Census: Population of geographic area in persons as of April 1, 2010 according to 2010 census
*Estimates Base: Base for estimates of population in persons for each geopgraphic region
*2010: Estimate of population in persons for each geopgraphic region for July 1, 2010
*2011: Estimate of population in persons for each geopgraphic region for July 1, 2011
*2012: Estimate of population in persons for each geopgraphic region for July 1, 2012
*2013: Estimate of population in persons for each geopgraphic region for July 1, 2013
*2014: Estimate of population in persons for each geopgraphic region for July 1, 2014
*2015: Estimate of population in persons for each geopgraphic region for July 1, 2015
*2016: Estimate of population in persons for each geopgraphic region for July 1, 2016
*2017: Estimate of population in persons for each geopgraphic region for July 1, 2017
*2018: Estimate of population in persons for each geopgraphic region for July 1, 2018
*2019: Estimate of population in persons for each geopgraphic region for July 1, 2019

COVID19 Data (COVID_County_04-12-2020.csv)
*FIPS: FIPS Code unique code to identify each county or county-equivalent
*Admin2: Geopgraphic Region (e.g., County) name
*Province_State: Province or State of geographic region
*Country_Region: Country or region of geographic region
*Last_Update: The time and date the entry was last updated
*Lat: Lattitude of region centroid
*Long_: Longitude of region centroid
*Confirmed: Number of confirmed COVID-19 cases in the geographic region
*Deaths: Number of confirmed deaths due to COVID-19 in the geographic region
*Recovered: Number of confirmed recoveries from COVID-19 in the geographic region
*Active: Number of active COVID-19 cases in the geographic region
*Combined_Key: Combined name of the geographic region (e.g., County Name, State, Country)

US Coal Mine Shapefiles (CoalMines_US_2018.shp)
*Shapefile and associated files describing the centroid location of all active coal mines (surface and underground) in the US

US County Shapefiles (tl_2019_us_county.shp)
*Shapefile and associated files with the boundaries of all US Counties

US State Shapefiles (tl_2019_us_state.shp)
*Shapefile and associated files with boundaries of all US States


## Scripts and code

ProjectAnalysis.rmd: R Markdown file containing preliminary code for gathering, tidying, and analysing data for this project.


## Quality assurance/quality control

At this time, I have not explored the data enough to have determined the necessary QA/QC measures to take.

One step I will take to check the GIS data and analysis is to produce a map that can be visually inspected for accuracy (e.g., are there coal mines in all the counties identified as mining counties).

I will also make sure that all of the counties in the COVID dataset match with a county in the Census data.