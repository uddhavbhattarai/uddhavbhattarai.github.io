---
layout: page
title: Robotic Pollination System
description: Robotic system for precision pollination in tree fruit crops.
img: assets/img/Robotic_PollinationSetup.jpg
importance: 5
category: Robotics, and Control
giscus_comments: false
related_publications: true

---

Similar to blossom thinning system, the Robotic Pollination System consisted of machine vision system (Intel RealSense D435i) integrated with mechatronic system involving UR5e 6-degrees of freedom robotic manipulator and end-effector. The end-effector system consisted electrostatic sprayer system to spray positively charged pollen particles to apple flower clusters. Details: {% cite bhattarai2025vision %}.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Robotic_PollinationSetup.jpg" title="robotic pollination system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Integrated system during field evaluation.
</div>

The software architecture was divided into three distinct components: perception, planning and actuation as illustrated below.  The machine vision system consisted the pipeline for registered RGB-D data acquisition, flower cluster detection and segmentation, and 3D localization in the camera coordinate space. The planning component was responsible for controlling overall system operation and coordination with the machine vision and electrostatic sprayer whule managing maniuplator motion.

<div class="row justify-content-sm-center">
    <div class="col-sm-11 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/SoftwareArchitecturePollination.png" title="Software framework of robotic pollination system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Software framework of robotic pollination system.
</div>

Apple canopy branches were netted weeks prior to blooming. Nets were removed during experiement trial followed by re-netting to prevent post experiment pollination via natural pollination.


<div class="row justify-content-sm-center">
    <div class="col-sm-11 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/PollinationInAction.png" title="Robotic system in action during field trials" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Robotic system in action during field trials
</div>






<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Endeffectorcloseup.jpg" title="end-effector closeup view" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/HoneycrispGood.jpg" title="robotically pollinated Honeycrisp apples" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left/Top] Close-up view of electrostatic sprayer nozzle and camera. [Right/Bottom] Honeycrisp apples pollinated via robotic pollination.
</div>


The initial field trial results were promising. However, fruit set differed between apple varieties. In the Honeycrisp variety, the robotic pollination system achieved a fruit set of 34.8% of sprayed flowers with 87.5% of flower clusters having at least one fruit. In Fuji apples, it achieved lower pollination success, with 7.2% of sprayed flowers setting fruit and 20.6% of clusters having at least one fruit. The system cycle time was 6.5 seconds per cluster. Fruit quality was comparable to those from natural pollination. This is a promising first step. System needs further improvement to enhance viability of pollen solution, and comprehensive study on the optimal time window to spray pollen solution.

<hr>
**SKILLS:** Python, OpenCV, Open3D, TensorFlow, NumPy, Pandas, Robot Operating System (ROS), Linux, Arduino, Autodesk Inventor