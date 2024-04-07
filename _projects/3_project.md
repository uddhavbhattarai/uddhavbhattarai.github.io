---
layout: page
title: Weakly-supervised object counting
description: Deep regression-based weakly-supervised approach for flower and fruit counting in orchard images.
img: assets/img/CountNet.png
importance: 3
category: work
related_publications: true
---

CountNet consisted three computational blocks connected sequentially: VGG-16 as feature extraction block, Global Average Pooling (GAP) as feature reduction block, and fully connected network as count computation block. The counting process was weakly supervised in the sense that the neural network learns based only on the count information without any explicit information on the object of interest (flower/fruit). Details: {% cite bhattarai2022weakly %}

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/CountNet.png" title="CountNet Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Architecture of proposed CountNet. Countnet consisted sequential connection of VGG16, GAP, and fully connected network.
</div>
Experiments were conducted in images acquired in an unstructured commercial orchard environment. Once the count results were obtained was critically important to analyze and understand if the network was actually looking into the relevant features to come up with the specific count decision. To evaluate the functionality of CountNet twoactivation map visualization techniques: Score-
CAM (highlight relevant regions) and Guided Backpropagation (highlights relevant flower and fruit features) were adopted and implemented.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/flowerfeatures.png" title="Analysis of activated flower features" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left] Closeup view of apple canopy image  during full bloom. [Center] Highlighted regions contributing to count obtained from Score-CAM. [Right] Highlighted features contributing to count obtained from Guided Backpropagation.
</div>

The most activated features were petal edges for full bloom flowers, and late pink flower blob for Late Pink stage flowers.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/fruitfeatures.png" title="Analysis of activated fruit features" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left] Closeup view of apple canopy image  during full bloom. [Center] Highlighted regions contributing to count obtained from Score-CAM. [Right] Highlighted features contributing to count obtained from Guided Backpropagation.
</div>
The most activated features for were fruit edges and calyx (if present in image).

Results showed a lowest Mean Absolute
Error (MAE)/Root Mean Square Error (RMSE) of 12.0/18.4 (Avg. flowers/image:69) and 2.9/4.3 (Avg. apples/image:48) for the apple flower and fruit dataset respectively.
