---
title: "Seniority Reloaded"
date: "2023-10-09"
tags: [hiring]
description: It's about the tech except it's not
permalink: posts/{{ title | slug }}.html
---

I generally don't speak much about technology - probably because they are so many people doing that already, and probably better, but mostly because I think it's generally a bad prism.

As in: I'm active in technology but most of the issues and decisions are take are not technology driven - and I don't think they should.

We used to joke years ago with Gilbert West about our advice for people asking us "What language should I use" when starting a new business - the answer was pretty much "It does not matter".

I still believe in that (sort of), but I also think there is now (probably since a while) a "default" language - python.

## Why

Basically it does everything well enough to be a "Swiss Knife":

- Want to do a web application? Django is a very solid, mature, rich ecosystem, battery included framework. It can pretty much support whatever you want, from full stack to just backend (thanks to Django Rest Framework) if you really want to have a React or other front end with it.
- Need to script/do some automation? Python is installed (or installable) pretty much everywhere, is easy/convenient to use as a scripting language
- Need data transformation or data science ? Python is one of the two languages with real ecosystems there (the other being R), and the only one which is also a "general purpose" language.

Basically - you can build 98% of the startups/companies with that. It's also widely used, good documentation, lots of developers to hire.

## But you can use more than one language, right?

So, yes, but it come with a price - multiple ones actually:

- It makes your infrastructure more complex - even doing separate app for front & back does. Suddently you need to servers.
- Features are just longer: something that was some Python & a bit of HTML is suddenly some Python API, then a client to parse it and show it using React
- Your team need either to all know both languages or you need to split them in separated teams, with the associated costs and coordinations headaches.

## It's true of other languages

Honestly? No. The only one that come close to that is JavaScript. I don't think it's as productive on the backend (there is no direct equivalent to Django in JavaScript). It can work for mobile apps (using React Native), so that's a plus, but as a scripting or data language it's nowhere as good.

## It's not aboout the language

As usual - there is nothing here that is specific to the language itself or its technical capacity - it's a combination of ecosystem, history and market share. You could argue that those are a result of the language capabilities - but that's just not true.

So if you ask me about languages or what to use for your startup - let's just use Python.
