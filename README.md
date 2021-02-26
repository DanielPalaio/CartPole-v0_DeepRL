# OpenAI CartPole-v0 DeepRL-based solutions
Using Deep Q-Network (DQN), Dueling DQN, and Dueling Double DQN (D3QN)

# Software/Requirements
Module | Software/Hardware
------------- | -------------
Python IDE | Pycharm
Deep Learning library | Tensorflow + Keras
GPU | GeForce MX 250
Interpreter | Python 3.8
Python Environment | Anaconda
Packages | requirements.txt

**To setup Pycharm + Anaconda + GPU, consult the setup file [here](setup.txt)**  
**To import the required packages, [requirements.txt](DQN/requirements.txt), type the following instruction in the project environment terminal:**  
> pip install -r requirements.txt

# :warning: **WARNING** :warning:  

# OpenAI CartPole-v0
**Actions:**<br />
0 - Push cart to the left    
1 - Push cart to the right

**States:**<br />
0 - Cart position  
1 - Cart velocity  
2 - Pole angle  
3 - Pole velocity at tip

**Rewards:**<br />
Scalar value (1) for every step taken

**Episode termination:**<br />
Pole angle is more than ±12°  
Cart position is more than ±2.4 (center of the cart reaches the edge of the display)  
Episode length is greater than 200  
  
# Deep Reinforcement Learning framework
<p align="center">
  <img width="500" height="225" src="https://user-images.githubusercontent.com/79323290/109228274-817c6380-77b9-11eb-9e33-ddf9d8813521.png">
</p>

# Deep Q-Network (DQN)
<p align="center">
  <img width="850" height="550" src="https://user-images.githubusercontent.com/79323290/109228829-56deda80-77ba-11eb-8d3c-59e2669c5ebe.png">
</p>

<table>
<tr><th> Train </th><th> Test </th></tr>
<tr><td>

| Parameter | Value |
|--|--|
| Number of episodes | 400 |
| Learning rate  | 0.001 |
| Discount Factor | 0.99 |
| Epsilon | 1.0 |
| Batch size | 64 |
| TargetNet update rate (steps) | 100 |
| Actions (CartPole-v0 env) | 2 |
| States (CartPole-v0 env) | 4 |

</td><td>

| Parameter | Value |
|--|--|
| Number of episodes | 100 |
| Epsilon | 0.01 |
| Actions (CartPole-v0 env) | 2 |
| States (CartPole-v0 env) | 4 |

</td></tr> </table>

<p align="center">
  <img width="700" height="350" src="https://user-images.githubusercontent.com/79323290/109236928-85fc4880-77c8-11eb-8f5f-48fea7f19900.png">
</p>

> **Network model used for testing:** 'saved_networks/dqn_model10' (tf model, also available in .h5 file)  
