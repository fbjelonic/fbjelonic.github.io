---
title: "2WD Rosduino"
collection: projects
excerpt: "ROS-controlled Arduino robot with manual and autonomous driving modes."
date: 2020-05-30
author_profile: false
# optional:
excerpt: "A differential-drive Arduino robot controlled via ROS and an Xbox controller, featuring both teleoperation and autonomous obstacle avoidance. This project introduced the foundations of robotic control architectures and real-time communication pipelines.<br/><img src='/images/rosduino_full_teaser.jpg'>"
# layout: single   # or another layout your theme provides
---

# 2WD ROSduino  
*Differential-drive Arduino robot with ROS-based remote control and autonomous mode*

---

<img src='/images/rosduino_full_teaser.jpg'>

## Abstract

This project focuses on building a compact two-wheel differential-drive robot using standard electronic components and an Arduino-based control architecture.

The platform supports two operating modes:
- 🎮 **Remote control via Xbox controller**
- 🤖 **Autonomous navigation using an ultrasonic distance sensor**

The primary challenges involved designing a reliable electrical circuit, establishing a feasible **ROS communication architecture**, and implementing real-time control logic in C++.  
The final result and real-world operation can be seen in the [video section](#video) below.


---

## Background Story

During the winter semester 2019/2020, I participated in — and won — a robotics challenge at **TU Darmstadt**. The competition involved autonomous pick-and-place of tennis balls using a TurtleBot3 equipped with a 5-DOF gripper arm.

<img src='/images/robotic_challenge_winner.jpg'>

A recording of the final run can be found here:  
🎥 [https://youtu.be/cxs0oeeQU-w](https://youtu.be/cxs0oeeQU-w)

The prize was a standard Arduino-based 2WD car kit — which became the foundation for this project.

Initially, my goals were simple:
- Convert the kit into a remote-controlled vehicle  
- Use an Xbox controller for intuitive control  
- Integrate it with ROS for extensibility  

This led to the introduction of a Raspberry Pi 4B as an intermediate control layer. While technically functional, it quickly revealed two limitations:
- The platform was **overpowered from a computing perspective**  
- The mechanical drivetrain was **underpowered**

These insights eventually motivated the transition to the more ambitious [Autonomous Driller](/projects/autonomous_driller/) project.

---

## Assembly

The base kit consisted of a standard 2WD chassis, dual DC motors, and a basic Arduino controller.

<img src='/images/arduino_assembly.png'>

The full system architecture with my custom upgrades included:
- Arduino Uno for low-level motor control  
- Raspberry Pi 4B for ROS integration  
- Motor driver module  
- Battery pack  
- Ultrasonic sensor for obstacle detection  

The assembly process involved modifying the standard kit for better cable routing, stable motor mounting, sensor integration and micro-controller integration.

---

## Controller-to-Arduino Communication

The control pipeline was structured as follows:

Xbox Controller → Laptop → ROS Node → Raspberry Pi → Arduino


### Communication Roles

- **Xbox Controller**  
  Provides user input via joystick and buttons.

- **Laptop**  
  Maps controller input to velocity commands and transmits via ROS.

- **Raspberry Pi**  
  Acts as the ROS master node, handling command processing and forwarding.

- **Arduino**  
  Executes low-level motor control through PWM signals.

This architecture allowed seamless switching between:
- Manual teleoperation  
- Autonomous obstacle-avoidance mode  

---

## Autonomous Mode

In autonomous mode, the ultrasonic sensor continuously measured distances ahead.  
Simple logic ensured:
- Forward movement if clear  
- Rotation if obstacle detected  
- Adaptive correction depending on distance thresholds  

This mode served as an introduction to sensor-based feedback control and robotic decision-making.

---

## Video

First functional test with Xbox remote control and ROS-based communication:

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/arduinoBot_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    Remote Controlled Test of the 2WD Rosduino
  </figcaption>
</div>

---

## Key Takeaways

This project marked my first end-to-end robotics system combining:
- Hardware assembly  
- C++ embedded programming  
- ROS architecture  
- Real-world teleoperation  

Although simple in hindsight, it laid the foundation for more complex systems — and ultimately inspired the transition toward high-performance autonomous platforms.

---

*Small robot. First control loop. Big curiosity.*
