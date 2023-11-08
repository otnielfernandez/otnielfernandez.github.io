---
name: Homework 8 project
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: Showcase project using Vega-lite
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Example including vega-lite

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

```

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/newplot.json" style="width: 100%"></vegachart>

This is the interactive plot.

### Description:

This interactive plot includes the comparison between the year a building was acquired and the square footage of that building, filtered by building type and (when hovered over) the user can see the total floors of that building. I decided to utilize temporal datatypes as well as quantitative data types for the x and y, respectively. This was because the plot would be a lot of points, so I decided that a line plot would not be appropriate. Additionally, I added a color field where the building color would update based on the type of building. I choseto do this by the building type because it seems to be correlated with the year and the total square footage it has. Lastly, I added a tooltip field where the total floors would appear if you hovered over them. One  I did was make sure that people could see the total floors when they hovered over it

<vegachart schema-url="{{ site.baseurl }}/assets/json/uninteractive_plot.json" style="width: 100%"></vegachart>

Uninteractive plot.

### Description:

This uninteractive plot compares the top 10 cities with the most square footage, ranked. I decided to transform the plot by aggregating the total square footage by city. Additionally, I used the .transform_window option to perform calculations on a specific subset of data. I chose to use a subset because including all of the cities in this dataset would make too much noise within the plot. Additionally, I added a filter so that the top cities would only be included. Lastly, I included an encoding where the square footage total is quantitative and the city is ordinal, and adjusted the height.

## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

