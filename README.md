# Udacity Deep Reinforcement Learning Nanodegree

## Project 2: Continuous Control

### Project details

This project trains an agent to keep a double-jointed arm in a moving target location using the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

This code solves the multi-agent version of the environment which has a slightly different barrier, to take into account the presence of many agents (20). In particular, the agents must get an average score of +30 (over 100 consecutive episodes, and over all agents).

### Distributed Training

There are two separate versions of the Unity environment:

- The first version contains a single agent.
- The second version contains 20 identical agents, each with its own copy of the environment.

The focus of this project is solving the second version of the environment.

### Solving the Environment

- The First Version
    - The task is episodic, and the environment is considered solved when the agent gets an average score of +30 over 100 consecutive episodes.
- The Second Version
    - The environment is considered solved when the agents get an average score of +30 over 100 consecutive episodes, averaged over all agents. Specifically, after each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores. This yields an average score for each episode (where the average is over all 20 agents).

### Getting Started

1. Clone and install dependences for the Udacity DeepRL Nanodegree found at [Udacity DeepRL](https://github.com/udacity/deep-reinforcement-learning#dependencies), which are required by this DDPG agent's implementation

2. This project requires `python 3.6` and a Unity virtual environment. You do not need to install Unity directly for this project. Instead, you can download a pre-build environment from one of the following links based on your operating system::<br>

<b>Version 1: One (1) Agent:<b><br>

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

<b>Version 2: Twenty (20) Agents:</b><br>

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

Alternatively, if you'd like to train the agent on a Virtual Machine and don't have a virtual screen enabled, download the headless version of the environment:

- Version 1: Linux (headless): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip)
- Version 2: Linux (headless): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip)

Run `source ./install.sh` to install the required python dependencies.

3. Clone this GitHub repository and unzip the Unity continous control environment into its root directory.

### Instructions

To train the agent run all the cells in [Continuous_Control.ipynb](Continuous_Control.ipynb) notebook.

Description of the implementation is provided in [report.md](report.md).
For technical details see the code in the notebook.

Agent's weights are stored in [checkpoint_actor.pth](checkpoint_actor.pth) and [checkpoint_critic.pth](checkpoint_critic.pth)
