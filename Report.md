# Report on Project 1 Navigation

For this project, the navigation problem is set up using a DQN algoithm to help learn solve the problem.
The report explains the learning algorithm using the parameters, the architecture, rewards, and future imporovements.

### Environment Details

The environment is based on Unity ML-Agents

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Agent Implementation

Deep Q Networks: [Deep Q-Networks](https://pytorch.org/tutorials/intermediate/reinforcement_q_learning.html)

Deep Q Learning approach is:
1. Bridges the work between high dimensional sensory inputs and actions.
2. Results in the artificial agent to learn from an array of challenges.

References:
- UDacity Deep Reinforecment learning lesson
- https://web.stanford.edu/class/psych209/Readings/MnihEtAlHassibis15NatureControlDeepRL.pdf
- https://www.mlq.ai/deep-reinforcement-learning-pytorch-implementation/


### Model Architecture

![Alt text](https://github.com/dmoreno757/DRL-Navigation/blob/main/algorithm.PNG "Algorithm")

There files used for this development:
1. model.py
2. dqnAgent.py
3. Navigation.ipynb

For the network its using:
 - Passing in parameters where you can change rapidly for testing
 - Its using three fully connected
 - For forwarding using the RELU, where it replaces all negative inputs to 0 and all non negative are left unchanged
 - Where we run the model is from the notebook, highly recommend to update the values from there to test your configuration

Parameters used:
BUFFER_SIZE = int(1e5)  
BATCH_SIZE = 64         
GAMMA = 0.99            
TAU = 1e-3              
LR = 5e-4               
UPDATE_EVERY = 4 

### Rewards
Rewards per episode
We can see in my setup we accomplish the rewards in 322 episodes.

![Alt text](https://github.com/dmoreno757/DRL-Navigation/blob/main/reward.PNG "Score")

### For Future Work:

This project is from Udacity course where you can get the base files from their github to start fresh. 
For my future work I will like to develop two DQN where I can train to two agents to fight for the death to see which model
is better. Using this agent will train and see if a human being can be beat from the agent.



