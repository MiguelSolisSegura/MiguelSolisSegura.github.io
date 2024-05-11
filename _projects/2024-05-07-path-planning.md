---
title: 'Mobile Robot Path Planning with Nav2 and Dijkstra’s Algorithm'
subtitle: 'Implementing Dijkstra's Algorithm as an Exercise in Path Planning'
featured_image: 'project_data/2024-05-07-path-planning/cover.gif'
date: 2024-05-07
---

## Introduction
This project serves as a comprehensive demonstration of robotics theory and 3D kinematics through the simulation and control of a three-jointed anthropomorphic arm. It emphasizes the application of Denavit-Hartenberg (DH) parameters to meticulously compute both forward and inverse kinematics, showcasing a deep understanding of robotics principles in practical scenarios.

## Objectives
- To apply Denavit-Hartenberg parameters in setting up and validating kinematic models for a 3D robotic arm.
- To develop robust simulation and control systems that can accurately predict and manipulate joint behaviors in 3D space.

## Tools and Technologies

- **Programming Languages:** Python
- **Frameworks and Libraries:** ROS, RViz, Gazebo
- **Additional Tools:** Custom RQT plugins, visualization markers
- **Version Control:** Git

## Source Code
- [GitHub 3D Kinematics Repository](https://github.com/MiguelSolisSegura/arm_kinematics)

## Process and Development
The project followed a structured approach, focusing primarily on the kinematic analysis and control of the robotic arm.

### Kinematic Framework Setup
**Denavit-Hartenberg Configuration:** Precisely defined each joint and link using the DH parameters, which are crucial for the kinematic chain calculations.

**Simulation and Visualization:** Configured and launched the Gazebo and RViz environments to dynamically simulate and visualize the arm's movements based on the kinematic models.

### Kinematic Analysis and Validation
**Forward Kinematics:** Implemented scripts to calculate the position and orientation of the end-effector for given joint configurations, using the established DH parameters.

**Inverse Kinematics:** Developed and tested algorithms capable of determining viable joint configurations to achieve desired end-effector positions, ensuring the solutions respected physical joint constraints.

### Motion Planning
**Complex Path Following:** Engineered motion planning algorithms to command the arm along predetermined 3D trajectories, highlighting the arm’s capability to execute complex movements smoothly.

![](/project_data/2024-05-11-arm-kinematics/kinematics.gif)

## Results
The project effectively demonstrated the application of fundamental robotics theories in a 3D context, using kinematic calculations to drive realistic simulations and precise control of an anthropomorphic robotic arm.

## Key Insights
- Mastery of Denavit-Hartenberg parameters is essential for accurate kinematic modeling and control in robotics.
- Theoretical knowledge in robotics can be effectively translated into practical applications that simulate real-world scenarios.