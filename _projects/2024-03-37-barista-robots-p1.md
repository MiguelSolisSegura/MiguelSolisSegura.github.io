---
title: 'Development of a Simulated "Catch Me If You Can" Game with TF and URDF/XACRO (I)'
subtitle: 'Engineering a Dynamic Robot Chase Simulation Using Advanced Robotics Modeling Techniques'
featured_image: 'project_data/2024-03-27-barista-robots-p1/barista_robot.gif'
date: 2024-03-27
---

## Introduction
In the evolving landscape of robotics, the simulation of interactive and dynamic games poses a unique challenge and opportunity for learning. This project focuses on creating a "Catch Me If You Can" game simulation featuring two robotic characters, Rick and Morty, utilizing the Robot Operating System 2 (ROS2) along with URDF and XACRO for advanced robotic modeling. The project aims to simulate an engaging chase game where one robot attempts to escape while the other pursues, leveraging the power of TF frames for accurate localization and tracking.

## Objectives
- To model the robots using Unified Robot Description Format (URDF). 
- Enhance the design with XACRO macros for modular and maintainable code.

## Tools and Technologies

- **Programming Languages:** XML for URDF/XACRO
- **Frameworks and Libraries:** ROS2, urdf, ros_tf2
- **Simulation Environment:** Gazebo Classic
- **CAD & Modelling:** Autodesk Fusion, Blender
- **Version Control:** Git

## Source Code
- [GitHub Barista Robots Repository](https://github.com/MiguelSolisSegura/barista_robots)

## Process and Development
The development journey is bifurcated into creating the base robot model with URDF and refining the model using XACRO macros, alongside setting up a playful simulation environment. The robots were modeled after the following real barista robots:

![](/project_data/2024-03-27-barista-robots-p1/rick_and_morty.jpg)
![](/project_data/2024-03-27-barista-robots-p1/barista_robot_drawing.png)


### Base Robot Model Creation
**Initial Setup:** Commenced with cloning the essential repositories and configuring the Git environment tailored for the project requirements.

**Robot Modeling:** A detailed robot model for Rick and Morty was constructed using URDF, including elements like the mobile robot base, top plate, and sensory equipment such as a laser scanner and wheel encoders. To ensure precise modelling after the dimensions given, the parts of the robot were design in Autodesk Fusion and the textures were applied using Blender.

The final result was validated on RVIZ to ensure the correct position of link frames and laser sensor functionality.

![](/project_data/2024-03-27-barista-robots-p1/barista_robot.gif)

### Refinement with XACRO Macros
**XACRO Implementation:** Transitioned the URDF model to XACRO to utilize macros for a more modular and maintainable structure, facilitating easier updates and alterations to the robot model.

**Simulation Environment Setup:** Utilized Gazebo for the simulation environment, ensuring that the robots movements were accurate while controlled using the differential drive plugin.

![](/project_data/2024-03-27-barista-robots-p1/gazebo.png)

## Results
The culmination of this project is a fully functional simulation of the barista robot, showcasing the flexibility and capabilities of ROS2 alongside URDF and XACRO in robotic modeling. 

## Key Insights
- The project highlights the significance of modular design in robotics, showcasing the benefits of using XACRO over plain URDF for complex models.
- It is necessary to add a negligible inertia to reference links in order to avoid a fusion of them with other links in Gazebo. 
