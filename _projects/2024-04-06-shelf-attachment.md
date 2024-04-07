---
title: 'Warehouse Robotics: Shelf Approach and Attachment Using ROS2'
subtitle: 'Practical Implementation of RB1 Robot Shelf Detection and Attachment'
featured_image: 'project_data/2024-04-06-shelf-attachment/robot_shelf_cover.gif'
date: 2024-04-06
---

## Introduction
This project focuses on the practical application of robotics in a warehouse setting, specifically programming an RB1 robot to approach, detect, and attach to shelves. By utilizing ROS2, this work contributes to the broader field of warehouse robotics, aiming to streamline specific tasks such as shelf interaction. While the project is performed on a simulated version of a commercial robot, it showcases the potential of applying ROS2 in real-world scenarios.

## Objectives
- Develop a workflow enabling the RB1 robot to autonomously navigate towards and attach to a warehouse shelf.
- Utilize ROS2 features to facilitate precise robot movements and shelf detection.

## Tools and Technologies

- **Programming Languages:** Python, C++
- **Frameworks and Libraries:** ROS2, Gazebo
- **Robotics Hardware:** RB1 Robot by Robotinik
- **Version Control:** Git

## Source Code
- [GitHub Repository](https://github.com/MiguelSolisSegura/checkpoint9)

## Process and Development
The development process is organized into two main stages, focusing on guiding the robot towards the shelf and ensuring a successful attachment, with a strong emphasis on the specific functionalities provided by ROS2.

### Pre-Approach Motion
The project begins with setting up a ROS2 node responsible for moving the robot close to the shelf, relying on laser scan data to navigate safely.

- **ROS1 Bridge:** To accommodate the RB1's ROS1 framework, a bridge to ROS2 is established, allowing for the integration of new ROS2 functionalities into the existing system.

### Final Approach and Attachment
In the subsequent phase, the robot employs ROS2 services to detect the shelf's location accurately and to initiate the attachment process.

- **Shelf Detection:** A ROS2 service server is implemented to process laser scan data, identifying shelf leg markers through intensity values. A corresponding service client in the robot's control node initiates this detection process.

![](/project_data/2024-04-06-shelf-attachment/reflective.png)

- **Robot Movement and Attachment:** The project leverages ROS2's TF (Transform) library to manage spatial relations between the robot and the shelf, guiding the robot's final approach. Once in position, the robot attaches to the shelf, with the process governed by custom ROS2 service messages.

![](/project_data/2024-04-06-shelf-attachment/rviz.png)

![](/project_data/2024-04-06-shelf-attachment/robot_shelf.gif)

## Results
This project enables the RB1 robot to perform targeted shelf approach and attachment tasks within a simulated warehouse environment. By employing ROS2’s advanced features, such as node parameters and TF, the robot can execute these tasks with a notable degree of precision and reliability.

## Key Insights
- Utilizing ROS2’s capabilities for service communication and spatial transformations presents a flexible approach to robot task programming.
- The project illustrates the potential of ROS2 in enhancing robot performance for specific operational tasks within warehouse settings, pointing towards further exploration and application in robotics.
