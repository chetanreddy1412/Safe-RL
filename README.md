# Safe-RL

One of the main challenges in implementation of RL in  real life applications is safety.  Particularly,  the  undesired and harmful behaviour of RL agents involving humans is one of the major safety concerns. Utilizing the human in the RL agent as an active participant has been an active area of research, labelled as, human-in-the-loop RL. In this work, we propose to model  human participants as a constraint provider. Humans can provide context specific constraints to ensure safety. This leads to formulation of constrained Markov Decision Process (MDP). In this work, it is proposed to develop a framework for safe human-in-the-loop RL with human being a constraint provider. 

## Implementation
1. The human provides a conservative safe set and an action set which ensures that the agent never leaves the safe set.
2. We define three regions in the state space - marginally safe set, safe set and unsafe set.
3. The agent is free to take its own action in the safe set.
4. In the marginally safe set, action masking would be employed and an action is chosen from a conservative action set.
5. The algorithm is implemented for continuous control using DDPG (Deep Deterministic Policy Gradients). 

## Results in Inverted Pendulum Environment:
1. Before training - We see that only the conservative action (Torque = ± 2) is taken which ensures safety but has low performance and efficiency. The state space trajectories for the first three episodes of training are shown:
<img width="1113" alt="Before_Training_Trajectories" src="https://github.com/chetanreddy1412/Safe-RL/assets/60615610/3973534b-22a0-4d3b-a616-60b82ef24abd">



https://github.com/chetanreddy1412/Safe-RL/assets/60615610/4e8b2a59-7e5b-433a-a956-1583164c0cd0


2. After Training - In addition to 100% safety, the pendulum achieves high performance with lower input torque. The state space trajectories of the learnt agent is depicted below:
<img width="1131" alt="After_Training_Trajectories" src="https://github.com/chetanreddy1412/Safe-RL/assets/60615610/7e99ecf5-ae46-465b-8f60-aa02c6093101">


https://github.com/chetanreddy1412/Safe-RL/assets/60615610/90b09130-b31a-4f9e-839e-6c286326f444




