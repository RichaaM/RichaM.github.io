---
layout: page
title: Planning Optimal Low-Thrust Proximity Maneuvers
description: Planning and Decision-Making in Robotics
img: assets/img/dream_planning.gif
importance: 1
category: work
related_publications: 
---

This project was accomplished as part of my [Planning and Decision-Making in Robotics](https://www.cs.cmu.edu/~maxim/classes/robotplanning_grad/) class, taught by [Pr. Maxim Likhachev](http://www.cs.cmu.edu/~maxim/).

Designing low-thrust trajectories for spacecraft maneuvers involves significant challenges due to the highly nonlinear dynamics, limited control authority, and extensive duration of trajectories spanning weeks or months. To address this problem, we leverage RRT*, an optimal kinodynamic sampling-based planner, and incorporate a heuristic based on the Linear Quadratic Regulator (LQR) for node extension and distance computations. This heuristic employs the LQR cost-to-go metric to produce paths that are locally optimal and dynamically feasible according to the LQR's quadratic cost, leading to a more effective search within the state space. We demonstrate our algorithm in the case of spacecraft proximity operations with obstacles for varying values of penalty on the control action. Additionally, we assess the actual thrust usage through a custom Time-Varying LQR (TVLQR) to track the generated trajectory, demonstrating the effectiveness of our approach. 

The project code is available here (C++): [Github Repository](https://github.com/Ibrassow/optimal-sampling-low-thrust)


The final report is available here: [Submitted Report](https://drive.google.com/file/d/1PTZc9Sl97MjSKvq5S3sFOHdUj97W1TjP/view)


Here is an excerpt of the [Final Presentation Slides (3min)](https://docs.google.com/presentation/d/1NIKLd9NjFxcs-A3EObMwHn_rSwJb_773/edit?usp=sharing&ouid=109638445335937349831&rtpof=true&sd=true):

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/planning_proj/planning-pres1.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/planning_proj/planning-pres2.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/planning_proj/planning-pres3.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/planning_proj/planning-pres4.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/planning_proj/planning-pres5.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Live demo

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/planning_proj/sampling_demo.gif" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
