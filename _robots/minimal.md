---
title: "Minimal"
excerpt: "Minimal is a small-scale, mostly 3D-printed quadruped roughly the size of a standard stair, built with high-performance pseudo–direct-drive actuators and variable-gear joints.<br/><img src='/images/minimal.webp' alt='Minimal small-scale quadruped robot' loading='lazy'>"
collection: robots
---

I used Minimal as a fast, lightweight platform to validate the core components of PACE — especially actuator modeling, parameter identification, and sim-to-real locomotion transfer. Its small size, 3D-printed structure, and pseudo–direct-drive variable-gear actuators made it ideal for rapid experimentation, allowing me to iterate on models, rewards, and control strategies far more quickly than on larger systems.

On the real robot, I deployed the learned controllers to test robustness under challenging conditions relative to its scale: steep obstacles, uneven surfaces, and full stair climbs that match nearly the robot’s own height. Through repeated hardware experiments, I refined both the controller and the simulation fidelity, ultimately demonstrating that even a small, low-cost platform can achieve reliable stair ascent and agile terrain traversal when powered by accurate actuator models and a well-designed sim-to-real pipeline.

Beyond the research contributions, I also acted as Minimal’s “parent,” taking responsibility for its day-to-day reliability as a hardware platform. This included debugging actuator electronics, fixing mechanical failures in the 3D-printed structure, tuning low-level controllers, and ensuring that experiments could run consistently without unexpected hardware issues. By keeping the robot stable, calibrated, and operational, I enabled fast iteration cycles for sim-to-real experiments and made Minimal a dependable small-scale testbed for PACE.

<figure class="site-media">
  <video autoplay loop muted playsinline preload="metadata">
    <source src="/images/minimal_stairs_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    Minimal continuously walking upstairs.
  </figcaption>
</figure>
