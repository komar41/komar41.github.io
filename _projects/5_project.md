---
layout: page
title: US Gun Deaths
description: Visualization tool to inspect number of gun deaths in the US states and cities in year 2013
img: "assets/img/projects/us_gun_deaths/thumbnail.png"
importance: 5
category: Other
---

<h4><u>Access this project</u></h4>
<b>Demo URL:</b> <a href='https://komar41.github.io/us-gun-deaths'>https://komar41.github.io/us-gun-deaths/</a> <br>
<b>GitHub repo: </b> <a href='https://github.com/komar41/us-gun-deaths'>https://github.com/komar41/us-gun-deaths</a> <br>
<b>Tools used: </b> Python, NumPy, Pandas, JavaScript, HTML, CSS, SVG, D3.js.

<p align='justify'>
This project aims to visualize and analyze gun-related deaths across the United States, providing insights into the distribution and patterns of these incidents. By presenting data through various interactive and informative visualizations, we seek to offer a comprehensive understanding of gun deaths at both state and city levels. The project incorporates multiple visualization techniques to showcase different aspects of the data, including geographic distribution, gender ratios, and age group breakdowns. Our goal is to create an accessible and informative tool for researchers, policymakers, and the general public to explore this critical issue.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/us-gun-deaths/raw/main/img/Final.png" alt="US Gun Death Visualization" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>

<h4><u>Components</u></h4>
<h5>1. Choropleth Map & Bubble Chart Overlay</h5>
<p align='justify'>
<ul>
    <li>The choropleth map visualizes the distribution of US gun deaths across all states</li>
    <li>Legend showing colors for each class of the distribution: 0-10, 11-50, etc</li>
    <li>A title with instructions on how to interact with the map</li>
    <li>The overlaid bubbles on the map to show city-scale distribution. Circle sizes represent death counts.</li>
    <li>Proper normalization used for circle sizes for accurate representation</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/us-gun-deaths/raw/main/img/WhiteHat1.png" alt="Choropleth Map & Bubble Chart Overlay" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5>2. Pie Chart & Horizontal Bar Chart (on hover)</h5>
<p align='justify'>
<ul>
    <li>Pie chart shows gender distribution for a selected state/city. Includes exact numbers for each gender</li>
    <li>Horizontal bar chart displays age distribution for the same selected state/city. Includes exact numbers for each age group</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/us-gun-deaths/raw/main/img/WhiteHat2.png" alt="Pie Chart & Horizontal Bar Chart" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5><u>3. State-wide Bar Chart</u></h5>
<p align='justify'>
<ul>
    <li>Located at the bottom of the visualization</li>
    <li>Shows death counts across all states in one view</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/us-gun-deaths/raw/main/img/WhiteHat3.png" alt="State-wide Bar Chart" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>Interaction Features</u></h4>
<p align='justify'>
<ul>
    <li>Hover over states/cities to display detailed pie and bar charts</li>
    <li>Title above the hover charts displays the selected state/city and total death count</li>
</ul>
</p>
<h4><u>Visualization Inspirations</u></h4>
<p align='justify'>
<ul>
    <li><a href="https://bl.ocks.org/wboykinm/dbbe50d1023f90d4e241712395c27fb3">Bill Morris (Choropleth Map)</a></li>
    <li><a href="https://d3-graph-gallery.com/">D3 Graph Gallery</a></li>
    <li><a href="https://github.com/academind/d3js-basics/tree/d3-demo-finished">Michelle Chandra (Basic US State Map)</a></li>
    <li><a href="http://bl.ocks.org/michellechandra/0b2ce4923dc9b5809922">Academind</a></li>
</ul>
</p>
<h4><u>Additional Resources</u></h4>
<p align='justify'>
<ul>
    <li><a href="https://stackoverflow.com/">Stack Overflow</a></li>
</ul>
</p>
