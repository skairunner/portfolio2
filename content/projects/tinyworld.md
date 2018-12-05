---
title: "TinyWorld"
date: 2018-06-15T14:47:41-04:00

caption: "A top-down view of a procedurally generated tinyworld."
github: true
githuburl: "https://github.com/skairunner/Graphics-Final-Project"
img: "terraingen.png"
languages: ["javascript"]
link: "https://terrain.skye.im"
platform: "Web"
role: "Procedural generation developer"
summary: "Procedural 3D landscape"
teamsize: "3"
tech: ["three.js"]
thumb: "terraingen.thumb.png"
---

Tinyworld is a web-app that displays an entirely procedurally generated, peaceful landscape, including terrain coloring.

I wrote most of the code that decided the actual generation of the terrain as well as the face colors. Other members of the team decided the creative direction and implemented controls or the water effects.

The terrain uses a modification of the ever-present Perlin noise algorithm to generate flatter terrain that still preserves some extremes, called *exponential Perlin noise* and presented in [Parberry (2015)](https://larc.unt.edu/ian/research/tobler/). The terrain is overall much flatter than typical Perlin noise-based terrain, which not only provides the impression of more 'realistic' terrain but also avoids tiring the viewer, thus making the few extremes that do exist more impactful.