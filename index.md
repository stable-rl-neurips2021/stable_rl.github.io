## Stability Aware Policy Learning via Krasovskii's Approach with Application to Voltage Control

We provide our new experiment results in this webpage.

### OpenAI Pendulum Swingup task

#### Performance comparison of the learned policies

Table 1: Performance of different learnt policies on 200 different test episodes with different initial angle and angular velocity.
| Method                          |Cost Mean              |Cost Standard deviation |
| ------------------------------- |-----------------------|------------------------|
| DDPG                            | -137.52               |  82.50                 |
| Stable-DDPG                     | -128.56               |  76.30                 |
| Jointly learning method [ref 16]| -370.37               |  279.37                |

#### Training curse of DDPG v.s. Stable-DDPG
<img src="training.png" class="img-responsive" alt=""> </div>


### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/stable-rl-neurips2021/stable_rl.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
