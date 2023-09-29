---
content_type: page
description: This section contains lecture slides and lab handouts.
learning_resource_types: []
ocw_type: SupplementalResourceSection
title: Lectures and Labs
uid: bf60161f-a614-ddc2-b359-59acdf14d2cb
video_metadata:
  youtube_id: null
---

The lab handouts below contain references to code and other files, which can be found in the {{% resource_link 4d40d34c-91f7-6621-3408-733271e4b1c3 "Datasets and Code" %}} section.

Day 0: Setup
------------

Before the class, please set up the environment. You will need to install some software and packages and download some datasets to get started. You can find the datasets in the {{% resource_link 4d40d34c-91f7-6621-3408-733271e4b1c3 "Datasets and Code" %}} section. Note that the presidential contributions dataset can be downloaded from either the Federal Election Commission link given on page 4 of the setup instructions, or from the Datasets and Code section.

Lecture ({{% resource_link 42d3a025-06e3-a2bb-b8c1-c8eb120bfe3b "PDF" %}})  
Setup instructions ({{% resource_link b34a71a3-18b7-8cae-5720-e5f6625a75b1 "PDF" %}})

Day 1: Let's play with some data!
---------------------------------

Today we will analyze the presidential campaign contributions dataset. We will go through the full process of downloading a new dataset, the initial steps of understanding the data, visualizing it, coming up with hypotheses, and exploring the dataset. Hopefully, you'll learn something new about presidential elections.

Lecture ({{% resource_link 5798f33c-524d-917a-be52-819adb68fc5f "PDF - 1.0MB" %}})  
Lab handout ({{% resource_link 0cf5cabd-adce-c527-77c5-f5020341a6c6 "PDF" %}})

Day 2: Visualizations
---------------------

Today, we will do more with matplotlib: bar graphs, line graphs, box plots, scatter plots, and choropleth (map) plots. We will also learn to create figures with multiple sub-figures, and customize labels, colors, error bars, etc. We will give you a basic understanding of how plotting works, which should be enough for a majority of the charts that you will want to create.

Lecture ({{% resource_link bcbf1667-eaa6-4ca6-43e9-23fd884520bb "PDF" %}})  
Lab handout ({{% resource_link 30d5bbd6-d59d-6eda-c96d-214ff773f274 "PDF" %}})

Day 3: Hypothesis Testing
-------------------------

So far, we've plotted and visualized data in various ways. Today, we'll see how to statistically back up some of the observations we've made in looking at our data. Statistics is a tool that helps separate news-making data-backed stories from one-off anecdotes. Usually, both kinds of stories start with a hunch, and statistics helps us quantify the evidence backing that hunch.

Whenever you have a hunch (a _hypothesis_ in statistician-speak), the first thing to do is to look at some summary statistics (e.g., averages), and explore the data graphically as we did yesterday. If the visualizations seem to support your hunch, you will move into hypothesis-testing mode.

Lecture ({{% resource_link 19e0a9fa-c5ec-1471-15bc-e81ba4daa68f "PDF" %}})  
Lab handout ({{% resource_link 5a85b1b2-4821-29e6-633c-a47a06cc59d5 "PDF" %}})

Day 3 (cont.): Regression
-------------------------

We hear about correlations every day. Various health outcomes are correlated with socioeconomic status. Iodine supplementation in infants is correlated with higher IQ. Models are everywhere as well. An object falling for _t_ seconds moves .5_gt_{{< sup "2" >}} meters. You can calculate correlation and build approximate models using several techniques, but the simplest and most popular technique by far is linear regression. Let's see how it works!

Lab handout ({{% resource_link 7efe00f1-2b11-fefc-7374-e366957f63b0 "PDF" %}})  
County Health Rankings: explanation of .csv files ([TXT](./resolveuid/7cf9e4578674871f88fc11228a9ebf1a))

Day 4: Text Processing
----------------------

Today we will discuss text processing. Our exercises will be grounded in an email dataset (either yours or Kenneth Lay's). After today, you will be able to compute the most important terms in a particular email, find emails similar to the one you are reading, and find people that tend to send you similar emails. And since emails are just text documents, this applies to any text document you can think of, like webpages, articles, or tweets.

Lecture ({{% resource_link 293f219a-b7d7-2951-1209-d12e5c9735c8 "PDF" %}})  
Lab handout ({{% resource_link a78a2c26-4fe2-3c37-6429-41f568335a3d "PDF" %}})

Day 5: Processing Large Datasets
--------------------------------

On day 4, we saw how to process text data using the Enron email dataset. In reality, we only processed a small fraction of the entire dataset: about 15 megabytes of Kenneth Lay's emails. The entire dataset containing many Enron employees' mailboxes is 1.3 gigabytes, about 87 times than what we worked with. And what if we worked on GMail, Yahoo! Mail, or Hotmail? We'd have several petabytes worth of emails, at least 71 million times the size of the data we dealt with.

All that data would take a while to process, and it certainly couldn't fit on or be crunched by a single laptop. We'd have to store the data on many machines, and we'd have to process it (tokenize it, calculate TF-IDF) using multiple machines. Let's start with a simple word count example, then rewrite it in MapReduce, then run MapReduce on 20 machines using Amazon's EMR, and finally write a big-person MapReduce workflow to calculate TF-IDF.

Lecture ({{% resource_link 4e9970d7-4fb0-9522-7b69-2be7fd134815 "PDF" %}})  
Lab handout ({{% resource_link 7397e445-47d8-915e-d63e-fe69409d0ae2 "PDF" %}})

### AWS S3 Instructions

In the AWS S3 section of the lab handout, the link to the full Enron dataset no longer works (it was only intended for in-class use). Instead, download the Enron email dataset from the {{% resource_link 4d40d34c-91f7-6621-3408-733271e4b1c3 "Datasets and Code" %}} section. After unzipping the files, use encode\_emails.py ({{% resource_link 620d0f58-9d79-058a-796f-c66b268663c4 "PY" %}}) to encode the emails into a json format that the mrjob MapReduce library can read:

> python encode\_emails.py \[input root folder\] \[output folder\]

The script will traverse through the \[input root folder\] and encode every text document (email) into a json encoded document stored at the corresponding location under the \[output folder\].

Day 6: Course Recap
-------------------

This day also contained student presentations, which are not included on OCW.

Lecture ({{% resource_link 9d352b3c-ac15-8c5e-f71c-dc7804544311 "PDF" %}})