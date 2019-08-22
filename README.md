# Project 3: Collaboration and Competition
This Repo consists of Udacity's DRLND project3

## Project Environment and Dependencies
The code is written in Python3 and PyTorch.  Unityagents package has the problem environment, described in the section below.
Dependencies are specified in the requirements file and can be installed by:
```
pip install -r requirements.txt
```

## RL Problem Environment
This project uses Tennis environment, from Unity.

![GitHub Logo](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/images/tennis.png)

The Tennis environment can be downloaded here: [Tennis Environment on Mac](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
This yields a single score for each episode.
The environment is considered solved, when the average (over 100 episodes) of those scores is at least +0.5.


## Training the Agent
The individual cells in notebook ```Tennis.ipynb``` can be executed sequentially to train the agent. Note that after training, this file saves the actor and critic NN weigths in the checkpoint.pth files.  Additionally, note that these files are provided in the git repo and a re-run will cause these files to be generated with the new run.

If you just want to see the performance, the use the ```Saved_Agent.ipynb```. Execute the only cell in the notebook.  The code loads the actor and critic NN weights and runs the environment for 200 time steps before terminating.
