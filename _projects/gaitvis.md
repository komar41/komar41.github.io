---
layout: page
title: GaitVis
description: Visualization tool to explore gait features and differentiating healthy adults and patients
img: "assets/img/projects/gaitvis/thumbnail.png"
importance: 8
category: Other
---

<h4><u>Access this project</u></h4>
<b>Demo URL:</b> <a href='https://komar41.github.io/gaitvis'>https://komar41.github.io/gaitvis</a> <br>
<b>GitHub repo:</b> <a href='https://github.com/komar41/gaitvis'>https://github.com/komar41/gaitvis</a> <br>
<b>Demo Video:</b> <a href='https://youtu.be/Ma3Z5PUPIko'>https://youtu.be/Ma3Z5PUPIko</a> <br>
<b>Presentation:</b> <a href='https://github.com/komar41/gaitvis/blob/main/presentation.pptx'>https://github.com/komar41/gaitvis/blob/main/presentation.pptx</a> <br>
<b>Tools used:</b> Python, NumPy, Pandas, JavaScript, HTML, CSS, SVG, D3.js.
<p align='justify'>
GaitVis is a visualization tool designed to explore gait characteristics among stroke survivor patients and healthy older adults. The project aims to aid clinicians and researchers in effectively differentiating gait characteristics between these two groups. Additionally, it seeks to explore correlations between gait characteristics and gait recovery, potentially uncovering previously unseen patterns in the data and helping to transform rehabilitation strategies for stroke survivor patients.
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/Final.png" alt="GaitVis" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>Project Objectives</u></h4>
<p align='justify'>
<ul>
    <li>Explore correlations between gait features and stroke survivor patients' physical recovery time.</li>
    <li>Estimate the risk of falling for stroke survivor patients.</li>
    <li>Evaluate patients' current state and suggest appropriate training strategies.</li>
    <li>Compare gait characteristics between stroke survivor patients and healthy older adults.</li>
</ul>
</p>
<h4><u>Requirement Analysis</u></h4>
<h5>Users</h5>
<p align='justify'>
<ul>
    <li>Primary users: Gait researchers</li>
    <li>Secondary users: Clinicians of Physical Therapy</li>
    <li>Frequency: Users would access the system frequently</li>
</ul>
</p>
<h5>Tasks</h5>
<p align='justify'>
High-level tasks:
<ul>
    <li>Explore correlations between gait features and recovery time</li>
    <li>Estimate fall risk for stroke survivor patients</li>
    <li>Evaluate current patient state and suggest training strategies</li>
    <li>Compare gait characteristics between patient groups</li>
</ul>
Detailed tasks:
<ul>
    <li>Data access and filtering</li>
    <li>Computation of gait characteristics</li>
    <li>Statistical analysis</li>
    <li>Interactive visualizations</li>
    <li>Data export capabilities</li>
</ul>
</p>
<h5>Non-functional Requirements</h5>
<p align='justify'>
<ul>
    <li>Performance: Low latency visualizations and fast processing</li>
    <li>Privacy: Deidentified subject data</li>
    <li>Accessibility: Responsive UI for various screen sizes</li>
    <li>Usability: User-friendly interfaces for non-CS users</li>
    <li>Documentation: Step-by-step guide for new users</li>
</ul>
</p>
<h4><u>Data and Tasks Abstraction</u></h4>
<h5>Data Abstraction</h5>
<p align='justify'>
<ul>
    <li>Demographics data: Table with items (patients) and attributes (age, gender, height, etc.)</li>
    <li>Ground Reaction Force Data: Time-series table with force attributes</li>
    <li>Joint Angle Data: Time-series table with angle attributes</li>
</ul>
</p>
<h5>Task Abstraction</h5>
<p align='justify'>
<ul>
    <li>Analyze: Compare gait characteristics between groups and trials</li>
    <li>Search: Look up specific patient data or group data</li>
    <li>Filter: By property values, missing attributes, or extreme values</li>
    <li>Query: Identify patient information and statistics</li>
    <li>Compare: Ground reaction forces, joint angle data, and other gait features</li>
</ul>
</p>
<h4><u>State-of-the-Art Report</u></h4>
<p align='justify'>
<ul>
    <li>Existing tools like OpenSim, Tableau, and MATLAB have limitations in flexibility, interactivity, or specialization for gait analysis</li>
    <li>Previous research has focused on virtual environments, wearable technology, and specific patient groups</li>
    <li>Gaps identified in comparative analysis tools and comprehensive gait visualization systems</li>
</ul>
</p>
<h4><u>Functional Specifications</u></h4>
<h5>Scenarios</h5>
<p align='justify'>
<ul>
    <li>Statistical Representation of Patient Data</li>
    <li>Search and analyze the gait trial of a group of patients</li>
    <li>Compare two gait trials</li>
</ul>
</p>
<h5>Goals and Targets</h5>
<p align='justify'>
Low Targets:
<ul>
    <li>Display gait characteristics for a single trial</li>
    <li>Compute additional gait features</li>
    <li>Show data distribution of patients</li>
</ul>
Desirable Targets:
<ul>
    <li>Data filtering capabilities</li>
    <li>Comparison between trials or groups</li>
</ul>
High Targets:
<ul>
    <li>Create stick figure motion animation</li>
    <li>Estimate fall risk for patients</li>
</ul>
</p>
<h4><u>Prototypes</u></h4>
<p align='justify'>
Multiple iterations of prototypes were developed, focusing on different aspects:
<ul>
    <li>Statistical representation of patient data</li>
    <li>Group analysis capabilities</li>
    <li>Comparison of gait trials</li>
    <li>Novel GRF encoding</li>
    <li>Interactive features and linked views</li>
