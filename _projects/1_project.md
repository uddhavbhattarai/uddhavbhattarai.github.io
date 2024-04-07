---
layout: page
title: Robotic Blossom Thinning System
description: Robotic system for precision blossom thinning in tree fruit crops.
img: assets/img/OverallSystem.jpg
importance: 1
category: work
related_publications: true
---

The Robotic Blossom Thinning System consisted of machine vision system (Intel RealSense D435i) integrated with mechatronic system involving UR5e 6-degrees of freedom robotic manipulator and end-effector. End-effector was developed by using strings commercial trimmers. Initial segmentation of apple flower clusters was achieved through Mask-RCNN, followed by 3D cluster pose estimation. Manipulator motion planning utilized Robot Operating System (ROS) MoveIt. Thinning operations were executed by directing the end effector orthogonal to the cluster surface center or boundary. Details: {% cite bhattarai2023design %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/segmented_image_01.jpg" title="Segmentation results Mask R-CNN" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/closeup_orientation.png" title="Canopy with segmented clusters and their pose" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left] Segmentation results from Mask-RCNN algorithm during field trial. [Right] visualization of apple canopy. Different colored clusters represent different instances of segmentation results. The red arrows represent estimated cluster position and orientation, which were used to control the approach direction of the end-effector.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/OverallSystem.jpg" title="Overall integrated system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Integrated system during field evaluation in commercial apple orchard in Washington State, USA.
</div>

Two thinning approaches were used to evaluate the capability of system for proportional blossom thinning i) Boundary thinning: end-effector actuated around cluster boundary. ii) Center thinning: end -effector actuated at cluster centroid.

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ThinningStrategy-min_1.png" title="Images during field trial" class="img-fluid rounded z-depth-1" %}
    </div>

</div>
<div class="caption">
    Images depicting integrated system in action during the field evaluation.
</div>

Boundary thinning approach thinned 67.3% of flowers from the target clusters with cycle time of 9.0 seconds per cluster. Center thinning approach thinned 59.4% of flowers with cycle time of 7.2 seconds per cluster.

