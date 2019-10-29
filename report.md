# Report

## Learning algorithm

This project uses the Deep Deterministic Policy Gradients (DDPG) algorithm as described in the [original paper](https://arxiv.org/pdf/1509.02971.pdf).

DDPG makes use of an actor and a critic to learn continuous actions. The actor learns how to act by directly estimating the optimal policy and maximizing reward through gradient ascent, and the critic generates Q-values for state-action pairs which are used to compute a temporal-difference (TD) error at each time step. The actor takes the current state as input and outputs one (or more) real values representing an action chosen from a continuous action space. The critic outputs an estimated Q-value given the current state and the actors action. DDPG also uses a replay buffer (experience replay) to sample batches of uncorrelated experiences for training. Additionally, we use the Ornstein–Uhlenbeck process to add noise to the actions. This encourages exploration of the action space.
Parameters for the networks can be found in the model.py and ddpg_agent.py

## Future Work

Testing different algorithms - In the original paper the authors discuss many algorithms which may receive better results for this task including TRPO and PILCO as well as other algorithm that were tested for this task like PPO, A3C and D4PG