</ul>
</p>
<h5><ins>Sketches</ins></h5>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/s1-1.png" alt="Sketch 1" class="img-fluid rounded z-depth-1">
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/s1-2.png" alt="Sketch 2" class="img-fluid rounded z-depth-1">
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/s2-1.png" alt="Sketch 3" class="img-fluid rounded z-depth-1">
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/s2-2.png" alt="Sketch 4" class="img-fluid rounded z-depth-1">
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/s3-1.png" alt="Sketch 5" class="img-fluid rounded z-depth-1">
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/s3-2.png" alt="Sketch 6" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>Final Composite Sketch</u></h4>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/final-composite-sketch.png" alt="Final Composite Sketch" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>Final Visualization Components</u></h4>
<h5>1. Novel Ground Reaction Force (GRF) Encoding</h5>
<p align='justify'>
<ul>
    <li>Displays GRFs for both feet</li>
    <li>Updates based on selected trial and time slider</li>
    <li>GRF values divided into three groups: low, mid, and high</li>
    <li>Color-coded legend for anterior-posterior (AP), mediolateral (ML), and vertical (VT) forces</li>
    <li>Time slider controls the displayed timestep</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/novel-encoding.png" alt="Novel Ground Reaction Force (GRF) Encoding" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5>2. Line Charts for GRF and Joint Angle Values</h5>
<p align='justify'>
<ul>
    <li>Four line charts updated upon trial selection</li>
    <li>Legends indicate types of forces/angles</li>
    <li>Hover tooltips show exact force/angle values at each timestep</li>
    <li>Black and yellow dashed lines indicate toe-off and touch-down timesteps</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/time-series.png" alt="Line Charts for GRF and Joint Angle Values" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5>3. Histogram for Patient Feature Distribution</h5>
<p align='justify'>
<ul>
    <li>Located in the top-left section</li>
    <li>Displays distribution of general features (e.g., age, height, gender, ankle width)</li>
    <li>Represents data for the entire patient dataset</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/dist-dem.png" alt="Histogram for Patient Feature Distribution" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5>4. Spider Chart for Gait Feature Comparison</h5>
<p align='justify'>
<ul>
    <li>Positioned in the top-middle section</li>
    <li>Compares gait features for up to three trials</li>
    <li>Hover effect highlights the selected trial's spread</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/compare-trials.png" alt="Spider Chart for Gait Feature Comparison" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h5>5. Parallel Coordinate Plot for Group Comparison</h5>
<p align='justify'>
<ul>
    <li>Located in the top-right section</li>
    <li>Compares gait features between two different groups of patients</li>
    <li>Hover effect highlights the group a selected trial belongs to</li>
</ul>
</p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img src="https://github.com/komar41/gaitvis/raw/main/img/compare-patient-groups.png" alt="Parallel Coordinate Plot for Group Comparison" class="img-fluid rounded z-depth-1">
    </div>
</div>
<br>
<h4><u>Key Features</u></h4>
<p align='justify'>
<ul>
    <li>Interactive elements throughout all visualizations</li>
    <li>Linked updates between visualizations upon trial selection</li>
    <li>Ability to compare multiple trials and patient groups</li>
    <li>Time-based analysis for GRF and joint angle data</li>
</ul>
</p>
<h4><u>Current Limitations</u></h4>
<p align='justify'>
<ul>
    <li>Histogram, spider chart, and parallel coordinate plot use mock data (pending real data integration)</li>
    <li>Limited to comparing up to three trials in the spider chart</li>
</ul>
</p>
<h4><u>Future Enhancements</u></h4>
<p align='justify'>
<ul>
    <li>Integration of real patient data for all charts</li>
    <li>Implementation of brushing and linking between charts</li>
    <li>Addition of search and query options based on patient features</li>
    <li>Optimization of chart layout and positioning</li>
    <li>Option to switch between multi-patient and single-patient views</li>
</ul>
</p>

<h4><u>Technical Details</u></h4>
<p align='justify'>
<ul>
    <li>Technologies: HTML, CSS, JavaScript, D3.js, Python, Pandas</li>
    <li>Version Control: Git</li>
    <li>Hosted on GitHub Pages</li>
</ul>
</p>
<h4><u>Future Work</u></h4>
<p align='justify'>
<ul>
    <li>Integrate real patient data for histogram, spider chart, and parallel coordinate plot</li>
    <li>Implement brushing and linking between charts</li>
    <li>Add option to choose between multi-patient and single-patient views</li>
    <li>Optimize layout and positioning of plots</li>
    <li>Incorporate search and query options based on sociodemographic and gait features</li>
</ul>
</p>
<h4><u>Expert's Feedback</u></h4>
<p align='justify'>
<ul>
    <li>Expressed satisfaction with the project's progress and its potential as a visualization tool for gait analytics. Key points:</li>
    <li>Impressed with various tasks the interface can perform</li>
    <li>Appreciated the novel encoding for comparing force intensities</li>
    <li>Suggested implementing brushing and linking between charts</li>
    <li>Recommended adding options for multi-patient and single-patient views</li>
    <li>Suggested refining the overall positioning of plots</li>
    <li>Expressed satisfaction with the team's effort</li>
</ul>
Overall, the experts believed the project is on track to become a great visualization tool for gait analytics tasks.
</p>
<br>
<h4><u>Team</u></h4>
<p align='justify'>
<ul>
    <li>Kazi Shahrukh Omar</li>
    <li>Soham Pradhan</li>
    <li>Sajal Kherde</li>
    <li>Shuaijie Wang</li>
    <li>Tanvi Bhatt</li>
    <li>Fabio Miranda</li>
</ul>
</p>
