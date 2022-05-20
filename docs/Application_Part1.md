---
layout: default
title: Set Up
parent: Lab Application
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
---



# Google Earth Engine Sign Up

We are going to use Google Earth Engine (GEE) to download some satelite data.  This will require a Google account so that you can access GEE and Google Drive.  

**1**{: .label .label-red } Go to [google.com](https://www.google.com/) and create an account following the Sign In button if you don't already have one.

* A google account will give you access to google drive with 15 GB free storage space!  This could be a useful resource when working on your final projects!

**2**{: .label .label-red } Then got to [earthengine](https://earthengine.google.com/) and sign up

* Choose sign up in the top right.
* Follow the instructions to sign up using your Google account.  
* Once you have gone through the sign up process, you can close GEE.  We'll go back to it later.

**Note** If you are unable to create an account, contact your TA for a link to the data set.

# Create a Project

**1**{: .label .label-blue } Create a new project in ArcPro called Van_NDVI.  You can reference the [Module 1](https://june-skeeter.github.io/Module1_GEOS270/docs/Application_Part3.html#setting-up-a-project) for a refresher on setting up a project.


**2**{: .label .label-blue } We're going to work with some Canadian Census Data.  It has already been downloaded for you, we'll learn how to download census data in Module 3.  For now, use the button below to download the data.

* Extract the Van_Census.zip file to your newly created project Van_NDVI folder.

[Download](https://github.com/June-Skeeter/Module2_GEOS270/raw/main/data/Van_Census.zip){: .btn .btn-blue }




## Set Up Your GeoDatabase

By default, ArcPro creates a geodatabase with every new project.  You will see one called **Van_NDVI.gdb** in your project folder.

**Geodatabase**: A file management structure that is unique to ESRI products. You don't have to store your data in a geodatabase (.gdb), but they have some enhanced functionality that makes them better than regular folders in some circumstances.  One helpful thing we can do in a .gdb, is create a feature dataset to store our census data.

**Feature Dataset**: A collections of feature classes that are all in the same coordinate system.  When you add a data to a feature dataset, it will *automatically* be projected into the coordinate system we specify.  This can help us avoid making mistakes like working with data that is in the wrong coordinate system!  We are going to use a Universal Transverse Mercator projection  (UTM Zone 10N) since we are working with a small area (Vancouver).  

**Feature Class**: A vector data layer stored in a geodatabase.  Its a special file type created by ESRI to store data effectively within ArcGIS Pro.  When vector data layers are not stored in a geodatabase, they are stored in other formats, such as shapefiles or geojsons.  We'll cover the distinctions more in lecture.

Follow the steps below to setup your geodatabase.  You can reference the video to see how to create one.

**1**{: .label .label-red } Create a new Feature Dataset named **CensusData** feature dataset.

* Right click Van_NDVI.gdb >> New Feature Dataset

**2**{: .label .label-red } Set the Coordinate System to NAD 1983 UTM Zone 10N

* **NAD 1983** is the name of the datum (North American Datum 1983), **UTM Zone 10N** is the name of the projection (Universal Transverse Mercator, Zone 10 N)
 * You can set this coordinate system to your favorites by right clicking and selecting add to favorites.  This will make it easier to find in the future!

**3**{: .label .label-red } After you click Run, it will appear in your Van_NDVI.gdb.  Now we're going to add some census data.  

* Right click on your newly created **CensusData** feature dataset >> Import Feature Class(es) 
* Add the two census data layers you downloaded: **Van_DA_2016.shp** and **VanCMS_CT_2016.shp** 

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


# Create the Project Boundary File

We need to create a simple boundary file to upload to Google Earth Engine so we can download satellite for our study area.  We can do this quickly using the dissolve tool.

**1**{: .label .label-red } In the Geoprocessing pane, find the Dissolve tool.

**2**{: .label .label-red } Set VanCMA_CT_2016 as the input

* **Note**: The output will be saved to your Van_NDVI.gdb as a feature class by default, but feature classes can not be read by Google Earth Engine.

* *Instead*: save the output as a **Shapefile** (.shp) one level up in your Van_NDVI project folder and name it **Boundary**.  Shapefiles are just a different way of storing vector data.

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
