---
title: "Raycaster3"
date: 2016-06-15T14:47:41-04:00

caption: "A sample render from Raycaster3, showing the reflection feature and the available geometry."
github: true
githuburl: "https://github.com/skairunner/raycaster3"
img: "raycaster3.png"
languages: ["python"]
technologies: ["python"]
categories: ["graphics", "game dev", "simulation"]
link: "#"
platform: "Desktop"
role: "Developer"
summary: "Bottom-up 3D renderer in Python"
teamsize: "1"
thumb: "raycaster3.thumb.png"
---

Raycaster3 is a simple recursive raytracer, built from the ground-up. It accepts a JSON format configuration file and uses `pyeuclid` for geometry. I calculate collisions from rays 'fired' through each screen pixel, then calculate secondary or tertiary rays that result from reflection as well, and sum up the results for the final render. Raycaster3 builds on the experience I gained coding a [previous one](https://github.com/Skyyrunner/Raytracer). For example, camera rotation is implemented with quaternions. Features include:

* render spheres and planes
* Show reflections up to a specified number of bounces
* camera rotation and translation
* multiple objects and lights
* easy task distribution, lending itself well to multiple threads or even machines

However, due to limitations of Python, render speeds are not fast enough for a realtime display and are instead saved as a file. Additionally, the most typical triangle geometry is not supported, nor are more advanced features such as refraction, global illumination, or caustics.