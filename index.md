## Stability Aware Policy Learning via Krasovskii's Approach with Application to Voltage Control

We provide our new experiment results in this webpage.

### OpenAI Pendulum Swingup task

#### Training curse of DDPG v.s. Stable-DDPG
<img src="training.png" class="img-responsive" alt=""> 
Fig. Average episode reward for DDPG vs Stable-DDPG on pendulum-v0. The horizonal axis indicates the training iteration, and the vertical axis is the average reward. Plotted curves are average over 5 random seeds, and the shaded region show the standard derivation.

#### Performance comparison of the final learned policies

Table 1: Performance of different learnt policies on 200 different test episodes with different initial angle and angular velocity.
| Method                          |Cost Mean              |Cost Standard deviation |
| ------------------------------- |-----------------------|------------------------|
| DDPG                            | -137.52               |  82.50                 |
| Stable-DDPG                     | -128.56               |  76.30                 |
| Jointly learning method [ref 16]| -370.37               |  279.37                |

The policy learnt from [ref 16] has the form: 

#### Videos


## Voltage Control

### Visualization of DDPG, Stable-DDPG and Baseline Linear Policy

<img src="voltage_policy.png" class="img-responsive" alt=""> 

### DDPG v.s. Stable-DDPG v.s. Baseline Linear Policy

As shown in Fig 4 in the submitted paper, baseline DDPG does not guarantee stability and thus can lead to ``infinite'' voltage recovery time and control cost. To obtain a reasonable comparison, we limit the max episode length to be T= 100, and compare the voltage recovery time (steps) and reactive power consumption (MVar) on 500 different voltage violation scenarios. Here are the results.

<img src="voltage_500.png" class="img-responsive" alt=""> 

Out of the 500 scenarios, we found that DDPG is able to stabilize 288 scenarios. For the scenarios baseline DDPG can stabilize, we observed that it can further reduce the control cost and recovery time, compared to Stable-DDPG and linear policy, possibly due to the more expressive power of standard neural network compared to monotone network.

<img src="voltage_stable.png" class="img-responsive" alt=""> 

