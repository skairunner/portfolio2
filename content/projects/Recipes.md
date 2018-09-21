---
title: "Recipe recommender"
date: 2016-11-15T14:47:41-04:00

github: false
img: "recipes.png"
link: "#"
summary: "Recipe recommending depending on ingredients"
tech: ["javascript", "d3", "python", "sql"]
thumb: "recipes.thumb.png"
---

Created in a hackathon along with 2 other teammates. This web app takes a list of ingredients you have on hand, and searches for a recipe you can create either using only ingredients you have, or those you can make with *n* extra ingredients, where *n* can be provided by the user.

My contribution to the project was the client and the backend infrastructure.

* SQLite to create a database API for my other teammates to use
* queries and abstracted into a set of functions, so that when we migrate to a different database such as PostgreSQL, only the API internals will need to change.
* A webserver using Cherrypy, to serve the files and handle search requests
* d3 for DOM manipulations, data representation, and dynamic pages.