---
title: 'Simulation and Control Design in RB-1 Robotnik Robot'
subtitle: 'Practical Applications of ROS, Gazebo, and Autodesk Fusion in Robotics'
featured_image: 'project_data/2024-03-05-gazebo/cover.gif'
date: 2024-03-08
---

## Introduction 

The Robotics Operating System (ROS) and Gazebo are pivotal in robotics, offering a framework for developing robot software and a simulation environment for testing robotic systems, respectively. This portfolio entry, 'Simulation and Control Design in RB-1 Robotnik Robot,' showcases the use of ROS and Gazebo, along with Autodesk Fusion, to develop a simplified version of the RB-1 Robotnik robot. Highlighting the integration of these tools in robot simulation and control, this project exemplifies how such technologies are crucial for advancing robotics research and development. Through this work, the entry illustrates the key role of ROS and Gazebo in facilitating the complex process of robotic system design and testing, contributing valuable insights into the field of robotics.

## Objectives
- Create a detailed Gazebo simulation of the RB-1 Robotnik, emphasizing accurate structure and sensor simulation.
- Develop custom ROS services to enhance the RB-1 Robotnik's control and interaction within its simulated environment.

## Tools and Technologies
- ROS (Robot Operating System)
- Gazebo and Gazebo Classic for simulation
- RViz for component visualization
- Autodesk Fusion for part schematic design
- C++ for ROS node development
- Custom ROS services for added functionalities

## Source Code 
[GitHub Repository](https://github.com/MiguelSolisSegura/my_rb1_robot)

## Process and Development

### Foundation: Simulating RB-1 Robotnik
The project initiated with the RB-1 Robotnik's definition using the Unified Robot Description Format (URDF), followed by component visualization with RViz. Part schematics were meticulously designed in Autodesk Fusion, ensuring an accurate representation of the robot's model for simulation.

![](/project_data/2024-03-05-gazebo/dimensions.png)

![](/project_data/2024-03-05-gazebo/rviz.gif)

In Gazebo, the simulated environment was prepared for the robot's mobility, facilitated by a differential drive mechanism. This setup was essential for enabling smooth navigation. Furthermore, a Lidar sensor was integrated into the robot's model to enhance its ability to navigate by detecting obstacles and mapping its surroundings.

![](/project_data/2024-03-05-gazebo/motion_reduced.gif)

### Control Enhancement: Custom ROS Services
The development phase extended to improving the robot's control through custom ROS services. A new package, `my_rb1_ros`, was created to house the `rotate_service.cpp` script, introducing a service that allowed for the robot to be rotated based on user input specifying the desired angle.

A custom ROS message, `Rotate.srv`, was defined to facilitate the command and feedback mechanism, enabling users to request a rotation and receive acknowledgment upon completion. The precision of movement was ensured through the utilization of Odometry data, which proved vital for accurate control.

![](/project_data/2024-03-08-ros/spin.gif)

## Results
The culmination of this project saw the RB-1 Robotnik capable of not only basic navigation within its environment but also responding to enhanced control commands for rotation, making the simulation more interactive. The development process provided valuable insights into both the foundational aspects of robotic simulation and the complexities of implementing custom control mechanisms.

## Key Insights
- Establishing a robust simulation environment is fundamental before introducing more sophisticated functionalities.
- The integration of custom ROS services significantly improves the simulation's interactivity and control capabilities.
- Achieving precise control, such as accurate rotation, is reliant on a thorough understanding and application of Odometry data.