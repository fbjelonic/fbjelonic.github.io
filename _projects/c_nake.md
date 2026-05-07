---
title: "C-nake"
collection: projects
date: 2019-04-06
author_profile: false
excerpt: "A classic Snake game implemented in pure C++ for the command line, developed as a learning project to explore real-time logic, input handling, and object-oriented programming principles.<br/><img src='/images/cnake_teaser.webp' alt='C-nake terminal game teaser' loading='lazy'>"
---

# C-nake  
*Classic Snake game implemented in C++ for the command line*

---

<img src='/images/cnake_teaser.webp' alt='C-nake terminal Snake game teaser' loading='lazy'>

## Abstract

**C-nake** is a minimalistic implementation of the classic *Snake* game (originally introduced in 1976), written entirely in **C++** and running inside the command prompt.

The project focuses on logic, performance, and clean code structure rather than graphical user interfaces. It was developed as a personal learning challenge and served as my first deeper dive into both **C++** and **object-oriented programming**.

---

## Background

This project was created during my **second semester in Hong Kong (February 2019)**.  
At the time, my primary programming experience was limited to MATLAB, and I wanted to expand my skill set into lower-level, performance-oriented languages.

After the traditional *Hello World* experiment in C++, I set myself a challenge:

> Build the Snake game from scratch — without any tutorial.

I deliberately avoided graphical frameworks and opted for a **pure terminal-based implementation**, focusing on:
- Game logic design  
- Input handling  
- Real-time updates  
- Memory and performance control  

Remarkably, a basic functional version was completed within a single day.

---

## From Procedural to Object-Oriented Design

A few weeks later, I decided to revisit the project with a second goal:  
learn and apply **object-oriented programming principles** properly.

Using the excellent resource  
📘 [learncpp.com by Alex Allain](https://www.learncpp.com/)  
I restructured the entire codebase into a fully object-oriented design.

This refactor introduced:
- Encapsulated game state  
- Dedicated classes for snake, board and logic  
- Cleaner separation of responsibilities  
- Easier extendability

The transformation from procedural to OOP not only improved the codebase but significantly deepened my understanding of modern C++ design.

---

## Features

- Real-time keyboard input
- Dynamic snake growth
- Collision detection
- Score tracking
- Smooth terminal rendering
- Object-oriented architecture

All implemented without external libraries.

---

## Video Demonstration

Gameplay of the terminal-based C-nake:

<figure class="site-media">
  <video autoplay loop muted playsinline preload="metadata">
    <source src="/images/snake_full_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    C-nake in a linux terminal.
  </figcaption>
</figure>

---

## Key Takeaways

This project marked an important milestone in my programming journey:
- First real C++ application  
- First encounter with OOP design patterns  
- Strengthened understanding of logic flow and memory handling  
- A practical reminder that simple projects can be powerful learning tools

---

*No graphics. No gimmicks. Just pure logic.*
