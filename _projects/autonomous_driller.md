---
title: "Autonomous Driller"
collection: projects
excerpt: "Autonomous rover built from a drill motor with custom 3D-printed chassis and ROS-based navigation."
date: 2021-07-10
author_profile: false
# optional:
excerpt: "A high-torque vehicle powered by a repurposed drilling machine motor, combining 3D-printed mechanics with ROS-based perception, SLAM, and navigation. Designed as an experimental platform for exploration and autonomous delivery.<br/><img src='/images/driller_new_teaser.png'>"
# layout: single   # or another layout your theme provides
---

# The Autonomous Driller  
*3D-printed autonomous vehicle powered by a repurposed drilling machine*

---

<img src='/images/driller_new_teaser.png'>

## Abstract

This project explores the construction of a 3D-printed autonomous vehicle designed for exploration and small-scale delivery — most notably, serving chocolate to detected humans on demand.

The platform combines repurposed hardware with modern robotics techniques. For perception, mapping, and human detection, an **Intel RealSense D455 depth camera** is used, enabling real-time SLAM and navigation.

A natural question arises: *Why is it called the Driller?*  
The answer lies in its heart — quite literally.  
You can read the full story [below](#what-does-a-car-have-to-do-with-a-driller).


---

## Background

After completing my previous project, the [2WD ROSduino](/projects/2wdarduino/), I wanted to take the next step: autonomy.

I began researching suitable sensors for navigation:

- Raspberry Pi Camera Module – ~50 USD  
- RP LIDAR – ~120 USD  
- Depth Camera – ~240 USD  

Compared to the base ROSduino cost (~40 USD), this felt excessive. Then came an unexpected twist: my father presented me with a broken drilling machine.

That moment sparked an idea.  
Instead of upgrading a small robot car, why not build something entirely new?

This is how the concept of the **Autonomous Driller** was born.

---

## What does a car have to do with a driller?

When my father casually asked:

> *“Do you need parts from this? It’s broken and I don’t need it anymore.”*

I saw opportunity where others saw scrap.

I opened the casing and discovered an impressive compact engineering system: a small motor paired with a powerful planetary gearbox.

<img src='/images/drill_engine_opened.jpg'>

The motor was rated at:

**750 W ≈ 1 HP**

For comparison:
- Typical ROSduino motors: ~25 W  
- This motor: 30× more powerful  

The first challenge was control. I purchased a PWM MOSFET motor controller and tested the setup successfully — confirming that the motor could be reused.

Below: early experiments holding the motor while testing output torque.

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/drill_engine_control_test_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    First motor drive test.
  </figcaption>
</div>

---

## From aluminium to 3D printing

With a functioning drivetrain, I began designing the vehicle chassis.  
My first iteration used aluminium sheets scavenged from my father’s workshop — purely as a rapid prototype.

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/alu_sheet_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    First aluminium sheet test.
  </figcaption>
</div>

While functional, this approach lacked precision and scalability. I transitioned to 3D printing and used **Tinkercad** for fast CAD prototyping. Components were first modeled at real scale:

- Drill motor
- Li-ion battery
- Motor controller
- Arduino Uno
- Raspberry Pi


For the base chassis, I adapted the excellent open-source design  
[Tarmo3 by Kris Shellman](https://www.thingiverse.com/thing:3547058), and fully redesigned the drivetrain, axle system, and gear layout to support significantly higher torque.


Initial drivetrain test:

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/first_transmission_test_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    First actuated drive-train test.
  </figcaption>
</div>


And the assembled structure including electronics:

<img src='/images/auto_driller_full.jpg'>

---

## ROS Communication

This vehicle runs on a distributed ROS architecture:

- MOSFET: low-level motor control
- Raspberry Pi: execution and middleware
- Laptop: monitoring and command interface

Communication happens via SSH and WiFi using the ROS master-slave model.  

---

## Outtakes & Lessons Learned

### Never connect a high-power motor directly to a battery

Out of curiosity (and slight laziness), I bypassed the controller and connected the 750 W motor directly to the battery.

The result: instantaneous peak-torque and structural failure.

No injuries, only learning.

<img src='/images/engine_to_chassis.jpg'>

<img src='/images/car_wheel_destroyed.jpg'>

<img src='/images/wheel_destroyed.jpg'>


---

## First Test Drive

The first successful remote-controlled test run of the Autonomous Driller. I capped the output power at 10%.


<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/first_test_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    First full system test.
  </figcaption>
</div>

---

*High torque. High curiosity. Low budget.*