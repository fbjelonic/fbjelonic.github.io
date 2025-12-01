---
title: "Learning quiet walking for a small home robot"
collection: publications
category: conferences
permalink: /publication/quiet_walk
excerpt: 'This paper introduces a reinforcement learning approach for generating quiet and stable walking behaviors in small home robots, focusing on minimizing acoustic emissions while preserving locomotion robustness and natural motion.'
date: 2025-05-19
venue: 'IEEE International Conference on Robotics and Automation (ICRA)'
# slidesurl: 'https://academicpages.github.io/files/slides1.pdf'
paperurl: 'https://arxiv.org/pdf/2502.10983'
bibtexurl: '/files/bibtex_quiet_walk.bib'
citation: 'R. Watanabe, T. Miki, F. Shi, Y. Kadokawa, F. Bjelonic, K. Kawaharazuka, A. Cramariuc, and M. Hutter, “Learning Quiet Walking for a Small Home Robot,” in <i>Proc. IEEE Int. Conf. on Robotics and Automation (ICRA)</i>, 2025.'
---

This work addresses the problem of excessive foot-step noise when quadruped robots walk in home environments — a major obstacle for their acceptance as household companions. The paper proposes a sim-to-real reinforcement learning framework that minimizes foot contact velocity (a major contributor to footstep sound), by allowing the policy to dynamically adjust PD gains per joint, using foot-contact sensors to modulate damping/stiffening, and applying curriculum learning to gradually penalize high-contact velocities. 

Experiments with a small home robot show that the learned policy produces significantly quieter walking compared both to a standard RL baseline and to carefully hand-tuned commercial controllers. The study demonstrates the feasibility of noise-aware locomotion and highlights the trade-off between noise reduction and robustness, paving the way for more user-friendly robots operating in domestic environments. 
