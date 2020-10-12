---
title: "2WD ROSduino"
permalink: /projects/2wdarduino/
excerpt: "Diff drive arduino car with remote control thrugh xbox controller"
driveId: 14wZwPdzL3B1WAysCzQ7stzg9jj2E2J8t/preview
toc: true
---
## Abstract

In this project, I used a couple of standard electronic parts to build an arduino car. It is either remote controlled by a xbox controller or autonomous with a sonic sensor. The challenge here was to figure out the electric circuit, a feasable ROS communication structure and implementing it all with C++. The final result can be seen [here](#video).

{% include figure image_path="/assets/images/rosduino_full.jpg" alt="this is a placeholder image" caption="Full remote controlled robot" %}

## Background story

In winter 2019/2020 I won a robotics challenge at TU Darmstadt. In short, it is about autonomous pick-and-place of tennisballs with a [Turtlebot3](https://www.turtlebot.com/) and an additional gripper arm with 5 degrees of freedom.

{% include figure image_path="/assets/images/robotic_challenge_winner.jpg" alt="this is a placeholder image" caption="TU Darmstadt robotics challenge winner 2019/2020" %}

You can have a look at the finals in [YouTube](https://youtu.be/cxs0oeeQU-w). The price was an arduino powered 2wd car set ([Assembly](#assembly)).

- after finished, I wanted it to be remote controlled
- bought raspberry pi 4B to make it remote controlled
- overkill, to make it autonomous, and not enough engin power
- lead to my recent project

## Assembly

{% include figure image_path="/assets/images/arduino_assembly.png" alt="this is a placeholder image" caption="Arduino car assembly parts" %}

## Controller to Arduino communication

- explain communication between controller - laptop, laptop - raspberry pi, raspberry pi - Arduino

## Video

{% include googleDrivePlayer.html id=page.driveId %}
