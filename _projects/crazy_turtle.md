---
title: "Crazy Turtle"
collection: projects
excerpt: "Advanced feedback control experiments for ROS turtlesim with dynamic wall avoidance."
date: 2019-08-15
author_profile: false
# optional:
excerpt: "An advanced control framework for ROS turtlesim implementing non-blocking goal navigation, feedback control, and intelligent wall avoidance using action-server-based communication.<br/><img src='/images/crazy_turtle_teaser.png'>"
# layout: single   # or another layout your theme provides
---

# Crazy Turtle  
*Advanced feedback control for ROS turtlesim with wall-avoidance and action-based goal handling*

---

<img src='/images/crazy_turtle_teaser.png'>

## Abstract

This project explores the design and implementation of two feedback controllers for the ROS **turtlesim** environment, enhanced with a dynamic wall-avoidance strategy and an action-based goal interface.

Instead of relying on blocking terminal commands, the system utilizes:
- A **ROS service** for user interaction
- A **ROS action server** for goal tracking and execution

This architecture allows the user to change target positions for the turtle at any time without interrupting execution. The service node handles user input and forwards goals to the action server, which continuously steers the turtle toward the target while reporting state feedback such as distance and velocity.

As a result, goal updates are smooth, responsive, and non-blocking — closely mimicking real robotic control pipelines.


---

## Background

I began learning **ROS** in mid-2019. Like many others, my journey started with the official tutorials, where one of the first visual tools introduced is the widely-known **turtlesim**.

The typical beginner setup involves:
- Running the turtlesim simulator
- Controlling the turtle via keyboard input using `teleop_twist_keyboard`

While simple, this environment quickly became a playground for experimenting with control logic.

After mastering manual control, I aimed to push it further:
- Replace manual steering with autonomous control
- Introduce intelligent wall avoidance
- Integrate goal-based navigation logic

Thus, the *Crazy Turtle* was born.

---

## Feedback Control with Wall Avoidance

Two different feedback control strategies were implemented and compared. Both aimed to steer the turtle toward a specified target while avoiding collisions with the simulation boundaries.

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/lets_go_turtle_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    Wall avoidance using control barrier functions.
  </figcaption>
</div>

### Core Concepts

- Continuous distance feedback to the goal  
- Heading angle correction based on target orientation  
- Penalization near boundaries using a wall cost function  

The wall avoidance is implemented through a penalty-based approach. The closer the turtle approaches the boundary, the higher the cost applied to the control signal.

<img src='/images/wallbump.png'>

To maintain numerical stability in simulation, the cost function is clipped:

```python
cost = min(cost, 20)
```


This prevents extreme corrective forces that lead to oscillations or instability near corners.



---

## ROS Communication Architecture

Two additional ROS nodes were introduced:

### 1. Service Node
- Accepts user-defined turtle position goals
- Forwards goal requests to the action node

### 2. Action Node
- Executes navigation toward the goal
- Publishes feedback (current position, remaining distance)
- Allows real-time goal modification without blocking

<img src='/images/rqt_graph_crazy_turtle.jpg'>


### Why use an Action Server?

| Feature | Service | Action |
|--------|---------|--------|
| Blocking | Yes | No |
| Feedback | No | Yes |
| Goal modification | No | Yes |
| Continuous execution | No | Yes |

Using an action server enables interactive, real-time control — similar to real-world navigation stacks.

---

## Implementation Highlights

- Feedback-based pose control  
- Online goal switching without execution interruption  
- Dynamic obstacle (wall) avoidance  
- ROS message-based modularity  
- Action-service hybrid communication

This structure closely follows patterns seen in professional robotic navigation systems.

---

## Video Demonstration

Final demonstration showing dynamic goal switching and continuous wall-avoidance behavior:

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/turtle_full_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    Running both controllers in the turtle simulator.
  </figcaption>
</div>

---

## Key Takeaways

This project provided hands-on experience with:
- ROS action architecture  
- Feedback control design  
- Wall avoidance logic  
- Non-blocking robotic command interfaces  

It was a crucial step toward more advanced navigation and autonomy pipelines — and a playful experiment in making a simple turtle behave intelligently.

---

*Small turtle. Serious control theory.*
