- # Episode in RL
	- reinforcement learning, an episode refers to a complete sequence of interactions between an agent and an environment. An episode begins when the agent first interacts with the environment, and it ends when the environment reaches a terminal state or when a predetermined number of steps have been taken.
	- During an episode, the agent takes actions based on its current state and receives rewards based on its actions. The goal of the agent is typically to maximize the cumulative reward it receives over the course of an episode.
	- Episodes are used to structure the training process in reinforcement learning. The agent typically learns by interacting with the environment through a series of episodes, and its performance is evaluated based on the total reward it receives over the course of each episode.
-
- # Next Observation in RL
	- the array returned by the _next_observation() method is used as the observation or state of the environment. The observation is passed to the agent as input and is used to determine the agent's next action.
-
- # Step
	- reinforcement learning, a step refers to a single time step in an episode, during which the agent takes an action and the environment transitions to a new state and provides a reward.
	- In the `gym` library, the `step()` method of an environment is used to advance the environment by one step and return the new state, reward, and other information to the agent.
	- ```
	  import gym
	  
	  # Create the environment
	  env = gym.make("MountainCar-v0")
	  
	  # Reset the environment
	  state = env.reset()
	  
	  # Take a step in the environment
	  state, reward, done, _ = env.step(0)
	  
	  ```
	- In this example, the `env.step(0)` method takes a step in the environment by applying the action `0`
	- (e.g., moving left) and returns the new state, reward, and a boolean 
	  flag indicating whether the episode is over. The agent can then use this
	   information to update its internal state and make a decision about its 
	  next action.