---
title: "2021 Wrap Up - on the technical side"
date: "2022-01-10"
tags: [blog]
decription: Back to (technical) work
permalink: posts/{{ title | slug }}.html
---

## A year of technical work

I blogged last week about [my 2021 Wrap Up](/posts/2021-wrap-up.html) - this is also a good opportunity to look at what I've learn in this first year of "back to technical work".

A few months ago I started a small Excel file, putting the date and the technology each time I learned something new - which is quite often.

Thanks to that file (and some sketchy souvenirs), I was able to put some things together here. Like many people, I don't always think I'm learning that much - until I do this kind of exercises.

So, in no specific order, some things I learned this year - technical edition.

### Hooks first React

I'm not new to React, but I had to create a couple of new applications this year (plus teach some React at [BlindCode](https://www.joyouscoding.com/posts/teaching-react-to-blind-students.html)) so I did wrote a good amount of "modern react" - which means functional components and hooks. While none of my apps are that complicated, I was quite happy with the results:

- No class components at all. No "didComponentMount" or anything like that.
- State management with useState is a breeze...
- ... even more combined with useEffect for things like API calls

Result is smaller, cleaner and more readable code - something that make me love developing applications with React even more.

### React Native

My mobile development experience is quite limited - as a mostly web dev, technologies like cordova or react native that allows me to use my web knowledge are a godsend. I taught some React Native at [BlindCode](https://www.joyouscoding.com/posts/teaching-react-to-blind-students.html), so I had to learn it too.

Thanks to [React Native](https://facebook.github.io/react-native/) and [Expo](https://expo.io/) we were able to create a couple of simple apps, interacting with various Open Data APIs. Aside from reusing my skills in React, I appreciated quick development/test cycle, with Expo providing an easy deployment on mobile devices without having to deal with the App/Play store shenanigans.

I understand none of those technologies are as good as working directly with the native environment, but they are easy to start with and productive - something that's usually critical in the scarce, startup environments I tend to work in.

### Linked Data

This is more obscure, so I'll explain - Linked Datal is a W3C initiative to publish data in a way that make it easy for them to be connected with each other - even with other providers. In concrete words it means using URI as records identifiers and graph formats like RDF as data structure.

While I appreciate Linked Data goals, I still feel like this is reinventing the wheel on the technical side:

- New database engines
- New query language
- New API standards

Anyway, applying my own advice of "using what's there", I did dive into the Linked Data world, learning:

- SPARQL - a graph traversal query language to retrieve data from a Linked Data database like...
- Apache Jena - the leading open source Linked Data database. While the community there was incredibly welcoming (ask a question on the mailing list, get answers by people writing books on the topic), managing Jena and getting clear profiling information about query was quite a challenge.
- GraphDB - another Linked Data database, created by OntoText. Not open source at all, but there is a free version. I gave it a try one day after yet another bad fight with Jena, and ended up with much better performance - so I switched to it. In the meantime I've learn that most people actually use Virtuoso - yet another commerical but with some free version engine.

I'm still wondering if a "Linked Data on top of existing technologies" would not have been better (PostGres, SQL, REST or GraphQL, etc). The problem with "starting from scratch" is that you compete against incredibly mature and efficient solutions - and also that your community is very small in comparison. So you have very smart people working to solve problems that have been solved 20 years ago by much bigger teams.

Going Linked Data still look like a risky bet in that regard - people I've spoken to in the area are convinced it's going to best best big thing. I'm not sure - but heh, better this than blokchain.

### Mongo

- Mongo aggregations 
- Mongoose

### Linux admin



### Command line

- sed
- sort command on Linux
- find
- grep

### Kafka

Kafka consumers

### Much more Python

First year writing more Python than Ruby

### Solid

Some Solid API

### NLP

Basic NLP with Spacy

### Tools and Platforms

I followed the game rules as I restarted blogging and [picked up a new platform](https://www.joyouscoding.com/posts/picking-a-blog-engine-in-2021.html). So I learned a new static site generator, [Eleventy](https://11ty.dev/), and a new hosting/deployment platform, [Netlify](https://www.netlify.com/).

In both case, if you are familiar with that space (SSGs and PAASs respectively), switching is actually quite easy. I used Jekyll, Heroku and GitHub pages before, so the switch was not that hard.

While I've been working alone a lot this year, I still needed some basic CI/CD functionalities - and end up learning the minimum amount of GitHub actions. The tools generally works and if you are using GitHub anyway it means avoiding the "one more tool" issue.

On both personal (I want to keep things simple) and organisational (if I don't need to ask for more accesses/money, better), it's a significant edge.

Lastly, we did give part of the [SkillsUnion](https://www.skillsunion.com) courses using [Code Sandbox](https://codesandbox.io/) - pretty much a VS Code and basic terminal running in the browser. Main reason was that it means we could start teaching (some) code without the students having to:

1. Learn Git
2. Install a lot of things

on day 1.

It does the job - but if I have to design such a course again, I'll get the minimal setup & Git on day one, and use the opportunity for the students to learn about Git & managing their own environment - something quite critical to a developer's job anyway.

### Drupal

That one was challenging and interesting. I did some PHP code a good while ago, but I was not exactly prepared for Drupal. Lacking better words, Drupal is a whole ecosystem it itself - I can jump from Rails to Django or Laravel easily, because in the end they are using very similar concepts. Drupal is... _different_. Coming from a more "traidiotional" web development background, nothing made sense initally.

My goal was limited - create a small Drupal plugin to fetch data using an API and show them on the screen in a dedicated widget. The actual code part did not take me more than a couple of hours - but getting there was another matter entirely. 

I was lucky to have support - from a colleague in the Drupal world since years, and from the [Drupal slack](https://drupal.slack.com) that I heartily recommand.

Among others, somethings I had to wrap my head around:

- It's normal to checkout the whole Drupal project & make modifications where you need them (you can and should of course create your own modules, but the repo will still have every source line inside).
- Model wise, everything is a "Node" - a piece of content that has a type and can have quite different structures. 
- Documentation is plentyfull, but difference between versions can bite you severaly - be careful to check the version of anything you read

Thanks to the support, this ended up going relatively fast (still needed a couple of days just to figure it out) - but I know I barely scratched the surface. 

### Nginx

- Basic config. 

### Docker

Docker compose
docker container ps & friends
Some docker

## Afterthoughts

To be very clear- I did not become an expert in any of those. I'm still a practioneer - I learn to be able to achieve my (customer's) goal - not to get complete knowledge about a topic.

I either have deepened my knowledge in areas I knew already (like React or Python) or I have learned something new (like Solid, Kafka, Docker, Nginx, Drupal, Netlify, etc.). For the latter it means I learned enough to do my job - sometime with help - and that next time I stumble on those topics, I'll be a bit less frightened (and a bit more efficient too).

Learning is still something I find a lot of personal satisfaction in - so I hope 2022 will be as good as 2021 in that regard.