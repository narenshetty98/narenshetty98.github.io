---
name: Building Inventory Visualizations
tools: [Python, Altair, Vega-Lite]
image: assets/pngs/Prewview.png
description: This project includes static and interactive visualizations built using Altair and Vega-Lite for building inventory data analysis.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Building Inventory Visualizations

This project showcases two data visualizations based on a dataset of building inventories:

1. **Static Line Chart**: Shows the average number of floors acquired by year.
2. **Interactive Bar Chart**: Displays the top 10 counties with the most buildings, categorized by usage description.

We used Python and Altair to create the visualizations, and they are rendered dynamically using Vega-Lite JSON files.

---

## Static Line Chart
The **Static Line Chart** illustrates the average number of floors acquired by year.



<vegachart schema-url="/assets/json/line_chart.json" style="width: 100%;"></vegachart>

### Write-Up

#### Description
This line chart visualizes the trend of the average number of floors in buildings acquired over time. The x-axis represents the year of acquisition, while the y-axis displays the average number of floors in the buildings acquired in that year. The visualization provides insights into how building trends have evolved, highlighting significant peaks and declines in construction practices. We can see that as the years evolve, the average number of floors have actually reduced, this might be because of efficient house planning or constructing houses with larger bases, this might also be due to the fact more people are opting to choose houses with lesser number of floors and the demand for houses with more floors gradually declined.

#### Design Choices
The chart uses **position encoding** for both the x-axis  and y-axis. A line chart was chosen because it is ideal for showing changes over time. Each data point is marked to emphasize individual years, helping to identify specific trends. The absence of a color scheme in this static plot keeps the focus on the temporal progression of the data without distractions. We can clearly identify the decline in the number of floors as the years go by and the color scheme emphasises this aspect.

#### Data Transformations
The dataset was aggregated to calculate the **mean number of floors** for each acquisition year. Missing years or sparse data points were handled by filtering out null values and ensuring consistent x-axis labeling. Python’s `groupby` and `mean` methods in Pandas were used to compute the averages.

#### Changes from Homework #7
There were no similarities to homework 7 - this submission, Altair was used for its more declarative syntax. The data transformation steps were used but streamlined to integrate with Altair's data model.



---

## Interactive Bar Chart
The **Interactive Bar Chart** shows the top 10 counties with the most buildings, categorized by their usage description.

<vegachart schema-url="/assets/json/interactive_bar%20chart.json" style="width: 100%;"></vegachart>

### Write-Up

#### Description
This bar chart illustrates the top 10 counties with the highest number of buildings, categorized by their usage (e.g., Residential, Business, Industrial). The x-axis shows the number of buildings, and the y-axis lists the counties. Each bar is segmented by usage description, with distinct colors representing different usage categories.

#### Design Choices
The visualization uses **bar encoding** for the count of buildings and a **categorical color scheme** to encode the usage description. The chosen color palette ensures that each usage category is easily distinguishable. The y-axis was sorted by the total number of buildings to emphasize the relative dominance of each county. The chart's stacked bar format provides a comprehensive view of the contribution of different usage categories to the total building count.

#### Data Transformations
The raw dataset was grouped by county and usage description to compute the total building count for each combination. Only the top 10 counties (by total building count) were retained, and the data was pivoted to prepare for a stacked representation. Filters were applied to remove null or insignificant categories.

#### Changes from Homework #7
This chart was enhanced with interactivity and a categorical filter for usage descriptions. Additionally, Altair was used to incorporate seamless interactivity  and there were no similarities to homework 7.

#### Interactivity
This bar chart includes a **filter widget** for usage descriptions. Users can select a specific usage category (e.g., "Residential" or "Unusual") to dynamically filter the chart. This interactivity enhances the visualization by enabling a detailed exploration of specific subsets of the data, making it more engaging and informative for end users.

---

## Search the Data & Methods

Below are links to access the dataset and the analysis notebook:

<div class="left">
{% include elements/button.html link="https://github.com/narenshetty98/narenshetty98.github.io/blob/main/assets/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/narenshetty98/narenshetty98.github.io/blob/main/python_notebooks/Visualisations.ipynb" text="The Analysis" %}
</div>
