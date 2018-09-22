---
title: "Jeeves Course Planner"
date: 2018-09-15T14:47:41-04:00

caption: "Jeeves in use."
github: true
githuburl: "https://github.com/skairunner/JeevesCoursePlanner"
img: "jeeves.png"
link: "http://jeeves.skye.tech/"
summary: "Visual course-planning webapp for NYU"
languages: ["typescript", "python"]
role: "Main developer"
platform: "Web"
teamsize: "1+"
tech: ["d3", "yarn", "selenium"]
thumb: "jeeves.thumb.png"
---

Jeeves Course Planner is a web-app and tool built for students at New York University to help select courses. It includes the ability to quickly filter courses, check time conflicts, and preview a schedule on a calendar. It was created in response to the school-provided alternative, Albert. Albert is built on a technology stack vendored by Oracle and displays a lack of quick filtering, no way to visually compare schedules, and sluggish response times, which adds up to a poor user experience--every interaction is an AJAX request, including simple things like expanding course descriptions.

The web-app is written in Typescript, using d3.js for manipulating the DOM. The app uses Yarn to build and manage dependencies. The data is extracted from Albert using a script that controls Selenium, which also subsequently processes and cleans the data for consumption by the client. 

I have maintained Albert for 3 years circa late 2018. For the most recent class registration session, Google Analytics confirms that I had 509 unique users and 1300 sessions over a period of 2 months. Because the userbase for Jeeves has a uniquely high ratio of users who use adblocking programs, my real userbase is likely around 700. Jeeves is a free and open source program, and I have received contributions from classmates to fix bugs or implement features.