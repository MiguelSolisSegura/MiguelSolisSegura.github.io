---
title: 'Development of a Simulated "Catch Me If You Can" Game with TF and URDF (II)'
subtitle: 'Enhancing Robotics Simulation with Interactive Chase Mechanics'
featured_image: 'project_data/2024-03-31-barista-robots-p2/robot_chase.gif'
date: 2024-03-31
---

## Introduction
The adventure of Rick and Morty, the café robots, continues with the advanced robot chase simulation project. Building on the initial robot modeling work, this phase introduces dynamic interaction between the two robots. Leveraging ROS2, TF (Transform Frames), and C++, an engaging "Catch Me If You Can" game is developed, where Rick actively pursues Morty within a simulated environment. This project illustrates the application of TF in robotics for real-time tracking and interaction.

## Objectives
- To simulate a dynamic and interactive chase game within a Gazebo environment, showcasing the use of TF for robot tracking.
- To develop a ROS2 node in C++ that enables one robot to chase another based on real-time location data.

## Tools and Technologies

- **Programming Languages:** C++
- **Frameworks and Libraries:** ROS2, TF2
- **Simulation Environment:** Gazebo Classic
- **Version Control:** Git

## Source Code
- [GitHub Robot Chase Repository](https://github.com/MiguelSolisSegura/robot_chase)
- [Related Project](https://miguelsolissegura.com/project/barista-robots-p1)

## Process and Development
The project is segmented into simulating multiple robots within the same environment and implementing the chase logic.

### Simulation of Multiple Robots
**Launching Multiple Robots:** A new launch file, `barista_two_robots.launch.py`, is introduced to initialize Gazebo and Rviz with both robot models simultaneously, ensuring unique namespaces to avoid any conflicts in node names, topics, and TF frames.

### Robot Chase Implementation
**Chase Algorithm Development:** In the `robot_chase` ROS2 package, a C++ node is crafted that continuously calculates the distance and angle between Rick and Morty using TF. Based on these calculations, Rick adjusts his velocity to chase Morty within the simulation.

![](/project_data/2024-03-31-barista-robots-p2/rviz.png)

**Interactive Chase Mechanics:** Using `teleop_twist_keyboard`, the movements of Morty are controlled, testing the responsiveness and agility of Rick's pursuit algorithms in real-time.

![](/project_data/2024-03-31-barista-robots-p2/robot_chase.gif)

## Results
This project's completion has enabled a working simulation where one robot, Rick, can chase another, Morty, in real time. By utilizing ROS2 and TF, the game demonstrates an effective use of transformation frames for tracking and interaction in a robotics context. Rick's pursuit of Morty in the simulation offers a glimpse into how TF can be applied to create interactive robot behaviors, even in scenarios that might involve dozens of robotic units.

## Key Insights
- Frame ids published by sensors are critical to properly represent their data in Rviz with multi-robot setups.
- Future enhancements could explore more complex chase strategies, incorporating obstacle avoidance and path planning to enrich the dynamics of the game.

