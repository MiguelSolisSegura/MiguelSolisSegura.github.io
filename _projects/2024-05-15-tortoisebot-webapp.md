---
title: 'Web Development for Robotics: TortoiseBot Control Interface'
subtitle: 'Creating a User-Friendly Web Application for TortoiseBot Operation and Mapping'
featured_image: 'project_data/2024-05-15-tortoisebot-webapp/cover.gif'
date: 2024-05-15
---

## Introduction

As robotics continues to evolve, the need for intuitive and user-friendly interfaces becomes paramount, especially for users who are not experts in robotics or ROS. This project showcases the development of a comprehensive web application designed to control and monitor the TortoiseBot robot. By leveraging modern web technologies and ROS, this project aims to provide an accessible interface for robot teleoperation and environmental mapping.

## Objectives

- Develop a web application that allows operators to control the TortoiseBot and monitor its status.
- Implement features that display the generated map, a 3D model of the robot, and the camera feed in real time.
- Integrate a virtual joystick for manual control and waypoint buttons for automated navigation.

## Tools and Technologies

- **Programming Languages:** JavaScript, HTML, CSS
- **Frameworks and Libraries:** ROS, Vue.js, Bootstrap
- **Simulation Environment:** Gazebo
- **Version Control:** Git

## Source Code

- [GitHub TortoiseBot WebApp Repository](https://github.com/MiguelSolisSegura/tortoisebot_webapp)

## Interface Components

The web application was developed with a focus on providing an intuitive and user-friendly interface. Here are the main components implemented:

### Map Visualization

The interface includes a dynamic map visualization that displays the environment as it is being mapped by the TortoiseBot. This allows the operator to see the progress in real time and understand the layout of the environment. The map is continuously updated to reflect the latest data collected by the robot's sensors.

![](/project_data/2024-05-15-tortoisebot-webapp/map.gif)


### 3D Robot Model

A 3D model of the TortoiseBot is displayed within the web application, providing a visual representation of the robot. This helps users to better understand the robot's orientation and movements within the mapped environment. The 3D model is interactive, allowing users to view the robot from different angles.

![](/project_data/2024-05-15-tortoisebot-webapp/model.gif)

### Camera View

The camera view component streams real-time video from the TortoiseBot's onboard camera. This feature is crucial for operators to visually monitor the robot's surroundings and make informed decisions during teleoperation. The camera feed is integrated seamlessly into the interface for easy access and continuous monitoring.

![](/project_data/2024-05-15-tortoisebot-webapp/camera.gif)

### Virtual Joystick

To enable manual control of the TortoiseBot, a virtual joystick is included in the interface. This joystick allows operators to drive the robot manually, providing an intuitive way to control its movements. The joystick is responsive and designed to mimic the controls of a physical joystick, making it easy for users to navigate the robot through the environment.

![](/project_data/2024-05-15-tortoisebot-webapp/joystick.gif)

### Waypoint Buttons

For automated navigation, the interface includes waypoint buttons that allow users to send the TortoiseBot to specific pre-defined locations. These waypoints are strategically placed to help in mapping the entire environment efficiently. By clicking on a waypoint button, the operator can instruct the robot to move to that location autonomously.

![](/project_data/2024-05-15-tortoisebot-webapp/buttons.gif)

## Results

The developed web application successfully integrated with ROS to provide a user-friendly interface for controlling and monitoring the TortoiseBot. The application allowed users to visualize the map, view the robot's 3D model and camera feed, and control the robot using a virtual joystick and waypoint buttons.

![](/project_data/2024-05-15-tortoisebot-webapp/cover.gif)

## Key Insights

- The project demonstrated the potential of combining web development technologies with ROS to create accessible interfaces for robotics applications.
- Future enhancements could include more advanced mapping features and additional controls for enhanced robot navigation.