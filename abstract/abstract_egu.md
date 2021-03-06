---
title: "Geocomputation with R"
author: |
   | Jannes Muenchow^1^, Robin Lovelace^2^ and Jakub Nowosad^3^
   |
   | ^1^Friedrich Schiller University of Jena ^2^University of Leeds ^3^Adam Mickiewicz University in Poznan
institute: 
   - $^1$Löbdergraben 32, 07743 Jena
output: html_document
bibliography: references.bib
---

R is probably the most important statistical computing language in academia.
With more than 10,000 packages it has been extended in many directions, including a huge support for geospatial data [see https://cran.r-project.org/web/views/Spatial.html and @bivand_applied_2013].
R's flexibility and statistical capabilities have made it attractive for people working in Earth, planetary and space sciences and a need for geographic data science.

This course will introduce the audience to R's geographical capabilities, building on the book [Geocomputation with R](https://geocompr.robinlovelace.net/) by the workshop authors [@lovelace_geocomputation_2018]. 
It will cover four topics and provide a solid foundation for attendees to apply R to a range of geographic data: <!--or spatial problems?-->

- R's implementation of the two most important spatial data models - vector [@pebesma_simple_2018] and raster [@hijmans_raster_2017]. 
- Spatial data visualization with R.
- Bridges to dedicated GIS software such as QGIS.
- Statistical learning with geographic data.

Understanding data models is vital for working with geographic data in R.
Maps, based on the data, can display complex information in a beautiful way while allowing for first inferences about spatial relationships and patterns.
R has already become a Geographic Information System (GIS) [@bivand_applied_2013] - a system for the analysis, manipulation and visualization of geographic data [@longley_geographic_2015].
However, R was not designed as a GIS, and therefore computing large amounts of geographic data in R can be cumbersome.
Even more important, R is missing hundreds of geoalgorithms which are readily available in common Desktop GIS.
To deal with these shortcomings R packages have been developed allowing R to interface with GIS software.
As an example, we will introduce the **RQGIS** [@muenchow_rqgis:_2017] package for this purpose but also comment on other R-GIS bridges such as **RSAGA** [@brenning_rsaga_2018] and **rgrass7** [@bivand_rgrass7_2017].
We will use **RQGIS** to compute terrain attributes (catchment area, catchment slope, SAGA wetness index, etc.) which we will subsequently use to model and predict spatially landslide susceptibility with the help of statistical learning techniques such as GLMs, GAMs and random forests [@james_introduction_2013]. 
Hence, we show by example how to combine the best of two worlds: the geoprocessing power of a GIS and the (geo-)statistical data science power of R.
The short course will consist of a mixture of presentations, live code demos and short interactive exercises if time allows.

## Learning objectives

By the end of this workshop, the participants should:

* Know how to handle the two spatial data models (vector and raster) in R.
* Import/export different geographic data formats.
* Know the importance of coordinate reference systems.
* Be able to visualize geographic data in a compelling fashion.
* Know about geospatial software interfaces and how they are integrated with R (GEOS, GDAL, QGIS, GRASS, SAGA).
* Know about the specific challenges when modeling geographic data.

## Software requirements

* Latest version of [R](https://cloud.r-project.org/) and [RStudio](https://www.rstudio.com/products/rstudio/download/#download)
* R packages: sf, raster, RQGIS, RSAGA, spData, tmap, tidyverse, mlr
* QGIS (including SAGA and GRASS), please follow our [installation guide](https://cran.r-project.org/web/packages/RQGIS/vignettes/install_guide.html#arch-linux) to make sure that **RQGIS** can work with QGIS  

## References
