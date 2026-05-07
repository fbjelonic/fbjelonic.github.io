---
title: "ANYmal"
excerpt: "ANYmal is a compact, electrically driven quadruped with torque-controlled joints and a sealed, lightweight frame. It integrates lidar, cameras, and inertial sensors for reliable state estimation and locomotion on uneven terrain.<br/><img src='/images/anymal.jpg' alt='ANYmal quadruped robot' loading='lazy'>"
collection: robots
---

I used ANYmal as a testbed to investigate energy-efficient legged locomotion: by equipping its knee joints with parallel elastic actuators, I explored how passive elasticity reduces torque requirements and impact loads in walking and stair climbing. 

Moreover, I developed a sim-to-real framework that integrates physics-grounded actuator modeling for ANYmal, using reinforcement learning to produce locomotion policies whose energy cost of transport is ≈ 32% lower than prior baselines — showing robust, efficient walking on the real robot.

<figure class="site-media">
  <video autoplay loop muted playsinline preload="metadata">
    <source src="/images/anymal_running_track_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    ANYmal on the running track, walking for 4km
  </figcaption>
</figure>
