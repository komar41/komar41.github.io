---
layout: page
title: Gait Event Detection
description: A Bi-GRU model for automatic gait event detection using angle, marker, and force data
img: "assets/img/projects/gait_event_detection/architecture.png"
importance: 2
category: Research
related_publications: wang2025automatic
---

<h5 align='justify'>Automatic Gait Event Detection in Older Adults During Perturbed Walking </h5>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="../../assets/img/projects/gait_event_detection/architecture.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    
        <b>Figure:</b> Multi-layer neural network architecture featuring bidirectional GRU Layers for automatic gait event detection.
    
</div>

`Abstract`

<p align='justify'>
Accurate detection of gait events in older adults, particularly during perturbed walking, is essential for evaluating balance control and fall risk. Traditional force plate-based methods often face limitations in perturbed walking scenarios due to the difficulty in landing cleanly on the force plates. Subsequently, previous studies have not addressed gait event automatic detection methods for perturbed walking. This study introduces an automated gait event detection method using a bidirectional gated recurrent unit (Bi-GRU) model, leveraging ground reaction force, joint angles, and marker data, for both regular and perturbed walking scenarios from 307 healthy older adults. Our marker-based model achieved over 97% accuracy with a mean error of less than 14 ms in detecting touchdown (TD) and liftoff (LO) events for both walking scenarios. The results highlight the efficacy of kinematic approaches, demonstrating their potential in gait event detection for clinical settings. When integrated with wearable sensors or computer vision techniques, these methods enable real-time, precise monitoring of gait patterns, which is helpful for applying personalized programs for fall prevention. This work takes a significant step forward in automated gait analysis for perturbed walking, offering a reliable method for evaluating gait patterns, balance control, and fall risk in clinical settings.
</p>
