# CartPole
Buidling neural network to solve OpenAI's cart pole balancing environment.

https://user-images.githubusercontent.com/26003031/188318174-c09a0556-8e7d-4d87-bc72-0ff7dee310a3.mov

### Description
This environment corresponds to the version of the cart-pole problem described by Barto, Sutton, and Anderson in ["Neuronlike Adaptive Elements That Can Solve Difficult Learning Control Problem"](https://ieeexplore.ieee.org/document/6313077).
A pole is attached by an un-actuated joint to a cart, which moves along a frictionless track. The pendulum is placed upright on the cart and the goal is to balance the pole by applying forces in the left and right direction on the cart.

### Rewards
Since the goal is to keep the pole upright for as long as possible, a reward of `+1` for every step taken, including the termination step, is allotted. The threshold for rewards is 50.

### Starting State
All observations are assigned a uniformly random value in `(0.0, 2.0)`
