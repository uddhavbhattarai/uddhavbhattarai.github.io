---
layout: page
title: deep regression based object density estimation, localization, and counting
description:
img: assets/img/DSC09300_overlaid.png
importance: 5
category: work
---
We propose a deep regression-based approach that leverages dot annotations to estimate flower and fruit density, location and count. It avoids the complex and time-consuming process of explicitly detecting and counting each object. Instead, the model directly predicts a density map where the sum of pixel intensities corresponds to the flower or fruit count.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_167.jpg" title="canopy image with early stage flowers" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_167_overlaid.png" title="canopy with overlaid density map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left] Canopy image with early stage flower. [Right] Canopy with early stage flower with overlaid density map generated from proposed approach.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/DSC09300.jpg" title="canopy image with full bloom flowers" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/DSC09300_overlaid.png" title="canopy with overlaid density map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left] Canopy image with full bloom flower. [Right] Canopy with full bloom flower with overlaid density map generated from proposed approach.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/000281.png" title="canopy image with harvest ready apples" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/000281_overlaid.png" title="canopy with overlaid density map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left] Canopy image with harvest ready apples. [Right] Canopy with harvest ready apples with overlaid density map generated from proposed approach.
</div>

Once the density maps were generated post-processing algorithm was developed to estimate flower and fruit location.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2d_wall_opened_IMG_20.png" title="canopy image with harvest ready apples" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2d_wall_fruit_000774.jpg" title="canopy with overlaid density map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Localization results for full bloom flowers and harvest heady apples.
</div>