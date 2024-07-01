---
title: "Domain Adaptation in Transformer models: Question Answering of Dutch Government Policies"
date: 2022-08-04T23:15:00+07:00
slug: domainadaptationintransformers
category: projects
showTableOfContents: true
tags: ["First Post", "Hello World"]
summary:
description: 
cover:
  image:
  alt:
  caption:
  relative: true
draft: false
---

# Intro
During my Master's in Data Science at the University of Amsterdam, I worked on creating a Question Answering (QA) system for Dutch government policies using transformer models. This research aimed to improve how these models handle specific domains like government policies. In this blog post, I'll share my approach, the new dataset we developed, and the key findings that enhanced the performance of our QA system.

# Academic presentation
In November 2023, I presented my research at the University of Evora in Portugal. The audience consisted of academic researchers specializing in various AI fields, including computer vision, optimization, and other areas. I was part of the natural language processing group. Following this presentation, the research was published in collaboration with my UVA supervisor.

I met many cool people during this event, with whom I am still in contact. This experience not only helped me share my work but also allowed me to network with other AI professionals.

![Presentation at University of Evora](img//Evora-academics-nov24.JPG)
Evora, Portugal - November 24 2023


# Abstract

Automatic answering questions helps users in finding information efficiently, in contrast with web search engines that require keywords to be provided and large texts to be processed. The first Dutch Question Answering (QA) system uses basic natural language processing techniques based on text similarity between the question and the answer. After the introduction of pre-trained transformer-based models like BERT, higher scores were achieved with over 7.7% improvement for the General Language Understanding Evaluation (GLUE) score.

Pre-trained transformer-based models tend to over-generalize when applied to a specific domain, leading to less precise context-specific outputs. There is a marked research gap in experiment strategies to adapt these models effectively for domain-specific applications. Additionally, there is a lack of Dutch resources for automatic question answering, as the only existing dataset, Dutch SQuAD, is a translation of the SQuAD dataset in English.

We propose a new dataset, PolicyQA, containing questions and answers about Dutch government policies and use domain adaptation techniques to address the generalizability problem of transformer-based models.

The experimental setup includes the Long Short-Term memory (LSTM), a baseline neural network, and three BERT-based models, mBert, RobBERT, and BERTje, with domain adaptation. The datasets used for testing are the proposed PolicyQA dataset and the existing Dutch SQuAD.

From the results, we found that the multilanguage BERT-model, mBert, outperforms the Dutch BERT-based models (RobBERT and BERTje) on the both datasets. By introducing fine-tuning, a domain adaptation technique, the mBert model improved to 94.10% of F1-score, a gain of 226% compared to its performance without fine-tuning.

# Full-text article
[Read article](https://link.springer.com/chapter/10.1007/978-3-031-48232-8_19)