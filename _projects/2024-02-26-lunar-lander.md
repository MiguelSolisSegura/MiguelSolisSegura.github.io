---
title: 'Mastering Lunar Landing through Reinforcement Learning'
subtitle: 'An Application of RL in Simulated Environments'
featured_image: 'project_data/2024-02-26-lunar-lander/policy.gif'
date: 2024-02-27
---

**Introduction:**

Reinforcement Learning (RL) is a pivotal technology in robotics and autonomous systems, enabling decision-making under uncertainty. This project demonstrates the application of RL in a controlled environment, specifically focusing on the task of landing a module on the lunar surface—a foundational step towards applying RL in more complex real-world scenarios.

**Objectives:**

- To apply reinforcement learning principles in a simulated lunar landing scenario.
- To train an agent to successfully land on the lunar surface using the Gymnasium environment.

**Technologies and Tools:**

- **Programming Language:** Python
- **Frameworks:** Gymnasium (for the RL environment), Stable Baselines3 (for RL agent development)
- **Tools:** Google Colab
- **Version Control:** Git

**Source Code:** [Trained Agent on HuggingFace](https://huggingface.co/miguelsolis/ppo-LunarLander-v2)

**Process and Development:**

The project began with a foundational exploration of reinforcement learning, aiming to understand how agents learn from interactions to achieve specific objectives. Utilizing the Gymnasium lunar lander environment, the project focused on training an agent to make decisions that result in a successful landing.

***Key Features of the Lunar Lander Environment:***

- **Objective:** Safely land the lunar module on a designated pad, achieving a soft landing without tilting.
- **Actions:** The agent chooses from discrete actions, such as firing different engines, to control the module's orientation and descent.
- **State Space:** Includes the module's position, velocity, angle, angular velocity, and leg contact with the ground.
- **Rewards:** Points are awarded or subtracted based on landing precision, fuel efficiency, and avoidance of crashes.

***Implementation Using Stable Baselines 3:***

Stable Baselines 3 facilitated the application of the Proximal Policy Optimization (PPO) algorithm, a policy improvement method that ensures gradual and effective learning. The integration with the lunar lander environment involved setting up the environment, training the agent with PPO, and evaluating the model's performance.

***Training and Evaluation:***

- The environment was vectorized for simultaneous training instances, speeding up the learning process.
- The agent was trained over 200,000 steps, with its performance evaluated in new instances to validate learning outcomes.

![](/project_data/2024-02-26-lunar-lander/policy.gif)

**Results:**

The project successfully trained an RL agent capable of executing safe and efficient landings within the lunar lander environment. The agent demonstrated a high success rate, showcasing the practical application of reinforcement learning in a simulated task.

**Key Insights:**

This exploration into reinforcement learning, through the lens of a simulated lunar landing, illustrates the potential of RL in robotics and autonomous systems. The project serves as a foundation for further research and application in more complex and real-world scenarios.