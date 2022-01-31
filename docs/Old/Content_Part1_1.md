---
layout: default
title: Raster Data
parent: Data Models
grand_parent: Content
nav_order: 1
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# Raster Data

A simple but storage intensive method for representing data that is widely ustilized in GIS.  Rasters are commonly encountered as: satellite and drone imagery, elevation models, climate data, model outputs, and scanned maps.   

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/Raster.html" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/Raster.html" target="_blank">View Image in New Tab</a>

## File Types

Raster data can come in many different formats.  **GeoTIFF** which has the extension .tif is one of the most common/functional is the .  This format is based of the Tag Image File Format (TIFF), a common file type used by graphic artists and photographers.  A TIFF file stores metadata (data about the data) as tags.  For instance, your camera might store a tag that describes the make and model of the camera and another for the date the photo was taken when it saves a picture. A GeoTIFF is a standard .tif image format plus additional tags spatial tags denoting spatial information including: 

* Extent (minimum x,y and maximum x,y)
* Resolution (cell size)
* Projection, Coordinate system, and datum

Other file types you will likely encounter when working with raster data include:
* 1) IMG - A proprietary image format commonly used by ESRI products
* 2) JPEG2000 - A geospatial version of the common .jpg image type
* 3) ASCII - An older human readable format (simple text file) with slower performance than the types listed above.

---

# Assessment Questions

### QC1

The ______ data model represents space as a continuous grid of ______ which each contain a single ______.



