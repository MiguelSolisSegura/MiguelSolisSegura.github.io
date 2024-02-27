---
title: 'Safe Descent: Mastering Lunar Landing'
subtitle: 'An introduction to Reinforcement Learning'
featured_image: 'project_data/2024-02-26-lunar-lander/cover.jpg'
---

In the current project I embarked on an exploratory journey into the fascinating world of reinforcement learning (RL), with a focus on mastering the complex dynamics of landing a module on the lunar surface. The primary goal was to demonstrate how reinforcement learning has the potential to simulate and solve real-world problems, such as precision landing in space missions. By leveraging the Gymnasium's lunar lander environment, this project showcases the potential of RL in robotics and its significance in achieving autonomous decision-making under uncertain conditions.

### Objectives:
- To understand and apply the basics of reinforcement learning in a practical scenario.
- To train an agent capable of successfully landing on the lunar surface within the Gymnasium's lunar lander environment.
- To highlight the importance of reinforcement learning in robotics, particularly in tasks requiring precise control and decision-making.

### Technologies and Tools:
- **Programming Language:** Python
- **Libraries/Frameworks:** Gymnasium (for RL environment), Stable Baselines3 (for creating the RL agent).
- **Tools:** Google Colab (for code experimentation and demonstration)
- **Version Control:** Git (for code repository management)

### Process and Development:
The development of the current project began with a foundational study of reinforcement learning principles, focusing on understanding how agents learn from interactions within an environment to achieve specific goals. The Gymnasium's lunar lander environment served as a perfect sandbox for applying these concepts, requiring the agent to make a series of decisions to land safely on the lunar surface.

The Lunar Lander environment, as hosted by Gymnasium (formerly known as Gym by OpenAI), is a simulation used in reinforcement learning (RL) to train agents to perform the task of landing a spacecraft on the surface of the moon. This environment is part of the Box2D group of environments, which are based on the Box2D physics engine, offering a realistic simulation of physical systems. The Lunar Lander environment specifically challenges agents to safely land a lunar module on the moon, navigating through the perils of space flight with limited fuel and in the presence of gravity.

#### Key Features of the Lunar Lander Environment:

- **Objective:** The main goal is to land the lunar module between two flags marking the landing pad. The landing must be soft, and the module must remain upright to achieve a successful landing. The environment is considered solved when the agent achieves a score of 200 points over 100 consecutive trials.

- **Actions:** The agent can perform discrete actions such as doing nothing, firing the left orientation engine, firing the main engine, or firing the right orientation engine. These actions allow the module to control its angle and descent speed.

- **State Space:** The environment provides an observation space that includes information such as the module's position, velocity, angle, angular velocity, and whether each leg is in contact with the ground. This comprehensive state representation enables the agent to make informed decisions to achieve a safe landing.

- **Rewards:** The reward system in the Lunar Lander environment is designed to encourage successful landings while penalizing excessive fuel use and crashes. Points are awarded for landing on the landing pad and for fuel-efficient flight, whereas points are subtracted for using fuel and for crashing or coming down too hard.

- **Graphics and Physics:** The environment features simple yet effective 2D graphics that visually represent the lunar module, the landing area, and the surrounding space. The physics engine accurately models gravity, inertia, and the effects of the module's thrusters, providing a realistic landing experience.

- **Customization:** While the basic setup of the Lunar Lander environment is fixed, researchers and developers can tweak certain parameters or the reward structure to experiment with different learning strategies or to increase the challenge for the RL agent.

This environment is widely used in RL research and education due to its balance of simplicity and complexity. It provides a clear, achievable objective, a rich set of actions and states for the agent to learn from, and a direct analogy to real-world challenges in space exploration. The Lunar Lander environment serves as an excellent platform for both beginners and experienced practitioners in reinforcement learning to develop, test, and refine their algorithms.


### Stable Baselines 3: An Introduction

Stable Baselines 3 (SB3) is a popular library in the field of reinforcement learning (RL) that provides implementations of state-of-the-art RL algorithms. It is designed for ease of use, efficiency, and reproducibility. Built on PyTorch, SB3 allows both novices and experts to leverage powerful RL algorithms for training, evaluating, and deploying agents that can learn from their environment. The library focuses on providing a simple and consistent API, comprehensive documentation, and a collection of pre-trained models to facilitate the development of RL applications.

### Proximal Policy Optimization (PPO): A High-Level Overview

Proximal Policy Optimization (PPO) is an advanced policy gradient method used in reinforcement learning. It addresses the challenges of training stability and sample efficiency that are common in other policy gradient methods like TRPO (Trust Region Policy Optimization). PPO achieves this by optimizing a surrogate objective function, which ensures that the policy update steps are not too large, preventing destabilizing updates to the policy.

PPO is characterized by two main features:
- **Clipped Surrogate Objective:** PPO limits the policy update step by clipping the probability ratio between the new and old policies, ensuring modest updates and preventing the policy from changing too drastically in a single iteration.
- **Multiple Epochs of Stochastic Gradient Descent (SGD):** Unlike some algorithms that update the policy from a batch of experiences only once, PPO iterates over the same batch multiple times to perform more fine-grained updates.

This combination of strategies makes PPO particularly appealing for a wide range of applications, including robotics, gaming, and beyond, due to its balance between simplicity, efficiency, and effectiveness.

### Integration with the Lunar Lander Environment: Code Snippets Explained

The integration of Stable Baselines 3 with the Gymnasium's Lunar Lander environment is a practical example of how to apply PPO for training an RL agent. Below is a breakdown of the code snippets provided, illustrating the setup, training, and evaluation process.

**Environment Setup**

```python
import gymnasium as gym

# First, we create our environment called LunarLander-v2
env = gym.make("LunarLander-v2")

# Then we reset this environment
observation, info = env.reset()
```

This snippet is about initializing the Lunar Lander environment. The `gym.make("LunarLander-v2")` command creates an instance of the Lunar Lander environment, and `env.reset()` initializes it, returning the first observation.

**Training with PPO**

```python
# Vectorize the environment
env = make_vec_env('LunarLander-v2', n_envs=16)
model = PPO("MlpPolicy", env, verbose=1)
model.learn(total_timesteps=int(2e5))
```

In this part, `make_vec_env` is used to vectorize the environment, allowing the PPO model to train across multiple instances (16 in this case) simultaneously, which significantly speeds up the training process. The model is instantiated with a Multi-Layer Perceptron (MLP) policy and trained for a total of 200,000 timesteps, leveraging the PPO algorithm.

**Evaluating the Model**

```python
# Create a new environment for evaluation
eval_env = gym.make('LunarLander-v2')

# Evaluate the model with 10 evaluation episodes and deterministic=True
mean_reward, std_reward = evaluate_policy(model, eval_env, n_eval_episodes=10)
```

After training, the model's performance is evaluated on a new instance of the environment. The `evaluate_policy` function runs the trained model for 10 episodes, using a deterministic approach to action selection. This evaluates the agent's performance in terms of average reward and its consistency (standard deviation).

### Results and Impact:
The project culminated in the successful development of an RL agent capable of consistently achieving safe and efficient landings in the lunar lander environment. Key outcomes include:

- A trained agent demonstrating a high success rate in landing simulations.
- An initial understanding of reinforcement learning principles and their application in solving complex, dynamic problems.

**Additional Resources:**
- *Link to the GitHub repository containing the trained agent.* [Placeholder for GitHub repository link]
- *Link to a video showcasing the trained agent successfully landing.* [Placeholder for video link]