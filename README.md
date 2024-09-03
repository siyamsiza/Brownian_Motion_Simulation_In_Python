
# Random Walk and Brownian Motion Simulations in Python
This repository contains Python implementations for simulating both Random Walks and Brownian Motion. These simulations serve as a practical demonstration of two fundamental concepts in stochastic processes.

## Overview
**Random Walk**: A mathematical formalization where an entity takes steps either to the left or right with equal probability. It is often used to model various phenomena in fields such as economics, physics, and computer science.

**Brownian Motion**: Also known as a Wiener process, it describes continuous random motion and is crucial in finance for modeling stock prices through stochastic calculus.

## Contents
### Random Walk Simulation

A simple implementation that generates a random walk using discrete steps.
Utilizes NumPy for numerical operations and Matplotlib for plotting the results.

### Brownian Motion Simulation

A simulation that models Brownian motion using normally distributed increments.
Similar to the random walk but represents continuous movement over time.

## Requirements
To run the simulations, you will need:

- Python 3.x
- NumPy
- Matplotlib

You can install the required packages using pip:

pip install numpy matplotlib

## Usage

Clone this repository to your local machine:

git clone https://github.com/siyamsiza/Brownian_Motion_Simulation_In_Python


## Code Implementation

### Random Walk Simulation Code

import numpy as np

import matplotlib.pyplot as plt

### Parameters

num_steps = 1000

steps = np.random.choice([-1, 1], size=num_steps)  # Randomly choose -1 or 1 for each step

random_walk = np.cumsum(steps)  # Cumulative sum to get the position at each step

### Plotting the random walk

plt.figure(figsize=(10, 6))

plt.plot(random_walk)

plt.title('Random Walk Simulation')

plt.xlabel('Number of Steps')

plt.ylabel('Position')

plt.grid()

plt.show()

### Brownian Motion Simulation Code

import numpy as np

import matplotlib.pyplot as plt

### Parameters

num_steps = 1000

dt = 0.01  # Time increment

steps = np.random.normal(loc=0, scale=np.sqrt(dt), size=num_steps)  # Normal distribution for increments

brownian_motion = np.cumsum(steps)  # Cumulative sum to get the position at each time step

### Plotting Brownian motion

plt.figure(figsize=(10, 6))

plt.plot(brownian_motion)

plt.title('Brownian Motion Simulation')

plt.xlabel('Time Steps')

plt.ylabel('Position')

plt.grid()

plt.show()

## Conclusion

Both simulations illustrate key concepts in stochastic processes and have applications across various scientific fields. The Random Walk consists of discrete steps taken at fixed intervals, while Brownian Motion represents continuous movement.
