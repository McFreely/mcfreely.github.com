---
layout: post
title: Making Zurb Foundation 5 to work with Ember-tools
category: draft
description: 
image: 
status:
tags:
- To be defined
---

## Introduction
I wanted to include the wonderful css framework [foundation](http://foundaiton.com) on a project i'm working on. Being an Ember project, I started using ember-tool for easier build management. One of the problem I ran into was to integrate correctly Foundation with ember-tool. I struggled for a few hour to make the TopBar element to work as intended.

Thnaks to a nice _discuss.ember_ post by Joe Fiorini responding to jtrinker, and a bit of fiddling, I was able to make it work. Here are the steps.

## Including the Foundation Library

When you set up a project with ember-tools everything needed is included already. 

{{ Image }}
In the file app.js, you can see that it load all dependencies when the application start. Which is nice if you only want Ember. The problems start when you want to add other vendor libraries. At least Foudation library. One of the dependency of Foundation is jQuery, which is also one of Ember. Requiring Foundation like the rest is causing an issue where jQuery is required twice and all hell break loose.

The solution is to require only ember-data in the config/app.js file (for the store declaration to work), and the rest is required as usual in the index.html file :

{{ image }}

The order is important. Once this is done, the Foudation.js loads correctly and you can continue on.

## Using views for the plugins

The idea is to use a component to load the plugin you want (in my case, this was the topbar) while the ember application is rendered. If you do it as per Foudation documentation, the js plugin never loads after ember. This is because Foundation apply the plugin on document ready, about at the same time Ember render the templates, and it stays in DOM limbo forever.
Component are nifty Ember Objects for reusable ui pieces. Perfect for what we want.
Rather than explain it once again, and much less elegantly, i will link to the Jsbin made by jtrinker:

{{ JsBin }}

Voila.



