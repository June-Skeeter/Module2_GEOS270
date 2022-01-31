---
layout: default
title: Assessment Key
nav_order: 5
parent: Potat
---

# Assessment
{: .no_toc }

You can use the course Canvas page to complete the quiz, written submission, and files uploads.  I suggest you download write down your answers as you progress through the Content and Application sections then upload your answers to canvas once you have finished the module.

1. TOC
{:toc}

---

# Module Quiz

All quiz answers are multiple choice, numeric input, fill in the blank, etc. type questions.  They can be submitted via the Module 1 Quiz that can be found on the Canvas page.  You will have unlimited attempts to take the quiz.

## Application Questions

[**QA1**](Application_Part3.md#qa1)
For every $100 increase in income at the CT level, how much does rental price increase?

$2.66
Correct:  **2.56 - 2.76**
Half Pts:  **2.46 - 2.86**


[**QA2**](Application_Part3.md#qa2)
What is the r2 score for this model?

r2 = 0.38

Correct:  **0.37 - 0.39**
Half Pts:  **0.33 - 0.43**


[**QA3**](Application_Part3.md#qa3)
Which Census Unit displays a more direct relationship between income and housing?
- DA
- CT
- About the same

Correct:  **CT**

[**Q4**](Application_Part3.md#qa3)
Which value denotes the lower bound of the "Green Vegetation Class?"

0.606867

Correct:  **0.597 - 0.617**
Half Pts:  **0.557 - 0.657**


[**Q5**](Application_Part4.md#qa5)
What is the DAUID of the DA with the highest Mean NDVI value?  *Hint* Double clicking on Green Veg Area in the attribute table allows you to sort in ascending/descending order.

59151219

[**Q6**](Application_Part4.md#qa6)
What is the DAUID of the DA with the highest Green Veg Area?

59153586

[**QA7**](Application_Part4.md#qa7)
Is the DA with the highest mean NDVI value the same as the DA with the greatest area of green vegetation? Y/N

Correct:  **N**

[**QA8**](Application_Part4.md#qa8)
Create a scatter plot, with the Mean NDVI value (Output from Method 1) on the X-axis and Green Veg Area Sum (Output from Method 2) on the Y-axis.  What is the R2 value? 

0.11 
Correct:  **0.1 - 0.12**
Half Pts:  **0.06 - 0.16**

[**QA9**](Application_Part4.md#qa9)
The r2 score indicates Mean NDVI value is [Strong/Moderate/Weak/Very Weak] predictor of Green Veg Area.

Correct:  **Very Weak**
Half Pts:  

[**QA10**](Application_Part4.md#qa10)
Change the Y-axis to Income and leave the X-axis as Mean NDVI, note the R2 score.  Now change the X-axis to the Green Veg Area Sum and note the R2 score.  Which variable has a "stronger" relationship with income? [Green Veg Area/Mean NDVI]

Green area & income (r2=0.014) Mean NDIV (r2=0.058). Mean NDVI has "stronger relationship"
Correct:  **Green Veg Area**

[**QA11**](Application_Part4.md#qa11)
Are either of these variables strongly linked to income? [Yes/No/Just Mean NDIV/Just Green Veg Area]

NO, r2 0=no relationship, 1 = perfect relationship.  These values are low
Correct:  **No**


[**QA12**](Application_Part5.md#qa12)
Create a scatter plot, with the Mean NDVI value (Output from Method 1) on the X-axis and Green Vegetation Fraction (Normalized Output from Method 2) on the Y-axis.  What is the R2 value? 

0.64
Correct:  **0.63 - 0.65**
Half Pts:  **0.59 - 0.69**


[**QA13**](Application_Part5.md#qa13)
The r2 score indicates Mean NDVI value is [Strong/Moderate/Weak/Very Weak] predictor of Green Veg Area.

Correct:  **Moderate**
Half Pts:  

---

## Content Questions

[**QC1**](Content_Part1.md#qc1)
The ______ data model represents space as a continuous grid of ______ which each contain a single ______.

**0**
Correct:  **Raster**
Half Pts:  

**1**
Correct:  **Cells, Pixels, equal sized cells**
Half Pts:  

**2**
Correct:  **Value, attribute, non-spatial attribute**
Half Pts:  given value


[**QC2**](Content_Part1.md#qc2)
The ______ data model represents features in space as discrete two-dimensional ______ , one-dimensional ______ , and/or "zero-dimensional"  points.  Attribute information is stored separately in a ______.

**0**
Correct:  **Vector**
Half Pts:  

**1**
Correct:  **Polygons, polygon data**
Half Pts:  

**2**
Correct:  **Lines, line data**
Half Pts:  

**3**
Correct:  **Table, database table, tablular format, data table, attribute table**
Half Pts:  file, database, tubular data, different table, tabular



[**QC3**](Content_Part2.md#qc3)
______ objects have well defined boundaries.  They are countable, meaning there is only a ______ number of them.

**0**
Correct:  **Discrete**
Half Pts:  Discrete Objects

**1**
Correct:  **Finite, Limited, specific, countable**
Half Pts:  exact, certain, set, fixed


[**QC4**](Content_Part2.md#qc4)
______ fields lack well defined boundaries.  Because of this, they can be measured at an ______ number of locations.

**0**
Correct:  **Continuous**
Half Pts:  Continuous Fields

**1**
Correct:  **Infinite, Unlimited, any, endless**
Half Pts:  arbitrary, unspecified, uncountable

[**QC5**](Content_Part2.md#qc5)
Both types of phenomena can be represented using either the raster or vector data model.  However, ______ phenomena are generally better represented by the vector model and ______ phenomena are better represented by the raster data model.

**0**
Correct:  **Continuous**
Half Pts:  Continuous Fields

**1**
Correct:  **Discrete**
Half Pts:  Discrete Object

[**QC6**](Content_Part2.md#qc6)
Higher resolution rasters have smaller cells which means they take less memory to store [T/F]

Correct:  **FALSE** - storage space is dictated by the number of cells, not the cell size **but** if trying to store equivalent areas, the storage space will be greater for higher resolution.


[**QC7**](Content_Part2.md#qc7)
The ______ problem pertains to how we assign data values to grid cells that cover more than one value.

Correct:  **Mixed Pixel, Mixed Cell, mixed-pixel**
Half Pts:  boundary delineation, Mixed Pixel Problem

[**QC8**](Content_Part2.md#qc8)
Resolution is a property of the [data/map/both], scale is a property of the [data/map/both].

**0**
Correct:  **Both**
Half Pts:  

**1**
Correct:  **Map**
Half Pts:  


[**QC9**](Content_Part2.md#qc9)
Polygons in a vector dataset can be single part or multipart [T/F].

{0: {'Correct': 'TRUE'}}
Correct:  **TRUE**


---

# Module Assignment 60Pts

All written answers should be numbered and record in one document, saved as a .pdf, and uploaded to canvas.  The file submissions should also be saved as .pdf and uploaded as a separate document.  **Written answers can be as brief as you want as long as they answer the question.**

## Application Questions

### Written Answers

[**WA1**](Application_Part2.md#wa1) 8 pts
What is NDVI and what is it used for?  Describe the patterns you see in NDVI across the metro Vancouver area.

NDVI is a metric for gauging vegetation health/density/"greenness".  It is based off the differential reflectivity between red (low for plants) and near infrared (high for plants).  Across metro van - water/concrete low, residential w/ tree cover medium, forests/agriculture high


[**WA2**](Application_Part3.md#wa3) 2 pts
What are the differences you notice between the CTs and DAs in terms of size and population?

CDAs are smaller population/size wise, DAs give full coverage CTs only in CMA (metro areas)

[**WA3**](Application_Part5.md#wa3) 8 pts
What does data normalization do? How does normalizing effect the relationship with income? Create a new chart with Green Vegetation Fraction on the X-axis and Income on the Y-axis to find out.  How does this compare to when we were looking at the relationship between Total Green Vegetation Area and income?


Normalizing accounts for a confounding/secondary/other variable by dividing the variable of interest by the confounder.  This helps control for correlation between the two variables. The R2 score goes up to 0.083, Accounting for the different sizes of the DA "improves" the relationship. But not by much

[**WA4**](Application_Part6.md#wa4) 12 pts
What do the results of this analysis show?  Are there any improvement you think we could make to this analysis?

The relationship isn't strong, probably because there are other factors that are determine where people with limited resources can afford to live and where those with money choose to live. (7.5 pts)


Things to look at might include: housing cost (rent or land value) instead of income.  Both NDVI & green area combined (eg. multivariate linear regression). Excluding downtown core and focus on just medium density residential areas.  Account for water/beaches (also attracts high income but low NDIV)  .  These are just possible suggestions, they don't have to list these anything that makes sense counts (7.5 pts for listing two or more suggestions, 3.25 pts if just one).


### File Submissions

[**FA1**](Application_Part6.md#fa1) - 25 pts (see breakdown - tally by this instead of rubric)
Export your Layout as a .pdf and upload it to Canvas.

See example map:


Map showing proper mean NDVI (not green fraction) - 5pts

Chart showing proper mean green fraction vs income (not NDVI) - 5pts

Source statement (Name/source/data/date) - 4ts (1 off for name/date etc.)

Clean presentation & appropriate elements (Text is descriptive/not cut off, north arrow, legend, scale text) - 6 pts

Projection and scale 1:100,000 (should be obvious if the left it in Lambert conformal, Vancouver will be slanted)  - 5pts


---

## Content Questions 

[**WC1**](Content_Part2.md#wc1) - 5pts
Briefly discuss what resolution means with regards to raster and vector data.  

Raster resolution is defined by the cell size - smaller cells = higher resolution
Vector resolution is less straightforward.  Determined by density of points representing polygons/lines.

---

# Rubric 

All written answers and file submissions will be scored using this generic rubric.  Your TA will provide brief comments where applicable.  For more feedback you can follow up with your TA.

|Score|Comments            |
|-----|--------------------|
| 0%  |Missing             |
| 25% |Insufficient        |
| 50% |Below Expectations  |
| 75% |Met Expectations    |
| 100%|Exceeds Expectations|
