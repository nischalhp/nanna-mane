---
title: Pycon India 2015 - Dev sprint 
tags : ["data", "community", "conference", "d3.js", "visualisation"]
date : "2015-07-28"
type : "passages"
---

# Pycon India 2015 - Dev Sprint - Data Science/ Visualization 
Dev sprint as we had know, is a day that is dedicated to solving bugs of a  project or sometimes working on building a new project itself. Never having done a dev sprint before, we chose to bridge the gap between performing data science in python and a way to visualize them in the world of javascript.

So we all know [D3] (http://d3js.org/) is amazing for visualization and we wanted to do what [Vincent] (https://github.com/wrobstory/vincent) was doing for [Vega] (https://github.com/vega/vega) and make it compatible for Vega 2.0. Atleast that was the idea. [We did some planning prior to the dev sprint and it really helped us to understand which parts each of us would be mentoring](https://hackpad.com/PyCon-IN-2015-DevSprint-Viz-Eqkdzm3EFDR)

There were 4 of us [Amit Kapoor] (www.twitter.com/amitkaps) , [Bargava](www.twitter.com/bargava), [Raghotham] (www.twitter.com/raghothams) and [I] (www.twitter.com/nischalhp)  who were conducting this dev sprint and how we achieve our dev sprint was pretty open ended. We started the day at around 10 in the morning and pitched our idea to the developers who were assembled to conquer the dev sprint. About 10 engineers loved our idea and we started discussing on what we wanted to solve. @amitkaps took a session on visualization and showed the need for building the bridge between python and d3 visualization. 

Once people had a hang of basic visualization, we wanted to build barchart and scatter plot in d3 by generating vega-spec.

So we started off the dev sprint in style, created a slack group and a github repository for adding code. We also planned on how we would achieve this:

1) Build python Bar chart and Scatter chart classes that can generate vega-lite spec.
2) Build a python module to generate the Data json from Pandas dataframe that can be added to vega-lite spec.
3) Inject the js and html content required to render the chart in ipython notebook.
4) Pass the vega-lite spec to the vega-lite library to generate the vega spec that in turn generates the chart in ipython notebook.

All these tasks looked very easy for us to solve as we had almost 7 more hours for the dev-sprint to end, but as we started hacking ,along came the roadblocks. The major ones were:

1) How to split work among interested people.
2) Understanding how to generate vega-lite spec.
3) Understanding how to generate vega spec from vega-lite spec.
4) How to get javascript and html content to render in ipython notebook.

Solving these roadblocks is what made the dev-sprint an awesome experience.

1) We solved the problem of splitting work by asking people how proficient they were with pandas and python , the interest levels they had to learn and made 2 small teams of 3 people each to build python modules to generate bar chart and scatter plot vega-lite specs.

2) Vega-lite has very little documentation on what happens inside vega-lite and we solved this by forking the project and debugging the code. It was a wonderful experience as we were understanding and reading good code.

3) After we debugged the vega-lite code we were able to pinpoint to the function that generate the vega spec and we just had to re purpose the javascripts to do the same.

4) We found a lot of open source projects and documentation on how we could use js and html inside an ipython notebook and this really helped us integrate the whole thing at ease.

By the end of day we were able to generate vega-lite spec from a python module on reading a csv via pandas into data frame and using that to generate the vega-lite spec. We had the bar chart to work independently by using the generated vega-lite spec. We still needed to integrate all of them into one single project. We called it a day off and decided to kick start the hacking next day post pycon talks. 

We started hacking as per schedule the next and after another hour of debugging and doing some experiments we finally finished what we were set out to do and this gave all of us a High. A high of achievement and working together to generate an open source project that solved a problem. [This was the outcome of the sprint](https://github.com/nischalhp/python-devsprint-viz).

The experience of the dev-sprint was exhilarating as we got to meet so many new engineers, aspiring students and people from different walks of life coming together to solve something different and wonderful. This makes us believe more in hacking together to solve problems and truly realize the power of open source. 