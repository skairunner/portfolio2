---
title: "Image Scrapbook"
date: 2018-12-24T14:47:41-04:00

caption: "Public gallery page of Image Scrapbook"
github: true
githuburl: "https://github.com/gpDA/ImageScrapBook"
img: "imagescrapbook.png"
link: "#"
platform: "Desktop"
role: "Team leader"
summary: "Cloud-native image scrapbooking service"
teamsize: 3
technologies: ["python", "javascript", "bootstrap", "kubernetes", "docker", "postgresql", "s3"]
categories: ["full stack", "web dev", "devops"]
thumb: "imagescrapbook.thumb.png"
---

Image Scrapbook is a proof-of-concept, cloud native app made as a team during NYU's Large Scale Webapps class in Fall 2018. It is a web app plus a browser extension that allows users to select an image they are viewing on any website and saves the source image in their personal gallery. Image Scrapbook also allows for some simple social features, such as sharing images to friends on the site. It is built using Django for the webserver backed by a Postgres database. All aspects of the program are containerized and managed by Kubernetes, allowing easy scaling of resources in the event that it is required.

One of the services composing Image Scrapbook is a "thumbnailer" service. It is in charge of processing incoming images and creating thumbnails out of them. Although this process could be included on the webserver, it is  more CPU intensive than the other tasks a webserver would handle, and so I factored it out to allow for separate scaling. Each thumbnail process is a Celery worker running a script that uses Python Imaging Library to resize images. These workers are assigned tasks by the RabbitMQ server, also in a separate container, and upload the result thumbnails to Amazon S3, mocked with Minio.

I also implemented the Kubernetes configuration, packing each element into a Docker image and assigning permanent backing stores to the RabbitMQ and Postgres images. I wrote a deploy script that tears down and restarts the Kubernetes cluster, allowing for rapid and reproducible deployments. This was particularly useful because Google Cloud resources are relatively expensive for our use-case, so we could painlessly offline the webapp until it is needed, e.g. during the demo. Having a deployed script that is known to perform well helps to eliminate the common situation of tech demos not working when the program ran perfectly well in development.

As the team leader, I had to familiarize myself with the entire app, helping guide the design as well as ensuring that each component, worked on separately, was seamlessly interoperable with the others. Although my main area of work was the backend and devops, I am confident in my knowledge of the entire system, and I believe this familiarity helped me troubleshoot problems in other components.
