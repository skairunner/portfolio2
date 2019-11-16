---
title: "KSE"
date: 2019-11-07T14:47:41-04:00

caption: "An example of KSE in usage in conjunction with Spriter"
github: true
githuburl: "https://github.com/skairunner/kanimal-SE"
img: "kse.png"
link: "https://github.com/skairunner/kanimal-SE/releases"
platform: "CLI"
role: "Developer"
summary: "Tool to convert between cutout (vector) animation formats"
teamsize: 1
technologies: ["c-sharp", "appveyor"]
categories: ["tool", "graphics", "game dev", "ci-cd", "library"]
thumb: "kse.thumb.gif"
---

kanimal SE (KSE) is an open source library and command-line interface (CLI) tool that converts between cut-out animation formats, including kanim (Klei animation) and scml (Spriter) using a common, intermediate in-memory format. KSE was developed to support *Oxygen Not Included* modding. The project is an extension of kparserX, which itself is an extension of kparser by Davis Cook (@daviscook477).

Modding games such as *Oxygen Not Included* poses many unique challenges. For *Oxygen Not Included* in particular, adding new assets to the game requires compiling to Klei, the developer's proprietary animation format. Although the format is well-understood, the developers are understandably reluctant to release their internal tools. Therefore, a method to convert between an open format to the Klei format is required.

kparser is the most-used conversion program in the *Oxygen Not Included* modding community, written supporting Java 9+ and two formats, Klei format and Spriter format (.scml, project files for a free, but not open software). It has many drawbacks, though, due to its status as a rough, proof-of-concept tool that was not developed further. Klei format animations consist of three files of separate file types (.png, _anim.bytes, _build.bytes), and kparser requires users to provide the files as absolute paths in a specific order. The program crashes with an unintuitive error message when these requirements are not fulfilled. kparser has many other implicit, poorly-documented requirements that respectively crash with a null reference exception. kparserX is a fork of kparser that attempts to address these issues, but others were not so easily solvable. The common Java version distributed at java.org is version 8, while kparser/X requires version 9+, again posing a barrier to entry. .NET Core allows for trivial cross-platform support with self-contained programs, and the vast majority of the *Oxygen Not Included* community is more proficient with C# as well, so I decided to first port kparser/X to C# then refactor and add usability improvements that help ensure the principle of least surprise is preserved.

KSE is structured as a typical CLI tool: the functionality is contained within a relatively clean API with no CLI, and a separate CLI program is written which interfaces between the command line and the library. Moving away from passing path strings to methods to passing Stream objects, which can represent files, in-memory objects, or even network streams allows more flexibility when extending KSE and also helps keep the API clean, and was an obvious choice. The functionality of kparserX is split into Readers (KanimReader, ScmlReader) and Writers (KanimWriter, ScmlWriter), which respectively read into and write out from a loosely-defined, common in-memory format. This architectural decision also allows for easier extension of KSE for formats beside the initially supported two, such as an alternative editor format like Adobe Animate or Synfig, or alternative target formats such as .gif. 

I also enhanced the ScmlReader capabilities. Spriter operates on the concept of "keyframes", and when values for a sprite are not explicitly specified in a given keyframe Spriter interpolates the values from the last known and subsequent known values. kparser/X does not support this feature, but KSE does. Other features include the ability to consume Spriter files with "animation bones" without crashing as well as supporting sprite substitutions.

I intend to continue maintaining KSE, eliminating unexpected errors and ensuring that fatal errors are easy to understand and fix. KSE has Continuous Delivery (CD) targetting three platforms (Windows, MacOS, Linux) and two formats (self-contained and framework-dependent) hosted on AppVeyor, so improvements will be effortless to deliver.
