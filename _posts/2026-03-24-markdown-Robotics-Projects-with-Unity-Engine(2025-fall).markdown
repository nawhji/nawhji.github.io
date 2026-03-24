---
title: "Robotics Projects with Unity Engine (Fall 2025)"
layout: post
date: 2025-03-24 14:00
headerImage: false
tags:
- Unity Engine
- Robotics
- Teleoperation
- Automation
- Shared Autonomy
star: false
projcets: true
author: Sehyun
Description: :)
---

During Fall 2025, I worked on three robotics projects in Unity Engine.

Although each project was different, they all shared the same core task: making a rocket or robot platform reach a target location. What changed from project to project was the way the robot was controlled. The first project focused on **teleoperation**, where a human directly controlled the robot. The second explored **automation**, where the robot navigated on its own. The third moved to **shared autonomy**, where human guidance and robot decision-making were combined in the same system.

## Project 1: Teleoperation

The first project was about building a system that allowed a human operator to directly control a rocket in Unity.

<video controls width="100%">
  <source src="{{ '/assets/videos/robotics/Project1.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

The final system used:

- a physical joystick for steering
- a brake input for speed control
- a two-engine synchronized rocket design

The key idea behind this project was straightforward: even if a robot is technically capable of complex movement, that does not automatically make it easy for a person to control. I tested different engine configurations and found that simpler designs often worked better in practice. The final two-engine synchronized setup was not the most complicated option, but it gave the operator the most stable and intuitive control. As a result, it was easier to steer the rocket precisely and reach the target reliably.

## Project 2: Automation

The second project shifted the focus from human control to autonomous control.

Here, the robot had to move through the course by itself. Instead of relying on an operator to decide when to turn, slow down, or correct its path, the control system had to make those decisions automatically.

<video controls width="100%">
  <source src="{{ '/assets/videos/robotics/Project2.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

The final system used:

- checkpoint-based navigation
- a hybrid turning strategy
- **Stop & Go** control for sharp corners
- **Smooth Move** control for gentle turns and curved sections

The reason for this design was that different parts of the course required different types of motion. Sharp turns demanded careful, controlled movement, while smoother sections rewarded continuous motion and higher speed. A single control strategy was not enough to handle both well. The final hybrid design combined the strengths of two approaches: it slowed down and turned carefully when precision was important, and it kept moving smoothly when the path allowed faster travel. This made the system both more stable and more efficient.

## Project 3: Shared Autonomy

The third project expanded the problem into a more complex multi-agent environment.

In this project, the system included a **mothership** and multiple **drones** moving through a maze-like space. The main challenge was deciding how much of the system should be controlled by the user and how much should be handled autonomously.

<video controls width="100%">
  <source src="{{ '/assets/videos/robotics/Project3.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

The final system used:

- a manually guided mothership
- cell-based path control for high-level movement
- Pure Pursuit-based smoothing for more natural motion
- autonomous drones for local exploration
- LiDAR-based sensing for navigation and obstacle detection

This design was chosen because making the entire system fully autonomous created too much complexity. If both the mothership and the drones tried to make all decisions on their own, coordination became much harder and the overall system was more difficult to manage. The final shared-autonomy design divided the roles more effectively: the user provided high-level guidance for the mothership, while the drones handled local exploration on their own. This made the system easier to control, easier to understand, and still capable of performing autonomous tasks where autonomy was most useful.

## Overall

Taken together, these three projects were a way of exploring three different ways robots can be controlled:

- direct human control
- full autonomous control
- a hybrid of human guidance and autonomous behavior

Working on them in sequence helped me compare not just what each approach could do, but also when each one made the most sense. In the end, the projects were not only about getting a robot to a destination, but also about understanding how control design affects usability, reliability, and system complexity.

👉 **For details, please [see the full reports](https://drive.google.com/drive/folders/169nSQI1yt9CRAS2JoC18Pr9eyPm98yVr).**