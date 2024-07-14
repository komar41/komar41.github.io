---
layout: page
title: Street Network Shadow
description: Visualizing the distribution of accumulated shadows in streets of Chicago for three seasons
img: "assets/img/projects/street_network_shadow/thumbnail.gif"
importance: 9
category: Other
---

<h4><u>Access this project</u></h4>
<b>GitHub repo:</b> <a href='https://github.com/komar41/street-network-shadow'>https://github.com/komar41/street-network-shadow</a> <br>
<b>Tools used:</b> Angular, TypeScript, Python, GeoPandas, Flask, D3.js, OpenLayers, HTML, CSS.
<p align='justify'>
This project aims to visualize the distribution of accumulated shadows for each season of the year across Chicago's street network. By presenting data through interactive map and chart visualizations, we seek to offer a comprehensive understanding of shadow patterns at the street segment level. The project incorporates multiple visualization techniques to showcase different aspects of the data, including geographic distribution and seasonal variations. Our goal is to create an accessible and informative tool for urban planners, researchers, and the general public to explore the impact of shadows on the urban environment.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/street-network-shadow/raw/main/chicago.gif" alt="Street Network Shadow Vis" class="img-fluid rounded z-depth-1" style="width: 70%;">
    </div>
</div>
<br>
<h4><u>Components</u></h4>
<h5>1. <a href="https://openlayers.org/">OpenLayers Map</a></h5>
<p align='justify'>
<ul>
    <li>Displays the street network of Chicago</li>
    <li><a href="https://openlayers.org/en/latest/apidoc/module-ol_layer_Tile-TileLayer.html">TileLayer</a> for base map visualization</li>
    <li>Centered on Chicago coordinates</li>
    <li>Interactive selection functionality allowing users to draw and translate arbitrary polygons</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://raw.githubusercontent.com/uic-big-data/fall-2021-assignment-2/main/map.png" alt="Assignment 2 map" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<h5>2. Distribution Chart</h5>
<p align='justify'>
<ul>
    <li>Visualizes the distribution of shadow values for all seasons</li>
    <li>Updates based on the user's polygon selection on the map</li>
    <li>Provides comparative view of shadow patterns across different seasons</li>
</ul>
</p>
<h4><u>Interaction Features</u></h4>
<p align='justify'>
<ul>
    <li>Draw arbitrary polygons on the map to select areas of interest</li>
    <li>Translate selected polygons to adjust the area of focus</li>
    <li>Dynamic updates of the distribution chart based on map selection</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://raw.githubusercontent.com/uic-big-data/fall-2021-assignment-2/main/selection.png" alt="Assignment 2 selection" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<h4><u>Data Sources</u></h4>
<p align='justify'>
Download the datasets <a href="https://raw.githubusercontent.com/uic-big-data/fall-2021-assignment-2/main/chicago-street-shadow.geojson">here</a>, and find more information <a href="https://fmiranda.me/publications/shadow-accrual-maps/">here</a> and <a href="https://github.com/VIDA-NYU/shadow-accrual-maps/">here</a>.
<ul>
    <li>Accumulated shadow data for three key dates:
        <ul>
            <li>June 21 (summer solstice)</li>
            <li>September 22 (autumnal equinox)</li>
            <li>December 21 (winter solstice)</li>
        </ul>
    </li>
    <li>Shadow data aggregated at the street segment level</li>
    <li>Time range: 1.5 hours after sunrise to 1.5 hours before sunset</li>
</ul>
</p>
<h4><u>Technical Implementation</u></h4>
<h5>Front-end</h5>
<p align='justify'>
<ul>
    <li><a href="https://angular.dev/">Angular framework</a> for component-based architecture</li>
    <li><a href="https://d3js.org/">D3.js</a> for creating interactive data visualizations</li>
    <li><a href="https://openlayers.org/">OpenLayers</a> for map rendering and interactions</li>
</ul>
</p>
<h5>Back-end</h5>
<p align='justify'>
<ul>
    <li><a href="https://flask.palletsprojects.com/">Flask</a> server to handle API requests</li>
    <li><a href="https://geopandas.org/">GeoPandas</a> for processing and serving geospatial data</li>
</ul>
</p>
<h4><u>Setup Instructions</u></h4>
<h5>Front-end setup:</h5>
<pre><code>ng new vis
cd vis
ng generate component map
ng generate component chart
ng generate service data
npm install --save-dev d3 ol @types/d3 @types/ol
npm install
</code></pre>
<h5>Back-end setup:</h5>
<pre><code>conda create --name geopandas
conda activate geopandas
conda install geopandas flask
</code></pre>
