---
title: "Crazy Turtle"
permalink: /projects/crazy_turtle/
excerpt: "Controller for turtle simulation from ROS turtlesim"
driveId: 1cyWFjvttOCzMIfpwzMksLqbJhj8I6O2v/preview
driveId2: 1Qhk23Z0r8yTBbZDFcm9wc3Ma3nm2_7An/preview
toc: true
---

## Abstract

In this project I developed two different feedback controller for the ROS turtle simulation with a wall avoidance algorithm. The implementation of mine uses an action server, so that the user can set and change goals whenever it is needed (non-blocking). Because setting an action goal in terminal is not as convenient as calling a ROS service, I made the action communication completely by the software. This means, the user only has to call the service server, which handles the rest. 

Afterwards, the service node sends the desired turtle position to the action node. The controller starts steering the turtle towards the goal while sending information about the turtle state and distance to the goal. Since it is an action message, it is non-blocking and the user might change the goal whenever desired.

{% include figure image_path="/assets/images/crazy_turtle_teaser.png" alt="this is a placeholder image" caption="Crazy turtle in action" %}

## Background story

   I started learning [ROS](https://www.ros.org/) back in July 2019. The first tutorials are pretty basic. You start
installing ROS and the first tutorial tasks are to simply download and run pre-made ROS packages. One
of the first ones is the [turtesim](http://wiki.ros.org/turtlesim) simulator. Pretty basic and quite fun. It is a turtle, moving around in a colored plane. The normal task is to start two ROS nodes, the simulator and the [teleop-twist-keyboard](http://wiki.ros.org/teleop_twist_keyboard). Afterwards, you should be able to steer the little turtle around with your arrow keys. Then, the fun began. :smirk:

## Feedback control with wall avoidance

- explain feedback control and point to image in rqt graph
- explain 2 different approaches
- explain wall avoidance with penalty function
	- explain why I used min{cost, 20} (simulation gets instable)

{% include googleDrivePlayer.html id=page.driveId %}

{% include figure image_path="/assets/images/wallbump.png" alt="this is a placeholder image" caption="Wall avoidance cost function. 3D plot created with MATLAB" %}


## ROS communication

- explain 2 added ros nodes
- explain ros action msg and ros service msg and differences
- action is non blocking, can be changed every time

{% include figure image_path="/assets/images/rqt_graph_crazy_turtle.jpg" alt="this is a placeholder image" caption="rqt-Graph of ROS nodes and topics communication" %}


## Video

{% include googleDrivePlayer.html id=page.driveId2 %}
