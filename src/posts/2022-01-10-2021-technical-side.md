---
title: "2021 Wrap Up - on the technical side"
date: "2022-01-09"
tags: [blog]
description: Back to (technical) work
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

### Solid

Sort of similar but different - our [Osoc]() application was Solid based (by request) - pretty much a proof of concept of what an image library application could be in a Solid world.

For those that never touched it, [Solid](https://solidproject.org/) is a specification about data interchange with one key aspect - the data stays under the control of the person (versus Google or Facebook). Fathered by none other than Tim Berners-Lee, Solid makes a lot of sense technically and ethically.

Creating the app was mostly straighforward - in a way it's defining a Solid-compliant data model then create a client app using the existing Solid APIs.

My doubts here are more on the market side - none of the big players have any interest of using or even tolerating this approach - I don't see them going there without being forced to, which looks unlikely.

### Mongo

Among others I was handed a Mongo backed web application - I also wrote some Mongo courses, so I finally (?) worked a bit with one of the most popular NoSQL database. I don't know if this comes from the bias of having 20+ years of familiarity with SQL, but I found that writing Mongo queries had quite a steep learning curve.

Basics things are, well, basic, but more advanced cases get complex fast when dealing with non trivial aggregations. As with SPARQL, the tooling is also not as good as in SQL (ie: EXPLAIN & others).

I know Mongo can be quite fast - but I'm still unconvinced by the "benefits" of [schemaless](https://www.joyouscoding.com/posts/my-problem-with-nosql.html). I used Mongoose (a JavaScript/Mongo ODM) for some lessons and while it is quite nice in itself, it's a good example of "if the schema is not in the database it will need to be somewhere else" - and I'm quitte happy to have it in the database generally.

### Linux admin and the command line

Due to taking over some admin work at [IOS Press](https://www.iospress.com/), I had to improve a bit my Linux administration skills. I used `sed` to replace some lines in a very large CSV, `find` and `grep` in combination to retreive all files containing specific text, `find` again to identify files with bad permissions, etc.

I also discovered so. many. ways of having background processes running on a given Ubunut machine:

- Cron to launch jobs on schedule
- Incron to watch changes in files and launch jobs when they happen
- Tmux to keep jobs running in the background

I also learned that `pstree` can be a life saver when trying to identify the root process of a complex tree of subsystems.

### Kafka

I've heard of Kafka several time, but always tought that:

- It was insanely complicated
- It was only for a few people doing super complex stuff

It ends up that both those ideas were false - while I would clearly not use Kafka without needs, used "by the book" it's not that complicated, and can solve a quite common problem: garanteeing good reception and processing of a message.

In the [Shayp](https://www.shayp.com/) case it was about various IOT devices events, but it could be API calls or anything. 

Combined with vendor hosting (Azure in this case), it means that even if your application is down (something that will happen), the event will still be in Kafka's queue, ready to be processed once your application will be back online - garanteeing "no data loss", something not that easy for a small startup.

### (Much) more Python

This is probably the first year I wrote more Python than Ruby (on the server, as if I take everything into account, it's probably JavaScript that tops it all). 10 years ago I created a startup. We needed to pick a language and framework for the usual "web page facing database" kind of application.

We flipped a coin between Ruby on Rails and Python/Django (two solid options - at the time and now). I wonder how my career will have evolved should the coin had fallen on the Python side.

10 years later, I would probably have just picked Python. I did not change opinion about the language (I still love Ruby) - but Python popularity and the rise of data analytics made it a much more obvious choice today. I miss a bit of the _fluency_ of Ruby, and some of the magic of Rails, but generally speaking I learned to like Python a lot, and I assume I'll use it more and more.

This year I used Python for web development (Django), web development (Flask), scrapping web pages (Beautiful Soup), process automation, data analysis (pandas and friends), and even a bit of machine learning (scikit-learn) and NLP (SpaCy, see below) - a testament to the language & ecosystem versatility.

### NLP

The whole premise of [newscheck](https://www.newscheck.info) was based on extracting article titles from websites and then identifying people names on them to finally make statistics on their gender. I had every piece but the "identifying people" working in my head before even starting:

- Create a small web app using Django
- Use a Django command to run the analysis
- Trigger the command every day using the Heroku scheduler
- Save results in a database

So my first prototype was just running a NER (named entity recognition) on the titles to see if I could get a good result. I don't know much about NLP, NER or related concepts - so I did some googling to find what people were using nowaday, and looks like it's [SpaCy](https://spacy.io/).

Once the model (different per language!) is loaded, SpaCy can be run in a couple of lines of code. I know the analysis could be much better, but it does the job for now and allowed me to go live.

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

So is the time for a confession - I generally despise/fear server admin stuff. When coding, if I make a mistake I can just fix it. Even if it's commited already, I can find the exact place back and do a PR. I also normally have a staging environment (and my local one). In other words - I've a lot of mecanisms in place to help me fix the inevitable mistakes.

I generally find system adminstration much less forgiving - a small error in a nginx or iptable config file can pretty much shut down your production, and not every action can be reversed. I think this is due to both the nature of the work and my lack of experience with it (at least compared to web development).

So my main coping strategy has been to find a way not to do that part of the job - either because there is a team/colleague in charge of it or (better) because we delegate that responsibility to a provider (I _love_ heroku for that reason - I code my app, they manage the production).

As [IOS Press](https://iospress.com) one man development team, there is only me, and we can't use something like Heroku for various reasons, so I had to dig a bit more into system administration.

In order to get more reproductible configurations, I'm moving most things to [Docker](https://docs.docker.com/get-docker/) and Docker Compose (see below) - but I still needed some basic configuration. Having no real experience in either Nginx or Apache, I asked a more knowledgeable colleague what to pick and got as message "Nginx is slightly simpler to configure" - so I went for it.

All said and done - it's not that frightening, as long as I can test on something else than production. I did not need too much:

- Serving a single folder of static file
- Acting as a proxy to a Flask app for some more dynamic content
- SSL certification via Let's Encrypt and Certbot

Aside from losing two hours on a missing trailing slash for the Flask proxypass, this was relatively straightforward, with the whole config being less than 30 lines long.

I still prefer to rely on Heroku or a more knowledgeable colleague for this kind of tasks - but I'll clearly be less frightened the next time I've to do it.

### Docker

Following the previous topic - I wanted to have reproductible configurations, and looks like docker is the way to go - it also meant I could test a lot of things locally and expect them to run mostly the same on the remote system.

I did not get into fancy stuff like Kubernetes (I deploy to a single server anyway) - just defined a Dockerfile per service, combined in a Docker Compose file for the whole stack. The general idea is that if an image exist, you can just use it (in this case you don't have a Dockerfile at all - just a reference to the image in the Docker Compose file), if it does not you can build it but you can also easily extend a given image - using it as a starting point for your own.

It is even possible to configure Nginx that way - using the base image and just putting your own configuration in.

It's not deployed yet - but feels promising.

## Afterthoughts

To be very clear- I did not become an expert in any of those. I'm still a practioneer - I learn to be able to achieve my (customer's) goal - not to get complete knowledge about a topic.

I either have deepened my knowledge in areas I knew already (like React or Python) or I have learned something new (like Solid, Kafka, Docker, Nginx, Drupal, Netlify, etc.). For the latter it means I learned enough to do my job - sometime with help - and that next time I stumble on those topics, I'll be a bit less frightened (and a bit more efficient too).

Learning is still something I find a lot of personal satisfaction in - so I hope 2022 will be as good as 2021 in that regard.