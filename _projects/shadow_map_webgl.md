---
layout: page
title: Shadow Map WebGL
description: Shadow mapping for urban settings using WebGL
img: "assets/img/projects/shadow_map_webgl/thumbnail.gif"
importance: 10
category: Other
---

<h4><u>Access this project</u></h4>
<b>Demo URL:</b> <a href='https://komar41.github.io/shadow-maps-webgl/'>https://komar41.github.io/shadow-maps-webgl/</a> <br>
<b>GitHub repo:</b> <a href='https://github.com/komar41/shadow-maps-webgl/'>https://github.com/komar41/shadow-maps-webgl/</a> <br>
<b>Tools used:</b> WebGL, JavaScript, HTML, CSS.
<p align='justify'>
This project aims to implement shadow mapping techniques for urban settings using WebGL. By rendering shadows from directional light sources on 3D city models, we provide a tool for visualizing and analyzing shadow patterns in urban environments. The project incorporates multiple rendering techniques to showcase different aspects of shadow mapping, including perspective and orthographic projections, adjustable light directions, and optional advanced features.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/shadow-maps-webgl/raw/main/manhattan.gif" alt="Manhattan shadow" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>How to run</u></h4>
<p align='justify'>
<ol>
    <li>Go to the deployed site: <a href='https://komar41.github.io/shadow-maps-webgl/'>https://komar41.github.io/shadow-maps-webgl/</a></li>
    <li>Download the JSON file for <a href="https://fmiranda.me/courses/cs425-spring-2021/manhattan.json.zip">Manhattan</a> or <a href="https://fmiranda.me/courses/cs425-spring-2021/chicago.json.zip">Chicago</a>.</li>
    <li>Unzip the downloaded file to extract the JSON.</li>
    <li>In the configuration panel, locate the file input option.</li>
    <li>Click on the file input and select the extracted JSON file (manhattan.json or chicago.json).</li>
</ol>
</p>
<h4><u>Components</u></h4>
<h5>1. 3D Urban Model Rendering</h5>
<p align='justify'>
<ul>
    <li>Renders a 3D city model based on JSON file input</li>
    <li>Supports multiple layers: buildings, water, parks, and surface</li>
    <li>Uses unique buffer and VAO for each layer</li>
    <li>Implements normal-based shading for building sides</li>
</ul>
</p>
<h5>2. Shadow Mapping</h5>
<p align='justify'>
<ul>
    <li>Implements shadow mapping technique for directional light</li>
    <li>Supports both perspective and orthographic projections</li>
    <li>Allows adjustable light direction</li>
</ul>
</p>
<h5>3. Configuration Panel</h5>
<p align='justify'>
<ul>
    <li>Dropdown menu for projection type selection (perspective/orthographic)</li>
    <li>Slider for adjusting light direction (0-360 degrees)</li>
    <li>Checkbox for toggling shadow map texture display</li>
    <li>File input for loading JSON city models</li>
</ul>
</p>
<h5>4. Camera Controls</h5>
<p align='justify'>
<ul>
    <li>Interactive camera rotation around the model's centerpoint</li>
    <li>Smooth transitions between different viewpoints</li>
</ul>
</p>
<h5>5. Shadow Map Visualization</h5>
<p align='justify'>
<ul>
    <li>Renders the shadow map texture to screen when enabled</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/shadow-maps-webgl/raw/main/shadowmap.gif" alt="Shadow map" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>Interaction Features</u></h4>
<p align='justify'>
<ul>
    <li>Rotate camera view by moving the mouse around the canvas</li>
    <li>Adjust light direction using the slider</li>
    <li>Toggle between perspective and orthographic projections</li>
    <li>Upload custom city models in JSON format</li>
    <li>Optional: View raw shadow map texture</li>
</ul>
</p>
<h4><u>Technical Details</u></h4>
<p align='justify'>
<ul>
    <li>Implements multiple shader programs: ShadowMapProgram, RenderToScreenProgram, LayerProgram</li>
    <li>Uses Framebuffer Objects (FBO) for off-screen rendering</li>
    <li>Supports JSON file parsing for city model data</li>
    <li>Implements matrix operations for view, model, and projection transformations</li>
</ul>
</p>
<h4><u>Data Format</u></h4>
<p align='justify'>
The project uses a specific JSON format for city models, including:
<ul>
    <li>Coordinates, indices, and colors for buildings, water, parks, and surface layers</li>
    <li>Normal data for building layers</li>
</ul>
<b>Example JSON structure:</b>

<pre><code>{
    "buildings": {
        "coordinates": [...],
        "indices": [...],
        "normals": [...],
        "color": [r,g,b,a]
    },
    "water": {...},
    "parks": {...},
    "surface": {...}
}</code></pre>
</p>
