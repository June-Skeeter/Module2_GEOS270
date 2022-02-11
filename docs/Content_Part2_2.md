---
layout: default
title: Vector Data
parent: Spatial Data Models
grand_parent: Lecture Content
nav_order: 3
---
<!-- 
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>
 -->

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


Download the slides as a .pdf [here](https://raw.githubusercontent.com/June-Skeeter/Module2_GEOS270/main/docs/content/Vector.pdf)


## Sample GeoJson File

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

