---
title: Tweetlyze
tags : ["Master thesis", "twitter", "data analysis"]
date : "2014-06-30"
type : "passages"
---

# Tweetlyze- Twitter Data Extraction

I started off my MS project on trying to understand Twitter trends and  predict the sectors that are affected by the trend , thereby helping people make better business decisions.

I had to throw this idea away as it required a lot of groundwork to be done in understanding various sectors and what can be affected and what not.

But I was sure i wanted to do something with Twitter trends , so i thought why not build a trend summarizer. Trends are so abstract sometimes that it is really hard to know what they are actually talking about. I wanted to solve this problem.

But to solve that problem , I was in need of huge amounts of twitter data related to trends and with respect to time. So I then realized there were two problems I needed to solve:

    1. Extraction framework to get Twitter Data      
    2. Using this data to build a summarizer.

This post is about all the decisions I took in building a fairly scalable **twitter data extraction framework**

At first I started understanding the difference between **streaming API** and the **REST API** of twitter. I realized I did not have the infrastructure to handle streaming API and there are some problems with using streaming API as well.
For ex: If i give a search tag to the streaming API, it returns all the tweets that contain that tag and also the tweets in which the tag might be a part of the statement. This would require building an additional cleansing framework and having access to big infrastructure. I did not want to take this route.

For my experiment the twitter REST API looked solid.
 
I had ways to get trends for a given location.      
I had ways to get tweets related to a trend.    
I knew what the rate limits were per call/per app.    
I had access to varying URL parameters to reduce replication of data.    

This was my starting point. I was at a point where I could start writing some basic code to fetch data and see what the data looks like.

This is where I encountered **another problem**. There were so many frameworks to access twitter REST API using `oauth` and all of them had weird ways of doing it. Maybe i am not used to looking at complex methods or I maybe dumb.

I thought why use some other framework to connect , when I could write something on my own that uses basic `oauth` libraries and connect to twitter. > Voila - I could do it with close to 20 lines of code.
Now I had an oauth established connection to the twitter REST API via my twitter app.

I then used the oauth approved object to make calls to find trends and look at the tweets.

All of these calls returned data in the form of  `JSON`. 
Now I had a tough call to take on which database to use. JSON data was screaming at me to use `NoSQL`. But then i needed relational mapping between data. I had read enough about NoSQL that it was poor when it comes to handling relations.

So i was thinking i would store all of my raw data on `MongoDB` and then run some scripts to process them and push them into a relationalDB.
I had almost started working on this when my friend raghotham(www.raghothams.in) pointed out, why not use `Postgresql 9.3`.
It is a relational DB , has JSON Store and also other cool features like building indexes in varied ways and huge community to offer help.
I was extremely pleased to know something like this existed and I decided on using Postgresql for 2 reasons.


    1. It reduced my stack.    
    2. I had complete control over raw data and processed data at one place.


I created the schema on Postgresql based on my the relations i had defined.
At this current state I had the following things working:

    1. Connect to twitter app using oAuth.    
    2. Making twitter API calls using the oAuth object.    
    3. Writing back the JSON response into Postgresql.    

Phew.

 Now I needed to scale. I had to get in more data and I had to get data continuously to build the summarizer. I had a rate limits problem and also how i would get data by spreading calls through out the day.

I was pondering on how to this , then I thought why not create multiple twitter apps as each app has a quota of calls for a time window.
This lead to creation of multiple email accounts and their respective twitter apps.
Now i had to spread calls evenly for each app based on the number of search tags I had and for a given time window.

WOW , such constraints,much AMAZE!

So I ended up writing a module that instantiates all the Twitter apps I have created , create multiple copies of the oAuth object and push them onto a `BlockingLinkedQueue`.

Problem 1 solved.

Then I used an executor framework to create multiple threads that picks up oAuth objects from the queue and makes respective calls and puts them back into the queue.

After i reached my limit for the window , i added a Thread.sleep() mechanism to refresh the quota of all my apps.

Problem 2 and 3 solved.

Now i had a mechanism that scaled , fetched more data , always within rate limits and the calls were evenly spread out over the day there by reducing redundant data.

This is in short how I built a twitter data extraction framework.

PS: Will add more details about every module I used to build this, once I find some time. 
