---
layout: page
title: Semi-supervised approach object density estimation, localization, and counting
description:
img: assets/img/DSC09300_overlaid.png
importance: 3
category: Deep/Machine Learning, and Computer Vision
related_publications: true

---

Proposed AgRegNet, a powerful attention-based deep regression network designed to simultaneously estimate density, localize, and count objects in complex scenes with minimal point annotations. It bypasses the need for complex and resource intensive object detection or polygon annotations, directly generating high-fidelity density maps whose pixel sum yields accurate object counts. Delivers high accuracy in both sparse and dense object distributions with heavy occlusion. Details: {% cite bhattarai2024agregnet %}


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_167.jpg" title="canopy image with early stage flowers" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/IMG_167_overlaid.png" title="canopy with overlaid density map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left/Top] Canopy image with early stage flower. [Right/Bottom] Canopy with early stage flower with overlaid density map generated from proposed approach.
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
    [Left/Top] Canopy image with full bloom flower. [Right/Bottom] Canopy with full bloom flower with overlaid density map generated from proposed approach.
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
    [Left/Top] Canopy image with harvest ready apples. [Right/Bottom] Canopy with harvest ready apples with overlaid density map generated from proposed approach.
</div>

Once the density maps were generated, a post-processing algorithm was developed to estimate flower and fruit location. The individual flowers and fruits were localized by identifying local peaks corresponding to object centroids. The predicted peaks were then matched to ground truth annotations using a bipartite graph matching with the Hungarian algorithm for precise one-to-one correspondence.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2d_wall_opened_IMG_20.png" title="canopy image with harvest ready apples" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2d_wall_fruit_000774.jpg" title="canopy with overlaid density map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Zoom in for better view] Localization results for full bloom flowers and harvest heady apples. Red: ground truth, Blue: True Positive, Magenta: False Negative, and Yellow: False positive. Cyan: Line connecting ground truth to the true positive
</div>

For flower images, AgRegNet achieved density map similarity score of 93.8 out of 100, an object counting accuracy of 87.3%, and a localization accuracy score of 0.81 (on a scale of 0 to 1). For fruit images, the model reached a density map similarity score of 91.0, counting accuracy of 94.4%, and a localization accuracy of 0.93, demonstrating strong performance in both visual scene understanding and object localization.

[Contact me](mailto:uddhavbhattarai@outlook.com) for code and dataset.
<hr>
**SKILLS:** Python, OpenCV, PyTorch, NumPy, Pandas, Scikit-learn, Linux  
