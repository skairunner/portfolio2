---
title: "Recipe recommender"
date: 2016-11-15T14:47:41-04:00

caption: "A typical usage of the webapp. Given four ingredients, recipes that can be made with some combination of said ingredients are displayed."
github: false
img: "recipes.png"
languages: ["javascript", "python"]
link: "#"
platform: "Web"
summary: "Recipe recommending by ingredients owned"
role: "Team leader, developer"
categories: ["full stack"]
technologies: ["d3", "javascript", "python", "sql"]
teamsize: "3"
thumb: "recipes.thumb.png"
---

Recipe Recommender (RR) is a web-app that finds recipes. In particular, it takes into consideration the ingredients the user already has, helping the user find recipes to make while only additionally purchasing a few more ingredients.

RR was created during Hack Shanghai, hosted at NYU Shanghai, with a team of 3. My contribution to the project was the client and the backend infrastructure. We used SQLite to store data, with an internal API to allow switching SQLite with a different SQL implementation such as PostgreSQL. I also implemented an ingredient "stemming" algorithm, which treated similar ingredients as one--e.g. *a can of peas* and *fresh peas* becomes a single *peas* for the purposes of the search.