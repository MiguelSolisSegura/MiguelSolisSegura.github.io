---
title: 'Comprehensive Code Testing in ROS1 and ROS2'
subtitle: 'Implementing and Verifying Waypoint Navigation for TortoiseBot'
featured_image: 'project_data/2024-05-21-tortoisebot-tests/tortoisebot_waypoint.gif'
date: 2024-05-21
---

## Introduction
In software development, especially within robotics, the importance of rigorous code testing cannot be overstated. This project emphasizes the development and implementation of in-depth tests for waypoint navigation capabilities in the TortoiseBot robot using both ROS1 and ROS2. By creating and executing comprehensive tests, we ensure the reliability, accuracy, and robustness of the navigation algorithms, ultimately leading to more dependable autonomous operations.

## Objectives
- Develop a ROS1 package to implement waypoint navigation for the TortoiseBot.
- Port the ROS1 implementation to ROS2, utilizing C++ for enhanced performance.
- Create and execute comprehensive tests to verify the accuracy and reliability of the robot's navigation in both ROS1 and ROS2 environments.

## Tools and Technologies

- **Programming Languages:** Python (ROS1), C++ (ROS2)
- **Frameworks and Libraries:** ROS1, ROS2, actionlib (ROS1), rclcpp (ROS2)
- **Simulation Environment:** Gazebo
- **Testing Frameworks:** rostest (ROS1), GTest (ROS2)
- **Version Control:** Git

## Source Code
- [GitHub ROS1 Waypoint Navigation Repository](https://github.com/MiguelSolisSegura/ros1_testing.git)
- [GitHub ROS2 Waypoint Navigation Repository](https://github.com/MiguelSolisSegura/ros2_testing.git)

## Process and Development
The project is divided into two main parts: developing the waypoint navigation in ROS1 and porting it to ROS2, followed by creating and running tests to ensure functionality and reliability.

### ROS1 Waypoint Navigation
**Initial Setup:** The ROS1 environment was configured by sourcing the necessary setup files and launching the TortoiseBot simulation in Gazebo. The `tortoisebot_action_server.py` script was developed to handle waypoint navigation using ROS action servers.

**Waypoint Navigation Implementation:** The action server receives waypoint goals and controls the TortoiseBot to navigate towards these waypoints. The navigation logic includes adjusting the robot's orientation and linear movement to reach the desired position with precision.

### ROS2 Waypoint Navigation
**Porting to ROS2:** The waypoint navigation functionality was ported to ROS2 using C++. The `tortoisebot_action_server.cpp` script was developed, maintaining the same logic as the ROS1 implementation but leveraging ROS2's improved features and performance benefits.

### Testing Framework Implementation
**ROS1 Testing:** 
- A comprehensive set of tests was created using `rostest` to verify the waypoint navigation.
- The tests checked that the end position [X, Y] of the robot matched the expected goal within an acceptable error margin.
- The tests also verified that the robot's final orientation [Yaw] was correct based on the goal.

**ROS2 Testing:**
- The ROS1 tests were ported to ROS2 using GTest.
- The same criteria were used to ensure the robot reached the desired waypoints and orientations accurately.

**Launch and Execute Tests:** 
- For ROS1, the tests were executed using `rostest`, and the results were validated to ensure all tests passed.
- For ROS2, the tests were executed using `colcon test`, with results analyzed to confirm accuracy and reliability.

![](/project_data/2024-05-21-tortoisebot-tests/tortoisebot_waypoint.gif)

## Results
The implementation of rigorous testing frameworks for both ROS1 and ROS2 ensured that the TortoiseBot's waypoint navigation was reliable and accurate. The comprehensive tests verified that the robot could consistently reach the specified waypoints and orientations within the defined error margins, highlighting the importance and effectiveness of thorough testing in robotics software development.

## Key Insights
- The project's success underscores the critical role of comprehensive testing in ensuring reliable and accurate navigation algorithms in robotics.
- Future work could explore additional testing scenarios and further automation of the testing process to enhance robustness and efficiency.

