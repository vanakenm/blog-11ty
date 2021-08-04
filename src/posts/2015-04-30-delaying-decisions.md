---
title:  "Delaying Decisions"
date:   "2015-04-29"
tags: [process]
decription: Why are we so keen to decide on a maximum of topics when we know the least about them.
permalink: posts/{{ title | slug }}.html
---

Second post inspired by my experience as a coach at [LeWagon Bootcamp](http://lewagon.org/program). For those that missed the first, it's just [there](http://vanakenm.github.io/blog/2015/04/14/10-percent-working.html).

## Projects

LeWagon Bootcamp [program](http://lewagon.org/program) ends up with the students working in groups on their own projects. This means larger, more complex problems to solve.

Once they had their user stories written, most of them starting asking themselves questions:

* How are we going to compute the user balance from him transactions?
* How can we import those XML data into the database?
* What javascript library should we use to show a sound player on our page?

## Good questions, Bad timing

Now, those are actually good questions - they were going to need those answers at some point during the project.

But there lies the catch: most of those questions were related to user stories they would cleary not start right away so even if they needed the answers, *they did not need them now*.

## Project knowledge

When you are working on a project, chances are good that your knowledge of what you need to achieve (technical, functional or whatever) will be *increasing* as the project advance:

![Project Knowledge]({{ site.url }}/blog/img/project-knowledge.png)
<sub class="pull-right">graph thanks to http://xkcdgraphs.com/</sub>

Another take on that graph is that the very start of the project is the time where you know it the worse.

In other words, *taking a maximum of decisions at the very beginning of the projects means taking them when you know almost nothing about it*... which does not look a very good idea.

## When to spike?

Now, this does not means I want to throw all design away - I just want them to be tackled when they are useful and not before. A specific and very valid case for tackling a point very early in the project is *if there is a doubt that it may be impossible to do*. In that situation, a spike should probably be started right away.

As a small example, a student of the promotion had a transaction workflow that involved scanning a QR code. Now, the application itself was web-based, so the question "can I use the phone QR code scanner inside my (web) application" did arise. I encouraged the student to quickly make tests to see what was possible, as this had a great impact on his main feature.

## Back to work

Whatever project you find yourself in, when a discussion starts on a subject, the good question is not "do we need to know this" but

*"Do we need to know this >now<"*

Applying this simple rule on a general basis would have avoided a lot of ultimately fruitless discussions in a significant part of my projects.

