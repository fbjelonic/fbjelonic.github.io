---
title: "Minimal"
excerpt: "Minimal is a small-scale, mostly 3D-printed quadruped roughly the size of a standard stair, built with high-performance pseudo–direct-drive actuators and variable-gear joints.<br/><img src='/images/minimal.jpeg'>"
collection: robots
---

I used Minimal as a fast, lightweight platform to validate the core components of PACE — especially actuator modeling, parameter identification, and sim-to-real locomotion transfer. Its small size, 3D-printed structure, and pseudo–direct-drive variable-gear actuators made it ideal for rapid experimentation, allowing me to iterate on models, rewards, and control strategies far more quickly than on larger systems.

On the real robot, I deployed the learned controllers to test robustness under challenging conditions relative to its scale: steep obstacles, uneven surfaces, and full stair climbs that match nearly the robot’s own height. Through repeated hardware experiments, I refined both the controller and the simulation fidelity, ultimately demonstrating that even a small, low-cost platform can achieve reliable stair ascent and agile terrain traversal when powered by accurate actuator models and a well-designed sim-to-real pipeline.

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/minimal_stairs_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    Minimal continuously walking upstairs.
  </figcaption>
</div>
