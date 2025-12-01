---
title: "Tytan"
excerpt: "Tytan is a high-torque quadruped built by combining the ANYmal main body with low-inertia, torque-dense legs. It is custom built at the Robotic Systems Lab.<br/><img src='/images/tytan.png'>"
collection: robots
---

I used Tytan as the primary platform to demonstrate large-scale sim-to-real transfer, deploying reinforcement-learning locomotion controllers trained entirely in simulation onto a real, torque-dense quadruped. My work focused on building the full simulation pipeline, developing high-fidelity actuator models, and validating that learned policies generalize to high-speed locomotion, heavy payloads, and diverse terrain conditions on the real robot.

At the same time, I acted as Tytan’s “parent”: I was responsible for the robot’s overall reliability — from software integration and low-level controller debugging to diagnosing electrical issues, sensor problems, and mechanical failures. Much of the project involved making Tytan a robust, everyday-usable research platform, ensuring that experiments ran smoothly and that the learned controllers could be evaluated safely and consistently in the real world.

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/tytan_pushing_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    Tytan rejecting external disturbances.
  </figcaption>
</div>
