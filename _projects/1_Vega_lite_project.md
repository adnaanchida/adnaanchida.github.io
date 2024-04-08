---
name: Homework 10, Visualization 
image: https://icons.veryicon.com/png/o/business/chart-icon/visualization-icon-07-07.png
description: This includes the 2 charts 
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework 8, Data Viz
### Link to Python file: 

<div class="right">
{% include elements/button.html link="https://github.com/achuri2/achuri2.github.io/blob/43b8e2792e0c749f185fc34589000000950fab31/Churi_Akshant-Malik_Smit-Choudhari_Samruddhi-assignment10.ipynb" text="Python Jupyter Notebook" %}
</div>


## Drag and Select Bars on 1st Plot to Interact With 2nd Plot

This visualization has 2 plots which are interconnected to each other. 

PLOT 1:

Description:
The first plot shows the average of total floors with respect to the buildings acquired by different Agencies. Plot 1 shows the average Square footage of buildings acquired by the Agencies using bar plots. The density of these floors are calculated by aggregating the total floors for each agency with respect to the building they have acquired over the years and these are shown using a color theme. It can be observed that the Department of Revenue has highest average total floors but still the median square footage is not the highest. 

DESIGN CHOICES

Encodings: 
It is very important to have proper encoding for these plots. The encoding types used in PLOT 1 are Position Channel(x,y) and mark property channel(color). The x value is {"field":'Agency Name', "type":"ordinal"} and y value is {"field":'Total Floors', "type":"quantitative", "aggregate":"average"}. The parameters for color are {"field":'Square Footage',"type":"quantitative", "aggregate":"average"}.

Colormaps:The default color has been chosen for bar plot 1 and the opacity has been set to 0.9.

Transformations: 
Removed the null values from dataset.

Overlap with Homework #9: 
The idea and the code has been taken from Assignment 9 (https://starboard.gg/nb/noPXJg6). It did not have any interactivity before, but we have introduced it in this.

PLOT 2:
The plot 2 shows the median square footage of different buildings acquired by the agencies which have different Building Status. When the building status is 'In progress' the median square footage is the highest. 

DESIGN CHOICES MADE

Encodings:
It is very important to have proper encoding for these plots. The encoding types used in PLOT 1 are Position Channel(x,y) and mark property channel(color). The x value is {"field":'Bldg Status', "type":"ordinal"} and y value is {"field":'Square Footage', "type":"quantitative", "aggregate":"median"}. 

Colormaps:
The color for bar chart has been chosen to be red the opacity has been set to 0.6.

Transformations: 
Removed the null values from dataset.

Overlap with Homework #9: 
The idea and the code has been taken from Assignment 9 (https://starboard.gg/nb/noPXJg6). It did not have any interactivity before, but we have introduced it in this.


INTERACTIVITY:
To make it more interesting we have made these plots interlinked to each other. This can be done dragging and selecting the bars of the first plot. Based on the area you have dragged, the median square footages for different buildings (acquired by selected agencies) with different status get updated on the second plot. 



<vegachart schema-url="{{ site.baseurl }}/assets/json/file.json" style="width: 100%"></vegachart>
### Link to Data

<div class="right">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="link to data" %}
</div>

