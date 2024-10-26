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
git clone https://github.com/Spooke02/DQN-Car-Racing.git
cd DQN-Car-Racing
```

Create a Virtual Environment and activate it:

- In the project directory, open a terminal and run:

  ```bash
  python -m venv myvenv
  ```

- Activate the Virtual Environment:

  - On Windows:
    
    ```bash
    venv_name\Scripts\activate
    ```
    
  - On macOS/Linux:
    
    ```bash
    source venv_name/bin/activate
    ```

Among the multiple dependencies used, NEAT is to be installed manually.

NEAT (NeuroEvolution of Augmenting Topologies)

- Overview: NEAT is a Python library for neuroevolution.
  
- Installation:
  
  - Using pip (Recommended):
    
    Open your terminal/command prompt and run:
    
    ```bash
    pip install neat-python
    ```
    
  - Using conda (Alternative):
    
    If you use Anaconda or Miniconda, you can also install via Conda (though it might not always have the latest version):
    
    ```bash
    conda install -c conda-forge neat-python
    ```

## Usage

After installation, you can run the training script:

```bash
python newcar.py
```

You can also modify parameters in config.py to adjust the training settings, such as the number of episodes, learning rate, and more.

To change the map, go to game_map in run_simulation function:

```bash
def run_simulation(genomes, config):
    ...
    # Clock Settings
    # Font Settings & Loading Map
    clock = pygame.time.Clock()
    generation_font = pygame.font.SysFont("Arial", 30)
    alive_font = pygame.font.SysFont("Arial", 20)
    game_map = pygame.image.load('map5.png').convert() # Change the Map

    global current_generation
    current_generation += 1
    ...
```

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

