---
title: "Distributed Cracker"
date: 2017-12-15T14:47:41-04:00

github: true
githuburl: "https://github.com/skairunner/distributed-pwforcer"
img: "dcp.png"
languages: ["C"]
link: "#"
report: "/dcp_report.pdf"
role: "Developer"
summary: "Distributed threaded password cracker"
platform: "Linux/Ubuntu"
teamsize: "1"
tech: ["POSIX"]
thumb: "dcp.thumb.png"
---

Distributed Cracking Program, or DCP, is a distributed password brute-forcer, coded for the final project of Operating Systems with Professor Olivier Marin. Full technical details are specified in the report (above). DCP is a server-client model, where clients connect via internet to the main server to receive work, in this case brute-forcing from a list of passwords. Each client attempts to take full advantage of its available processing power, spawning worker threads and distributing work between them.

DCP is very much a proof-of-concept, because instead of using existing parallel processing methods such as OpenMPI/OpenMP/GPU-based methods, I implemented a message-passing interface from the ground-up, including a packet API. Additionally, all interthread communication was written with POSIX primitives such as mutexes or semaphores. 