---
layout: default
title: Vector Data
parent: Data Models
grand_parent: Content
nav_order: 2
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# Vector Data

In GIS, vector data are commonly encountered as: political boundaries, cenus data, pathways (road, trails, etc.), point location (stop sign, fire hydrant), etc.

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/Vector.html" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/Vector.html" target="_blank">View Image in New Tab</a>

## File Types

Like raster data, vector data can also come in many different formats. The **shapefile** format which has the extension .shp is one of the most common file types you will encounter.  A .shp file stores the geographic coordinates of each vertex in the vector, as well as metadata including:

* The spatial extent of the shapefile (i.e. geographic area that the shapefile covers). The spatial extent for a shapefile represents the combined extent for all spatial objects in the shapefile.
* Object type - whether the shapefile includes points, lines, or polygons.
* Coordinate reference system (CRS)
* Attributes - for example, a line shapefile that contains the locations of streams, might contain the name of each stream.

Because the structure of points, lines, and polygons are different, each individual shapefile can only contain one vector type (all points, all lines or all polygons). You will not find a mixture of point, line and polygon objects in a single shapefile.

**GeoJSON** is a simple, lightweight format for storing a variety of geographic data structures.  It is most commonly encountered in web mapping and other open source applications.  GeoJSON supports the following geometries: Point, Line, Polygon, MultiPoint, MultiLine, and MultiPolygon objects.  Unlike with shapefiles, one GeoJSON file can contain any mix of geometries. An objects with and its attributes are a Feature object. A set of Features is a FeatureCollection.  GeoJSON has the added benefit of allowing you to encode stylistic choices within the file.  If you'd like to explore this format a bit more, take the code below and paste it [here](https://geojson.io/#map=2/20.0/0.0).  You can make changes and see them reflected on your the map.

```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "marker-color": "#blue",
        "marker-size": "medium",
        "marker-symbol": "circle",
        "Name": "Vancouver"
      },
      "geometry": {
        "type": "Point",
        "coordinates": [
          -123.04687499999999,
          49.23912083246698
        ]
      }
    },
    {
      "type": "Feature",
      "properties": {
        "marker-color": "red",
        "marker-size": "medium",
        "marker-symbol": "square",
        "Name": "Victoria"
      },
      "geometry": {
        "type": "Point",
        "coordinates": [
          -123.40942382812501,
          48.516604348867475
        ]
      }
    }
  ]
}
```
**Simple text files** are human readable file formats (.txt, .csv) that are suitable for storing point and attribute data.  You will often encounter .txt or .csv files when working with weather data for instance (see Table).  Coordinates (typically latitude and longitude) are stored in a text files along with the other attributes.  We can bring this type of file into a GIS, but we need to convert the data to point features before we can display it. 

*Canadian Weather Station File*

|          Name          |    Province    |Climate ID|Latitude (Decimal Degrees)|Longitude (Decimal Degrees)|
|------------------------|----------------|---------:|-------------------------:|--------------------------:|
|ACTIVE PASS             |BRITISH COLUMBIA|   1010066|                     48.87|                    -123.28|
|ALBERT HEAD             |BRITISH COLUMBIA|   1010235|                     48.40|                    -123.48|
|BAMBERTON OCEAN CEMENT  |BRITISH COLUMBIA|   1010595|                     48.58|                    -123.52|
|BEAR CREEK              |BRITISH COLUMBIA|   1010720|                     48.50|                    -124.00|
|BEAVER LAKE             |BRITISH COLUMBIA|   1010774|                     48.50|                    -123.35|
|BECHER BAY              |BRITISH COLUMBIA|   1010780|                     48.33|                    -123.63|
|BRENTWOOD BAY 2         |BRITISH COLUMBIA|   1010960|                     48.60|                    -123.47|
|BRENTWOOD CLARKE ROAD   |BRITISH COLUMBIA|   1010961|                     48.57|                    -123.45|
|BRENTWOOD W SAANICH RD  |BRITISH COLUMBIA|   1010965|                     48.57|                    -123.43|
|CENTRAL SAANICH VEYANESS|BRITISH COLUMBIA|   1011467|                     48.58|                    -123.42|




---

# Assessment Questions

### QC2

The ______ data model represents features in space as discrete two-dimensional ______ , one-dimensional ______ , and/or "zero-dimensional"  points.  Attribute information is stored separately in a ______.