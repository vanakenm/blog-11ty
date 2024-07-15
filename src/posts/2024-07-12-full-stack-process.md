---
title: Why I hire Full Stack Developers and why you should too 
date: "2024-15-07"
tags: [hiring]
description: It's about business value
permalink: posts/{{ title | slug }}.html
---

# What?

I hear and read a lot about development teams efficiency - while I'm no specialist of  the [Theory Of Constraints](https://blog.logrocket.com/product-management/how-to-utilize-the-theory-of-constraints/), I've come to see most productivity issues as *organizational* in nature - much more often than *technical* (bad tools, languages, frameworks, etc).

To explain how this leads me to go against the industry tide and favor hiring full stack developers require a small trip back in time.

## In the beginning we were all full stacks

When I started my career ("I was there 3000 year ago") about 20 years ago now, we were all "full stack developers" - we just did not use the term, as there was no other kind of developer anyway. That was before the ubiquity of the web too so we already had client & server in the same language (Java for me at the time).

Then the web came, and we were doing HTML with small bits of dynamic code in the middle of the pages using some template or all purpose language sprinkled in the middle. The web was all about Requests & Responses - in other words you send an URL and got back a page - which was unchanging until you put another url (directly or via a link or a form button).

## JavaScript and Client-side logic

Then Netscape (the dominant browser at the time) enabled a small, quickly made language called "JavaScript" (because Java was popular at the time, so I looked like a good idea to name the new language "something like Java" - despite both language being pretty much unrelated). 

This allowed to have code run directly in the browser, which means on the user's own machine (the "client"), which means we did not had to wait for a page reload to update small parts of the page. This made possible a bunch of small interaction, user feedback, etc (especially as CSS was nowhere as powerful as it is now, so JavaScript was the only way). 

As JavaScript was not fully standardized across browsers (looking at you, Internet Explorer), some people stared JavaScript libraries to help manage this and a bunch of standard problems - jQuery (but also moo tools, Prototype, etc).

Then one more thing happened - the oddly named ["XMLHTTPRequest"](https://en.wikipedia.org/wiki/XMLHttpRequest) that allowed pages to call the server without reloading the page - which means you could (for example) show new messages as they arrived, even after the initial load of the page. This combined with the dynamic nature of JavaScript means we could run some "logic" on the front end and update the page accordingly - while or even before sending updates to the server.

But to this point it was still mostly "full stack developer work". 

## Rise of front end frameworks and specialization

What changed "everything" in terms of web development (team) organization was the emergence then prevalence of "front end frameworks" - things like Backbone, Angular or React (or Svelte, Vue, etc). Those technologies made a lot of the modern web app possible (Twitter, Facebook, etc). For smaller companies, it means making dynamic front end was made possible (by tools created by [FAANG](https://en.wikipedia.org/wiki/Big_Tech#FAANG) companies to solve problems *they* had - but that's another topic).

Suddenly it was no more about "sprinkling JavaScript" on a HTML front end served by a PHP/Java/C#/Python/Ruby/Whatever backend - the JavaScript front end was an app on its own, as complex (or more complex in some cases) than the backend. Learning and mastering those frameworks was no piece of cake either, so specialization started to happen - a split between "Backend Developers" (using one backend language and tacking business logic, DB relations, etc) and "Frontend Developers" (using a JavaScript framework and tackling fetching data from the server, showing it, managing interactions, etc).

Then we had to coin a work for those that were still doing everything - "Full Stack Developers" - in a world that was increasingly creating jobs for either front or backend (I've read somewhere that this was made "so that startups could justify doing a feature with 2 developers instead of one in a time of abundant capital").

# Solo efficiency vs Team efficiency

So, how is this linked to team organization and Theory of Constraints?

## Let's code a feature

In the "old/full stack" model, if you had a couple of features to implement, you put a developer on it to do it "end to end" - you of course have some kind of review cycle (technical, functional or both), but that was mostly it.

Now what you need is:

- Split the feature description between backend and frontend work (this may be trivial - or not, depending on the feature and level of preparation)
- Give the backend part to Sarah.
- Once Sarah is done, she can transfer it to her front end colleague Bob and go work on the next feature
- Bob do the front then move it to review/staging/QA

This works (sort of) but create a good bunch of new problems:

- What if Bob discover that something is missing (he needed this "network" field that Sarah did not include in the API) - he needs to go back to Sarah - but in the meantime, she's busy on the next backend feature, so she need to stop that, go back to the previous feature and make her update. Maybe it's not something missing, but that the way the API is organized is not practical from the front end, etc
- When QA arrive, if a problem is found that need to be solved on the backend, Sarah is probably days/weeks out of her work there - getting back there is going to be complicated
- When trouble happen the responsibility is split - it makes it complicated to solve a problem quickly 

You can work around those things, of course (Sarah & Bob can work together for a while at the start of the feature, a first analysis can be done so that the API is negotiated from the start, etc) - but the flow becomes inevitably more complex. This can be compensated somewhat by the fact that both Sarah & Bob are specialists in their own areas and hence more efficient - but my experience show again that the flow is the primary factor of efficiency.

## Team dynamics

Getting an higher view show that the situation is actually even worse than that - as we know need to acknowledge the frontend/backend divide not only in our work but also in our team organization. The previous team of 4 is now... 2 frontend and 2 backend? Or 3 and 1? Or 1 and 3? What if the proportion of backend versus frontend work is not stable in time (in my experience it is not - my current work at [Farm For Good](https://farmforgood.org) started full on Excel parsing, indicator computations etc... before moving toward a much more user focused set of functionalities)? 

This means I'm not only losing time in the feature flow - I'm also losing a lot of flexibility in my team organization. Developers (me included) tend to take pride & ownership in their work - but this make it very difficult as it's always split in two. Team ownership is a thing, but it's again much more complex.

The endgame of that specialization logic is the kind of "software factory" you see at Big Companies - where each team is boxed between two walls and a feature go across all of them (like "system", "business logic", "interface", ...) - making sure no one is at any chance of feeling responsible for anything - and devoid of any chance of any cogs in the machine to improve on the Plan.

# Advice

My ecosystem is generally small teams or companies - let's say one to ten developers. In those environments, **I heavily recommend to go for full stack developers**. Some kind of specialization is welcome (not everyone is at the same level in everything), but at least people **able** and **willing** to work on both parts. 

This means I can assign end-to-end features to developers - which do not prevent them to go to the "local expert" on a specific topic. Frontend heavy features can still be assigned accordingly, etc.

The "split model" just creates far too many constraints on the delivery to be productive, once you factor the whole team.

Not everyone will be at ease with that - and that's ok (it's totally ok decide to specialize as a developer - I've seen a lot of people recommending it) - it just means those profiles are a bad match for such a team. Being very open and clear about how the team works should be part of any job opening - it's already complicated enough if you don't hide crucial information.

Opinions? Let me know on LinkedIn!