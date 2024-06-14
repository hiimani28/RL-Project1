# Bandit Learning Algorithms
## Overview
This repository contains the code and report for an assignment on bandit learning algorithms. The goal of this assignment is to experiment with various bandit learning algorithms, implement them from scratch, and compare their performance. The comparison is based on two metrics: (1) the average accumulated reward and (2) the proportion of time the optimal action is taken.

The assignment consists of two parts:

Part 1: Stationary Reward Distributions <br>
Part 2: Non-Stationary Reward Distributions <br>

## Repository Structure
.ipynb_checkpoints/: Contains Jupyter notebook checkpoints.
rl-a1.pdf: Project description
<br>Part_1_RL_Project1.ipynb: Jupyter notebook for Part 1: Stationary Reward Distributions. 
<br>Part2-Drift_change.ipynb: Jupyter notebook for the drift change experiment in Part 2.
<br>Part2_AbruptChange.ipynb: Jupyter notebook for the abrupt change experiment in Part 2.
<br>Part2_mean_reverting_change.ipynb: Jupyter notebook for the mean-reverting change experiment in Part 2.

## Requirements
To replicate the results in this repository, you will need the following packages:
Python 3.x <br>
NumPy<br>
Matplotlib<br>
Seaborn<br>
Jupyter Notebook<br>

## Instructions
<b> Part 1: Stationary Reward Distributions </b>
For each method, we repeated the experiment for 1000 different bandit problems (1000 sets of ten mean parameters), and 10,000 steps.

1. Greedy with Non-Optimistic Initial Values:
Initialize the action value estimates to 0. Use the incremental implementation of the simple average method.

2. Epsilon-Greedy with Different Choices of Epsilon: Experimented with different values of epsilon and used pilot runs to choose the best epsilon value.

3. Optimistic Starting Values with a Greedy Approach: Assume knowledge of the means of each reward distribution to set optimistic initial values. (5)

4. Gradient Bandit Algorithm: Experimented with different learning rates (α) to determine the best one. The average reward acquired by the algorithm at each time step.

<b> Part 2: Non-Stationary Reward Distributions </b>
1. Gradual Changes: Applied a drift change (µt = µt−1 + ϵt) where ϵt =  N(0, 0.001²).
2. Applied a mean-reverting change (µt = κµt−1 + ϵt) where κ = 0.5 and ϵt ~ N(0, 0.01²).
3. Abrupt Changes: At each time step, with probability 0.005, permuted the means corresponding to each reward distribution.

## Evaluation

Compared optimistic greedy method, ϵ-greedy with a fixed step size, and ϵ-greedy with a decreasing step size.
Run the algorithm on 1000 repetitions of the non-stationary problem and report the distribution of the average reward attained at the terminal step using box plots.
Results


## Authors
This project was completed by Himani Thakkar and Parinaz Shiri. If you have any questions or need further assistance, please feel free to contact us.
