---
layout: post
title: The Architecture of RDC
category: technical
image: /images/banners/hallway.jpg
alt: Inception hallway scene
tags: Niemeyer
---

Before anything else, please allow me to put a little disclaimer.

The further description is neither exhaustive nor definitive. This is a plan, not a HD picture. Since I want and need to develop this project in an iterative manner, to test my early assumptions and advance with more confidence, it is highly probable it will change as the project evolve. Especially when it will be in its final form, where everything is automatised. but let's not put the horses before the cart.

I shall attempt to explain thouroughtly how I decided to articulate this app. to resume the basic idea:

Take tweets about a movie and aggregate them, analyse them with a sentiment analysis algorithm, put them in a database, complete them with classic infos about them (poster, year, ...) and finally dipslay the results to the audience. That's it for the basic concept.

I started imagining how i could make that work in a rails application. However, I was afraid of having a big thing of an app doing everything. That idea wasn't attractive, for obvious reasons. While reading a post about AWS, everything clicked. I was to decompose everything and make each element work with others like the platform itself do.

Photo of the general schema

A true lightbulb moment. It allowed me a bit more freedom in the way i could envision and develop the app. Or AppS, I should say...
It will be three diffent apps, each with a precise function. Here they are:

## The Dashboard

This is the back office of the project. I will allow me to manage the movie and their tweets, the database of tweets to be analysed, and in the future, to monitor various statistics and states.

Basically, I poll the Twitter Search API to obtain the tweet given a movie title, put all of them in a hash, and store the Title/Hash pair in a mongo document.

Why did I chose Mongoid? For the ease of development, while I figure all the details of the implement. It's more than probable that once i will have everything figured and the project running smoothly, I will convert to a traditional SQL db (most likely Postgresql).

## The Analysis

I will explain more about this part in a future post, discussing the different possible algorithms, which one i choose and maybe the various heuristics to tune it.

For now, know that the analysis part will take the movie objects (the pairs), iterate over the hash of tweets. It will then take the results and put them in a second db, this time a SQL db from the start, and complete them with classic info for movies, like the poster, the date of release, etc ...
This will allow for the third part to enter.

## The FrontSite

This will be the part that the end user will use and interact with. I want this part to be static, because minimal interaction is needed for the user, after, she will only _consume_ data, not have any effect on it.

It is still a bit unclear at the moment i'm writing how i will achieve this part, since i'm not there yet.

## Conclusion

So this is the plan for the first version of the concept. I will most certainly write a second iteration once the project is mature and automatic enough. I think it will be interesting to compare the two versions.
