---
title: 'Automated TicTacToe Game with MyCobot 280'
subtitle: 'Developing an Intelligent Robotic Arm System for Interactive Gameplay'
featured_image: 'project_data/2024-08-07-tictactoe-robot/correct_motion.gif'
date: 2024-08-07
---

## Introduction
This project showcases the integration of multiple robotics and software engineering skills to create an automated TicTacToe game using the MyCobot 280 robotic arm. The project involves setting up a perception system to detect game moves, designing a decision-making algorithm for gameplay, implementing a motion planning system to control the robotic arm, and developing a web application for game management and monitoring.

## Objectives
- To configure a perception system that accurately detects the TicTacToe board and the moves made by players.
- To design and integrate an algorithm that decides the best moves for the robot during the game.
- To develop a motion planning system that controls the MyCobot 280 arm to draw on the board.
- To create a web application for managing and monitoring the game process.

## Tools and Technologies

- **Programming Languages:** Python, JavaScript, C++
- **Frameworks and Libraries:** ROS2, Moveit2, OpenCV, Bootstrap, Gazebo
- **Robotic Platform:** MyCobot 280
- **Version Control:** Git

## Source Code
- [GitHub RoboTicTacToe Repository](https://github.com/MiguelSolisSegura/robotic_tactoe)

## Live Presentation
You can view the project presentation and live demonstration featuring both simulated and real robots here.

<iframe src="https://youtu.be/0qSsqAPmwf8?si=_UhlefGksEGV9KXw&t=3105" width="640" height="360" frameborder="0" allowfullscreen></iframe>

## Process and Development
The project is divided into several key tasks, focusing on setting up the robotic arm control, developing the perception system, integrating decision-making algorithms and creating the web application.

### Task 1: Setting up Moveit2
**Initial Setup:** The MyCobot 280 arm was configured using Moveit2 for planning and executing trajectories.

**Moveit2 Package Configuration:** Controllers for the MyCobot 280 were properly configured, and a ROS2 node was created to interface with Moveit2, allowing for trajectory planning and execution.

![](/project_data/2024-08-07-tictactoe-robot/correct_motion.gif)

### Task 2: Setting up the Perception System
**Perception Node Development:** A perception node was developed using OpenCV to detect the TicTacToe board and recognize the moves made by players. The system captures images from a camera and processes them to identify the game state.

![](/project_data/2024-08-07-tictactoe-robot/top.gif)

![](/project_data/2024-08-07-tictactoe-robot/bottom.gif)

**Integration with Manipulation Pipeline:** The perception system was integrated with the motion planning system, enabling the robot to respond to detected moves.

### Task 3: Integrating the Decision-Making Algorithm
**Algorithm Development:**  A minimax algorithm was implemented to determine the best move for the robot based on the current state of the game. This algorithm was integrated with the perception and manipulation systems. The whole system was tested to guarantee robust decision-making process, ensuring competitive gameplay against human opponents.

### Task 4: Developing the Web Application
**Web Application Creation:** A web application was developed using Bootstrap. This application allows users to monitor and control the game, providing real-time updates and an intuitive interface.

![](/project_data/2024-08-07-tictactoe-robot/web_interface.png)

## Results
The integration of perception, decision-making, and motion control systems resulted in a fully functional TicTacToe-playing robotic arm. The web application provides an easy-to-use interface for managing and monitoring the game, making the system accessible to users without technical expertise.

## Key Insights
- The project's success highlights the effectiveness of integrating various robotics and software tools to create an interactive and intelligent system.
- Future enhancements could include improving the perception system's accuracy and extending the web application's features to offer more interactive experiences.

## Future Work
- Enhancing the perception system for better accuracy in different lighting conditions.
- Adding more interactive features to the web application, such as voice control and player statistics tracking.
- Exploring the use of machine learning to improve the robot's decision-making capabilities over time.