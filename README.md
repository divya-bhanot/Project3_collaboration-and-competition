[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42135622-e55fb586-7d12-11e8-8a54-3c31da15a90a.gif "Soccer"


# Project 3: Collaboration and Competition

### Introduction

For this project, you will work with the [Tennis](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment.

![Trained Agent][image1]

In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. 
If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.  Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own,
 local observation.  Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. 

The task is episodic, and in order to solve the environment, your agents
 must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single **score** for each episode.

The environment is considered solved, when the average (over 100 episodes) of those **scores** is at least +0.5.

I have leveraged Multi agent Deep Deterministic Policy Gradients (MADDPG) approach to solve this problem. Both the agents are modeled as 
per DDPG. Both agents use a common memory replay buffer.

### Getting Started

1. Using the workspace provided by udacity . Implementation is done using single python notebook by defining all
the required code componenets like replay memory, agent advances like how to select next action, which is next state
and doing a learning update at desired frequency.

Description for code files in git https://github.com/divya-bhanot/Project3_collaboration-and-competition:
Tennis.ipynb : It includes all the code base along with comments which defines model , agent and training the agent
Tennis.html: Html version of above jupyter notebook
savepoint_actor_agent_0.pth: Saved model weights of the successful actor agent 0.
savepoint_actor_agent_1.pth: Saved model weights of the successful actor agent 1.
savepoint_critic_agent_1.pth: Saved model weights of the successful critic agent 0.
savepoint_critic_agent_1.pth: Saved model weights of the successful critic agent 1.
unit-environment.log : log file from unity environment 
README.md: Environment set up instructions as well as code base description
Report.pdf: Final report for project

2. After successfully running the code, create a new git repo, clone the repositery to local and add all the code and required documentation
files. Commit the code and push the branch to remote repo. 

### Instructions

Follow the instructions in the code file  `Tennis.ipynb` to get started with training your own agent! 