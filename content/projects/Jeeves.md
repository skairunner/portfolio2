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
tech: ["d3"]
thumb: "jeeves.thumb.png"
---

Jeeves Course Planner is a tool built for students at New York University to help them select courses.

NYU's course selection tool, Albert, has many flaws. Chief among them are a lack of quick filtering, no way to visually compare schedules, and sluggish response times. I used Selenium to extract data from Albert, Python to index and process the data, and Typescript/d3.js for the frontend.

I have maintained Albert for 3 years circa late 2017. For the most recent class registration session, Google Analytics confirms that I had 509 unique users and 1300 sessions over a period of 2 months. Because the userbase for Jeeves has a uniquely high ratio of users who use adblocking programs, my real userbase is likely around 700.

Because Jeeves is open source, I was able to gain contributions from classmates to fix bugs or improve UI.