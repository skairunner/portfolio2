---
title: "Chartered Waters"
date: 2014-06-05T14:47:41-04:00

github: true
githuburl: "https://github.com/skairunner/ChartedWaters"
img: "charteredwaters.png"
link: "#"
platform: "Desktop"
role: "Developer"
summary: "Procedurally generated age of sail game"
teamsize: "1"
technologies: ["c++", "libtcod"]
categories: ["game dev", "simulation"]
thumb: "charteredwaters.thumb.png"
---

![UI view](/charteredwaters2.png)

Chartered Waters is a procedurally generated game set in a fictional Age of Sail. Heavily inspired by the game series *Uncharted Waters*, and in particular *Great Age of Sail Online*, the aim of the project was to create a world with a living economy and agents acting as merchants capable of making informed decisions, painting a backdrop on which the player could make her decisions and affect the economy.

* Merchants are modeled as agents with imperfect models of the world. Merchants make decisions on what items to purchase or sell and which city to go given their model of the world, and update that model as they gain more data.
* Pathing is implemented using a weighted A\* algorithm. Care is taken to cache results and optimize for CPU caches.
* Procedurally generated world, including terrain generated with Perlin noise, and a simple weather model for greenery. Cities are placed with a Brownian motion-based algorithm, causing one faction's settlements to occur in roughly proximate regions.

While there is no guarantee that it will run, a link to an executable can be found [here](charteredwaters_20140529.zip).