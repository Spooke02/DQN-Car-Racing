# DDQN Car Racing

This repository implements a Deep Reinforcement Learning (RL) approach to the Car Racing environment using Double Deep Q-Learning (DDQN). The objective is to train an agent to navigate a car through a racing track while maximizing rewards by making optimal driving decisions.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Architecture](#architecture)
- [Training](#training)
- [Features](#features)
- [Futurework](#futurework)
- [Contributing](#contributing)
- [License](#license)

## Installation

To set up the environment, clone the repository and install the required packages:

```bash
git clone https://github.com/CodeAndAction/DDQN-Car-Racing.git
cd DDQN-Car-Racing
pip install -r requirements.txt
```

## Usage

After installation, you can run the training script:

```bash
python train.py
```

You can also modify parameters in config.py to adjust the training settings, such as the number of episodes, learning rate, and more.

## Architecture

The project follows the DDQN algorithm, which uses two neural networks to stabilize training by reducing overestimation bias. The architecture includes:

- Agent: Implements the DDQN logic for action selection and learning.
- Environment: Interfaces with OpenAI's Gym to simulate the Car Racing environment.
- Replay Buffer: Stores experiences for training the agent.

## Training

The training process involves:

- Initializing the environment and the agent.
- Running episodes where the agent takes actions based on its policy.
- Collecting experiences in the replay buffer.
- Periodically updating the agent's network using sampled experiences.

The trained model is saved periodically to allow for future evaluation and fine-tuning.

## Features

- DDQN Algorithm: Explains how Double Deep Q-Learning helps in improving the stability of the training process.
- Customizable Hyperparameters: List key hyperparameters that users can modify for training, such as learning rate, exploration rate, and discount factor.
- Evaluation Metrics: Describe the metrics used to evaluate the agent's performance (e.g., average reward per episode).

## FutureWork

Outline potential future enhancements or features you plan to implement, such as:

- Adding more complex environments.
- Exploring other RL algorithms like DDPG or PPO.

## Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository and create a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

