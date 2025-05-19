---
layout: page
title: Weakly-supervised deep learning framework for counting
description: 
img: assets/img/CountNet.png
importance: 2
category: Deep/Machine Learning, and Computer Vision
related_publications: true
---

Proposed CountNet, a weakly supervised deep learning framework for object counting that eliminates the need for labor-intensive bounding-box or pixel-level annotations. CountNet learns to count solely from image-level count labels, without explicit information about object identity or position. The architecture is intentionally simple and consists of three sequential components: a VGG-16 network for feature extraction, a Global Average Pooling (GAP) layer for dimensionality reduction, and a fully connected network for final count regression. This design enables CountNet to infer object counts from images using only the total number of objects as supervision, making it suitable for scenarios where detailed annotations are unavailable or costly to obtain. Details: {% cite bhattarai2022weakly %}

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/CountNet.png" title="CountNet Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Architecture of proposed CountNet. Countnet consisted sequential connection of VGG16, GAP, and fully connected network.
</div>
Experiments were conducted in images acquired in an unstructured commercial orchard environment. Once the count results were obtained, it was critically important to analyze and understand if the network was actually looking into the relevant features to come up with the specific count decision. To evaluate the functionality two activation map visualization techniques: Score-
CAM (highlight relevant regions) and Guided Backpropagation (highlights relevant flower and fruit features) were adopted and implemented.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/flowerfeatures.png" title="Analysis of activated flower features" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left/Top] Closeup view of apple canopy image  during full bloom. [Center] Highlighted regions contributing to count obtained from Score-CAM. [Right/Bottom] Highlighted features contributing to count obtained from Guided Backpropagation.
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/fruitfeatures.png" title="Analysis of activated fruit features" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left/Top] Closeup view of apple canopy image  during full bloom. [Center] Highlighted regions contributing to count obtained from Score-CAM. [Right/Bottom] Highlighted features contributing to count obtained from Guided Backpropagation.
</div>

The most activated features for flower images were petal edges for full bloom flowers, and late pink flower blob for Late Pink stage flowers. The most activated features for harvest ready apples were fruit edges and calyx (if present in image). Results showed 82.6% accuracy in counting flowers and 93.94% accuracy in counting apples. CountNet showed superior counting performance when compared to Local Binary Pattern (LBP) feature extraction followed by Kernel Ridge Regression (KRR).

<hr>
**SKILLS:** Python, OpenCV, PyTorch, NumPy, Pandas, Scikit-learn, Linux