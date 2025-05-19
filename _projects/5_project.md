---
layout: page
title: Multimodal time-series model for activity recognition and yield estimation
description:
img: assets/img/YieldMapFinal.png
importance: 1
category: Deep/Machine Learning, and Computer Vision
related_publications: true

---
Developed and deployed multimodal time-series CNN-LSTM model to analyze 3000+ hours of sensor data to recognize worker activity and productivity followed by large scale data pipeline to process 100+ million data points to estimate strawberry yield and generate yield maps at commercial scale. Details: {% cite bhattarai2025data %} and {% cite bhattarai2025precision %}.

Deployed over 60 sensor-integrated picking carts across 17,862 m² of commercial strawberry field during a multi-month harvest season (April–October). Each cart was equipped with GPS, 3D accelerometers, and load cells, continuously collecting data at 10 Hz for 8–10 hours per harvest day, twice a week, resulting in terabytes of multimodal data. This data was streamed to a cloud-based server and processed using a robust pipeline. One of the major design decision was to make the system low cost, scalable, and practical for commercial use. Instead of high-cost RTK-GPS units, we adopted freely available Satellite-Based Augmentation System (SBAS) based GPS modules with a rated circular error probable (CEP) of 0.75 meters. 
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/iCarrito.png" title="icarrito" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/CarritoFieldDeployment.jpg" title="strawberry harvesting" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left] Sensor integrated picking cart (iCarrito) used for data collection. [Right] iCarrito deployed in the field during strawberry harvesting.
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/image7_annotated_example.png" title="input annotated data example" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Annotated data for traning the CNN-LSTM network. Data was annotated using automated labelling followed by manual refinement.
</div>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/image9_output.png" title="picker activity recogntion result" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Plot of harvest weight data along with ground truth annotated data and predicted activity recognition results. 
</div>

The developed multimodal time-series CNN-LSTM model achieved an accuracy of over 97% in recognizing worker activity. The deep learning model was integrated with unsupervised algorithms to develop a large-scale data pipeline to estimate yield and generate high-fidelity yield maps. Mathematical formulations were developed to model typical worker patterns and were used to correct errors caused by the manual nature of harvesting, sensor limitations, and variation due to how pickers handled the sensing modules.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1_raw_locations_annotated.png" title="raw cart traces" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/YieldMapFinal.png" title="yield map final" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    [Left] Raw cart traces during the commercial strawberry harvest using the sensing modules. [Right] Generated cumulative yield maps at field resolution of 1.63 m². Red: very low yield, Yellow: below average yield, Green: above average yield, Blue: very high yield.
</div>

The accuracy of the estimated yield was better than 94% with strong correlation (Pearson r = 0.99) with the grounf truth data.

<hr>
**SKILLS:** Python, TensorFlow, MLflow, AWS, Docker, Recurrent Neural Network (RNN), Long Short Term Memory (LSTM), NumPy, Pandas, Scikit-learn, QGIS, Raspberry Pi

