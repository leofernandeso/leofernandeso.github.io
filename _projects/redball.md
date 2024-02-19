---
layout: page
title: Task space control tracking with a UR-10 robot
description: Tracking objects with an UR10 robot.
img: assets/img/ur10.png
importance: 2
category: projects
---

### Overview

In a project for the Multisensory Robot Dynamic Manipulation course at TUM, I developed a task space controller for an UR-10 robot, enabling it to accurately track a red marker within its environment. This task was accomplished by integrating advanced control algorithms with a simplistic yet effective perception system, utilizing a RGB-D sensor to detect and locate the marker.

### Task space control

Task space control focuses on manipulating the end effector's (the tip of the robot) position and orientation to perform specific tasks. One of the primary challenges in implementing task space control is the infinite joint configurations that can achieve a single end effector position. The designed controller must cope with this fact by selecting the appropriate joint configuration in order to achieve the desired task.

Managing the UR-10 robot's six degrees of freedom for target tracking demanded a robust understanding of robot kinematics, dynamics, and control theory.

### Perception

The perception system for this project was the simplest/easiest you can think of. We used a calibrated RGB-D sensor in order to firstly locate the red/blue objects on the scene. After having the 2D pixel location of each one of them, we used a pinhole camera model to convert the 2D pixel locations and depth information into 3D coordinates. Since the computed coordinates might be quite noisy during tracking, we employed a simple complementary filter to get a more robust estimate of the object's 3D position.


### Final result
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <iframe width="768" height="512" src="https://www.youtube.com/embed/mMIfzPUeDyQ" frameborder="0" allowfullscreen></iframe>
    </div>
</div>

<br/>
<br/>
<br/>
<br/>

### Simulation with tracking

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <iframe width="768" height="512" src="https://www.youtube.com/embed/PlwzS3ZSvSQ" frameborder="0" allowfullscreen></iframe>
    </div>
</div>
