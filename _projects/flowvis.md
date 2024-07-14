---
layout: page
title: FlowVis
description: Computational fluid flow simulation of 3D point cloud data using three.js
img: "assets/img/projects/flowvis/thumbnail.png"
importance: 3
category: Other
---

<h4><u>Access this project</u></h4>
<b>Demo URL:</b> <a href='https://komar41.github.io/three-js-flow/'>https://komar41.github.io/three-js-flow/</a> <br>
<b>GitHub repo:</b> <a href='https://github.com/komar41/three-js-flow'>https://github.com/komar41/three-js-flow</a> <br>
<b>Tools used:</b> Three.js, D3.js, JavaScript, HTML, CSS.
<p align='justify'>
This project aims to visualize and analyze computational fluid flow simulation data from the San Diego Supercomputing Center using Three.js and D3.js. The goal is to create an interactive 3D visualization of the flow data, complemented by a linked 2D visualization. This project will provide insights into fluid dynamics while demonstrating various visualization techniques and interactions in a web-based environment.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/three-js-flow/raw/main/imgs/flow-final.png" alt="Flow Visualization with Three.js" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>Project Objectives</u></h4>
<p align='justify'>
<ul>
    <li>Load and display a 3D point cloud on the web</li>
    <li>Embed a 2D slice visualization within the 3D point cloud using D3.js</li>
    <li>Implement linked views, brushing and linking, view manipulation, and filtering</li>
</ul>
</p>
<h4><u>Visualization Components</u></h4>
<h5>1. 3D Point Cloud Visualization</h5>
<p align='justify'>
<ul>
    <li>Display the fluid flow data as a 3D point cloud</li>
    <li>Colormap the point cloud based on concentration values</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/three-js-flow/raw/main/imgs/flow-cylinder.png" alt="3D Point Cloud Visualization" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5>2. 2D Vertical Slice View</h5>
<p align='justify'>
<ul>
    <li>Create a second view using D3.js</li>
    <li>Display a vertical 2D slice of the data (XY slice with fixed Z value)</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/three-js-flow/raw/main/imgs/2d-vertical-slice.png" alt="2D Vertical Slice View" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5>3. Cut-Plane Filter</h5>
<p align='justify'>
<ul>
    <li>Add a vertical XY rectangle filter in the 3D view to link with the 2D slice within the 3D flow</li>
    <li>Allow user to move the rectangle through the flow along the Z axis</li>
</ul>

<h4><u>Interaction Features</u></h4>
<p align='justify'>
<ul>
    <li>Rotate the cylinder containing the flow</li>
    <li>Move the cut-plane filter along the Z axis</li>
    <li>Linked updates between 3D and 2D views</li>
</ul>
</p>
<h4><u>Data Source</u></h4>
<p align='justify'>
<ul>
    <li>Computational fluid flow simulation dataset from San Diego Supercomputing Center: <a href="http://www.uni-kl.de/sciviscontest/">http://www.uni-kl.de/sciviscontest/</a></li>
</ul>
</p>
<h4><u>Resources</u></h4>
<p align='justify'>
<ul>
    <li><a href="http://threejs.org/docs/">Three.js documentation and examples</a></li>
    <li><a href="https://stackoverflow.com/">Stack Overflow</a></li>
    <li><a href="https://d3-graph-gallery.com/">D3 Graph Gallery</a></li>
</ul>
</p>
