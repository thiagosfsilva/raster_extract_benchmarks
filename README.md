# Raster Extraction and Zonal Statistics Benchmark (Work In Progress)

Extracting pixel values from geospatial rasters based on vector regions is a common task in remote and GIS, and yet it there are limited choices of tools to accomplish such task.

More common are tools for the so-called "Zonal Statistics", which must necessarily perform this task as an intermediate step, before then calculating summary statistics for the pixels of each region/polygon/zone.

These tools can often require several hours to extract the information when dealing with high resolution / wide coverage / multiple band data and a large number of regions.

In an attempt to optimise this process, this ongoing benchmark will test and compare several tools available on commercial and open source software, and may hopefully help you save time when performing this task.

### Methods to test:

- ArcGIS Zonal Stats
- QGIS ZOnal Stats
- R raster::extract
- R exactextract::exactextract
- Python rasterstats
- [PyJeo extract](https://jeodpp.jrc.ec.europa.eu/services/processing/pyjeohelp/3_reference.html?highlight=extract#geometry._GeometryVect.extract)
- [pktools extractogr](http://pktools.nongnu.org/html/pkextractogr.html)
- ...

### Methodology:

- One high resolution.multiband dataset with dense polygion coverage

- Metrics:
  - Processing time
  - CPU usage (single core)
  - CPU usage (multi-core)
  - RAM usage
  - Cross-platform performance
