---
title: 'Autonomous Navigation System for Warehouse Robotics'
subtitle: 'Development and Integration of a Navigation Solution for the RB-1 Mobile Robot in a Warehouse Environment'
featured_image: 'project_data/2024-04-13-navigation-system/navigation.gif'
date: 2024-04-13
---

## Introduction
This project focuses on the implementation of an autonomous navigation system for the RB-1 mobile robot, designed to operate in a complex warehouse environment. Leveraging ROS 2, this initiative aimed to create, test, and refine a navigation system capable of real-time localization and route planning, ensuring efficient and safe robotic operations in warehouse settings.

## Objectives
- To create a detailed map of a simulated warehouse environment and localize the RB-1 within this map.
- To implement and configure the Nav2 system to manage navigation goals effectively.
- To set up a comprehensive navigation framework that integrates mapping, localization, and path planning functionalities.

## Tools and Technologies
- **Programming Languages:** Python, XML
- **Frameworks and Libraries:** ROS 2, Nav2, RViz2
- **Simulation Environment:** Gazebo
- **Version Control:** Git

## Source Code
- [GitHub Warehouse Navigation Repository](https://github.com/MiguelSolisSegura/warehouse_project)

## Process and Development
The development process is structured around three main components: mapping, localization, and navigation setup.

### Mapping
**Initial Setup:** Configured the ROS 2 environment and launched the Gazebo simulation of the warehouse.
**Mapping Implementation:** Utilized the Cartographer SLAM package to generate a real-time map of the simulated environment, which was visualized and verified using RViz2. The process was repeated for the real robot.

![Navigation System Visualization](/project_data/2024-04-13-navigation-system/mapping.gif)

### Localization
**AMCL Configuration:** Set up the Adaptive Monte Carlo Localization (AMCL) to ensure accurate robot positioning within the mapped environment.
**Testing and Validation:** Conducted tests in both simulated and real settings to confirm the effectiveness of the localization setup.

![Navigation System Visualization](/project_data/2024-04-13-navigation-system/localization.gif)

### Navigation Setup
**Nav2 Configuration:** Integrated and configured the Nav2 stack to handle navigation goals.
**Path Planning:** Developed a robust path planning system using the configured navigation nodes to allow the RB-1 to navigate autonomously and safely through the warehouse.

![Navigation System Visualization](/project_data/2024-04-13-navigation-system/navigation.gif)

## Results
The successful integration of the navigation system demonstrated the RB-1 robot's ability to autonomously navigate and adapt to the dynamic warehouse environment. The project highlighted the effectiveness of the Nav2 system and the importance of precise localization in complex indoor settings.

## Key Insights
- The critical role of accurate mapping in the success of autonomous navigation systems.
- The flexibility and robustness of ROS 2 and Nav2 in developing sophisticated robotic navigation solutions.
- Future improvements could include optimizing the navigation parameters for different types of warehouse layouts and conditions.


