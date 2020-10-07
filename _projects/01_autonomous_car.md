---
title: "Autonomous Driller"
permalink: /projects/autonomous_car/
excerpt: "A 3D printed autonomous car project"
toc: true
---

## Abstract

- Autonomous car
- exploration, mapping and delivery (of chocolate)

## Background story

- wanted to make rosduino autonomous
- adding a camera, lidar or even depth camera would be an overkill (in terms of cost)
- ROSduino was not strong enough (fast)
- as kid, always dreamed of making my own RC Car because they were usually too expensive.
- alltogether made me want to start this project

## What has the car to do with a "driller"?

- dad came to me and asked me: Do you need this old driller? Its broken and I do not need it anymore.

- show picture, how the machine looked like

- Searched for a capable device for PWM to control it with my arduino and tested it: it worked (show video of the drill engine at work)

- show picture of the drill engine on the car

## 3D printer car chassis

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
