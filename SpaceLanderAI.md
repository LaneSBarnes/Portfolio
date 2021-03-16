
# Space Lander AI
This project is an attempt to create an AI that can control the thrust of a lander and have it land on the ground safely.
I will use [ML-Agents Toolkit](https://github.com/Unity-Technologies/ml-agents/blob/main/README.md) in Unity game engine to create this environement and train the ML model.

## Motivation
While looking around the internet trying to find a fun ML project to do, I stumbled upon ML-Agents. I was originally thinking of finding a video game to make an AI for, but figured this would be better as I can create my own environment with my own problem to solve. To pick the problem, I was inspired by SpaceX's Falcon 9 stage landing

![_](Pictures/Falcon9.gif)

I watch many of SpaceX's streams and am blown away how they can manuever this massive object on this tiny barge. While this problem can be solved with kinematic equations and simple code, I wanted to try to teach an ML model to do this anyway.

## Environment
The environment we'll be working with is very simple: a cylinder (our lander) dropping onto a plane (our landing pad). The lander has mass and is pulled down by the force of gravity. For now, it is locked in the Y axis and cannot move in the X or Z directions. If it hits the landing pad with an impulse larger than a given threshold, the lander will crash. When the lander either crashes or lands safely, it will reset back up to a postion in the air where it will fall again. The gif below demonstrates what it looks like when a lander lands safely or crashes.

![_](Pictures/CrashVsLandingDemo.gif)

The first lander (very left) is thrusting upward at 9.81 m/s^2 which means that it is perfectly counteracting gravity and floating in the air. The second lander is thrusting a little below 9m/s^2 and decends slow enough to land safely. The third lander is JUST below the threshold of crashing. The fourth lander does not thrust enough and crashes. The last lander does not thrust at all and is in free fall.

Having just one lander will take too long to train, so we create multiple landers that all share the same brain and land as a group. We have 81 landers, which means the training session will be ~81X faster. We stop at this number as more landers cause the simulation to lag, giving us diminshing returns of training time.

A timelapse of the creation of the environment is shown below

![_](Pictures/LandingPadTimeLapse.gif)

## Training
To be Written

## Results
To be Written
