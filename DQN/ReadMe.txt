Trained on a NVIDIA GeForce MX 250

env = gym.make("CartPole-v0")
spec = gym.spec("CartPole-v0")

num_episodes=400
lr=0.001
discount_factor=0.99
num_actions=2
epsilon=1.0
batch_size=64
input_dim=4
update_rate=100

Test - 'saved_networks/dqn_model10'