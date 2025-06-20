---
layout: page
title: Multi-Task Perception System for Resource Constrained AUVs
description:
img: assets/img/detection/sys_diagram.jpg
importance: 1
category: Computer Vision
---

Autonomous Underwater Vehicle (AUV) perception systems often need to perform multiple perception tasks at once. Simply training a new model for each additional task places a heavy resource load on embedded devices -- which have limited storage, memory, and CPU throughput. Embedded device resource limitations mean auxiliary tasks such as wildlife detection may be replaced in favor of critical perception tasks.

- Major skills for this project include: Python, PyTorch, Ubuntu, Git, edge AI devices (Jetson Nano), and deep learning theory.

<div class="row justify-content-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/detection/sys_diagram.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Online Detection System Diagram
</div>

Additionally, the underwater domain has scarce realistic data, particularly for marine wildlife object detection. Existing large-scale, realistic, and varied datasets have labeling problems such as frequently missing annotations. This can heavily reduce accuracy.

<div class="row justify-content-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/detection/fnt_full_gt_sample.png" title="FathomNet GT" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sample ground-truth labeling for the FathomNet dataset. This is a valuable dataset due to its size and its realistic, varied images. However, missing annotations are common, as can be seen in the top-left and middle-left samples.
</div>

Between these two problems, automated wildlife detection on AUVs is a challenging goal.
We address these by developing a multi-task perception system with dynamically weighted loss functions, using a loss recalibration method to learn even from objects without annotations.

<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/detection/mtl_diagram.png" title="MTL Detection System Diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    MTL Detection System Diagram (best viewed in light mode)
</div>

Through our multi-task learning methodology, our model is able to learn three tasks using the same backbone: a critical perception task (docking station detection), an auxiliary wildlife detection task, as well as a training-only classification task used to supplement the training dataset with relevant underwater data.
