# Continuous Control

**The Environment**

This project works on the Reacher environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

**Distributed Training**

There are two separate versions of the Unity environment:

1. The first version contains a single agent.
2. The second version contains 20 identical agents each.

**Solving the Environment**

_**1: Solve the First Version**_

The task is episodic, and in order to solve the environment, the agent must get an average score of +30 over 100 consecutive episodes.

_**1: Solve the Second Version**_

The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents. In particular, the 20 agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). 

Specifically, after each episode, the rewards are added up for each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores. This yields an average score for each episode (where the average is over all 20 agents).

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. 

**Getting Started**

Follow the instructions below to explore the environment to learn how to use the Python API to control the agent(s).

Download the environment from one of the links below. You need only select the environment that matches your operating system:

Version 1: One (1) Agent

* Linux: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
* Mac OSX: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
* Windows (32-bit): click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
* Windows (64-bit): click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

Version 2: Twenty (20) Agents

*     Linux: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
*     Mac OSX: click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
*     Windows (32-bit): click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
*     Windows (64-bit): click [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)


Place the downloaded file(s) in the folder you cloned this repo to and unzip (or decompress) the file.

Create a Python environment for this project. I recommend using `conda` or `venv`.

Activate that environment and install dependencies:

`pip install -r requirements.txt`
