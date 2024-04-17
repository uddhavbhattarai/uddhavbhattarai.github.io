---
layout: page
title: Algorithms for precision picker activity recognition and yield estimation
description:
img: assets/img/yieldmapthumbnail.png
importance: 1
category: work
---
Our team modified picking carts during strawberry harvesting by instrumenting them with load cells to measure weight, Global Positioning System (GPS) to locate carts, and Inertial Measurement Unit (IMU) to measure cart motion.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/strawberryharvestingsalinas.jpg" title="strawberry harvesting" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Typical strawberry harvesting in commercial field in Salinas, CA.
</div>

For picker activity recognition, a deep neural network based on Convolution Neural Network (CNN), Long Short Term Memory (LSTM) was developed to classify timeseries data into "Pick" and "NoPick". Input data from sensors involved mass, latutude, longitude, ax, ay, az.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/image7_annotated_example.png" title="input annotated data example" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Annotated data for traning the CNN-LSTM network. Data was annotated using automated labelling followed by manual refinement.
</div>

Mass, acceleration, and velocity data were annotated and utilized to tran the network.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/image9_output.png" title="picker activity recogntion result" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Output of the proposed picker activity recogntion algorithm.
</div>

Furthermore, the time series data, including weight, geo-location, velocity, and acceleration, were fed to a novel yield estimation software pipeline that involved multiple stages of data processing and conditioning algorithms that generate harvested day yield maps. These yield maps were then integrated to create a desired resolution yield map (e.g., 1.2 m x 1.2 m grid) for the entire harvesting season. Preliminary evaluation showed that the proposed approach achieved 85.1% accuracy (Pearson r = 0.94) in estimating the total harvested tray count when compared with the grower’s records used to compensate the pickers.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/image12_yield_map.png" title="yield map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Yield map for single harvest day.
</div>

**SKILLS:** Python, TensorFlow, Convolution Neural Network (CNN), Recurrent Neural Network (RNN), Long Short Term Memory (LSTM), NumPy, Pandas, Scikit-learn, Linux, QGIS, Raspberry Pi
