---
title: "PCT Archive"
date: 2019-01-10T14:47:41-04:00

caption: ""
github: true
githuburl: "https://github.com/skairunner/pct-archive"
img: "pctarchive.png"
languages: ["python"]
link: "https://pctarchive.com"
platform: "Web"
role: "Full stack developer"
summary: "Short-form creative fiction archive"
teamsize: "1"
categories: ["full stack"]
technologies: ["django", "python", "elasticsearch", "postgresql", "oauth2", "discord.py"]
thumb: "pctarchive.thumb.png"
---

PCT Archive is a repository for short works of creative fiction ("snips"). It archives the contents of a "snip trade" channel on a Discord chat server and associates metadata with it, including characters, author and summary. The fiction is also searchable across multiple axes, including content and characters.

The snips are gathered from a Discord chat channel via the Discord API. Users can then authenticate with the archive through the Discord OAuth portal and edit or update their snips. Snips are stored in a PostgreSQL database as the primary source of truth, while documents are inserted into Elasticsearch for indexing purposes only. All searches are done via the Elasticsearch API, including filtering by author or character. The text query uses the `simple_string_query`, allowing for robust queries with natural fuzzy/OR results that the user expects.

Following the guidelines of progressive enhancement, PCT Archive is fully accessible on a Javascript-disabled (but otherwise modern) browser, while having convenience or aesthetic features added for those clients which do have Javascript.
