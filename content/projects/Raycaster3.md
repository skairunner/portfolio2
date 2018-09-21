---
title: "Raycaster3"
date: 2016-06-15T14:47:41-04:00

github: true
githuburl: "https://github.com/skairunner/raycaster3"
img: "raycaster3.png"
link: "http://trajectory.skye.tech/"
summary: "Bottom-up 3D renderer in Python"
tech: ["python"]
thumb: "raycaster3.thumb.png"
---

Using pyeuclid for geometry, JSON format for configuration files and pure Python
for the rest, I created a simple implementation of a recursive raytracer. This version builds on the experience I gained coding a [previous one](https://github.com/Skyyrunner/Raytracer). For example, camera rotation is implemented with quaternions. Features include:

* render spheres and planes
* Show reflections up to a specified number of bounces
* camera rotation and translation
* multiple objects and lights
* easy task distribution, lending itself well to multiple threads or even machines

However, due to limitations of Python, render speeds are not fast enough for a realtime display and are instead saved to a file.