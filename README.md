# CS-370 Pirate Intelligent Agent Portfolio

This repository contains my CS-370 Project Two artifact for the pirate intelligent agent project.

## Included Artifact

- `CS370_ProjectTwo_PirateAgent.ipynb`: Jupyter Notebook for the pirate intelligent agent, including the completed deep Q-learning training loop and final output checks.

## Reflection

For this project, I was given the starter notebook, the maze environment in `TreasureMaze.py`, and the experience replay structure in `GameExperience.py`. The provided code already handled the maze representation, valid movement rules, game state, replay memory structure, model setup, and helper functions for displaying and testing the maze. The code I created myself was mainly the Q-training implementation in the notebook. I completed the loop that resets the pirate from random free cells, chooses between exploration and exploitation, takes valid actions, stores each episode in replay memory, trains the neural network from replay batches, updates the target network, decays epsilon, and stops only after the agent reaches a 100% win rate and passes the completion check.

The biggest thing I learned from this project is that computer science is not just writing code that runs. A computer scientist takes a messy problem, breaks it into a structure the computer can work with, chooses an algorithm that fits that structure, and then proves the result actually works. In this case, the real problem was not "move a pirate around a maze." It was defining states, actions, rewards, memory, and evaluation clearly enough for the agent to learn a useful policy. That matters because the same kind of thinking shows up in real systems too. Recommendation tools, routing systems, automation, and AI agents all need the problem to be framed correctly before the model or algorithm can be trusted.

My approach as a computer scientist is to start with the constraints before jumping to the solution. For the pirate agent, that meant reading the provided classes, understanding what the model could observe, checking what actions were valid, and using small tests to make sure the training loop was learning the intended behavior. I also tried to keep the output readable. The final notebook shows real training progress and final checks without burying the grader in pages of raw logs. That is something I want to carry into professional work too: a solution should not only work internally, it should leave enough evidence that another person can understand what happened.

The ethical side is important even in a small game project because reinforcement learning depends heavily on reward design. If the reward is wrong, the agent can learn behavior that technically optimizes the number but misses the real goal. For end users, my responsibility is to build systems that are understandable, testable, and not overclaiming what the AI can do. For an organization, my responsibility is to make sure the system is reliable enough for the context, has clear limits, and can be monitored after release. In a higher-stakes AI system, I would want stronger validation, clear human override, privacy controls around any training data, and a way to detect when the model is being used outside the situation it was designed for.

AI use note: I used ChatGPT to help organize this README reflection and revise wording. I reviewed the final README and checked it against the course prompt before preparing the portfolio package (OpenAI, 2026).

## References

OpenAI. (2026). ChatGPT [Large language model]. https://chatgpt.com/
