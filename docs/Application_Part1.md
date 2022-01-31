---
layout: default
title: Set Up
parent: Lab Application
nav_order: 2
---

# Set Up Your GeoDatabase

By default, ArcPro creates a geodatabase when you start a new project.  Recall from Module 1: A geodatabase (.gdb) is a file management structure that is unique to ESRI products.  They are used to store files in Arc Pro. You don't have to store your data in a .gdb, Arc Pro can work with data stored in regular folders as well, but they have some enhanced functionality that makes them better in some circumstances.  One helpful thing we can do in a .gdb, is create a feature dataset to store our census data.

**Feature Datasets** are collections of **Feature Classes** that are all in the same coordinate system.  When you add a data to a feature dataset, it will *automatically* be projected into the coordinate system we specify.  This can help us avoid making mistakes like working with data that is in the wrong coordinate system!  We are going to use a Universal Transverse Mercator projection  (UTM Zone 10N) since we are working with a small area (Vancouver).  You can reference the video to see how to create one.

**1**{: .label .label-red } Create the an new Feature Dataset named **CensusData** Feature Dataset 

**2**{: .label .label-red } Set the Coordinate System to NAD 1983 UTM Zone 10N

* NAD 1983 is the name of the datum (North American Datum 1983)
* UTM Zone 10N is the name of the projection (Universal Transverse Mercator, Zone 10 N)
 * You can set this coordinate system to your favorites by right clicking and selecting add to favorites.  This will make it easier to find in the future!

**3**{: .label .label-red } Add **Van_DA_2016.shp** and **VanCMS_CT_2016.shp** from the Van_Census folder you downloaded.

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/videos/FeatureDataset.mp4" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/videos/FeatureDataset.mp4" target="_blank">View Image in New Tab</a>


## Create the Project Boundary File
We need to create a simple boundary file to upload to Google Earth Engine so we can download satellite for our study area.  We can do this quickly using the dissolve tool.

**1**{: .label .label-red } In the Geoprocessing pane, find the Dissolve tool.

**2**{: .label .label-red } Set VanCMA_CT_2016 as the input

* **Note**: Geoprocessing results are by default saved to your Van_NDVI.gdb, but files in .gdb are saved in a format that can't be read by Google Earth Engine.
* *Instead*: save the Output one level up in your Van_NDVI project folder and name it **Boundary**.


**3**{: .label .label-red } Remove this layer from your table of contents.  We don't need it in this map project.	

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/videos/Dissolve.mp4" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/videos/Dissolve.mp4" target="_blank">View Image in New Tab</a>
