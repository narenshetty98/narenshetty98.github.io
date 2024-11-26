---
layout: post
title: "Building Inventory Visualizations"
---

## Visualization 1: Static Line Chart
The first visualization is a **static line chart** that illustrates the **average number of floors in buildings acquired by year**.

- **Encodings**: 
  - The x-axis represents the **year acquired** (quantitative), and the y-axis represents the **average number of floors** (quantitative). 
  - The data points are marked with circles to indicate the exact averages for each year, making it easier to identify specific trends.
  
- **Design Choices**: 
  - A line chart is ideal for showing trends over time. The connected lines emphasize the continuity of building acquisitions across years, while the markers on the line add clarity to individual data points.
  - The tooltip provides additional detail by showing the exact year and the corresponding average number of floors, enhancing interactivity even in a static chart.

- **Data Transformation**: 
  - The dataset was grouped by `Year Acquired`, and the mean of `Total Floors` was calculated for each year to display trends. 
  - This approach ensures the visualization focuses on the aggregate trend, eliminating any noise from individual outliers in the dataset.

This chart effectively communicates how building acquisitions and their floor structures have evolved over time. For example, peaks in specific years highlight periods of significant acquisitions, while consistent declines may indicate changes in building practices or policies.

<iframe src="/assets/line_chart.html" width="700" height="400"></iframe>

---

## Visualization 2: Interactive Bar Chart
The second visualization is an **interactive bar chart** showcasing the **top 10 counties with the most buildings**, categorized by their **usage description**.

- **Encodings**:
  - The x-axis represents the **number of buildings** (quantitative), and the y-axis lists the **counties** (ordinal), sorted by total building count in descending order.
  - Bars are color-coded by the **usage description**, such as Assembly, Business, Storage, etc., to highlight how building purposes differ across counties.
  - Tooltips display detailed information for each bar, including the **county name**, **building count**, and the associated **usage description**.

- **Design Choices**:
  - The chart combines a horizontal bar layout with distinct colors for each usage description, making it easier to compare building counts across counties while understanding how their purposes vary.
  - Interactivity through tooltips allows users to explore the data in greater detail without cluttering the chart.

- **Data Transformation**:
  - The dataset was grouped by `County` and `Usage Description` to calculate the number of buildings per category.
  - The top 10 counties were determined based on total building counts. These counties were then filtered to focus only on their respective `Usage Descriptions`.

This chart provides meaningful insights into building distribution and usage trends. For instance, Cook County has the highest number of buildings, with a notable proportion allocated for Assembly and Business purposes. Such breakdowns are valuable for understanding regional priorities and development.

<iframe src="/assets/interactive_bar_chart.html" width="700" height="400"></iframe>

---

## Links
- [The Data](https://raw.githubusercontent.com/narenshetty98/narenshetty98.github.io/main/assets/building_inventory.csv)  
- [The Analysis](https://github.com/narenshetty98/narenshetty98.github.io/blob/main/python_notebooks/Visualisations.ipynb)
