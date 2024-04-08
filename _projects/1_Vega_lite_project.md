---
name: Homework 8, Visualization (Jekyll)
image: https://icons.veryicon.com/png/o/business/chart-icon/visualization-icon-07-07.png
description: This includes the 2 charts and the Write-Up
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework 8, Data Viz
### Link to Python file: 

<div class="right">
{% include elements/button.html link="https://github.com/adnaanchida/adnaanchida.github.io/blob/a8f0e8cee023b257d57f78dd79063f0784d4a537/homework8.ipynb" text="Python Jupyter Notebook" %}
</div>


## Drag and Select Bars on 1st Plot to Interact With 2nd Plot

This visualization has 2 plots which are interconnected to each other using interactivity and it also includes the Write-Up based on the rubric. 

PLOT 1:

Description:
The first graph illustrates the mean total floors concerning buildings obtained by various agencies. Plot 1 depicts the average square footage of buildings acquired by these agencies through bar plots. The floor density is determined by aggregating the total floors for each agency relative to the buildings they've acquired over time, showcased with a color scheme. Notably, despite the Department of Revenue having the highest average total floors, its median square footage isn't the highest.

DESIGN CHOICES

Encodings: 
It is very important to have proper encoding for these plots. The encoding types used in PLOT 1 are Position Channel(x,y) and mark property channel(color). The x value is {"field":'Agency Name', "type":"ordinal"} and y value is {"field":'Total Floors', "type":"quantitative", "aggregate":"average"}. The parameters for color are {"field":'Square Footage',"type":"quantitative", "aggregate":"average"}.

Colormaps: The default color has been chosen for bar plot 1 and the opacity has been set to 0.9.

Transformations: 
Removed the null values from dataset.

Overlap with Homework #7: 
The idea and the code has been taken from Homework 7 (https://starboard.gg/nb/neCjt6N). It did not have any interactivity before, but we have introduced it in this.

PLOT 2:
Plot 2 displays the median square footage of buildings acquired by agencies categorized by different Building Status. It's noteworthy that when the building status is 'In progress', the median square footage is at its peak.

DESIGN CHOICES MADE

Encodings:
It is very important to have proper encoding for these plots. The encoding types used in PLOT 1 are Position Channel(x,y) and mark property channel(color). The x value is {"field":'Bldg Status', "type":"ordinal"} and y value is {"field":'Square Footage', "type":"quantitative", "aggregate":"median"}. 

Colormaps:
The color for bar chart has been chosen to be red the opacity has been set to 0.6.

Transformations: 
Removed the null values from dataset.

Overlap with Homework #7: 
The idea and the code has been taken from Homework 7 (https://starboard.gg/nb/neCjt6N). It did not have any interactivity before, but we have introduced it in this.


INTERACTIVITY:
To make it more interesting we have made these plots interlinked to each other. This can be done dragging and selecting the bars of the first plot. Based on the area you have dragged, the median square footages for different buildings (acquired by selected agencies) with different status get updated on the second plot. 



<vegachart schema-url="{{ site.baseurl }}/assets/json/file.json" style="width: 100%"></vegachart>
### Link to Data

<div class="right">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv" text="link to data" %}
</div>

