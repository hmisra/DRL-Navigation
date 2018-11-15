
[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"
[dqn]: https://github.com/hmisra/DRL-Navigation/blob/master/dqn.png "Results"
# Navigation

### Introduction

For this project, I trained an agent to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.



## Training
### Set up for Linux
To train an agent using the code in this repository, you will need to follow the set up instructions below:
1. Create and activate a Python 3.6 environment using Anaconda (`env_name` can be replaced with any name):
``` bash
    $ conda create --name env_name python=3.6
    $ source activate env_name
```
2. Clone this repository and install the dependencies:
``` bash
    $ git clone https://github.com/hmisra/DRL-Navigation.git
    $ cd python
    $ pip install .
```
3. The structure of the code repository is as follows:
``` 
    p1_navigation/
        checkpoint.pth
        dqn_agent.py
        model.py
        unity-environment.log
        README.md
        p1_navigation_solution.ipynb
        Report.ipynb
    python/
    __pycache__/
 ```
4. Extract the banana.app.zip file in the directory.

5. Launch `p1_navigation_solution.ipynb` in Jupyter and start training the agent by executing the code in the notebook. 
``` bash
    $ jupyter notebook
```
### Understanding the files
1. `dqn_agent.py` contains the `Agent` and `ReplayBuffer` classes for the agent to interact with the environment.
2. `model.py` contains the Pytorch neural network used to approximate the Q-value functions that the agent will be using.
3. `p1_navigation_solution.ipynb` is the code entry point for starting the environment and the training loop.
4. `Report.ipynb` contains description of the solution and hyperparameters etc.
5. `unity-environment.log` is the log file that is created during the training loop.
6. `checkpoint.pth` contains the weights of the Pytorch model once the environment is successfully solved.
7. `banana.app.zip` contains the unity environment file.
8. `python\` directory contains all the dependencies.

### Results
![DQN][dqn]
