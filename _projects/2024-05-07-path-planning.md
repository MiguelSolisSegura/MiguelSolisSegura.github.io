---
title: 'Mobile Robot Path Planning with Nav2 and Dijkstra Algorithm'
subtitle: 'Implementing Dijkstra Algorithm as an Exercise in Path Planning'
featured_image: 'project_data/2024-05-07-path-planning/cover.gif'
date: 2024-05-07
---

## Introduction
Mobile robot path planning is a foundational skill in robotics, enabling robots to navigate environments autonomously and efficiently. This project served as an exercise in implementing Dijkstra's pathfinding algorithm from scratch using ROS2 and Nav2. By swapping out Nav2's default planner for a custom Dijkstra implementation, this project demonstrates how a widely recognized pathfinding algorithm can be used in a factory floor simulation to facilitate autonomous navigation.

## Objectives
- Replace the default Nav2 planner with a custom implementation of Dijkstra's Algorithm.
- Develop a functional pathfinding solution in C++ as a practical exercise in mobile robot navigation.

## Tools and Technologies
- **Programming Languages:** C++
- **Frameworks and Libraries:** ROS2, Nav2
- **Simulation Environment:** Gazebo
- **Version Control:** Git

## Source Code
- [GitHub Nav2 Dijkstra Planner Repository](https://github.com/MiguelSolisSegura/nav2_dijkstra_planner)

## Process and Development
The development process involved setting up the ROS2 workspace, configuring the Nav2 stack, implementing Dijkstra's pathfinding algorithm, and testing the solution within a simulated environment.

### Project Setup
**Environment Configuration:** The ROS2 workspace was prepared, and the starter code was cloned to initialize the Gazebo simulation and the Nav2 navigation stack.

**Planner Configuration:** In the Nav2 configuration file `planner_server.yaml`, the plugin for the `GridBased` planner was swapped to `nav2_dijkstra_planner/DijkstraGlobalPlanner`, pointing to the new planner's implementation.

**Simulation Launch:** Gazebo and Nav2 were launched to verify that the new planner loaded successfully and that the robot could be controlled via Rviz2.

### Implementation of Dijkstra’s Algorithm
**Initial Setup:** The initial setup required writing Dijkstra's pathfinding algorithm in C++ within the provided `nav2_dijkstra_planner.cpp` file.

**Algorithm Steps:**
- **Phase I:** Extract nodes with the lowest cost from the open list, marking them as visited while iterating toward the goal.

- **Case I and II:** Evaluate neighboring nodes based on whether they are already in the open list or closed list, updating their cost and parent nodes where necessary.

- **Phase II:** Once the goal is reached, the path is traced backward from the goal to the starting node using each node’s parent node.

**Testing and Verification:** The implementation was verified by launching Gazebo and Nav2 to ensure the new planner initialized correctly. Using Rviz2, goals were set at different locations on the map, and the robot navigated to them autonomously.

![](/project_data/2024-05-07-path-planning/robot_nav.gif)

## Results
The project successfully demonstrated how a well-known pathfinding algorithm like Dijkstra's could be implemented from scratch within the Nav2 framework. Although the planning process was slower than the default planner, the algorithm reliably computed paths that avoided obstacles and led the robot to the goal location.

## Key Insights
- Implementing a pathfinding algorithm requires careful attention to the logical flow and data structure setup.
- Variable names and comments play a crucial role in debugging and enhancing code readability.
- Although not optimized for speed, Dijkstra's Algorithm remains an effective pathfinding solution.
