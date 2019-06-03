---
title: Making architecture choices for small and big data problems
event: Strata California 2017 
event_url: https://conferences.oreilly.com/strata/strata-ca-2017
location: San Jose, United States of America
summary: Learn lessons from building end-to-end data science systems. Understand the importance of adopting software engineering practices 
abstract: "
Enterprises want to be data driven from the very beginning or want to join the race for data supremacy. Being data driven requires the system to store and process every single transaction and interaction the customer makes with the product, thus enabling the business to make better decisions.
<br>
But storing, processing, and analyzing data comes with a cost. This cost is distributed across the choice of technology, infrastructure, and go-to-market strategy.
<br>
Nischal HP and Raghotham Sripadraj share their experience building data science platforms for various enterprises, with an emphasis on making the right architecture choices for things such as databases, queues, caching mechanisms, distribution of the workload, underlying technology for machine learning and predicitive models, visualization, and prototyping. Nischal and Raghotham stress the importance of using distributed and fault-tolerant tools, which themselves come with the cost of managing the infrastructure (including, by implication, a dedicated team to monitor the infra). However, with small data, simple tools take you a long way.
<br>
Many things can go unnoticed in building an end-to-end data science system, like the importance of logging, building a data pipeline that sends notifications to the required medium of communication, exposing data science as a service via APIs, or A/B testing for data science-backed feature releases when required. Only when the data science solution is in production does it power the organization the right way.
<br>
When building data science products you should live by the motto “fail fast.” Nischal and Raghotham themselves have failed fast when making these choices, but in time they came to understand that adopting the latest and the coolest technology on the planet just for the sake of it is not the right thing to do.
"


# Talk start and end times.
#  End time can optionally be hidden by prefixing the line with `#`.
date: "2017-03-16T16:20:00Z"
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

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.

# Enable math on this page?
math: true
---
{{< gdocs src="https://docs.google.com/presentation/d/e/2PACX-1vT72BY_ol7e4QVMq01quMGCepism1Ara4t7mMWo-HR4tYw5wJK8IRL3AbiXMMQV-mblqXYwVJT3S5Tp/embed" >}}