![environment](https://user-images.githubusercontent.com/4408363/221556417-a85f6bce-c417-48e3-8056-f1a22bbbbf74.gif)

# Project 3: Collaboration and Competition
Collaboration and Competition is a project within the deep reinforcement learning that is udacity nanodegree.
Unity Machine Learning Agents (ML-Agents) is an open source Unity plug-in that allows games and simulations to be used as training environments for intelligent agents.
 
In this environment, two agents control the racket and bounce the ball across the net. If the ball hit by an agent goes over the net, it receives a reward of +0.1. If an agent drops the ball to the ground or hits the ball off the court, it receives a -0.01 reward. So, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.  Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. The observation space is 8 variables, but the state space, consisting of a stack of 3 observations for each agent, is 24 variables.

The task is episodic, and in each episode, the rewards received by each agent are added (without discounting), the larger of which is the score for that episode. To resolve the environment, an agent must have an average score (over 100 consecutive episodes) of +0.5.


# Requirement

* box2d 2.3.10
* box2d-py 2.3.8
* gym 0.26.2
* ipython 7.16.3
* matplotlib 3.3.4
* numpy 1.19.5
* pip 21.3.1
* python 3.6.15
* pytorch 0.4.0 


# Installation

Not all of the following steps may be necessary.
My operation system is Windows 10 Pro 64bit.
 
1.Create (and activate) a new environment with Python 3.6.
 
```
conda create --name drlnd python=3.6 
activate drlnd
```
2.Download SWIG, including the pre-built executable, and unzip it somewhere on your PC. Use SWIG 3.0.12.
Add the SWIG directory containing Swig.exe to the system PATH environment variable.

(https://sourceforge.net/projects/swig/files/swigwin/)

3.Install Microsoft Visual C++ 14.0. Available in "Microsoft Visual C++ Build Tools".

(https://visualstudio.microsoft.com/downloads/)

4.Install the base Gym library.

```
pip install gym
pip install box2d
conda install -c conda-forge box2d-py
```

5.Upgrade pip.
see:https://github.com/ijl/orjson/issues/192

Since execution as is will result in an error, do the following.

```
pip install --upgrade pip
```

6.Clone the Course Repository.
see:(https://github.com/udacity/deep-reinforcement-learning/issues/13)

```
git clone https://github.com/udacity/Value-based-methods.git
cd Value-based-methods/python
```

Since execution as is will result in an error, do the following.

On windows,

Open Value-based-methods/python/requirements.txt
Remove the line torch==0.4.0

On anaconda,

```
conda install pytorch=0.4.0 -c pytorch
cd Value-based-methods/python/
pip install .
```

7.Create an IPython kernel for the drlnd environment.

``` 
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

8.Install matplotlib.

```
conda install matplotlib
```

9.Before running code in a notebook, change the kernel to match the drlnd environment by using the drop-down Kernel menu.

10.Download the Unity Environment.

Windows (64-bit):
(https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

Then, place the file in the `p3_collab-compet/` folder in the course GitHub repository, and unzip (or decompress) the file.


# Instructions
 
Open the file `Continuous_Control.ipynb` (located in the `p3_collab-compet/` folder of the course GitHub repository).
Run through the cells, starting with the first cell.
Cells after "4.It's Your Turn!" are the implementation that uses a Python API to control the agent.
When the cell with the ddpg function is executed, training of the model begins.
To check agent behavior after training, run the cells after the ddpg function cell, load the weights after training, and run the ddpg function cell with the train_mode=False argument.
