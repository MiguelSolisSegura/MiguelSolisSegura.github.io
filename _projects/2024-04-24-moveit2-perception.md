---
title: 'Integrating Perception in Robotic Pick & Place Tasks'
subtitle: 'Enhancing Object Handling Automation with Advanced Perception Technologies'
featured_image: 'project_data/2024-04-24-moveit2-perception/pick_place_perception.gif'
date: 2024-04-24
---

## Introduction
Building on our [previous work](https://miguelsolissegura.com/project/moveit2-pick-place), this project enhances the basic Pick & Place operation by integrating perception capabilities. This development allows the robotic system to autonomously identify and locate objects to be manipulated, greatly improving task robustness and adaptability.

## Objectives
- Implement a perception node that detects and locates objects using a depth sensor.
- Integrate perception data into the Pick & Place sequence, enabling dynamic object handling based on real-time visual input.

## Tools and Technologies

- **Programming Languages:** C++
- **Frameworks and Libraries:** ROS 2, MoveIt2, Perception Pipeline
- **Robotics Hardware:** UR3e Robotic Arm, RGB-D Camera
- **Simulation Tools:** Gazebo, RViz
- **Version Control:** Git

## Source Code
- [GitHub Manipulation Project Repository](https://github.com/MiguelSolisSegura/manipulation_project)

## Process and Development
This project was divided into key development stages, focusing on the integration of perception technology with existing robotic control frameworks.

### Perception Node Development
**Setup:** Configured and tested the perception node to ensure accurate detection and localization of objects using the robot's mounted RGB-D camera.

**Integration:** Linked the perception node outputs directly to the MoveIt2 controlled Pick & Place task, allowing the robotic arm to adapt its operations based on real-time data.

![](/project_data/2024-04-24-moveit2-perception/pick_place_perception.gif)

### Real and Simulated Environment Testing
**Simulation Testing:** Validated the integrated system in a simulated environment to ensure accurate object detection and manipulation without any physical risks.

**Real Robot Testing:** After successful simulation tests, the system was implemented on the actual UR3e robotic arm to handle real objects, fine-tuning the perception algorithms and robotic movements for optimal performance.

## Results
The integration of perception technology allowed for a more dynamic and flexible robotic system. The UR3e arm successfully performed the Pick & Place tasks by dynamically locating and interacting with objects, demonstrating significant advancements over traditional pre-programmed robotic systems.

## Key Insights
- The project highlighted the importance of perception in robotic systems for increasing operational versatility and reliability.
- Further developments could include enhancing the system’s ability to handle objects of varying shapes and sizes and improving its responsiveness to changes in the environment.