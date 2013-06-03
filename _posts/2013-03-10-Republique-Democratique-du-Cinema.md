---
layout: post
title: RDC - République Démocratique du Cinéma
category: essay
image: /images/banners/liberte.jpg
alt: Liberté guidant le peuple
status: Draft n°2
confidence: Good
tags: Révolution
share: link
---

My new project. A really democratic movie review website. How does one achieve this? Why, with sentiment analysis of tweets. This is the first post in a long series, an introduction if you will.

### The inception

I wanted to play for a long time with Natural Language Processing (NLP) for a few reasons. First, because it's cool. Being a litterature geek, when i can combine code and prose, it's more than a pleasure. Second, while working on a few projects in pre-production (meaning: in a sketchbook), I realized that a lot of the underlying tchniques needed were often coming back to NLP. One of them being Sentiment Analysis. Sentiment analysis is practical. It is hands on application of NLP theories.

At the same time, I observed the cruel lack of good movies reviews sites in french. Except for a subpar and ads-ridden "imdb", there is not a lot. No RottenTomatoes (RT), no Flixster, no nothing.
So the idea to create something akin to RT came to mind, but with a spin. The reviews would not come from established professional critics but from average people. You, me and everybody else.

### Why do it, It already exists !

I am aware that such concepts have already been tested and approved, to various level of success. I want to do it for two reasons. First, because as I previously mentionned, it doesn't really exists in french, not that I know of.
Second, it will be a good learning opportunity on several aspects. The algorithmic aspect, but also the DevOps aspect.

After reading a discusion about AWS on HackerNews, I realized that the project could not only be decoupled in code but also in infrastructure. I will therefore try to write a couple articles about that solution, and how everything is working, both for the code and for the servers.

### The Project Plan
I will explain in a more in-depth fashion the "architecture" of the project in a future post. But for now, I'll just explain the broad view.

So, the idea is to take tweets about a movie, aggregate them, analyse them with a sentiment analysis algorithm, put them in a database, complete them with classic infos about them (poster, year, ...) and finally dipslay the results to the audience. That's it for the basic concept.

I want to ultimately streamline everything and make it entirely automatic if possible. I'm not there yet.

I am currently working on the MVP, after many nights of pondering of how to do it. I decided that if I continued to ponder on various little details, it will never be done. So yes, it is rudimentary at the moment. It's mostly a proof of concept.
You can check the advancement on github, everything starting with "RDC".

Sorry if this is not really a technical post, but it's more suited here.
In the next posts, i will explain furthermore, in no particular order: the detailed "architecture" of the project, the different parts of AWS, the possible algos for the analysis, how everything work together...