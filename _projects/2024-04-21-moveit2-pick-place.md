---
title: 'Basic Pick & Place Task Using MoveIt2 and UR3e'
subtitle: 'Automating Object Manipulation with Advanced Robotic Arm Control'
featured_image: 'project_data/2024-04-21-moveit2-pick-place/pick_place_cover.gif'
date: 2024-04-21
---

## Introduction
This project focuses on using the MoveIt2 framework with the UR3e robotic arm to execute a basic Pick & Place task. The task involves automating the process of picking up an object from one location on a table and placing it in another, a fundamental yet pivotal operation in robotics aimed at enhancing efficiency in industrial applications.

## Objectives
- Configure and utilize the MoveIt2 package for the UR3e robotic arm.
- Develop a C++ program using the Move Group Interface API for automated sequence execution.

## Tools and Technologies

- **Programming Languages:** C++
- **Frameworks and Libraries:** ROS 2, MoveIt2
- **Robotics Hardware:** UR3e Robotic Arm
- **Simulation Tools:** Gazebo, RViz
- **Version Control:** Git

## Source Code
- [GitHub Manipulation Project Repository](https://github.com/MiguelSolisSegura/manipulation_project)

## Process and Development
The project involves several critical phases, each designed to ensure the system's functionality both in simulation and on the actual hardware.

### MoveIt2 Configuration
**Setup:** Configured MoveIt2 for the UR3e arm using a specific URDF file, prepared both simulation and real robot environments.

**Implementation:** Utilized the Move Group Interface in C++ to control the robotic arm's trajectory in picking and placing tasks.

### Simulation and Real Robot Testing
**Simulation Testing:** Conducted initial tests in a simulated environment using Gazebo and RViz to validate the setup and execution of the robotic movements.

**Real Robot Testing:** Applied the developed program in a real-world setting with the UR3e arm to test and refine the pick and place operations. Adjustments were made based on the robot’s performance to ensure precise and reliable task execution.

![](/project_data/2024-04-21-moveit2-pick-place/pick_place.gif)

## Results
The project successfully demonstrated the integration of advanced robotic programming and hardware manipulation. The UR3e arm effectively executed the designated tasks in both simulated and real environments, proving the system's applicability for real-world industrial automation.

## Key Insights
- The versatility of the MoveIt2 framework and its compatibility with ROS 2 facilitates sophisticated robotic manipulations.
- Testing in real-world conditions is crucial for transitioning robotic applications from simulation to practical deployment.
