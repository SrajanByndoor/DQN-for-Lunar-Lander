# DQN-for-Lunar-Lander

## Description
This project implements a Deep Q-Network (DQN) reinforcement learning agent to master the LunarLander-v3 environment from OpenAI Gymnasium. The agent learns to autonomously control a lunar module, navigating physics to achieve successful soft landing on a designated landing pad/ output area.

## Objectives
Design and implement a deep reinforcement learning agent for the LunarLander-v3 environment using Deep Q-Network (DQN) algorithm. Train the agent over 1000 episodes to achieve successful lunar landings, demonstrating the progression from random actions to skilled control. Generate comprehensive visualizations including learning curves (rewards and training loss plots) and comparison videos between random and trained agent performance. The project aims to showcase practical implementation of advanced RL concepts including experience replay, target networks, and epsilon-greedy exploration strategies.

## Key Steps
### 1. Environment Setup & Neural Network Design
Initialize LunarLander-v3 environment with 8-dimensional state space (position, velocity, angle, sensors) and 4 discrete actions. Design a 3-layer neural network (128-128 hidden units) with ReLU activation and Xavier initialization. Configure PyTorch optimization with Adam optimizer and proper seed management for reproducible results.
### 2. DQN Algorithm Implementation
Implement core DQN components including dual networks (local and target), experience replay buffer with 100K capacity, and epsilon-greedy exploration strategy. Develop the learning loop with Q-target computation using Bellman equation, gradient descent on experience batches, and soft target network updates (τ=0.005).
### 3. Training Pipeline & Visualization
Execute 1000-episode training with epsilon decay (1.0→0.01) and progress monitoring. Implement comprehensive visualization tools including reward/loss plotting with moving averages, video generation for performance comparison, and model checkpoint saving for deployment.

## Results
### Training Performance & Metrics
Successfully trained DQN agent over 1000 episodes achieving consistent successful landings with average rewards exceeding +200 in final episodes, compared to random agent baseline of ~-200. Learning progression became evident after ~300 episodes with >90% landing success rate in final 100 episodes. Training curves demonstrated clear convergence without catastrophic failutres.

### Video Demonstrations:
Random Agent Performance - Chaotic, unsuccessful landing attempts:
https://drive.google.com/file/d/1bz5Xb0ZapV51egzPX9amAfw87DnP25Gl/view?usp
=sharing

Trained Agent Performance - Smooth, controlled successful landings
https://drive.google.com/file/d/11UBto2JWfE6pzRLac5lKrG4KzIlyotjF/view?usp=sh
aring
