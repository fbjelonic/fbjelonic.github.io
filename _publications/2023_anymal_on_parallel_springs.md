---
title: "Learning-based design and control for quadrupedal robots with parallel-elastic actuators"
collection: publications
category: manuscripts
permalink: /publication/anymal_on_parallel_springs
excerpt: 'This work presents a learning-based co-design approach that jointly optimizes compliant actuation and control policies, demonstrating improved energy efficiency and robust performance in quadrupedal robots equipped with parallel-elastic actuators.'
date: 2023-01-06
venue: 'IEEE Robotics and Automation Letters'
# slidesurl: 'https://academicpages.github.io/files/slides1.pdf'
paperurl: 'https://arxiv.org/pdf/2301.03509'
bibtexurl: '/files/bibtex_aops.bib'
citation: 'F. Bjelonic, J. Lee, P. Arm, D. Sako, D. Tateo, J. Peters, and M. Hutter, “Learning-based design and control for quadrupedal robots with parallel-elastic actuators,” <i>IEEE Robotics and Automation Letters</i>, vol. 8, no. 3, pp. 1611–1618, 2023.'
---
This paper presents a framework for co-optimizing both the mechanical design of parallel-elastic knee joints and locomotion controllers for quadrupedal robots. Instead of relying on human intuition or heuristics, we train a design-conditioned control policy via model-free Reinforcement Learning that works over a range of candidate spring parameters, then use Bayesian Optimization to identify the spring design that maximizes energy efficiency and performance.

Applied to the robot ANYmal, the optimized design reduces the required joint torques by ~30%, improves torque-square efficiency by ~33%, and enables ~11% longer operation time on flat terrain — all without compromising locomotion tracking or versatility on varying terrain.

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/aops_twitter_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    AoPS teaser.
  </figcaption>
</div>
