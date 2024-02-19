---
layout: page
title: AfternoonTea
description: Human activity understanding with computer vision
img: assets/img/afternoontea-thumbnail.png
importance: 3
category: projects
---

### Overview

This project employed an RGB-D sensor integrated with a SLAM system on a head-mounted camera. The goals consisted of:

- Given a 3D model for each object, track each of these objects in the environment.
- Detect user actions (e.g cooking, mixing, etc).


### Perception and localization

The SLAM system consistently tracked the head-mounted camera's pose, keeping the table within a fixed reference frame. Since we wanted to track the objects in the environment, it was necessary to keep track of the camera position with respect to a fixed coordinate frame in the scene. Therefore, a RGB-D SLAM system was employed to achieve that.

### Instance segmentation and object pose estimation

An instance segmentation module identified individual objects on the table, creating unique masks for each. These masks, when used in conjunction with depth information, enabled the computation of a point cloud for each object, which was then fed into an [ICP](https://en.wikipedia.org/wiki/Iterative_closest_point)-based tracking pipeline.

### Action classification

The project also featured an action classification module. By processing sequences of frames with an LSTM neural network, the system could classify user actions based on human movement.

Check the video below in order to visualize the final result!

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <iframe width="768" height="512" src="https://www.youtube.com/embed/E8QOpry4VkY" frameborder="0" allowfullscreen></iframe>
    </div>
</div>
