---
title: "Erosion sim"
date: 2016-03-15T14:47:41-04:00

github: true
githuburl: "https://github.com/Skyyrunner/FluidSim"
img: "watersim.png"
link: "#"
summary: "Virtual pipes-based water erosion sim"
tech: ["C++"]
thumb: "watersim.thumb.png"
---

This is a simulation of water, using the "virtual pipes" model described [in this paper](http://ww.w.roxlu.com/downloads/scholar/004.fluid.fast_hydrolic_erosion_simulation_and_visualisation.pdf). Water is placed in imaginary, discrete "boxes" and water flow is modeled as water transfer between two such boxes. Implemented with C++, with Allegro for the 2D info window and a DX11 renderer (made by Joshua Alway), this simulation utilizes up to 4 threads to more rapidly process each simulation step. It has a simulation speed of roughly 20fps at optimum.

<iframe width="560" height="315" src="https://www.youtube.com/embed/wyeOvM2rNd8" frameborder="0" allowfullscreen></iframe>