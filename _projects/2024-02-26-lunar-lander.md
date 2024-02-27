---
title: 'Mastering Lunar Landing'
subtitle: 'An introduction to Reinforcement Learning'
featured_image: 'project_data/2024-02-26-lunar-lander/cover.jpg'
---

![](/project_data/2024-02-26-lunar-lander/short_cover.jpg)

Imagine you're teaching a dog new tricks. You reward the dog with a treat when it does something right (like sitting on command) and perhaps withhold treats or give a gentle verbal cue when it does something wrong. Over time, the dog learns to perform the trick correctly to maximize its treats. This is the essence of reinforcement learning: an AI agent (like the dog) learns to make decisions by performing actions in an environment to achieve some goal, receiving rewards or penalties based on its actions.

Reinforcement Learning (RL) plays a significant role in robotics, particularly in tasks that require autonomous decision-making under uncertain conditions. RL algorithms enable robots to learn from their interactions with the environment, allowing them to adapt and improve their behavior over time. In robotics, RL finds applications in various domains such as:

- Autonomous navigation and path planning
- Manipulation and dexterous hand control
- Robot locomotion and motion control
- Task automation and optimization

In the current project I embarked on an exploratory journey into the fascinating world of reinforcement learning, with a focus on mastering the dynamics of landing a module on the lunar surface. The primary goal was to demonstrate how reinforcement learning has the potential to simulate and solve real-world problems, such as precision landing in space missions, starting with a simple example.

## Objectives:
- To understand and apply the basics of reinforcement learning in a practical scenario.
- To train an agent capable of successfully landing on the lunar surface within the Gymnasium's lunar lander environment.

## Technologies and Tools:
- **Programming Language:** Python
- **Frameworks:** Gymnasium (for RL environment), Stable Baselines3 (for creating the RL agent).
- **Tools:** Google Colab (for code experimentation and demonstration)
- **Version Control:** Git (for code repository management)

## Process and Development:
The development of the current project began with a foundational study of reinforcement learning principles, focusing on understanding how agents learn from interactions within an environment to achieve specific goals. The Gymnasium's lunar lander environment served as a perfect sandbox for applying these concepts, requiring the agent to make a series of decisions to land safely on the lunar surface.

### Key Features of the Lunar Lander Environment

The lunar lander, as any other RL environment, has several components that define its dynamics.

**Objective**: The main goal is to land the lunar module between two flags marking the landing pad. The landing must be soft, and the module must remain upright to achieve a successful landing. The environment is considered solved when the agent achieves a score of 200 points over 100 consecutive trials.

**Actions:** The agent can perform discrete actions such as doing nothing, firing the left orientation engine, firing the main engine, or firing the right orientation engine. These actions allow the module to control its angle and descent speed.

**State Space:** The environment provides an observation space that includes information such as the module's position, velocity, angle, angular velocity, and whether each leg is in contact with the ground. This comprehensive state representation enables the agent to make informed decisions to achieve a safe landing.

**Rewards:** The reward system in the Lunar Lander environment is designed to encourage successful landings while penalizing excessive fuel use and crashes. Points are awarded for landing on the landing pad and for fuel-efficient flight, whereas points are subtracted for using fuel and for crashing or coming down too hard.

### Stable Baselines 3

Stable Baselines 3 (SB3) is a popular library in the field of reinforcement learning that provides implementations of state-of-the-art RL algorithms. It is designed for ease of use, efficiency, and reproducibility. Built on PyTorch, SB3 allows both novices and experts to leverage powerful RL algorithms for training, evaluating, and deploying agents that can learn from their environment. The library focuses on providing a simple and consistent API, comprehensive documentation, and a collection of pre-trained models to facilitate the development of RL applications.

### Proximal Policy Optimization (PPO): A High-Level Overview

In RL, a "policy" is essentially the strategy that the AI agent follows to decide what action to take in a given situation. Think of it as the dog's thought process that leads it to decide whether to sit, stay, roll over, etc., based on the command given and its desire to get a treat.

PPO is a specific method used to teach the AI agent how to improve its policy (strategy) over time. It's like finding a more efficient way to teach the dog tricks, ensuring it learns faster and more reliably without getting confused or stuck on bad behaviors.

The "proximal" part of PPO is about keeping the new strategy (policy) close to the old one but slightly improved. Imagine if you suddenly changed how you teach the dog from one day to the next; the dog might get confused. PPO tries to avoid confusing the AI agent by making sure that updates to the policy are small but effective, helping it to learn steadily and avoid making big mistakes.

### Integration with the Lunar Lander Environment

The integration of Stable Baselines 3 with the Gymnasium's Lunar Lander environment is a practical example of how to apply PPO for training an RL agent. Below is a breakdown of a few code snippets of the implementation, illustrating the setup, training, and evaluation process.

**Environment Setup**

```python
import gymnasium as gym

# First, we create our environment called LunarLander-v2
env = gym.make("LunarLander-v2")

# Then we reset this environment to a known state
observation, info = env.reset()
```

This snippet is about initializing the Lunar Lander environment. The `gym.make("LunarLander-v2")` command creates an instance of the Lunar Lander environment, and `env.reset()` initializes it, returning the first observation.

**Training with PPO**

```python
# Vectorize the environment
env = make_vec_env('LunarLander-v2', n_envs=16)
# Instance the desired model
model = PPO("MlpPolicy", env, verbose=1)
# Train the agent over 200,000 steps
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

After training, the model's performance is evaluated on a new instance of the environment, a common practice to ensure the validity of results. The `evaluate_policy` function runs the trained model for 10 episodes, using a deterministic approach to action selection. This evaluates the agent's performance in terms of average reward and its consistency (standard deviation).

The criteria for considering a success in solving this environment, is a mean reward of 200 points after discounting one standard deviation. After the first training attempt, this condition was not met. Although it is possible to configure several parameters of the PPO algorithm, at the current state of my experience in the field, it was just easier to train the agent for longer. Without any further changes, the agent was able to accomplish the task successfully:

<iframe width="560" height="315" src="https://www.youtube.com/embed/ebK3ZIm31t4?si=zCAKrB_AcQr7cPJs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Results and Impact:
The project culminated in the successful development of an RL agent capable of consistently achieving safe and efficient landings in the lunar lander environment. Key outcomes include:

- A trained agent demonstrating a high success rate in landing simulations.
- An initial understanding of reinforcement learning principles and their application in solving complex, dynamic problems.

**Additional Resources:**
- [Link to the HuggingFace repository containing the trained agent](https://huggingface.co/miguelsolis/ppo-LunarLander-v2)