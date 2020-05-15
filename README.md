# SwarmQLearning

## WHAT IS IT?

This is a simulation of a robot swarm which explores its environment in search of a randomly generated goal. At first, the swarm explores randomly. A simple Q-learning algorithm is implemented in this model to allow the swarm to be trained to explore more effectively. 

The robots mark a square green when they move over it, and can sense whether a square is green or black. Robots can also communicate to one another whether there is unexplored space nearby. The Q-learning reward function rewards robots for moving onto unexplored spaces, for moving toward unexplored areas reported by other robots if they don't themselves see unexplored space, and for not running into obstacles.

When learning is enabled, the current learning rate is printed out in the console. It decreases during the learning process automatically to a minimum of 0.05.

## HOW TO USE IT

To reset the simulation and generate a new randomly generated environment with obstacles and a goal, use the "setup" button. 

To start the simulation, use the "go" button, which repeatedly has the robot swarm explore, calulating and storing rewards for each action a robot takes according to the Q-learning algorithm. When one of the robots finds the goal, a new environment will be generated automatically, the swarm will be reset to the center of the screen, and exploration and learning automatically continues. 

To create a file with a printout of the current Q-table and a list of the number of ticks taken to find the goal in each trial so far, use the "output" button.

To stop the robots from learning and to make all of their actions be decided according to the Q-table instead of possibly being randomly decided, turn on test-mode. This will not reset anything, just temporarily change the robot's behavior so you can more easily see what they have learned to do so far.

Similarly, you can turn off or on learning without changing or resetting anything else using the "learn" switch.

To run a test suite of 50 randomly generated environments, use the "test" button. This runs the swarm twice on each environment, once randomly and once with the learned policy, and prints the number of ticks each trial took to a file. It also prints the number of unexplored spaces at the end of each trial to a file.

Finally, use the "start-round" button to generate a new random environment and reset the robots without resetting the Q-table or anything else in the simulation.

## CREDITS AND REFERENCES

Created by Keara Berlin and Linnea Prehn for the AI Robotics capstone course at Macalester College, under the guidance of Prof. Susan Fox, Spring 2020.
