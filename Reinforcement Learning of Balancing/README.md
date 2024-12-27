# Deep Q-Learning Agent for CartPole-v1

This project implements a Deep Q-Learning (DQN) agent to solve the CartPole-v1 environment from OpenAI's Gym. The agent uses a neural network model to learn an optimal policy through interaction with the environment.

## Requirements

Ensure you have the following libraries installed:
- gym
- keras
- numpy
- random
- math

## Project Structure

- `model.py`: Contains the DQN model definition.
- `training.py`: Handles the training process, experience replay, and epsilon-greedy exploration.
- `run.py`: Starts the training loop and solves the environment.

## Training Parameters

- `n_episodes`: Number of episodes to run the training (default: 1000).
- `n_win_ticks`: Number of ticks required to consider the task solved (default: 195).
- `gamma`: Discount factor for future rewards (default: 1.0).
- `epsilon`: Exploration rate (initially high to explore more) (default: 1.0).
- `epsilon_min`: Minimum value for exploration rate (default: 0.01).
- `epsilon_decay`: Decay rate for epsilon (default: 0.995).
- `alpha`: Learning rate for the model optimizer (default: 0.01).
- `batch_size`: Size of the minibatch for training (default: 64).

## Model Architecture

The model is a simple feedforward neural network with:
- 4 input features (representing the state of the CartPole environment).
- 2 output neurons (representing the action space: left or right).
- Two hidden layers with 24 and 48 neurons respectively, using ReLU activation functions.

## Main Steps of the Training

1. **State Preprocessing**: States are reshaped and converted to numpy arrays before feeding them into the neural network.
2. **Action Selection**: The agent chooses actions based on an epsilon-greedy policy (exploring when epsilon is high and exploiting when it's low).
3. **Experience Replay**: The agent stores its experience (state, action, reward, next state, done flag) in a replay buffer. During training, the agent samples random minibatches from this buffer to update the Q-values.
4. **Model Update**: The Q-values are updated using the Bellman equation, and the model is trained on the batch.
5. **Epsilon Decay**: The exploration rate (`epsilon`) decays over time to gradually favor exploitation.

## Running the Training

To start training the agent, simply run the `run.py` file.

## Expected Output

The training will output the progress after every 20 episodes. Here's an example of the output:

```bash
[Episode 0] - Mean survival time over last 100 episodes was 12.0 ticks. 
[Episode 20] - Mean survival time over last 100 episodes was 10.33 ticks. ... 
[Episode 640] - Mean survival time over last 100 episodes was 172.16 ticks. 
[Episode 660] - Mean survival time over last 100 episodes was 168.49 ticks. ...

Ran 711 episodes. Solved after 611 trials.
```

The agent will solve the environment after the specified number of episodes if the mean survival time exceeds `n_win_ticks` for 100 consecutive episodes.

## Notes

- The `epsilon` value decays over time, allowing the agent to explore less and exploit more as it learns.
- The model is compiled with the Adam optimizer and uses a learning rate schedule to decay the learning rate over time.
- The environment is visualized during training (`render_mode='human'`), and the agent’s progress can be observed.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
