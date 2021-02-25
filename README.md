# OpenAI CartPole-v0 DeepRL-based solutions, using Deep Q-Network (DQN), Dueling DQN, and Dueling Double DQN (D3QN)


# OpenAI CartPole-v0:
Actions: <br />
  0 - Push cart to the left <br />   
  1 - Push cart to the right <br />

States:
  Type: Box(4)                    Min         Max
  0 - Cart position               -2.4        2.4
  1 - Cart velocity               -Inf        Inf
  2 - Pole angle                  -41.8º      41.8º
  3 - Pole velocity at tip        -Inf        Inf
Rewards:
  1 for every step taken
Episode termination:
  Pole angle is more than ±12°
  Cart position is more than ±2.4 (center of the cart reaches the edge of the display)
  Episode length is greater than 200
  
# Deep Q-Network (DQN)
