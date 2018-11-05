# Shuttle Radar Topography Mission

While making a map component I had to cobble together some shapefiles and heightmaps to get the effect I wanted. I heavily relied on ['Command Line Cartography'](https://medium.com/@mbostock/command-line-cartography-part-1-897aa8f8ca2c) by Mike Bostock.

The srtm.js has some routines that load srtm tiles, assemble them into grids, and resample them.

I use d3-contour to compute elevation contours and transform them back into spherical coordinates.

I also used d3-geo-projection to format some US census tract data.

![Example processed map](tracts/nv_screen.svg)

## Future Improvements
  - Add image processing capabilites to the srtm raster;
    - kernels for smoothing or derivatives
    - Dot product of normal vector for terrain shading
  - use a makefile to organize the workflow dependencies
  - Use TopoJSON to simply geometry and remove redundant data
  - Convert the srtm script into a node module usable from the command line
  - add a method to obtain arbitrary data from SRTM datasets
  - There is a newer version of [SRTM](https://lpdaac.usgs.gov/dataset_discovery/measures/measures_products_table)!

## Examples
 - Mike Bostock's [tutorial](https://medium.com/@mbostock/command-line-cartography-part-1-897aa8f8ca2c)
   - example [makefile](https://gist.github.com/johan/db11e7bd04f030031dae209fa1a6c3e4) by johan
 - Contour map [tutorial](https://www.axismaps.com/blog/2018/04/contours-in-browser/)
 - Another [topographic map](https://bl.ocks.org/hugolpz/6279966) scripted by Lopez Hugo
 - USGS's [SPCS](https://en.wikipedia.org/wiki/State_Plane_Coordinate_System)
 - [Noah Veltman's D3-friendly SPCS](https://github.com/veltman/d3-stateplane) by Noah Veltman
 - Here is an Bostock [example](https://bl.ocks.org/mbostock/83c0be21dba7602ee14982b020b12f51) which transforms contour coordinates back into spherical
 - Nice zoom effect by [Catherine Kerr](https://bl.ocks.org/catherinekerr/b3227f16cebc8dd8beee461a945fb323)
 - properly rescaling SVG by [chartio](https://chartio.com/resources/tutorials/how-to-resize-an-svg-when-the-window-is-resized-in-d3-js/)
 - Some [bash](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html#toc7) [guides](https://tiswww.case.edu/php/chet/bash/bashref.html)

## Geospatial Data
 - Obtained nevada data from the [US Census Bureau](https://www2.census.gov/geo/tiger/GENZ2017/shp/)
 - Well integrated vector and raster map data from [Natural Earth](http://naturalearthdata.com/)
 - Space shuttle radar height rasters [SRTM](https://dds.cr.usgs.gov/srtm/)
 - Here is a host of interesting data; [Distributed Active Archive Centers](https://earthdata.nasa.gov/about/daacs/daac-lpdaac)

## Tools
 - [MapShaper](https://mapshaper.org/)
 - [TopoJSON](https://github.com/topojson/topojson)
 - [Open Source Geospatial Foundation](https://www.osgeo.org/)
 - Shapefile [Specification](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf)
 - [GDAL](https://www.gdal.org/)
 - [ESRI](https://www.esri.com/en-us/arcgis/products/index)
 - [USGS Software](https://lta.cr.usgs.gov/get_data)
 - [TopoJSON](https://github.com/topojson/topojson) can simplify GeoJSON
