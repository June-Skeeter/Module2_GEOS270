---
layout: default
title: Lab Application
has_children: True
nav_order: 3
---

# Scenario
You have a research question:
What is the relationship between neighborhood green vegetation coverage and income in Vancouver?


## Workflow
How we will answer the question:

1) Estimate vegetation coverage with satellite data and overlay census data.

2) Plot the relationship between vegetation coverage and income and run linear regression analysis.

3) Visualize the results.


<iframe width="560" height="315" src="https://www.youtube.com/embed/yApif5mwUlw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Learning Objectives:

* Experience a Typical GIS Workflow
* Explore Canadian Census Data
* Download Data from Google Earth Engine
* Work with Raster and Vector Data Layers
* Conduct Spatial Analysis
* Normalize and Classify Data
* Create Charts

## Google Earth Engine Sign Up

There are a wide variety of data sources out there.  We'll cover some options in greater detail later.  For now, I'm going to provide you with the census data we'll use and we're going to rely on Google Earth Engine (GEE) to download a raster data layer.  This will require a Google account so that you can access GEE and Google Drive.  Go to [Google](https://www.google.com/) and create an account by following the Sign In button if you don't already have one.  Then follow [this link](https://earthengine.google.com/) and choose sign up in the top right.  Follow the instructions to sign up using your Google account.  Once you have an account setup, you can close GEE.  You'll go back to it later.

## Getting Started

Create a new project in ArcPro called Van_NDVI.


## Download the Census Data

Now download [the census data](https://github.com/June-Skeeter/Module3_GEOS270/blob/main/data/Van_Census.zip) and extract the Van_Census.zip file to your newly created Van_NDVI folder.


### Acknowledgments

- This lab was written by June Skeeter using content adapted from lab assignments created by Naomi Schwartz and Sally Hermansen. 
