# OpenAI CartPole-v0 DeepRL-based solutions
Using Deep Q-Network (DQN), Dueling DQN, and Dueling Double DQN (D3QN)

# Software/Requirements
Python IDE | Pycharm
------------- | -------------
Deep Learning library | Tensorflow + Keras
GPU | GeForce MX 250
Interpreter | Python 3.8
Python Environment | Anaconda
Packages | requirements.txt

**To setup Pycharm + Anaconda + GPU, consult the setup file [here](setup.txt)**  
**To import the required packages, [requirements.txt](DQN/requirements.txt), type the following instruction in the project environment terminal:**

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
  <img width="500" height="250" src="https://user-images.githubusercontent.com/79323290/109228274-817c6380-77b9-11eb-9e33-ddf9d8813521.png">
</p>

# Deep Q-Network (DQN)
<p align="center">
  <img width="700" height="500" src="https://user-images.githubusercontent.com/79323290/109228829-56deda80-77ba-11eb-8d3c-59e2669c5ebe.png">
</p>



Trained on a NVIDIA GeForce MX 250

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

num_episodes=400
lr=0.001
discount_factor=0.99

> **WARNING**: Be careful, or else!  
num_actions=2
epsilon=1.0
batch_size=64
input_dim=4
update_rate=100

Test - 'saved_networks/dqn_model10'
