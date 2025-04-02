---
layout: page
title: Robotics Course Redesign - Autonomous Systems
description:
img: assets/img/autsys/lab_arena.png
importance: 1
category: Robotics
---

Our robotics software development course, titled "Autonomous Systems", offers students practical experience with mobile robots and ROS -- a popular robotics middleware. In this project, I led upgrades to software and hardware; rebuilding our curriculum and lab content around ROS2 and Clearpath Robotics' Turtlebot4. This consisted of entirely new content for lab assignments, exam questions, and some lecture material. Additionally, I developed multi-robot and cross-OS(Windows/macOS/Ubuntu) solutions for restrictive networking and IT requirements.

- Major skills for this project include: Ubuntu, networking, Python, ROS/ROS2, microcontrollers, and mobile robotics theory.

<div class="row justify-content-around">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/ros_noetic.png" title="ROS Noetic Distro" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/ros2_humble.png" title="ROS2 Humble Distro" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Above are the final ROS distro (Noetic) and the ROS2 distro we moved to (Humble).
</div>
The first motivator for the redesign was the emergence of ROS2, a new robot software development middleware replacing ROS (Robot Operating System). ROS2 relies on a fundamentally different communication protocol from ROS, resulting in significant changes to syntax and functionality. This meant new tutorials needed to be written, especially due to limited and still-evolving ROS2 documentation. Next, all of the applicable lab content needed to be translated to ROS2-based assignments. However, most of these were not applicable and instead I created new content, due to the next major factor of the redesign: new hardware.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autsys/robot_uctronics.jpg" title="UCTronics Robot Car Kit" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autsys/turtlebot4_web.jpg" title="Turtlebot4" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    We upgraded our robot platform from a small Raspberry Pi car kit to the Turtlebot4 robot. This includes improved hardware and advanced sensors including optical encoder, 2D Lidar, and RGB-D camera.
</div>

New hardware was a critical upgrade to let students implement their code. For example, students' navigation algorithms require a 2D lidar for localization, a sensor that the car kits did not have. For the upgrade, I researched and selected the Turtlebot4 robots, designed lab content, and wrote supporting code to aid students in those assignments.

We ran into a lot of challenges, especially with providing reliable environments for all the students using Windows computers-- ROS/ROS2 relies on Ubuntu. I provided workspace solutions, despite extremely limited resources in a shared university computer lab. I also developed custom configurations for virtual machines and robots allowing VM-to-robot communication within university network requirements and despite high network traffic.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/lab_arena.png" title="Lab Arena and Turtlebot4" class="img-fluid rounded z-depth-1" %}
    </div>
<div class="caption">
    A student maps a classroom maze with a tele-operated Turtlebot4 as part of the Autonomous Navigation unit.
</div>

This course has been offered 4 times before the upgrade and is now on its second offering after the upgrade. It is now part of the core curriculum of Purdue's Autonomy, IOT, and Robotics Professional Master's program.