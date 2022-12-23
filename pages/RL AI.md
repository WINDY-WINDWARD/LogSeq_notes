- # Episode in RL
	- reinforcement learning, an episode refers to a complete sequence of interactions between an agent and an environment. An episode begins when the agent first interacts with the environment, and it ends when the environment reaches a terminal state or when a predetermined number of steps have been taken.
	- During an episode, the agent takes actions based on its current state and receives rewards based on its actions. The goal of the agent is typically to maximize the cumulative reward it receives over the course of an episode.
	- Episodes are used to structure the training process in reinforcement learning. The agent typically learns by interacting with the environment through a series of episodes, and its performance is evaluated based on the total reward it receives over the course of each episode.
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
- # Normalize Data
	- Normalizing data means scaling the data so that it has a mean of zero and a standard deviation of one. This process is often used to standardize the range and distribution of the data, which can make it easier to compare and analyze.
	  
	  There are several ways to normalize data, depending on the type and distribution of the data. Some common methods include:
	- **Min-max normalization:** This method scales the data to a fixed range, usually between 0 and 1. To normalize the data, you subtract the minimum value from each data point and divide the result by the range (i.e., the difference between the minimum and maximum values).
	- **Z-score normalization:** This method scales the data based on the mean and standard deviation of the data. To normalize the data, you subtract the mean from each data point and divide the result by the standard deviation.
	- **Decimal scaling:**  This method scales the data by multiplying it by a power of 10 and rounding to the nearest integer. This can be useful for data with a wide range of values, such as financial data.
	- Normalizing the data can be useful in machine learning and data analysis because it can help to remove the effects of scale and bias from the data. It can also help to stabilize the learning algorithms and improve the performance of the model.
-
- # MODEL OUTPT
- ```
  -------------------------------------
  | rollout/              |           |
  |    ep_len_mean        | 77.9      |
  |    ep_rew_mean        | -6.39e+07 |
  | time/                 |           |
  |    fps                | 70        |
  |    iterations         | 200       |
  |    time_elapsed       | 14        |
  |    total_timesteps    | 1000      |
  | train/                |           |
  |    entropy_loss       | -0.886    |
  |    explained_variance | -1.19e-07 |
  |    learning_rate      | 0.0007    |
  |    n_updates          | 199       |
  |    policy_loss        | -1.72e+06 |
  |    value_loss         | 5.04e+12  |
  -------------------------------------
  ```
	- The table provided contains various metrics that can be used to evaluate the performance of a reinforcement learning algorithm. Here is a brief explanation of each metric:
	- **rollout/ep_len_mean:** This is the mean episode length across all rollouts. It represents the average number of time steps it takes for an episode (a complete run of the environment) to finish.
	- **rollout/ep_rew_mean:** This is the mean episode reward across all rollouts. It represents the average reward received by the agent over the course of an episode.
	- **time/fps:** This is the frame rate (frames per second) of the environment. It represents the number of times the environment is updated per second.
	- **time/iterations:** This is the number of iterations (steps) taken by the agent in the environment.
	- **time/time_elapsed:** This is the time elapsed (in seconds) since the start of the training process.
	- **time/total_timesteps:** This is the total number of timesteps (steps) taken by the agent in the environment.
	- **train/entropy_loss:** This is the loss of the entropy term in the policy optimization process. The entropy term encourages exploration by adding a penalty for selecting actions that are too certain.
	- **train/explained_variance:** This is a measure of how well the value function approximator is fitting the returns. A high explained variance indicates that the value function is a good fit for the returns.
	- **train/learning_rate:** This is the learning rate used in the optimization process. It determines the step size taken by the optimizer when adjusting the model's parameters.
	- **train/n_updates:** This is the number of updates (steps) taken by the optimizer during the training process.
	- **train/policy_loss:** This is the loss of the policy (action selection) function in the policy optimization process.
	- **train/value_loss:** This is the loss of the value function in the policy optimization process. The value function estimates the expected reward for a given state or action.