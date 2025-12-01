---
title: "ANYmal"
excerpt: "ANYmal is a compact, electrically driven quadruped with torque-controlled joints and a sealed, lightweight frame. It integrates lidar, cameras, and inertial sensors for reliable state estimation and locomotion on uneven terrain.<br/><img src='/images/anymal.jpg'>"
collection: robots
---

I used ANYmal as a testbed to investigate energy-efficient legged locomotion: by equipping its knee joints with parallel elastic actuators, I explored how passive elasticity reduces torque requirements and impact loads in walking and stair climbing. 
arXiv

Moreover, I developed a sim-to-real framework that integrates physics-grounded actuator modeling for ANYmal, using reinforcement learning to produce locomotion policies whose energy cost of transport is ≈ 32% lower than prior baselines — showing robust, efficient walking on the real robot.

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/anymal_running_track_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    ANYmal on the running track, walking for 4km
  </figcaption>
</div>
