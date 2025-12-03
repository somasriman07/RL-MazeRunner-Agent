Reinforcement Learning Maze Runner Agent


This repository contains two reinforcement learning approaches applied to a 10x10 Maze Runner environment: Q-Learning and Linear Function Approximation. The environment consists of 100 discrete states, walls, potholes, a start point, and a goal. The agent must learn to reach the goal while avoiding traps and unnecessary penalties.




Project Summary
The Maze Runner environment includes:


Empty cells (normal movement)
Walls (invalid action with negative reward)
Potholes (instant termination with a strong negative penalty)
Goal (positive reward for reaching it)
Start position where the agent respawns each episode
The purpose of the project is to train an agent with no prior knowledge to discover the shortest and safest path using reinforcement learning.



Algorithms Implemented in This Repository


Q-Learning
Linear Function Approximation
Other algorithms such as SARSA, Monte Carlo Control, and Value Iteration were explored during the project, but only the Q-Learning and Linear FA implementations are uploaded here because these two directly represent the core learning behavior and comparison.
Q-Learning Overview
Q-Learning is the main algorithm used for training the agent. It is model-free, off-policy, and learns the optimal strategy by updating Q-values after each step. The agent uses an epsilon-greedy exploration strategy, starting with full exploration and gradually shifting toward exploitation as epsilon decays. Q-Learning showed stable learning, high success rate, and fast convergence in this maze environment.



Linear Function Approximation

Overview
Linear Function Approximation attempts to replace the Q-table with a weight-based function. Instead of storing Q-values for each state-action pair, the algorithm tries to approximate them using linear features. However, in a small and discrete 10x10 maze, Linear FA performed poorly. It produced unstable results, fluctuating step counts, slower learning, and lower overall performance compared to tabular Q-Learning. This comparison helps illustrate why approximation methods are beneficial mainly in large or continuous environments.
Unique Features Implemented
Strong negative reward for falling into potholes
Immediate episode termination after entering a trap
Red tile representation for potholes in GUI
Live status messages such as "Fell into Pothole"
Visual training graphs for reward, steps, epsilon decay, and Q-value progression




Files Included
Q_Learning.ipynb
LinearFA.ipynb
RL.pdf
Training Video
Q-Learning training video:
https://drive.google.com/file/d/1D0ycAMmUd5e0bK6NZCEm2E-uVsWJOx4I/view?usp=sharing



Summary
Tabular Q-Learning is highly stable and well-suited for small environments like this maze. Linear Function Approximation provides useful insight into function-based RL methods, but due to the small state space, it did not perform as well as Q-Learning. Together, these two algorithms provide a clear comparison between exact tabular learning and approximation-based learning.
Author
Sriman Soma
B.Tech Artificial Intelligence and Data Science
Reinforcement Learning and Machine Learning Enthusiast