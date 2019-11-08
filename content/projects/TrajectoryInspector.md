---
title: "Trajectory Inspector"
date: 2018-03-15T14:47:41-04:00

github: true
githuburl: "https://github.com/skairunner/TrajectoryInspector"
img: "trajectoryinspector.png"
languages: ["javascript", "python", "C#"]
link: "http://trajectory.skye.tech/"
platform: "Web"
report: "/trajectory-inspector.pdf"
role: "Research, developer"
summary: "Data vis project to map major physical airways"
teamsize: "1"
technologies: ["d3", "javascript", "c-sharp", "sql"]
categories: ["infoviz", "web dev"]
thumb: "trajectoryinspector.thumb.png"
---

Trajectory Inspector is a proof-of-concept web-app that analyzes aircraft GPS positioning data to cluster and display similar routes. Visualizing the paths airplanes take in the sky is not a simple problem. There are thousands of planes in a given area at once, and drawing the paths on top of each other often leads to tangled, unreadable messes. 

In Trajectory Inspector, I use the EDwP algorithm proposed by S. Ranu et al (2015) as a distance measure between trajectories, and Lu & Fu's nearest-neighbor clustering algorithm to decide which paths are similar. Similar paths have identical colors. The user can click on clusters to view all aircraft in that cluster, and interact with the aircraft list to filter which paths are currently visible on the map. 

To make Trajectory Inspector, I used multiple technologies, leveraging the advantages of each. The JSON file format is used as a common communication interface between component programs.

* `python 3` was used to handle the bulk of the scripting, including loading the raw sensor data into Postgre, processing data into path files, and the clustering.
* `C#` was used to calculate the EDwP distance between paths. I originally implemented the EDwP algorithm in Python, but it was prohibitively slow so I rewrote it in C#. On inputs of length 10, the Python implementation took **77s** to complete, while the C# rewrite took << 1s.
* `d3.js` and `javascript` was used as the client. d3.js is nearly a *lingua franca* of infoviz, and allows even complicated visualizations to be coded with little effort. I leveraged many ES6 features for quality of life.


Trajectory Inspector was my final project for Information Visualization with Dr. Nan Cao. The full list of citations can be found in the README.md [here](https://github.com/skairunner/TrajectoryInspector), and a report is available above.







