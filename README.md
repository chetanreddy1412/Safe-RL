# Safe-RL

One of the main challenges in implementation of RL in  real life applications is safety.  Particularly,  the  undesired and harmful behaviour of RL agents involving humans is one of the major safety concerns. Utilizing the human in the RL agent as an active participant has been an active area of research, labelled as, human-in-the-loop RL. In this work, we propose to model  human participants as a constraint provider. Humans can provide context specific constraints to ensure safety. This leads to formulation of constrained Markov Decision Process (MDP). In this work, it is proposed to develop a framework for safe human-in-the-loop RL with human being a constraint provider. 

## Implementation
1. The human provides a conservative safe set and an action set which ensures that the agent never leaves the safe set.
2. We define three regions in the state space - marginally safe set, safe set and unsafe set.
3. The agent is free to take its own action in the safe set.
4. In the marginally safe set, action masking would be employed and an action is chosen from a conservative action set.
5. The algorithm is implemented for continuous control using DDPG (Deep Deterministic Policy Gradients). 

## Results in Inverted Pendulum Environment:
1. Before training - We see that only the conservative action (Torque = ± 2) is taken which ensures safety but has low performance and efficiency 
   

https://github.com/chetanreddy1412/Safe-RL/assets/60615610/d0699be3-e6aa-4a37-a05f-7c686e5f6467

2. After Training - In addition to 100% safety, the pendulum achieves high performance with lower input torque


https://github.com/chetanreddy1412/Safe-RL/assets/60615610/e2b5eeca-2819-4b9a-88bd-1b500bada648



