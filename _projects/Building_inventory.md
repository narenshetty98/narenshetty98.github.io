---
name: Building Inventory Visualizations
tools: [Python, Altair, Vega-Lite]
image: assets/pngs/building_visualization_preview.png
description: This project includes static and interactive visualizations built using Altair and Vega-Lite for building inventory data analysis.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
---

# Building Inventory Visualizations

This project showcases two data visualizations based on a dataset of building inventories:

1. **Static Line Chart**: Shows the average number of floors acquired by year.
2. **Interactive Bar Chart**: Displays the top 10 counties with the most buildings, categorized by usage description.

We used Python and Altair to create the visualizations, and they are rendered dynamically using Vega-Lite JSON files.

---

## Static Line Chart
The **Static Line Chart** illustrates the average number of floors acquired by year.

<vegachart schema-url="{{ site.baseurl }}/assets/json/line_chart.json" style="width: 100%; height: 500px;"></vegachart>

---

## Interactive Bar Chart
The **Interactive Bar Chart** shows the top 10 counties with the most buildings, categorized by their usage description.

<vegachart schema-url="{{ site.baseurl }}/assets/json/interactive_bar_chart.json" style="width: 100%; height: 500px;"></vegachart>

---

## Search the Data & Methods

Below are links to access the dataset and the analysis notebook:

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/narenshetty98/narenshetty98.github.io/main/assets/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/narenshetty98/narenshetty98.github.io/blob/main/python_notebooks/Visualisations.ipynb" text="The Analysis" %}
</div>
