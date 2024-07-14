---
layout: page
title: Shadow Map
description: Tool to visualize accumulated shadows of Chicago for three seasons
img: "assets/img/projects/shadow_map/thumbnail.gif"
importance: 6
category: Other
---

<h4><u>Access this project</u></h4>
<b>GitHub repo:</b> <a href='https://github.com/komar41/shadow-accrual-maps'>https://github.com/komar41/shadow-accrual-maps</a> <br>
<b>Tools used:</b> Angular, TypeScript, D3.js, OpenLayers, HTML, CSS.
<p align='justify'>
This project aims to visualize the spatial distribution of accumulated shadows in Chicago for different seasons of the year. It provides an interactive web application that allows users to explore shadow patterns across the city, offering insights into how sunlight and shadows affect urban areas throughout the year.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="../../assets/img/projects/shadow_map/thumbnail.gif" alt="Shadow Accrual Maps" class="img-fluid rounded z-depth-1" style="width: 70%;">
    </div>
</div>
<br>
<h4><u>Components</u></h4>
<h5>1. <a href="https://openlayers.org/">OpenLayers Map</a></h5>
<p align='justify'>
<ul>
    <li>An interactive map centered on Chicago</li>
    <li>Uses OpenLayers with a TileLayer (e.g., OpenStreetMap)</li>
    <li>Centered at coordinates: -87.6298, 41.8781 (Chicago)</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://raw.githubusercontent.com/uic-big-data/fall-2021-assignment-1/main/map.png" alt="Assignment 1 map" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<h5>2. Shadow Overlay</h5>
<p align='justify'>
<ul>
    <li>An ImageLayer overlaid on the map showing accumulated shadows</li>
    <li>Uses RasterSource to transform shadow data into visible pixels</li>
    <li>Data for three days: June 21 (summer solstice), September 22 (autumnal equinox), December 21 (winter solstice)</li>
    <li>Shadows calculated from 1.5 hours after sunrise to 1.5 hours before sunset</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://raw.githubusercontent.com/uic-big-data/fall-2021-assignment-1/main/shadows.png" alt="Assignment 1 map" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<h5>3. Bar Chart</h5>
<p align='justify'>
<ul>
    <li>A D3.js bar chart displaying shadow information for the location under the mouse cursor</li>
    <li>Updates dynamically as the user moves the mouse over the map</li>
</ul>
</p>
<h4><u>Interaction Features</u></h4>
<p align='justify'>
<ul>
    <li>Mouse movement over the map triggers updates to the bar chart</li>
    <li>Displays shadow accumulation data for the specific location under the cursor</li>
</ul>
</p>
<h4><u>Project Structure</u></h4>
<p align='justify'>
<ul>
    <li>MapComponent: Handles the OpenLayers map and shadow overlay</li>
    <li>ChartComponent: Manages the D3.js bar chart visualization</li>
</ul>
</p>
<h4><u>Data</u></h4>
<p align='justify'>
<ul>
    <li>Shadow data provided in a hierarchical folder structure following slippy map tilenames</li>
    <li>Data stored in PNG files, with pixel values representing normalized minutes under shadow</li>
    <li>Three separate datasets for different seasons of the year</li>
</ul>
</p>
<h4><u>Development Setup</u></h4>
<p align='justify'>
1. Create a new Angular project: <code>ng new shadow-maps</code> <br>
2. Generate components:
<pre><code>ng generate component map
ng generate component chart</code></pre>
3. Install dependencies:
<pre><code>npm install --save-dev d3 ol @types/d3 @types/ol</code></pre>
4. Run <code>npm install</code> inside the <code>shadow-maps</code> folder
</p>
<br>

<h4><u>Additional Resources</u></h4>
<p align='justify'>
<ul>
    <li><a href="https://fmiranda.me/publications/shadow-accrual-maps/">Shadow Accrual Maps Publication</a></li>
    <li><a href="https://github.com/VIDA-NYU/shadow-accrual-maps/">Shadow Accrual Maps GitHub Repository</a></li>
</ul>
</p>
