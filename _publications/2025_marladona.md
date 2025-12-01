---
title: "Marladona-towards cooperative team play using multi-agent reinforcement learning"
collection: publications
category: conferences
permalink: /publication/marladona
excerpt: 'A multi-agent reinforcement learning framework for cooperative robotic team play, enabling coordinated behaviors and strategic interaction through decentralized policies and shared objectives.'
date: 2025-05-19
venue: 'IEEE International Conference on Robotics and Automation (ICRA)'
# slidesurl: 'https://academicpages.github.io/files/slides1.pdf'
paperurl: 'https://www.research-collection.ethz.ch/server/api/core/bitstreams/38b22ef1-7603-496f-804f-c9c56574e4dc/content'
bibtexurl: '/files/bibtex_marladona.bib'
citation: 'Z. Li, F. Bjelonic, V. Klemm, and M. Hutter, “Marladona – Towards cooperative team play using multi-agent reinforcement learning,” in <i>Proc. IEEE Int. Conf. on Robotics and Automation (ICRA)</i>, pp. 15014–15020, 2025.'
---
This paper presents MARLadona, a decentralized multi-agent reinforcement learning (MARL) framework capable of producing coordinated team play in robotic soccer — a domain that remains an unsolved benchmark for multi-agent systems. Built on a custom GPU-accelerated soccer environment implemented in Isaac Lab, the approach uses improved permutation-invariant entity encoders and a suite of curricula (initial positions, team-size variations, and self-play) to train agents end-to-end. Unlike many prior works that rely on scripted high-level actions or kinematic simulators, MARLadona models realistic physics and learns policies directly from low-level velocity commands.

The learned agents exhibit robust cooperation, passing, positioning, and role distribution across team sizes ranging from 1v1 to 11v11, generalizing far beyond the 3v3 setting used in training. In comprehensive evaluations against multiple baselines, including the world-champion HELIOS agent, MARLadona achieves a 66.8% win rate, demonstrates strong ball possession, and executes coordinated passing sequences. This work shows that scalable, physics-grounded MARL can produce sophisticated team behavior with minimal rewards and lightweight networks, marking a significant step toward real-world multi-robot collaboration.
