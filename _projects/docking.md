---
layout: page
title: Autonomous Underwater Docking and Recharging
description:
img: assets/img/docking/iver.png
importance: 1
category: Robotics
---

Autonomous Underwater Vehicles (AUVs) must be recovered manually in order to recharge. This project automates that by developing an autonomous docking strategy for AUVs. Since AUVs cannot receive GPS signal underwater, localization for underwater docking must be performed another way-- such as vision.

- Major skills for this project include: Python, Ubuntu, ROS, PyTorch, Git, CNNs, navigation algorithms, microcontrollers, field robotics, and deep learning.

<div class="row justify-content-around">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/docking/recovering_manual.jpg" title="Courtesy of Thunder Bay 2010 Expedition, NOAA-OER" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/docking/recovering_mechanical.jpg" title="Courtesy of Thunder Bay 2010 Expedition, NOAA-OER" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    AUV recovery is labor intensive, and makes long-term underwater missions costly. Often, AUVs are first retrieved manually by a small boat (left), then winched onto a larger vessel (right). Images courtesy of <a href="https://oceanexplorer.noaa.gov/explorations/10thunderbay/background/recovering/recovering.html" target="_blank">Thunder Bay 2010 Expedition</a>, NOAA-OER.
</div>

Our autonomous docking strategy consists of using dead-reckoning to estimate the AUV's pose, then switching to vision for fine-grained localization up until the (hopefully successful) docking attempt. We place a light beacon on the docking station for low-visibility waters, like the lake we often tested in.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/docking/iver.png" title="AUV and Docking Station" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The AUV we used to validate our methods is the IVER3 AUV (top left). A flat-funnel shaped docking station is used with a light beacon for autonomous visual identification (top right). The AUV and recharging station's electrodes make contact when the AUV is fully docked into the flat funnel (bottom).
</div>

At first, we attempted classical computer vision techniques to detect the light beacon, such as blob detection and brightest pixel methods. However, bubbles and sunlight interactions with the surface interfered heavily with these classical methods. We moved to a CNN-based method to learn a more robust model. I developed the CNN and integrated it into the AUV's perception system.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/docking/inference.jpg" title="CNN Inference Docking Station" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sample inference output of docking station detection CNN. Model both classifies whether a docking station is present and provides localization of the detected docking station.
</div>

I also provided engineering work, including installing new communications, camera, and power distribution systems in the AUV. I performed field work, testing our strategies at a local lake. Finally, over 4 days of field testing, we achieved a success rate of 71% (control has <5% success rate). Overall, this can be considered a major success and a step towards persistent underwater autonomy with AUVs. This work is currently under review at IEEE Journal of Ocean Engineering.
