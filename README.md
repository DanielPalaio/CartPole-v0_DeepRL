# OpenAI CartPole-v0 DeepRL-based solutions
Using Deep Q-Network (DQN), Dueling DQN, and Dueling Double DQN (D3QN)


# OpenAI CartPole-v0
Actions:<br />
0 - Push cart to the left    
1 - Push cart to the right

States:<br />
0 - Cart position  
1 - Cart velocity  
2 - Pole angle  
3 - Pole velocity at tip

Rewards:<br />
Scalar value (1) for every step taken

Episode termination:<br />
Pole angle is more than ±12°  
Cart position is more than ±2.4 (center of the cart reaches the edge of the display)  
Episode length is greater than 200  
  
# Deep Reinforcement Learning framework
<p align="center">
  <img width="460" height="600" src="https://user-images.githubusercontent.com/79323290/109228274-817c6380-77b9-11eb-9e33-ddf9d8813521.png">
</p>

# Deep Q-Network (DQN)
