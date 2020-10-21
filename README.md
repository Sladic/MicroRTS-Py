# Gym-MicroRTS

[<img src="https://img.shields.io/badge/discord-gym%20microrts-green?label=Discord&logo=discord&logoColor=ffffff&labelColor=7289DA&color=2c2f33">](https://discord.gg/5tHykF)


This repo contains the source code for the gym wrapper of MicroRTS authored by [Santiago Ontañón](https://github.com/santiontanon/microrts). 

# Get Started

Clone the repo

```bash
# make sure you have GIT LFS installed https://git-lfs.github.com/
$ git lfs clone https://github.com/vwxyzjn/gym-microrts.git && \
cd gym-microrts && \
pip install dacite && \
pip install -e .
$ python3 hello_world.py
```

And run either the `hello_world.py` referenced above or the following file
```python
import gym
import gym_microrts

env = gym.make("MicrortsMining-v1")
env.reset()
for _ in range(10000):
    env.render()
    env.step(env.action_space.sample())
env.close()
```
![demo.gif](demo.gif)

## All built artifacts

[http://microrts.s3-website-us-east-1.amazonaws.com/microrts/artifacts/](http://microrts.s3-website-us-east-1.amazonaws.com/microrts/artifacts/)

## Papers written using gym-microrts

* Comparing Observation and Action Representations for Deep Reinforcement Learning in MicroRTS (https://arxiv.org/abs/1910.12134)
    * Logged experiments https://app.wandb.ai/costa-huang/MicrortsRL


