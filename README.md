# Safe-RL

The ability to interact and explore an environment has enabled Reinforcement
Learning agents to generate incredible results in many complex tasks. However,
most of these results have been limited to simulated environments. One
of the biggest obstacles to moving from simulated environments to real-world
applications is safety. RL agents learn new tasks in uncertain environments
through extensive exploration and trial and error, which can sometimes violate
safety constraints and result in undesirable outcomes. Safe RL encapsulates
algorithms that deal with this tradeoff between exploration and safety. In this
study, we define a human-in-the-loop framework that ensures safety in both
training and deployment.



## Implementation
Our approach involves two steps: the first step is the utilization of expert
human input to establish a Safe State Space (SSS) and a corresponding Conservative
Safe Policy (CSP). In simple environments, the human directly provides
SSS and CSP while in complex environments, safe trajectories generated by the
human are used to estimate SSS and CSP. In the second step, we use a modified
version of the Deep Deterministic Policy Gradient algorithm augmented with
a safety layer (built using SSS and CSP) that is learned by the agent during
the training. We focus on continuous control environments which have a wide
range of applications in robotics and autonomous systems.


## Results:

https://github.com/chetanreddy1412/Safe-RL/assets/60615610/05f32efe-a3dc-41fd-815b-1825db87e244


1. Before training - We see that only the conservative action (Torque = ± 2) is taken which ensures safety but has low performance and efficiency. The state space trajectories for the first three episodes of training are shown:
<img width="1113" alt="Before_Training_Trajectories" src="https://github.com/chetanreddy1412/Safe-RL/assets/60615610/3973534b-22a0-4d3b-a616-60b82ef24abd">

Video:


https://github.com/chetanreddy1412/Safe-RL/assets/60615610/be49f325-0df4-4e68-8eef-577b3dab8cf3









2. After Training - In addition to 100% safety, the pendulum achieves high performance with lower input torque. The state space trajectories of the learnt agent is depicted below:
<img width="1131" alt="After_Training_Trajectories" src="https://github.com/chetanreddy1412/Safe-RL/assets/60615610/7e99ecf5-ae46-465b-8f60-aa02c6093101">

Video:


https://github.com/chetanreddy1412/Safe-RL/assets/60615610/f01a33d7-959e-4e58-896f-c1304261f588











