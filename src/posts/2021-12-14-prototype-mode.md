---
title: "Prototype mode"
date: "2021-12-13"
tags: [process]
decription: I'm all for good coding practices - until I'm not
permalink: posts/{{ title | slug }}.html
---

## Newscheck

Thanks to getting some days off between two missions, I've been able to take one card of my "project idea" board and actually implement it. The result is ["newscheck"](https://www.newscheck.info) - a web app that analyze the gender diversity of belgian headlines.

The usual problem of a "pet project" is quite similar to a startup first product - you need to ship something really fast, that still need to be "good enough" to at least attrack feedback. Actually, in my case, the "pet project" is a sort of "exageration" of the MVP project - I need to get it out "now" as there is a good chance the time window will close.

That first version is around 12 hours of work - for something that qualify as an MVP in my mind:

- It do something useful - well enough to be used
- It's usable - won't get any design award, but it won't drive people mad either

More importantly - it did attract some interest and feedback, which is probably an even better validation.

Now, I tend to think of myself as someone that cares about good code and good practices around it - I mean things such as unit tests, features branches, staging environments, etc...

Looking back at newscheck, I pretty much thrown everything away - I was just trying to get something out as fast as possible. In order to not call this "dirty work" or just "yolo", I'll call this "prototype mode".

## Prototype mode

This is a bit "what I do when coding alone with a very severe time constraint". Some things are part of my usual workflow/tool set, some are not. As usual, this is biased toward "web development".

- A good "heavy" web framework - I mean something like Django, Rails or Laravel more than Sinatra or Flask or Express - generally something that get you a lot of things out of the box and with a vast ecosystem (like: you don't want to spend 30 minutes on the user login part, having an admin interface helps too)
- Simple, "git push" based hosting (Heroku typically)
- Postgresql - could go easier with like sqlite, but Heroku manages PG as well and...
- Postgresql JSON fields. I'm quite sold on the relational vs NoSQL model, but having the option to put some semi-structured data without having to migrate or thing the model out from scratch is coo
- No unit test - manual test aka "is the feature working the way I want it"
- Some UI toolkit - ie something with components. I'm quite happy with my [Tailwind UI](tailwindui.com) purchase for this
- Trunk based development - good news is that is actually a [best practice](https://thinkinglabs.io/articles/2021/04/26/on-the-evilness-of-feature-branching.html) - even if I'm mostly using feature branches when working in a team (sometime even when working alone for the "easy compare")
- Working from the local machine on the production database - this helps iterating very quickly.

The general idea is to get a decent façade (features, UI) on what the end user can see - and anything that just works behind it.

## If you want to go fast, go alone

> "If you want to go gast, go alone, if you want to go far, go together"

One of the main goal is to make possible for this to be a "one person project". Most of the shortcuts are related to my own shortcomings - I'm mostly a backend developer, hence:

- Using something like Heroku to avoid the hassle (and time) of setting up a server and managing it.
- Using a UI toolkit to get something decent without having to call a designer.

Depending on your own strenghts, it could be the other way around - as a front end developer with good design skills for example, it may be good to look at things like firebase or other like that that can give you a functional backend/API with minimal coding.

## Downsides

While I love that (very short) phase of a project where could can release in hours, not days, a lot of practices are there for a good reason, and this is 1/dangerous 2/would fall apart quickly once you need to work with a team.

Dangerous mostly because any error will probably result in something broken on the user side - this happened several time with newscheck (like "I did not test what would happen in the dashboard if a source had no analysis yet). The idea behind the "prototype mode" is that you can break things - and also that you can fix them in minutes.

Would fall apart as once it's more than a single person working, you'll need either work separation (feature branches) or a way to know you did not break anything that does not rely on the end user (like, tests) - probably both.

Working directly on the production is a good way to a quick death as a startup - as mistakes __will__ happen (when, not if).
