---
title: "Autonomous Driller"
permalink: /projects/autonomous_car/
excerpt: "A 3D printed autonomous car project"
driveId1: 1j1vHs6Mp_OBxqUeil8ZxK2VZTNFb5jZu/preview
toc: true
---

## Abstract

In this project, I build a 3D printed, autonomous car for exploration and delivery. The main idea is to let the car drive around by itself and find humans to serve chocolate on demand. For the mapping, exploration and human detection, I use a [Depth Camera](https://www.intelrealsense.com/depth-camera-d455/) from Intel. You are curious about *Why the hell is it called a driller?*. You can find it out [here](#what-has-the-car-to-do-with-a-driller).

{% include figure image_path="/assets/images/auto_driller_full.jpg" alt="this is a placeholder image" caption="Current progress of the car" %}

## Background story

After I finished my main goal for the [2WD ROSduion](https://www.fbjelonic.com/projects/2wdarduino/), I wanted to make an autonomous upgrade. So I went on google and looked for prices of:

- Raspberry Pi Camera Module ~ 50 US$
- RP LIDAR ~ 120 US$
- Depth Camera ~ 200-300 US$

If you compare the prices to the base set for the 2WD ROSduino (~40 US$), this would be clearly an overkill for me. So what now?

Together with the coincidence with my dad, showing me his [broken drilling machine](#what-has-the-car-to-do-with-a-driller), I decided to start a new project, the **autonomous driller**.

## What has the car to do with a "driller"?

At the time, when I was thinking about making [2WD ROSduion](https://www.fbjelonic.com/projects/2wdarduino/) an autonomous car, my dad once came to me. He had an old drilling machine in his hands and asked me: 

> *Do you need parts from this? It is broken and I do not need it anymore*. 

It was an *'Eureka!'* moment for me. I decided to start something bigger: **A car with a drilling machine engine.**

I did not even know how it looked like from the inside. So I opened the case and took a glimps:

{% include figure image_path="/assets/images/drill_engine_opened.jpg" alt="this is a placeholder image" caption="Drilling machine from inside" %}

From an engineering point of view, it was a beautiful moment. Opening the case and seeing the planetary gear with an incredible translation and the very small electric engine. Sooner, I would find out, that this little engine had about 

750 watt [W] = 1 horsepower [HP]

which is about **30 times more than the ROSduino engines** (max. 25 W)!
Before I thought about the car itself, I had to figure out how to control the old engine. I did not even know which parts of the drilling machien were broken. I bought a PWM (pulse width modulation) MOSFET engine controller to test the capabilities. And it worked! Which meant, I can go on and figure out how to build the body of the car. See me struggling to hold the engine while testing:

{% include googleDrivePlayer.html id=page.driveId1 %}

## From aluminium sheets to 3d printer

- Started with self-made parts from aluminium sheets

- show picture of self made quarter car

- didn't look quite nice and I knew I had to weld some parts to make it durable

- then I started to think about 3D printing, I started to google before I "reinvent the wheel". And I found another person, who thought in a similar fashion

- took some parts there and did the whole drive train by myself.

- used tinkerCAD

## ROS Communication

- lap top is the master, and starts the ros master and RViz if needed

- lap top could be used in future to speed up computations together with the raspberry pi

- raspberry pi gets data from RealSense camera and uses the data for path planning and object detection / avoidance.

## Video

Insert Video here.
