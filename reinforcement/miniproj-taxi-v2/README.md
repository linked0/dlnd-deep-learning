Instructions
Open the workspace in the next concept in a new window.
![new_tab](./new-tab.gif)

Open the workspace in a new window.

Next, open a terminal by clicking on NEW TERMINAL. You will notice some output as the environment is configured.
![open-terminal](./open-terminal.gif)

Open a new terminal.

The workspace contains three files:

agent.py: Develop your reinforcement learning agent here. This is the only file that you should modify.
monitor.py: The interact function tests how well your agent learns from interaction with the environment.
main.py: Run this file in the terminal to check the performance of your agent.
Open all three of these files in the workspace.
![open-agent-monitor-main](./open-agent-monitor-main.gif)

Open agent.py, Monitor.py, and main.py.

Next, run main.py by executing python main.py in the terminal.
![run-main](./run-main.gif)

Run python main.py in the terminal.

When you run main.py, the agent that you specify in agent.py interacts with the environment for 20,000 episodes. The details of the interaction are specified in monitor.py, which returns two variables: avg_rewards and best_avg_reward.

avg_rewards is a deque where avg_rewards[i] is the average (undiscounted) return collected by the agent from episodes i+1 to episode i+100, inclusive. So, for instance, avg_rewards[0] is the average return collected by the agent over the first 100 episodes.
best_avg_reward is the largest entry in avg_rewards. This is the final score that you should use when determining how well your agent performed in the task.
Your assignment is to modify the agents.py file to improve the agent's performance.

Use the __init__() method to define any needed instance variables. Currently, we define the number of actions available to the agent (nA) and initialize the action values (Q) to an empty dictionary of arrays. Feel free to add more instance variables; for example, you may find it useful to define the value of epsilon if the agent uses an epsilon-greedy policy for selecting actions.
The select_action() method accepts the environment state as input and returns the agent's choice of action. The default code that we have provided randomly selects an action.
The step() method accepts a (state, action, reward, next_state) tuple as input, along with the done variable, which is True if the episode has ended. The default code (which you should certainly change!) increments the action value of the previous state-action pair by 1. You should change this method to use the sampled tuple of experience to update the agent's knowledge of the problem.
Once you have modified the function, you need only run python main.py to test your new agent.

While you are welcome to implement any algorithm of your choosing, note that it is possible to achieve satisfactory performance using some of the approaches that we have covered in the lessons.

Evaluate your Performance
OpenAI Gym defines "solving" this task as getting average return of 9.7 over 100 consecutive trials.

While this coding exercise is ungraded, we recommend that you try to attain an average return of at least 9.1 over 100 consecutive trials (best_avg_reward > 9.1).

Not sure where to start?
Note that this exercise is intentionally open-ended, and we won't provide an official solution. For help with this exercise, please reach out to your instructors and fellow students! As a first step, you should figure out how to adapt your implementation in the Temporal-Difference Methods lesson to implement an agent to learn in this new environment. The code will likely be very similar to the notebook from the Temporal-Difference Methods lesson, where you need only modify very few things to fit this slightly different format.

Share your Results
If you arrive at an implementation that you are proud of, please share your results with the student community! You can also reach out to ask questions, get implementation hints, share ideas, or find collaborators!

As a final step, towards sharing your ideas with the wider RL community, you may like to create a write-up and submit it to the OpenAI Gym Leaderboard!
