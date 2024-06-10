---
title: 'Docker for Robotics: TortoiseBot Simulation and Real Robot Setup'
subtitle: 'Streamlining Robot Bringup with Docker Containers'
featured_image: 'project_data/2024-06-09-tortoisebot-docker/cover.gif'
date: 2024-06-09
---

## Introduction
Containerizing robot applications significantly simplifies the process of setting up and using robots. This project focuses on creating Docker images for managing the bringup of the TortoiseBot robot, both in simulation and with the real robot, using ROS1 and ROS2. By leveraging Docker, this project aims to make robotics more accessible and manageable.

## Objectives
- To create Docker images for the TortoiseBot simulation and real robot systems.
- To implement Docker Compose files for easy container management and bringup of TortoiseBot environments.
- To ensure seamless integration and operation of all TortoiseBot systems within Docker containers.

## Tools and Technologies

- **Programming Languages:** Shell scripting
- **Frameworks and Libraries:** ROS1, ROS2, Docker, Docker Compose
- **Simulation Environment:** Gazebo, RViz2
- **Version Control:** Git

## Source Code
- [GitHub TortoiseBot ROS1 Docker Repository](https://github.com/MiguelSolisSegura/tortoisebot_ros1_docker)
- [GitHub TortoiseBot ROS2 Docker Repository](https://github.com/MiguelSolisSegura/tortoisebot_ros2_docker)

## Process and Development
The project is divided into four main tasks, focusing on the development of Docker images and Docker Compose files for both ROS1 and ROS2 environments. All the images created were uploaded to [Docker Hub](https://hub.docker.com/repository/docker/miguelsolissegura/miguelsolissegura-cp22/general) to facilitate installation for new users.

![](/project_data/2024-06-09-tortoisebot-docker/cover.gif)

### Task 1: ROS1 Docker Simulation
**Initial Setup:** Involved setting up the simulation environment and creating the necessary Docker images.

**Docker Images:** 
- `tortoisebot-ros1-gazebo`: Contains everything needed for starting the Gazebo simulation.
- `tortoisebot-ros1-slam`: Contains the mapping system.
- `tortoisebot-ros1-waypoints`: Contains the waypoints action server.
- `tortoisebot-ros1-webapp`: Contains the TortoiseBot web application.

**Docker Compose:** A Docker Compose file was created to start all the containers simultaneously, ensuring all systems are up and running.

### Task 2: ROS2 Docker Simulation
**Initial Setup:** Involved setting up the ROS2 environment and creating the necessary Docker images.

**Docker Images:** 
- `tortoisebot-ros2-gazebo`: Contains everything needed for starting the Gazebo simulation in ROS2.
- `tortoisebot-ros2-slam`: Contains the mapping system, including RViz2 for visualization.

**Docker Compose:** A Docker Compose file was created to start the Gazebo simulation, mapping nodes, and RViz2 for visualization.

### Task 3: ROS1 Real Robot
**Initial Setup:** Involved preparing the real robot environment and creating the necessary Docker images.

**Docker Images:** 
- `tortoisebot-ros1-real`: Contains everything needed for starting all the real robot systems, including the camera and laser.
- `tortoisebot-ros1-slam-real`: Contains the mapping system for the real robot.

**Docker Compose:** A Docker Compose file was created to start all the containers on the real robot via SSH.

### Task 4: ROS2 Real Robot
**Initial Setup:** Involved preparing the ROS2 real robot environment and creating the necessary Docker images.

**Docker Images:** 
- `tortoisebot-ros2-real`: Contains everything needed for starting all the real robot systems, including the camera and laser.
- `tortoisebot-ros2-slam-real`: Contains the mapping system for the real robot.

**Docker Compose:** A Docker Compose file was created to start all the containers on the real robot via SSH.



## Results
The creation and deployment of Docker images for both ROS1 and ROS2 environments allowed for efficient and streamlined bringup of the TortoiseBot simulation and real robot systems. This project demonstrates the power of containerization in robotics, enabling easy setup, management, and scaling of complex robotic applications.

## Key Insights
- The use of Docker significantly simplifies the deployment and management of robotic systems, making them more accessible to users with varying levels of experience.
- Future work may explore the automation of Docker image updates and the integration of more advanced features within the Docker containers.

