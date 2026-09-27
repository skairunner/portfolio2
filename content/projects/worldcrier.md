---
title: "Worldcrier"
date: 2026-07-14T20:28:28+02:00

caption: "Some example RSS embeds."
alt: "A screenshot of Discord. A bot named Worldcrier has sent two messages in the form of embeds, each with an article title, short blurb, link and time."
github: true
githuburl: "https://github.com/skairunner/worldcrier"
img: "worldcrier.png"
link: "#"
platform: "Server"
role: "Developer"
summary: "WorldAnvil RSS bot"
teamsize: 1
technologies: ["rust"]
categories: ["tool"]
thumb: "worldcrierlogo.png"
---

Worldcrier is a bot that reads the WorldAnvil RSS feed for my fiancée's world and posts new entries to a Discord announcements server. WorldAnvil provides a Discord embed webhook, but it is not customizable. So I created a Discord bot to address this need.

The `serenity` framework is used for the bot side. Discord is a highly realtime application, so its API is not simple to interface with and involves several complex topics. Serenity provides a fairly ergonomic wrapper around it.

Similar to [Commentater](/projects/commentater), launching Worldcrier spawns a task that periodically polls the RSS feed. Interestingly, it seems like there is no standard of how to get updates from RSS feeds. It feels like a relic of a different internet. The RSS feed items are upserted into an SQLite database.

The bot itself also periodically polls for items to send. It tries to prevent sending too many messages from a single world at once. Although I had thoughts of making it a multi-tenant system, it didn't seem necessary given that there was only one user.