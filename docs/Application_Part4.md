---
layout: default
title: Spatial Analysis
parent: Lab Application
nav_order: 5
---

# Spatial Analysis

We're going to look at two methods for overlaying a raster image and a vector layer: 1) **Zonal Statistics** and 2) **Raster to Polygon Conversion**.  Method 1 is a bit slightly faster and more precise, but can be applied in a more limited number of circumstances.  Method 2 induces some error when converting between data types (we will discuss more in lecture) and requires more steps, but it is more flexible.

# Zonal Statistics

We are going to overlay the vector data on the raster data to measure the mean NDVI value for each DA & CT using the Zonal Statistics as Table tool.  Then we will Join the resulting output table to display the mean NDVI values per DA & CT.  

**1**{: .label .label-red } Calculate the Zonal Statistics
* Find the Zonal Statistics as Table tool in the Geoprocessing pane.
* Choose Van_DA_2016 as the feature zone data.
* Set DAUID as the Zone Field
* Set your NDVI layer as the Input value raster. *Note use the projected NDVI image, not the classified image you creeted you created in the last step.*
* Select All statistics types
* Run

**2**{: .label .label-red } Join the Zonal Statistics table with the Van_DA_2016
* Right click on Van_DA_2016 and choose Joins and Relates > Add Join
* Set DAUID as the Input Join Field
* Choose the Zonal Statistics table as your input. *(the name should look something like ZonalST_Van_DA_1)*
* Make sure DAUID is selected as the Join Table Field as well
* Click OK

**3**{: .label .label-red } Inspect the Join
* Open the attribute table and note the new columns.
* Change the symbology, and choose Mean as the Field.
* Zoom in, turn Van_DA_2016 layer on/off, compare to the classification, NDVI layer, and base map.  Confirm the values make sense given the inputs.

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/videos/ZonalStats.mp4" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/videos/ZonalStats.mp4" target="_blank">View Image in New Tab</a>

### QA5
What is the DAUID of the DA with the highest Mean NDVI value?  *Hint* Double clicking on Green Veg Area in the attribute table allows you to sort in ascending/descending order.


# Raster to Polygon Conversion

We are going to convert the Classification raster layer to a vector data and select just the Green Vegetation.  We can then overlay the resulting vector layer with the Van_DA_2016 layer using an intersect.

**4**{: .label .label-red } Use the Raster to Polygon Tool
* Set the Classified NDVI image as the Input raster
* Choose Value as the Field

**5**{: .label .label-red } Set the Symbology to Unique Values
* Choose gridcode as the Field
* Zoom into somewhere of interest (eg. I chose Trout Lake), toggle the newly created vector layer on and off to see if it makes sense.

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/videos/RasterToPoly.mp4" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/videos/RasterToPoly.mp4" target="_blank">View Image in New Tab</a>

## Intersect
The [Intersect tool](https://pro.arcgis.com/en/pro-app/latest/tool-reference/analysis/intersect.htm) is one of the most useful vector - vector overlay operations.  It will combine the feature classes where they overlap and exclude all other areas 

**6**{: .label .label-red } Run the Intersect.

**7**{: .label .label-red } Change the symbology and open the attribute table to confirm the results look like what we'd expect.

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/videos/Intersect.mp4" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/videos/Intersect.mp4" target="_blank">View Image in New Tab</a>

## Add & Calculate Field

Adding new fields to our attribute table allows us to perform calculations or copy a subset of our data to a new column.

**8**{: .label .label-red } In the Van_DA_2016_Intersect layer, create a Green Veg Area Field.
* Right click on Field in the attribute table.
* Name the field Green_Veg_Area and give it an alias without the underscores.
  * Arc doesn't allow spaces in column names.
* Make sure the data type is Double.
  * Double is a type of data that allows for decimals.
* Make sure to save the field.
* Close the field window and go back to the attribute table.

**9**{: .label .label-red } Select only the green vegetation areas.
* Choose Select by Attribute: Where gridcode is equal to 3.
  * Select by attribute allows us to select rows/objects with a certain attribute.
  * It relies on something called a Structured Query Language (SQL).
  * We are selecting all rows "Where" our conditions are met.
  * Our condition is that grdicode (attribute from the NDVI layer representing vegetation category) is equal to 3 (green vegetation).

**10**{: .label .label-red } Calculate the Green Veg Area.
* Right click on Green Veg Area and choose calculate field.
  * This allows us to define a function and apply it.
* Set the expression to: Green_Veg_Area = Shape_Area as the.
  * *Note* you only need to complete the right side of the equation.
  * This will simply copy the shape area for the green vegetation areas, we will work with a mathematical expression on the next page.

**11**{: .label .label-red } Assign all other shapes a zero.
* We can quickly invert our selection.
* Calculate the field again, but with Green_Veg_Area = 0
  * We have selected girdcode 1 & 2 (Not vegetation) so they all get zeros.


<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/videos/AddField.mp4" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/videos/AddField.mp4" target="_blank">View Image in New Tab</a>


## Summary Table

Summarizing by a field (eg. DAUID - the Dissemination Unit ID) allows us to get statistics of interest for specific columns.

**12**{: .label .label-red } Get the sum of Green Veg Area by DA.
* Right click on DAUID and click Summarize.
* Set Green Veg Area as the Field and choose Sum as the statistic type.
* Make sure DAUID as the Case Field.
* The resulting table will show the total of just the green vegetation area per DA, and can be joined to the Van_DA_2016 layer.

<div style="overflow: hidden;
  padding-top: 56.25%;
  position: relative">
  <iframe src="content/videos/SummaryTable.mp4" title="Processes" scrolling="no" frameborder="0"
    style="border: 0;
   height: 100%;
   left: 0;
   position: absolute;
   top: 0;
   width: 100%;">
   <p>Your browser does not support iframes.</p>
 </iframe>
</div>
<a href="content/videos/SummaryTable.mp4" target="_blank">View Image in New Tab</a>


## Join Summary Table
Do a Join to add the Summary Table output to Van_DA_2016.  Following the same steps as above but use the Summary Table you just generated as the Join Table.

### QA6
What is the DAUID of the DA with the highest Green Veg Area?

### QA7
Is the DA with the highest mean NDVI value the same as the DA with the greatest area of green vegetation? Y/N

### QA8
Create a scatter plot, with the Mean NDVI value (Output from Method 1) on the X-axis Green and Veg Area Sum (Output from Method 2) on the Y-axis.  What is the R2 value? 

### QA9
The r2 score indicates Mean NDVI value is [Strong/Moderate/Weak/Very Weak] predictor of Green Veg Area.

### QA10
Change the Y-axis to Income and leave the X-axis as Mean NDVI, note the R2 score.  Now change the X-axis to the Green Veg Area Sum and note the R2 score.  Which variable has a "stronger" relationship with income? [Green Veg Area/Mean NDVI]

### QA11
Are either of these variables strongly linked to income? [Yes/No/Just Mean NDIV/Just Green Veg Area]







