
# Projet 1 Navigation

## Introduction

!(./navigation.gif)

This project trains an agent to interact with Udacity's Bananas World such that it learns to pickup the yellow banans (+1) and ignore the blue bananas (-1) within each episode.

The code is written in PyTorch and Python 3.

## Environment
The below is a paraphrasing from the Udacity course's repo regarding this project's environment:

The goal of the agent is to collect as many yellow bananas (+1) within a given time while avoiding blue bananas (-1). The goal is to get an average score of +13 over 100 consecutive episodes.

According to Udacity: "The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction." The agent is able to select from four discrete actions:

* 0 - move forward.
* 1 - move backward.
* 2 - turn left.
* 3 - turn right.

## Setup Instructions
## Getting Started

Follow the instructions defined [here](https://github.com/udacity/deep-reinforcement-learning/tree/master) for downloading and installing.

My installation was based on 
* Windows 10 x64-based PC
* Python 3.6.13 :: Anaconda, Inc.

## Download the Unity Environment
For this project, you will not need to install Unity - this is because we have already built the environment for you, and you can download it from one of the links below. You need only select the environment that matches your operating system:
* Windows (64-bit) [Download](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
* Windows (32-bit) [Download](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
* Linux [Download](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
* Mac OSX [Download](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)

Then, place the file in your Projet1_Bananas / folder, and unzip (or decompress) the file.

## Clone the Course Repository

```bash
# Instructions from Deep RL course for environment setup
conda create --name DRL_udacity_cpu python=3.6 
conda activate DRL_udacity_cpu

# after creating new conda python environment
cd <path/to/dev/directory>
git clone https://github.com/udacity/deep-reinforcement-learning.git
git clone https://github.com/Yoshiokha/Deep_Reinforcement_Learning_Nanodegree_UDACITY/Projet1_Bananas.git
pushd Projet1_Bananas

# Modify requirements.txt to download torch==0.4.0 using the link provided below. Standard installation methods using pip or conda do not work for this specific version. Please note, this link is only compatible with Windows systems. For other versions or operating systems, visit PyTorch's previous versions page to find the appropriate download link.https://pytorch.org/get-started/previous-versions/
pip install https://download.pytorch.org/whl/cpu/torch-0.4.0-cp36-cp36m-win_amd64.whl

# Consider updating the file path for unityagents in your requirements.txt file, which was originally cloned from Udacity. This adjustment will ensure that the correct version of unityagents is referenced, matching the specific needs of your project.
pip install -r requirements.txt

# Create an IPython kernel for the DRL_udacity_cpu environment
python -m ipykernel install --user --name DRL_udacity_cpu --display-name "Python 3.6 (DRL_udacity_cpu)"

popd
pushd Projet1_Bananas
```
## Training the Agent

To start training the agent:

1. Launch Jupyter Notebook by running `jupyter notebook` in your terminal.
2. Open the notebook `Navigation_loss_weights_gradiants.ipynb`.
3. Update the path to the Bananas environment in the notebook to match your local setup.
4. Execute the notebook cells to begin training the agent.

## Abstract

This [Report.pdf](./Report.pdf) report outlines the implementation and results of a Deep Q Network (DQN) applied to the Navigation problem from the Unity ML Agents environment. The goal is to train an agent to navigate a space and collect yellow bananas while avoiding blue ones. The DQN agent was successfully trained to achieve an average score of +13 over 100 consecutive episodes, indicating satisfactory learning and problem solving within the environment.
