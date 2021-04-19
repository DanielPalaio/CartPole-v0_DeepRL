# OpenAI CartPole-v0 DeepRL-based solutions
Using Deep Q-Network (DQN), Dueling DQN, and Dueling Double DQN (D3QN)  

Investigation under the development of the master thesis "DeepRL-based Motion Planning for Indoor Mobile Robot Navigation" @ Institute of Systems and Robotics - University of Coimbra (ISR-UC) 

# Software/Requirements
Module | Software/Hardware
------------- | -------------
Python IDE | Pycharm
Deep Learning library | Tensorflow + Keras
GPU | GeForce MX 250
Interpreter | Python 3.8
Python Environment | Anaconda
Packages | requirements.txt

**To setup Pycharm + Anaconda + GPU, consult the setup file [here](setup.txt)**.  
**To import the required packages, [requirements.txt](DQN/requirements.txt), type the following instruction in the project environment terminal:**  
> pip install -r requirements.txt

# :warning: **WARNING** :warning:  
The training generates a [.txt file](DQN/saved_networks.txt) that tracks the network models (in 'tf' and .h5 formats) that achieved the solved requirement of the environment. Additionally, an overview image (graph) of the training procedure is created.   
Keep in mind that to perform several training processes, the .txt, .png, and directory names must be change. Otherwise, information of previous trainings will get overwritten, and lost.  

Regarding testing, if you choose to load the .h5 model, a 5 episode training is done to initialize/build the keras.model network. Thus, the warnings above mentioned are also appliable to this situation.   
Loading the saved model in 'tf' is the recommended option. After finishing the testing, an overview image (graph) of the training procedure is also generated.  

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
12° < Pole angle (State 2) < -12°  
2.4 < Cart position (State 0) < -2.4  
Episode length > 200  

**Solved Requirement:**<br />
Average reward of 195.0 over 100 consecutive trials

# Deep Q-Learning framework
<p align="center">
  <img width="804" height="415" src="https://user-images.githubusercontent.com/79323290/115233659-19d6fa80-a110-11eb-8c68-09d365a54676.png">
</p>

# Deep Q-Network (DQN)
<p align="center">
  <img width="300" height="150" src="https://user-images.githubusercontent.com/79323290/115234204-a8e41280-a110-11eb-8cf1-12f0a7c62ae7.png">
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
  <img src="DQN/CartPole_Train.png" width="400" height="250" />
  <img src="DQN/CartPole_Test.png" width="400" height="250"/>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/79323290/109239128-ab8b5100-77cc-11eb-9294-d8f2703afeb8.gif" width="400" height="250" />
  <img src="https://user-images.githubusercontent.com/79323290/109238403-631f6380-77cb-11eb-9428-2e924dfbf532.gif" width="400" height="250"/>
</p>

> **Network model used for testing:** 'saved_networks/dqn_model10' ('tf' model, also available in .h5)  

# Dueling DQN
<p align="center">
  <img width="804" height="415" src="https://user-images.githubusercontent.com/79323290/109340340-cc9d8180-7860-11eb-9011-1ea05ef7fc75.png">
</p>

<table>
<tr><th> Train </th><th> Test </th></tr>
<tr><td>

| Parameter | Value |
|--|--|
| Number of episodes | 400 |
| Learning rate  | 0.00075 |
| Discount Factor | 0.99 |
| Epsilon | 1.0 |
| Batch size | 64 |
| TargetNet update rate (steps) | 120 |
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
  <img src="DuelingDQN/CartPole_Train.png" width="400" height="250" />
  <img src="DuelingDQN/CartPole_Test.png" width="400" height="250"/>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/79323290/109310276-38b9be80-783c-11eb-86a4-c3de0a222112.gif" width="400" height="250" />
  <img src="https://user-images.githubusercontent.com/79323290/109310670-bed60500-783c-11eb-8b33-f9d2024fed0a.gif" width="400" height="250" />
</p>

> **Network model used for testing:** 'saved_networks/duelingdqn_model20' ('tf' model, also available in .h5)  

# Dueling Double DQN (D3QN)
<p align="center">
  <img width="804" height="415" src="https://user-images.githubusercontent.com/79323290/109341984-1e470b80-7863-11eb-9c5b-33a967d6bdd9.png">
</p>

<table>
<tr><th> Train </th><th> Test </th></tr>
<tr><td>

| Parameter | Value |
|--|--|
| Number of episodes | 400 |
| Learning rate  | 0.00075 |
| Discount Factor | 0.99 |
| Epsilon | 1.0 |
| Batch size | 64 |
| TargetNet update rate (steps) | 120 |
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
  <img src="D3QN/CartPole_Train.png" width="400" height="250" />
  <img src="D3QN/CartPole_Test.png" width="400" height="250"/>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/79323290/109310287-3c4d4580-783c-11eb-84e5-75cc45f582f6.gif" width="400" height="250" />
  <img src="https://user-images.githubusercontent.com/79323290/109311042-31df7b80-783d-11eb-9d45-c8bea3401b0c.gif" width="400" height="250" />
</p>

> **Network model used for testing:** 'saved_networks/d3qn_model20' ('tf' model, also available in .h5)  
