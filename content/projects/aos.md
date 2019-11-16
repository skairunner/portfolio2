---
title: "Abstract OS Simulator"
date: 2019-05-07T14:47:41-04:00

caption: ""
github: true
githuburl: "https://github.com/gpDA/ImageScrapBook"
img: "aos.png"
link: "#"
platform: "Desktop"
role: "Academic developer"
summary: "High-level OS simulator for teaching purposes"
teamsize: 2
technologies: ["python", "typescript", "react", "d3"]
categories: ["educational", "simulation"]
thumb: "aos.thumb.png"
report: "https://docs.google.com/document/d/1EDVYRgEFvSVhhAnEA8ugyZNhRJxvgCUKs2Iopiilepw/edit?usp=sharing"
---

Abstract Operating System (AOS) is a simulation-based high-level teaching tool for teaching operating systems courses that runs in user-space, as well as a browser-based visual interface to interact with the AOS. Trial-and-error as well as immediate feedback are hallmarks of effective learning, especially in computer science, so a simplified but conceptually accurate operating system will likely provide large benefits. We built a virtual operating system that exposes clean interfaces for users to plug in their own algorithms for system processes such as memory allocation or process scheduling. Because our operating system is entirely ran in user-space, we can provide a complete picture of the current state of the system, and we can use any language for authoring the algorithms in question, though for our proof of concept we chose Python.

The simulation consists of the following components:  
1. An abstract operating system in Python, including simulated physical memory, memory management, abstract processes and schedulers  
2. A simple, script-like language to flexibly define process behaviour (i.e. how much work a process does, and how much resources it attempts to acquire) and resource acquisition  
3. A TOML-based scenario configuration file that defines the system state, including process spawning, simulated hardware specification, and resource availability  
4. A visualization written in React, a library that supports declarative rendering techniques, and d3.js, a target-independent library for rendering visualizations, primarily using SVG for display of information.  
