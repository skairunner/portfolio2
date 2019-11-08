---
title: "ErosionSim"
date: 2015-03-15T14:47:41-04:00

caption: "Simulation in progress, including a 3D view as well as informative panel views."
github: true
githuburl: "https://github.com/Skyyrunner/FluidSim"
img: "watersim.png"
languages: ["C++"]
link: "#"
platform: "Desktop"
role: "Developer"
summary: "Virtual pipes-based water erosion sim"
teamsize: "2"
categories: ["graphics", "simulation"]
technologies: ["c++", "dx11"]
thumb: "watersim.thumb.png"
---

ErosionSim is a simulation of erosion caused by the flow of water, with a real-time display of the deformed terrain. I implemented the "virtual pipes" model described in [Mei, Decaudin, Hu (2007)](/004.fluid.fast_hydrolic_erosion_simulation_and_visualisation.pdf). Water is placed in imaginary, discrete "boxes" and water flow is modeled as water transfer between two such boxes. When water moves faster, it picks up soil from the ground; when it moves slower, sediment is deposited, thus changing the landscape.

I coded ErosionSim in C++, with Allegro for the 2D info window and a DX11 renderer for the real-time view(made by Elise Alway). The simulation is threaded for performance, and has a simulation speed of roughly 20fps at optimum on a standard consumer-grade PC. Below is a video of a typical runtime experience. The mostly flat initial terrain ends up smoothed in places and deeply carved in others.

<iframe width="560" height="315" src="https://www.youtube.com/embed/wyeOvM2rNd8" frameborder="0" allowfullscreen></iframe>