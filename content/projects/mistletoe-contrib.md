---
title: "Mistletoe"
date: 2018-12-21T14:47:41-04:00

caption: "Contributed \"Limited HTML\" renderer to Markdown parser"
github: true
githuburl: "https://github.com/skairunner/mistletoe/tree/dev"
img: "mistletoe.thumb.png"
imgWidth: 256
link: "#"
platform: "Web"
role: "Open source contributor"
summary: "Contributed new renderer to Markdown parser"
teamsize: "1"
technologies: ["python", "markdown"]
categories: ["web dev", "library"]
thumb: "mistletoe.thumb.png"
---

[Mistletoe](https://github.com/miyuchina/mistletoe) is a pure Python, CommonMark-compliant Markdown renderer that supports multiple backends such as HTML, Jira docs, and different flavors of Markdown. Because it parses the input into an abstract syntax tree (AST) before rendering, Mistletoe is highly extensible to new targets.

I implemented a new render backend for a common use-case, Limited HTML. By default, Markdown operates on a trusted input model and allows you to embed arbitrary HTML in your Markdown that will be passed through to the final render target, if possible. When using Markdown as a simple formatting language in e.g. website comments, it's in the developer's best interest to disallow such arbitrary formatting because it is a very common attack vector.

My Limited HTML render target is a modification of the full HTML renderer that simply escapes the content of any blocks parsed as inline HTML. I read the source code as well as the documents to identify the architecture and inserted my new code in an appropriate location. I use this functionality on a number of my other projects, including [PCT Archive](/projects/pctarchive/).