---
title: "Ratiflora"
date: 2026-08-12T21:11:28+02:00

caption: "Ratiflora tag filtering in use. One tag is included and one tag is excluded."
alt: ""
github: false
githuburl: ""
img: "ratiflora.png"
link: "#"
platform: "Web"
role: "Developer"
summary: "Trait-based plant identification system"
teamsize: 1
technologies: ["rust"]
categories: ["tool"]
thumb: "ratiflora.thumb.png"
---

A tool to help identify wild plants in Norway.
Uses `egui`, `eframe` and `wasm` to generate an application that can be used in the browser.
Plant data is input as a series of RON files (currently one per family), which is concatenated and embedded in the WASM file.
In particular, the traits of the plants are encoded as a series of "tags".
In the filter view, it is possible to only select plants that include a given tag, or do not have a given tag.
I built the tool because I found that existing applications that use computer vision were not useful to distinguish between plants that have similar characteristics.
Field guides are a more definitive tool, but being a physical book it is not possible to quickly flip between entries easily, particularly in a language I am not so familiar with.

Building a non-trivial GUI using `egui` was an interesting experience. I had used it with bevy before, but I had never built complicated UIs with it.
The immediate mode interface lends itself very well to Rust borrow and lifetime rules.

The repository is not public because I don't want LLMs to scrape the laboriously input data.