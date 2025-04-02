---
layout: page
title: Hierarchical Image Classification for Long-Tailed Datasets
description:
img: assets/img/classifier/arch.png
importance:
category: Computer Vision
---

Wildlife image recognition is critical for fisheries, environmental and ecological research, and wildlife conservation. AUVs and vision methods are being increasingly used, however, marine biologists spend a lot of time re-training and re-developing new classification models because those models are not generalizable enough for use in a variety of wildlife populations. In this work I develop a generalizable hierarchical classifier for wildlife taxonomy in order to reduce time spent by researchers on vision model development.

- Major skills for this project include: Python, PyTorch, Ubuntu, CUDA, deep learning theory, and probability.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/classifier/hierarchical_constraint.png" title="Hierarchical Constraint" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/classifier/lt_distr.png" title="Long-Tailed Distribution" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/classifier/unknown_distr.png" title="Unknown Distribution" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Hierarchical Constraint. Middle: Long-Tailed Class Distribution. Right: Unknown Test Distribution. 
</div>

There are a few major challenges with wildlife taxonomy classification. These include the hierarchical constraint associated with taxonomic labeling, long-tailed/imbalanced class distributions, unknown class distributions at inference, and fine-grained visual features. Each of these challenges add a level of complexity to the classification problem, but they all may be addressed with a clever architecture:

<div class="row justify-content-center">
    <div class="col-sm-9 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/classifier/arch.png" title="Classifier Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    I developed a hierarchical classifier based on two state-of-the-art image classification methods. Together they address the three main challenges shown above. This classifier can simply be used alongside an off-the-shelf transformer backbone, which helps with the fine-grained features challenge.
</div>

This project was a major part of my master's thesis. I used Python and PyTorch for all training and inference code, as well as some basic bash scripts to help automate the trials. The training environment was in Ubuntu and accelerated with CUDA. I used quite a bit of deep learning theory from my coursework to design the model architecture.

This work outperforms the baseline in nearly all accuracy metrics, demonstrating improved generalizability to new domains such as new ecosystems or ever-changing wildlife populations! Keep an eye out for the final publication as it goes through the review process!
