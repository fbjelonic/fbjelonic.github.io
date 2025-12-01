---
title: "C-nake"
collection: projects
excerpt: "Minimalistic, terminal-based Snake game written from scratch in C++."
date: 2019-04-06
author_profile: false
# optional:
excerpt: "A classic Snake game implemented in pure C++ for the command line, developed as a learning project to explore real-time logic, input handling, and object-oriented programming principles.<br/><img src='/images/cnake_teaser.png'>"
# layout: single   # or another layout your theme provides
---

# C-nake  
*Classic Snake game implemented in C++ for the command line*

---

<img src='/images/cnake_teaser.png'>

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

<div style="max-width: 100%; margin: 1.5em 0;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.15);">
    <source src="/images/snake_full_web.mp4" type="video/mp4">
  </video>
  <figcaption style="text-align: center; font-size: 0.8em; color: #666; margin-top: 0.6em;">
    C-nake in a linux terminal.
  </figcaption>
</div>

---

## Key Takeaways

This project marked an important milestone in my programming journey:
- First real C++ application  
- First encounter with OOP design patterns  
- Strengthened understanding of logic flow and memory handling  
- A practical reminder that simple projects can be powerful learning tools

---

*No graphics. No gimmicks. Just pure logic.*
