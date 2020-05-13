---
title: "LA In Anarchy Map"
date: 2019-08-07T14:47:41-04:00

caption: "Main page of the LA In Anarchy map depicting main regions"
github: true
githuburl: "https://github.com/skairunner/laia-map"
img: "laiamap.png"
link: "https://skairunner.github.io/laia-map/"
platform: "Web"
role: "Developer"
summary: "Custom GIS-based points of interest map"
teamsize: 1
technologies: ["javascript", "react", "d3", "gis"]
categories: ["Web dev"]
thumb: "laiamap.thumb.png"
---

*LA In Anarchy* is a vampire-themed roleplaying community set in a fictional version of Los Angeles. Because not all members of the community are familiar with the geography of LA, I built a custom map based on freely available GIS data to illustrate the setting. Regions listed in the Los Angeles County GIS don't fully match with the conceptual regions as typically used by people, so I also used the LA Times Neighboorhoods database and merged the polygons to form one cohesive area. The UI is written in React, taking advantage of its declarative format to write a clean and usable interaction. I use d3 to render the GIS data, utilizing its map projection libraries, while the DOM is manipulated by React.
