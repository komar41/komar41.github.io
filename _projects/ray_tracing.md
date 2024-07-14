---
layout: page
title: Ray Tracing
description: Ray tracer using JavaScript and WebGL
img: "assets/img/projects/ray_tracing/thumbnail.png"
importance: 11
category: Other
---

<h4><u>Access this project</u></h4>
<b>Demo URL:</b> <a href='https://komar41.github.io/ray-tracing'>https://komar41.github.io/ray-tracing</a> <br>
<b>GitHub repo:</b> <a href='https://github.com/komar41/ray-tracing'>https://github.com/komar41/ray-tracing</a> <br>
<b>Tools used:</b> WebGL, JavaScript, HTML, CSS.
<p align='justify'>
This project implements a ray tracer using JavaScript. The application renders 3D scenes described in external JSON files, featuring camera attributes, objects (spheres and planes), and light sources. It demonstrates various lighting components and reflection effects.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/ray-tracing/raw/main/raytracer.png" alt="Assignment 3 example" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>How to Use</u></h4>
<p align='justify'>
<ol>
    <li>Visit the <a href='https://komar41.github.io/shadow-maps-webgl/'>live demo</a> or run the project locally.</li>
    <li>Use the configuration panel to upload a JSON scene file (e.g., <a href="https://github.com/komar41/ray-tracing/blob/main/scene-1.json">scene 1</a> or <a href="https://github.com/komar41/ray-tracing/blob/main/scene-2.json">scene 2</a>).</li>
    <li>Adjust rendering settings using the provided controls.</li>
    <li>Explore the rendered scene on the canvas.</li>
</ol>
</p>
<h4><u>Key Features</u></h4>
<h5>Ray Tracing Engine</h5>
<p align='justify'>
<ul>
    <li>Implements ray tracing algorithm for spheres and planes</li>
    <li>Calculates precise intersections between rays and objects</li>
    <li>Supports recursive ray tracing for reflections</li>
</ul>
</p>
<h5>Advanced Lighting Model</h5>
<p align='justify'>
<ul>
    <li>Utilizes Blinn-Phong shading model</li>
    <li>Incorporates ambient, diffuse, and specular lighting components</li>
    <li>Calculates shadows for realistic light interactions</li>
</ul>
</p>
<p align='justify'>
After adding ambient, the rendered scene should look like the following:
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/ray-tracing/raw/main/ambient.png" alt="Ambient component" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<p align='justify'>
After adding diffuse, the rendered scene should look like the following:
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/ray-tracing/raw/main/diffuse.png" alt="Diffuse component" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<p align='justify'>
After adding specular, the rendered scene should look like the following:
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/ray-tracing/raw/main/specular.png" alt="Specular component" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<p align='justify'>
Rendered scene with reflection considering a max depth of 1 should look like the following:
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/ray-tracing/raw/main/reflection_1.png" alt="Reflection component (depth 1)" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<p align='justify'>
Rendered scene with reflection considering a max depth of 5 should look like the following:
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/ray-tracing/raw/main/reflection_5.png" alt="Reflection component (depth 5)" class="img-fluid rounded z-depth-1" style="width: 50%;">
    </div>
</div>
<br>
<h5>Customizable Scene Rendering</h5>
<p align='justify'>
<ul>
    <li>Parses scene information from JSON files</li>
    <li>Supports flexible camera settings</li>
    <li>Allows for multiple light sources and object types</li>
</ul>
</p>
<h5>Interactive User Interface</h5>
<p align='justify'>
<ul>
    <li>Real-time rendering on HTML canvas</li>
    <li>Configuration panel for adjusting lighting components and reflection depth</li>
    <li>File upload functionality for custom scene descriptions</li>
</ul>
</p>
<h4><u>Technical Implementation</u></h4>
<h5>Core Classes</h5>
<p align='justify'>
<ol>
    <li><b>Ray:</b> Encapsulates ray properties (origin and direction)</li>
    <li><b>Intersection:</b> Stores intersection data (distance and point)</li>
    <li><b>Hit:</b> Combines intersection data with the intersected object</li>
</ol>
</p>
<h5>Key Functions</h5>
<p align='justify'>
<ul>
    <li><code>render()</code>: Initiates ray tracing for each pixel</li>
    <li><code>trace()</code>: Recursive function for tracing rays through the scene</li>
    <li><code>intersectObjects()</code>: Checks for intersections with all scene objects</li>
    <li><code>raySphereIntersection()</code> & <code>rayPlaneIntersection()</code>: Calculate specific object intersections</li>
    <li><code>shade()</code>: Applies the Blinn-Phong model and handles reflections</li>
    <li><code>isInShadow()</code>: Determines shadow casting for points</li>
</ul>
</p>
<h5>Utility Functions</h5>
<p align='justify'>
The project includes <code>utils.js</code> with vector operations such as:
<ul>
    <li>Dot product calculation</li>
    <li>Vector scaling, addition, and subtraction</li>
    <li>Vector length computation</li>
    <li>Ray reflection</li>
</ul>
</p>
<h4><u>Scene Description Format</u></h4>
<p align='justify'>
The application uses a JSON format for scene descriptions:
</p>
<pre><code>{
    "camera": {
        "position": [x, y, z],
        "fov": fovValue,
        "direction": [x, y, z]
    },
    "objects": [
        {
            "center": [x, y, z],
            "normal": [x, y, z],  // for planes
            "radius": value,      // for spheres
            "color": [r, g, b],
            "specularExponent": value,
            "specularK": value,
            "ambientK": value,
            "diffuseK": value,
            "reflectiveK": value,
            "type": "sphere" or "plane"
        }
    ],
    "lights": [
        {
            "position": [x, y, z]
        }
    ]
}</code></pre>
