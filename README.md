# SIT215 Artificial And Computational Intelligence: Reinforcement Learning
<!-- 
Author : adhitya ram 
Version: 0.0.2
 -->
## Agents and Environments

Three [OpenAI Gym](https://gym.openai.com/) environments were used:

## Taxi-v2 currently not availabe on open ai v 0.14.0 so i am using v 0.10.5  

1. [Taxi-v2](https://gym.openai.com/envs/Taxi-v2/) 
2. [Cartpole-v1](https://gym.openai.com/envs/CartPole-v1/)
3. [FrozenLake-v0](https://gym.openai.com/envs/FrozenLake-v0/)

Three agents have been developed:

1. [Random Agent](https://github.com/Roboromeo1/AI_final_project/blob/master/src/agents/random.py)
1. [QLearner Agent](https://github.com/Roboromeo1/AI_final_project/blob/master/src/agents/qlearner.py)
2. [TDLearner Agent](https://github.com/Roboromeo1/AI_final_project/blob/master/src/agents/tdlearner.py)

From my research, Temporal difference (TD) learning is a category of
reinforcement learning approaches that includes QLearning. The TD Learner is
an implementation of the SARSA algorithm.

Training and evaluation runs for combinations of agent and environemnt
are marshalled through a
[driver](https://github.com/Roboromeo1/AI_final_project/blob/master/src/driver.py).

The following runs are available:

- Taxi, Random Agent
- Taxi, QLearner Agent
- Cartpole, Random Agent
- Cartpole, QLearner Agent
- Cartpole, TDLearner Agent
- Frozen Lake, Random Agent
- Frozen Lake, QLearner Agent
- Frozen Lake, TDLearner Agent

## Setup

This project was built on macOS in Python 3. Dependency management was simplified
using [pipenv](https://pipenv.readthedocs.io/en/latest/).

Follow the instructions below to set up this project locally:

### macOS

1. Clone or download this repository to your local machine using the green
**Clone or download** button on
[GitHub](https://github.com/Roboromeo1/AI_final_project)
1. Install Python 3 using `brew install python3`
1. Install pipenv using `brew install pipenv`
1. Install all remaining dependencies using `pipenv install`

A list of project dependencies is contained in the `Pipfile`.

### Other platforms

If you are on another platform, refer to the
[Python download](https://www.python.org/downloads/) instructions for your OS.

Further assistance is available in
[this guide](https://wiki.python.org/moin/BeginnersGuide/Download).

Pip3 is likely installed with Python, depending on your platform. Pip3 can be
used to install the dependencies found in the Pipfile from the command line,
specifying it as the requirements source: `pip3 install -r Pipfile`.

If you prefer to install dependencies individually, The specific version of each
required is visible in the Pipfile.lock, eg:

```
        "gym": {
            "hashes": [
                "sha256:6baf3f3b163e237869d92a64daeaa88f14f62bb1105863e45312505a19dbd652"
            ],
            "index": "pypi",
            "version": "==0.10.5"
```

Pip3 can install individual dependencies using: `pip3 install gym==0.10.5`

Alternatively, if you are using a packaged distribution such as Anaconda, use
your package management tool to to install the relevant version of required
dependencies, referring to the Pipfile and Pipfile.lock.




### Verification

To verify installation, a tool has been provided.

To run this tool using pipenv, from the root of the project use:
`pipenv run python demos/environment_test.py`.

To run without pipenv, use `python demos/environment_test.py`.

If your environment is set up correctly, you will see a window with a random
agent operating the cartpole environment and observations from the environment
printed to the console.

## Usage

To use this project, first choose which combination of environment and agent
you would like to see training and evaluation results for. To set this, edit
the `run.py` script in the root of the project - you will need to uncomment
the function that triggers the run you are interested in.

Then, to begin the run using pipenv, call `pipenv run python run.py`.

Or without pipenv, `python run.py`.


