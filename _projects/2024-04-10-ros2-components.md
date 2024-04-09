---
title: 'Component-Based Programming with ROS2'
subtitle: 'Transitioning to ROS2 Components for Enhanced Modularity and Efficiency'
featured_image: 'project_data/2024-04-10-ros2-components/robot_component_cover.gif'
date: 2024-04-10
---

## Introduction
This project explores the advanced programming paradigm introduced in ROS2, focusing on converting traditional ROS2 nodes into components for a more modular and efficient design. The RB1 robot, simulated within a warehouse environment, serves as the platform for this exploration. Through the conversion of [previously developed nodes](https://miguelsolissegura.com/project/shelf-attachment) into components, this project not only demonstrates the practicality of component-based programming in ROS2 but also evaluates the advantages and limitations of this approach in comparison to traditional node-based programming.

## Objectives
- Convert existing ROS2 nodes into components for the RB1 robot, enhancing modularity and system organization.
- Experience and assess the differences, including the advantages and disadvantages, between traditional node-based programming and component-based programming in ROS2.

## Tools and Technologies

- **Programming Languages:** Python, C++
- **Frameworks and Libraries:** ROS2, Gazebo
- **Robotics Hardware:** RB1 Robot by Robotnik
- **Version Control:** Git

## Source Code
- [GitHub Repository](https://github.com/MiguelSolisSegura/checkpoint9)

## Process and Development
The development process is structured around the conversion of existing ROS2 nodes from [this previous entry](https://miguelsolissegura.com/project/shelf-attachment) into components, specifically focusing on the tasks of pre-approaching and attaching the RB1 robot to a warehouse shelf.

### Node to Component Conversion
The project initiates by creating a new branch named `composition` in the existing repository and introducing a new ROS2 package called `my_components`. The first step involves converting the `pre_approach.cpp` node into a new component named `PreApproach`, which facilitates the robot's initial movement towards the shelf.

- **Pre-Approach Component:** This component replicates the pre-approach behavior with hardcoded values instead of parameters, guiding the robot to face the shelf directly.

### Service-Based Components for Shelf Attachment
Following the initial pre-approach phase, two new components, `AttachServer` and `AttachClient`, are developed to manage the final attachment process.

- **AttachServer Component:** Implements a service server for the `/approach_shelf` service, triggering the robot's final approach to attach to the shelf using the manual-composition approach.
- **AttachClient Component:** Contains a service client that calls the `/approach_shelf` service, enabling the robot to initiate the final approach and attachment using the run-time composition approach.

A launch file, `attach_to_shelf.launch.py`, is created to facilitate the execution of these components, illustrating the practical deployment of component-based programming in ROS2.

![](/project_data/2024-04-10-ros2-components/robot_component_cover.gif)

## Results
Through the conversion of traditional nodes into ROS2 components, this project showcases a great example of programming modularity and efficiency. The RB1 robot's successful shelf attachment within the simulated warehouse environment validates the effectiveness of component-based programming in ROS2, highlighting its potential for future robotic applications.

## Key Insights
- Component-based programming in ROS2 offers enhanced modularity, allowing for more organized and maintainable codebases.
- The transition from traditional node-based to component-based programming involves a learning curve but results in a more efficient and scalable system architecture.
- This project underscores the importance of embracing new programming paradigms in ROS2 to leverage the full potential of robotics development and deployment.