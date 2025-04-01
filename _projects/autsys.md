---
layout: page
title: Autonomous Systems Course Redesign
description:
img: assets/img/autsys/lab_arena.png
importance: 1
category: Robotics
---

I led the course redesign for our mobile robotics software development course called "Autonomous Systems". This redesign included all brand new content for lab assignments, final project, exam questions, and some lecture material. I researched and selected new hardware: ClearPath Robotics' Turtlebot4 to be used alongside the new ROS2 assignments.

Major skills for this project included Ubuntu, Networking, Python, ROS/ROS2, and mobile robotics theory.

<div class="row justify-content-around">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/ros_noetic.png" title="ROS Noetic Distro Image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/ros2_humble.png" title="ROS2 Humble Distro Image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    One of the major driving forces behind this course redesign is the emergence of ROS2, a new robot software development middleware replacing ROS (Robot Operating System).
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/autsys/lab_arena.png" title="Lab Arena and Turtlebot4" class="img-fluid rounded z-depth-1" %}
    </div>Lab Arena and Turtlebot4>
<div class="caption">
    We upgrade our robot platform from a small raspberry pi car kit to the Turtlebot4 platform. This includes improved hardware and sensors including optical encoder, 2D Lidar, and RGB-D camera.
</div>

We ran into a lot of challenges, especially with providing reliable environments for all the students using Windows computers-- ROS/ROS2 relies on Ubuntu. I provided reliable workstation solutions given extremely limited resources in a university computer lab shared between multiple engineering classes. I also developed custom configurations for virtual machines and robots. This allowed robot communication within university network requirements and despite high network traffic.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/autsys/robot_uctronics.jpg" title="Old robot uctronics" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Work In Progress
</div>

