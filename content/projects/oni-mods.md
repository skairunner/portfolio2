---
title: "ONI mods"
date: 2019-09-07T14:47:41-04:00

caption: "Gallery of thumbnails for released mods."
github: true
githuburl: "https://github.com/skairunner/sky-oni-mods"
img: "oni-mods.png"
link: "#"
platform: "Desktop"
role: "Developer"
summary: "Add-ons for game Oxygen Not Included"
teamsize: 2
technologies: ["c-sharp", "unity"]
categories: ["game dev"]
thumb: "oni-mods.thumb.png"
---

I developed multiple popular mods for the game *Oxygen Not Included*, with a total of some ten thousand unique downloads. Some mods are less ambitious, adding new buildings that the player can build or otherwise filling in gaps in the base game, while others are more ambitious and overhaul large aspects of gameplay. I also worked with an artist to incorporate new assets into the game, handling the tooling pipeline of converting outside assets into a format recognized by the game. I used a common tool library (PLib) for modding the game, ensuring that I could preserve interoperability with other mods as well as minimize redundant code, and I interacted with the main developer behind PLib, pointing out bugs and making feature requests.

Because modding games requires an understanding of the code that can often only be attained by reading the decompiled source code for the base game, much of the time spent on creating mods was actually used to read source code and determine which aspects require modification. Some mods had simple, pre-defined insertion points, while the more complicated of my mods required understanding of C# IL, or touched multiple subsystems at once. Any API that exists for modding *Oxygen Not Included* is informal and subject to change, so continued maintenance was required for my mods when an update changed underlying structures my mod depends on. Handling bug reports was also part of maintenance, and I monitored both Github Issues and Steam Workshop comments.
