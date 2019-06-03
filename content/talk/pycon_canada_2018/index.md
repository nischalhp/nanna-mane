---
title: Building and scaling Deep Learning Services with Deep Learning Frameworks, Flask, Kubernetes and docker
event: Pycon Canada 2018
event_url: https://2018.pycon.ca
location: Toronto, Canada
summary: Deep learning systems have to be engineered in order to be used in solving an end to end business problem. One of the challenges in architecting and building deep learning systems are the areas of maintainability, scalability and deployments. I would like to discuss on how we solve this at omnius.

abstract: "
Building technology platforms with AI systems requires a lot more thought process in terms of architecture and choice of tooling. The reason for this is because there is need for brainstorming around scaling, monitoring, deploying and managing the deep learning service as you would manage any other service.
<br><br>
In this talk, I will be talking about how to take Deep Learning systems to production with the use of packages and tools like:
<br><br>

* Keras / Tensorflow / Pytorch - Deep learning frameworks providing the flexibility to write custom deep learning functions with lower level APIs
<br><br>
* Flask - Flask is a micro web-framework that allows you to write REST endpoints with minimal effort. Its simple and easy to use. When paired up with Gunicorn, you can take it into production with no effort. The idea of using Flask is to provide REST end points for prediction.
<br><br>
* Kubernetes & Docker- Managing microservices which have a bunch of dependencies is hard to manage. Docker provides the capability of putting all the required pieces of software to run a service into one single logical box, thereby managing all the dependencies with ease. Kubernetes on the other hand provides the capability to orchestrate and manage these docker containers and manage the infrastructure in automated fashion with inbuilt service discovery, load balancing, self correction systems.
<br><br>
* ElasticSearch, Logstash & Kibana - Logging is one of the most crucial components of managing and running systems in production. With ELK, you can ship and manage logs from various services and this provides a way to evaluate how the prediction system is working in production.
<br><br>
* Prometheus - A tool to monitor Kubernetes clusters. This is a neat dashboard integrated with Grafana that shows the consumption of CPU and memory for systems in production, helping in evaluating how big or small the clusters should be in order to keep up with SLAs.
<br><br>
* Model Versioning - A model versioning system implemented in python to manage deep learning models and version them, thereby providing the capability to reproduce the results from various experiments.
<br><br>
* Managing Data sets - An introduction to Git LFS and how to manage datasets. Extremely useful when working with the thought process of reproducible results.
<br><br>
The focus of this talk to is to shed light on the qualms of architecting, devops and management of deep learning systems in production.
"
# Talk start and end times.
#  End time can optionally be hidden by prefixing the line with `#`.
date: "2018-11-17T17:30:00Z"
all_day: false

authors: []
tags: []

# Is this a featured talk? (true/false)
featured: false

image:
  caption: ''
  focal_point: Right

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/nischalhp
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

math: true
---
{{< gdocs src="https://docs.google.com/presentation/d/e/2PACX-1vQKR_yj4QE_ZMhtuNEQ1_O1dIFvsCtJc6lrf6tJS27YxX7dArall3WpFU-iO5fcYT-3ZusYK2DUk62-/embed" >}}
