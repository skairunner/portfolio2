---
title: "Commentater"
date: 2025-04-27T14:47:41-04:00

caption: "The front page of Commentater."
github: true
githuburl: "https://github.com/skairunner/commentater"
img: "commentater.png"
link: "#"
platform: "Web"
role: "Developer"
summary: "Third party WorldAnvil comment management system"
teamsize: 1
technologies: ["rust", "postgresql"]
categories: ["full-stack", "web-dev", "tool"]
thumb: "commentater.thumb.png"
---

Commentater is a third party tool that helps with managing WorldAnvil comments. WorldAnvil is effectively a SaaS content management system platform focused around writing wiki articles about fictional worlds. It provides a simple CRUD REST API, but at the time of coding, comments were not available through the API. Therefore, I created a low-impact scraper to fetch some of the information required.

Commentater consists of two main parts, the webserver and the task queue. The task queue uses Postgres as a simple FIFO queue. It polls items from the queue table using manual locking to prevent duplicate work and scrapes the comments at a sedate rate. The comment HTML is parsed and inserted into the database.

The webserver then interprets the stored comment data and uses the WorldAnvil API to fetch other information required, such as world names, article names, and usernames. It displays articles which have unanswered comments. This is because it is in the interest of many WorldAnvil authors to actively engage with their readers. WorldAnvil did not have any native solution to this at the time -- although it delivered notifications when comments are made, there was nowhere to see an overview of comments.

I wrote the webserver using `axum`, a relatively well-known library in the Rust space. It was an educational experience to experience how surprisingly ergonomic handler approach taken. I had used both `async` (the keyword) and `tower` before at Cognite, and axum basically took those concepts and took it further for ease of use in the web space. I also tried using `terra`, which is conceptually a straightforward port of Jinja2 to Rust. It is reasonably usable, though the loss of type safety (values are mapped to JSON before being used in the templating engine) left something to be desired.