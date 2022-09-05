# CartPole
Buidling neural network to solve OpenAI's cart pole balancing environment.

https://user-images.githubusercontent.com/26003031/188318174-c09a0556-8e7d-4d87-bc72-0ff7dee310a3.mov

### Description
This environment corresponds to the version of the cart-pole problem described by Barto, Sutton, and Anderson in ["Neuronlike Adaptive Elements That Can Solve Difficult Learning Control Problem"](https://ieeexplore.ieee.org/document/6313077).
A pole is attached by an un-actuated joint to a cart, which moves along a frictionless track. The pendulum is placed upright on the cart and the goal is to balance the pole by applying forces in the left and right direction on the cart[^1]
[^1]: https://github.com/openai/gym/blob/master/gym/envs/classic_control/cartpole.py
### Rewards
Since the goal is to keep the pole upright for as long as possible, a reward of `+1` for every step taken, including the termination step, is allotted. The threshold for rewards is 50.

### Starting State
All observations are assigned a uniformly random value in `(0.0, 2.0)`

### Computational Graph for the Deep Reinforcement learning model.
![openaistuff](https://user-images.githubusercontent.com/26003031/188461338-c44be135-4130-42a1-8dbd-0a186a66cb55.png)
* It has 6 fully connected layers followed by dropout layers with categorical cross entropy loss and Adam optimizer with a learning rate of 1e-3.

### Accuracy
<img width="1051" alt="Screenshot 2022-09-05 at 3 30 49 PM" src="https://user-images.githubusercontent.com/26003031/188462689-c797c33d-1e3b-4f57-999d-c5eac88fa0bc.png">
(The accuracy here isnt that great since the model was only run for 30 epochs, if trained for longer the accuracy will get better.)

### Loss
<img width="1054" alt="Screenshot 2022-09-05 at 3 31 26 PM" src="https://user-images.githubusercontent.com/26003031/188463324-0e870b6d-0b01-435c-bbd2-51267fdc4137.png">


### Getting Started
To run CartPole locally perform the following steps (requires Python 3.7+):
1. ` git clone https://github.com/Suraj-Bhor/CartPole.git `
2. ` cd Cartpole `
3. ` pip install -r requirements.txt `
4. ` python cartpole.py `

### Visualize graphs
To visualize graphs the model saves the tensorboard checkpoints to `/tmp/tflearn_logs/`.
Once the model is trained you can visualize the results buy issuing the following command.
* ` tensorboard --logdir='/tmp/tflearn_logs' `
