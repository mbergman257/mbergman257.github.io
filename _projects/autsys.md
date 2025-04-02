---
layout: page
title: Robotics Course Redesign - Autonomous Systems
description:
img: assets/img/autsys/lab_arena.png
importance: 1
category: Robotics
---

Our robotics software development course, titled "Autonomous Systems", offers students practical experience with mobile robots and ROS -- a popular robotics middleware. In this project, I led an upgrade to the course content in both software and hardware; rebuilding our curriculum and lab content around ROS2 and Clearpath Robotics' Turtlebot4. This consisted of entirely new content for lab assignments, exam questions, and some lecture material. Additionally, I developed multi-robot and cross-OS(Windows/macOS/Ubuntu) solutions for challenging networking and IT requirements.

- Major skills for this project include: Ubuntu, networking, Python, ROS/ROS2, microcontrollers, and mobile robotics theory.

<div class="row justify-content-around">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/ros_noetic.png" title="ROS Noetic Distro" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/ros2_humble.png" title="ROS2 Humble Distro" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
Above are the final ROS distro (Noetic) and the ROS2 distro we moved to (Humble).
</div>
A major driving force behind the redesign is the emergence of ROS2, a new robot software development middleware replacing ROS (Robot Operating System). ROS2 relies on a fundamentally different communication protocol from ROS, resulting in significant changes to syntax and functionality. Part of this work included developing tutorials for students based on limited and evolving ROS2 documentation.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/lab_arena.png" title="Lab Arena and Turtlebot4" class="img-fluid rounded z-depth-1" %}
    </div>
<div class="caption">
    
</div>

While some old assignments could be translated, many labs needed new content because of different sensors on our hardware.

We ran into a lot of challenges, especially with providing reliable environments for all the students using Windows computers-- ROS/ROS2 relies on Ubuntu. I provided reliable workstation solutions given extremely limited resources in a university computer lab shared between multiple engineering classes. I also developed custom configurations for virtual machines and robots. This allowed robot communication within university network requirements and despite high network traffic.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autsys/robot_uctronics.jpg" title="UCTronics Robot Car Kit" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autsys/turtlebot4_web.jpg" title="Turtlebot4" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    We upgraded our robot platform from a small raspberry pi car kit to the Turtlebot4 platform. This includes improved hardware and sensors including optical encoder, 2D Lidar, and RGB-D camera.
</div>
