---
title: Kick-starting your journey in Data Engineering 
tags: [Data Engineer, Big Data, Data Warehouse]
style: fill
color: info
description: Introduction to the world of data engineering.
---

This is going to be a long series. Why? Because this series of blogs will involve everything from the inception of Big Data and understanding the problems associated with it, to the birth of Data Engineering. 

It will be a series consisting of individual blogs targeting big data concepts and tools used in this domain.

I will try to make them independent of each other, so that you can go forward and read them in any order you want. But, if you are a newbie, it's highly suggested you go through all the blogs. 

#### Introduction to Data Engineering

Ok, so let's start our journey. First I will set some context and share with you the reason I am writing this blog. 

Since you are here, you must be trying to learn DE in the first place. Mostly it may be due to you having such requirements in your workplace - your team may have decided to make fault-tolerant and scalable data pipelines (with the help of Airflow and Spark and a plethora of other technologies), and you want to learn this quickly so that you contribute. Or maybe you just have heard buzzwords like Kafka, Druid etc and you just want to learn it to stay relevant.

So, what do you do?  Straight dive into your browser and google out blogs on it and start reading about it.
**Stop**, this is not how you learn. Don't get me wrong here. I understand if you had not searched for blogs on Big Data you would not have got this blog itself. What I mean to say is, learning all the technologies and frameworks without understanding the bigger picture is the biggest mistake everyone makes. Failure of understanding the larger picture would prohibit you from becoming a good engineer who understands the entire data pipeline and not small parts of it.

With an assumption that you want to be on the side of a fully capable Data Engineer, we kick off the technical part for this blog.


#### What is Data Engineering and Who is a Data Engineer? 
Data engineering involves everything around managing the data in your workplace. The managing part can consist of consuming data from different sources, loading it into a warehouse and making the same data available for analysis for different teams in your workplace. This involves writing lots of code and maintaining infrastructure. All this has to be done using prevalent software engineering practices.
 
You have often heard, data is the new oil, and oil is crude, it has to be refined and stored before being distributed for consumption. The same goes for data, it's crude and making sense of huge amounts of data is tough. So you have to make a system that refines it to various levels so that it can be consumed by various sources. And you will be responsible and accountable for it. If anything breaks in oil extraction and refinement firms, dollars are lost, the same would be the case for data. But don't be afraid, the oil industry is one of the most mechanized and thriving industries in the world, the same can be the case with data.

So in a gist, a data engineer would write strong resilient pipelines that bring in data from heterogeneous sources and store it securely in a warehouse in a form to facilitate quick analysis upon the data by other teams in your workplace. But, this is just the tip of the iceberg, there are many more components associated with it.


#### Next, let's address the Data in Data Engineering.

I will keep it simple, we are generating huge amounts of data, of different types every day. That tells us about the main ‘V’s of Big Data - **Volume, Variety, Velocity**.

If you have any one of the above V in a large amount in your data, welcome to the big data world.



#### The million-dollar question - how do we handle big data? 

Let's start with the most obvious problem of storing and serving large amounts of data. For this we need better databases or storage mechanisms.

Let’s start with an incremental approach to answering this question.
  * Scale your infrastructure vertically. (i.e increase your processing power, add more cores, more RAM to your server, increase storage). If this solves your problem, stop now and get peaceful sleep until this approach fails.
  * Okay, so you have reached the limit of vertical scaling, what next? Partition your database and save it in different nodes to allow multiple reads and writes at the same time. Oh but wait, to allow multiple reads, the same data needs to be present in all the servers. That means you have to replicate the data into multiple partitions as soon as you receive a written request. If you can manage to do so, great, you have earned yourself another good night's sleep.
  * Good morning, one of your nodes is dead. Your system is again struggling to serve all your requests. So you need to get the node up and running and also ensure no data is lost, all the pending writes to the nodes must be saved in a queue and written to this node once this node is up. Great, you start working on this too and come up with a solution. Awesome.

![Alt Text](https://media.giphy.com/media/xTiN0uId37jNZCMLSM/giphy.gif)

But wouldn’t it be great if all of this can be done by a framework or a process through which we can handle the above problems more efficiently? Yes, we can.

The world of data engineering helps us in solving problems related to managing data in a resilient way with performance and also provides an interface for quick debugging.

But wait, is that it?
Is data engineering only focussed on storing and serving large amounts of data?

Of Course not. We’ll deep dive into more use cases and need for DE and the problems introduced with big data in the next blog.
