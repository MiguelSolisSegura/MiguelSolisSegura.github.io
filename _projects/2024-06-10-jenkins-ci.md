---
title: 'Continuous Integration for Robotics with Jenkins'
subtitle: 'Automating CI Processes for ROS1 and ROS2 Projects'
featured_image: 'project_data/2024-06-10-jenkins-ci/cover.gif'
date: 2024-06-10
---

## Introduction
Continuous Integration (CI) is essential in modern software development, ensuring that code changes are automatically tested and integrated, leading to more robust and reliable software. This project focuses on setting up a CI pipeline using Jenkins for ROS1 and ROS2 projects, automating the process to be triggered whenever a commit is pushed to a remote repository.

## Objectives
- To create a continuous integration pipeline using Jenkins for both ROS1 and ROS2 environments.
- To automate the testing and deployment processes for TortoiseBot simulation and waypoints action server.
- To ensure that the CI pipeline is triggered upon new commits or pull requests to the respective repositories.

## Tools and Technologies

- **Programming Languages:** Shell scripting, YAML
- **Frameworks and Libraries:** ROS1 Noetic, ROS2 Galactic, Jenkins, Docker, Docker Compose
- **Simulation Environment:** Gazebo
- **Version Control:** Git

## Source Code
- [GitHub ROS1 CI Repository](https://github.com/MiguelSolisSegura/ros1_ci)
- [GitHub ROS2 CI Repository](https://github.com/MiguelSolisSegura/ros2_ci)

## Process and Development
The project is divided into two main tasks, focusing on setting up CI pipelines for ROS1 and ROS2 environments using Jenkins and Docker.

### Task 1: ROS1 CI Pipeline
**Initial Setup:** Involved setting up the ROS1 environment and creating the necessary Docker image for the TortoiseBot simulation.

**Dockerfile Creation:** A Dockerfile was created to set up ROS Noetic, required Gazebo packages, TortoiseBot simulation packages, and the tortoisebot_waypoints package from Checkpoint 23.

**Jenkins Project Setup:**
- Created a Jenkins project to build the Docker image.
- Configured the project to run waypoints action server tests inside the Docker container.
- Automated the Jenkins project to build and test whenever a new pull request is accepted in the ros1_ci repository.

### Task 2: ROS2 CI Pipeline
**Initial Setup:** Involved setting up the ROS2 environment and creating the necessary Docker image for the TortoiseBot simulation.

**Dockerfile Creation:** A Dockerfile was created to set up ROS Galactic, required Gazebo packages, TortoiseBot simulation packages, and the tortoisebot_waypoints package.

**Jenkins Project Setup:**
- Created a Jenkins project to build the Docker image.
- Configured the project to run waypoints action server tests inside the Docker container.
- Automated the Jenkins project to build and test whenever a new pull request is accepted in the ros2_ci repository.

![](/project_data/2024-06-10-jenkins-ci/ci.gif)

## Results
The creation and deployment of CI pipelines using Jenkins for both ROS1 and ROS2 environments enabled automated testing and integration of TortoiseBot simulation and waypoints action server. This project demonstrates the importance and effectiveness of CI in robotics, ensuring code reliability and streamlining the development process.

## Key Insights
- The use of Jenkins and Docker significantly simplifies the CI process for robotic applications, making them more robust and easier to manage.
- Future work may explore integrating more complex test cases and expanding the CI pipeline to include additional robotic functionalities.

