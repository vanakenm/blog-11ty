---
title: Honey I shrunk the front end 
date: "2025-04-09"
tags: [tech]
description: Honey I shrunk the front end
permalink: posts/{{ title | slug }}.html
---

I ranted recently on the [benefits of Full Stack Developers](https://www.joyouscoding.com/posts/why-i-hire-full-stack-developers-and-why-you-should-too) and the simplification of the process that comes with it.

Those last years I have a technical stack that has become my "reasonable default" - Postgres, Django, React.

There are a lot of reasons those tech are popular - they work well, are well maintained, and are a good fit for a good number of projects (generally speaking I don't think your project has any specific technical requirements - in other words, most tech stacks will fit most business needs). 

While generally happy, I've been more and more concerned about advising that stack - or to be precise a specific part of it.

## SPAs

Most front end development nowadays is happening in "SPAs" (Single Page Applications) - something coded in React, Angular, Svelte or Vue. Basically we cut the application in two parts:

- A backend interacting with the database and doing (most of) the business logic, coded in whatever backend language you have (Python, PHP, Java, .NET, ...). This backend expose data and operations as an API (a set of url that are sending back json)
- A front end with the screens and interaction, that calls the backend, coded in JavaScript.

This separation has always existed logically - but now we're doing two complete separate applications, with widely different technologies & frameworks.

There are of course benefits - it has become massively easier to create "interactions heavy" applications, and we saw extremely nice components library emerge (things like Shad, MaterialUI, etc). But there are downsides too.

> SPA exist so that Startup could justify having two developers work on a feature instead of one
(found on internet)

I'm not saying it's /that/ bad but that sentence hit a bit too close to home

## The way before

Before the rise of those JavaScript framework, the way we did (web) interface was for the backend server to serve "HTML templates" - ie HTML files with some kind of specific tag able to insert dynamic contents - from JSP to Jinja to others. Any click on the page would generate a "full page reload", and dynamic elements needed to be done using some basic javascript (using things such as JQuery at the time). This worked quite well - and still does for a lot of standard applications.

## The good and the bad

I was working on a sort of ecommerce at the time - and I started to worry. Working on both sides of the app was fun - but it took time, too. One day I did an experiment and coded a couple of the pages using standard Django templates.

Result was:

- A lot less code (single routing, no need to develop a full API then digest it, ...)
- Lighter/faster pages (no need for 3MB of JavaScript upfront)
- Simpler infrastructure (a back end server and a database)
- SEO working "out of the box"
- Smaller set of tech - which means easier to hire

What I missed ? The app was doing full page reloads - but the pages are fast (and by the way, so does Amazon). Some more interactivity would be nice, but that's easy to add with "progressive enhancement" (JavaScript that adds some behaviour) - for example to have a search working on the products shown on the page (AlpineJS is great for this).

My biggest loss here are the components libraries - but even there I found options such as [TailGrids](https://tailgrids.com/) which offers components in HTML using Tailwind.

Note that this is in addition of not having to work with two developers each time as my comparison point is always a Full Stack Developer (me) - if this moves allow you to move from two dev on a feature to one, the benefits are much larger (in terms of flow).

## Conclusion

As usual in tech, we find ourselves using technologies developer by and for extremely large players (Google, Facebook, etc). This attract a lot of interest, talks, packages, etc - but none of this make them by default good for the 99% (looking at you, Kubernetes). Solution that were standard yesterday feels going against the wind nowadays.

I would not throw React(/Angular/...) away - some applications benefit a lot from it. But I think going "two apps for one" by default is a mistake I won't make again. If you are facing that question, ask yourself what are the actual benefits - as the costs are quite high.

