# Project 3: Reinforcement Learning

This project implements model-based and model-free reinforcement learning algorithms.

1. **Value Iteration Agent**: It utilizes an MDP and runs value iteration for set iterations before the constructor returns. It implements both asynchronous & prioritized sweeping.

2. **Q-Learning**: A RL agent that learns by trial and error from interactions with the environment through its update(state, action, nextState, reward) method. Approximate Q-learning is also implemented

## Running Pacman

The Python project uses the standard library and has no additional Python package dependencies. From the repository root, activate the shared environment and run the command from this directory:

```sh
source .env/bin/activate
cd 1-Introduccion/AI-Pacman-Projects-master/Reinforcement
python pacman.py -p PacmanQAgent -x 2000 -n 2010 -l smallGrid -a epsilon=0.1,alpha=0.3,gamma=0.7
```

To run another agent defined in this directory's `*Agents.py` files, replace `PacmanQAgent` after `-p` with that agent's class name.

The graphical display requires `tkinter`, which must be available in the Python installation. On macOS with Homebrew Python 3.14, install its native support with:

```sh
brew install python-tk@3.14
```

`python -m pip install tk` installs a separate PyPI package and does not provide Python's native `tkinter` module.
