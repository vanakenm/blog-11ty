---
title: Picking a mobile tech 
date: "2025-12-09"
tags: [tech, process]
description: Choosing between Flutter & React native in a small TBD team
permalink: posts/{{ title | slug }}.html
---

## Why

At a client, we're doing a web application that include a small use case for data reporting in the field (form + images). We've been working with a mobile first web app, but as time goes the connection issues (absence, low bandwidth, etc) had made clear we needed a "offline first" solution - in other words a mobile application.



## Context

Some important things here as there is not such thing as a "best tech choice" in generic terms - everything is about "what's the best tech *for us*". In other words - I'll explain our process and ultimate choice, but a lot of it is about who we are.

- We're a small (2.2 FTE) dev team with a high level of seniority (20y+) 
- Our expertise is mostly in web technologies, notably React that we use already in the same project, with styling using Tailwind
- We are operating in a trunk based development mode, deploying several times a day to production
- Our process is "Agile like" as in we are in close collaboration with our Product Owner & other stakeholder, with very fast validation cycle (our general appoach regarding any feature is "let's make the most simple option, release it and collect feedback before doing more")

With such a small team & a relatively clear goal, our first decision was to timebox the analysis time - once it was clear we had to pickup a tech we were on a Wednesday. Goal was to be decided for the next Monday last limit (we had several actions that required that decision, so we did not want to wait). All in all I thing we used between 4 and 8h of total person-time on this.

### Non functional requirements

Based on this we listed some things we wanted:

- Good/great Developer Experience ("DX"): we want our users to have a good experience, but we also need something where the dev team has a good one - this comes with things such as productive, easy to test, etc
- Easy to deploy (even if in test mode) all the way to a user phone
- Easy to update (possibly several time a day)

## Questions

I've tried to split the process into several steps showing our decision making

### Doing it ourselves vs outsourcing it

That's an important one - facing a technology that's new to the team and used (at least initially) for a specific use case, the first logical question is "are we doing that ourselves". For the expected "yeah but if we outsource we need to pay those people". Sure. But we're costing money too, and we could use the freed time to work on other features.

While we value expertise (see below) our way of working is pretty much incompatible with the usual "agency model" where we would have to give a very clear specification, get it done and then stop. We could in theory bring a single freelancer in for this, but this model would not work well with maintenance and we need to be able to update the application ourselves.

We went **against outsourcing because we wanted autonomy**.

Now we added a fine print to this one by recommending to The Powers That Pays that we go **for some hours of coaching by a freelancer senior in the exact technologies chosen**. Our frame was not "someone with X years of experience" but "someone that released & maintained at least 3-5 applications in that technology". We care about production stories ("Tales from the trenches"), not just years of work. 

### Native vs Cross Platform

That one was easy. We don't have the cost to go for two different mobile application, and the benefits (exact match to each platform, etc) are of very low value versus the cost for at least the next 2 years (which is a very long time for us).

So **we go cross platform**.

### Technologies to evaluate

A fast one - regarding cross platform mobile tech, we have only two real options: **flutter and React Native**. While some other exists (Kotlin Multi Platform, Xamarin, .NET Maui, Cordova), they are all either to old, too new or too niche to be considered.

We apply our baseline here regarding technologies which is we want something mature and widely used.

What made the rest of the process a bit more complex was that those two where obvious good choices (as in: we're confident we could deliver with both) - but we still had to pick and I was not ready for a dice roll yet.

### Process

Our first action was to decide what could help us to decide.

We listed:

- Making sure we have our requirements as clear as possible
- Writing down the context

Then on the actions:

- Asking specialists from our network (people with actual production experience)
- Reading articles about each tech (focus on stories of teams implementing one)
- Feed our context to a couple of AI to get some insights

Our goal through all this was not to answer "which one is good" (they both are) nor "which one if the best" (it all depends) but "which one is the most adequate for us".

### The specialists feedbacks

We reached in our networks for people with that "real world experience". My generally approach is to "shoot out" (in social networks or even on LinkedIn) for people that have experience and are ready to take a 30-60 minute call. I always offer to pay as those insights are very valuable and I feel that they should be compensated. For what it's worth, most people refuse to be paid for this kind of call, even when I tell them it won't lead to any contracting. In this case I was pretty clear that we intended to do the development ourselves.

Our main issue here is that almost no one has real world experience *in both Flutter and React Native*. Most experts were very happy with their own choices, but that did not lead to any help in terms of "picking" one.

### Some good articles

Timing was on our side as Vercel published an article about their experience building their first mobile app [using React Native](https://vercel.com/blog/how-we-built-the-v0-ios-app). One sided (as they did not expand on the reasons of their choices) but pretty useful anyway for a lot of "little things" to make the app better.

### The AI insights

We fed Claude with our context and options, and got quite a good report back:

### React Native

**Pros**

- Minimal learning curve - Your team already knows React; RN uses similar patterns (JSX, hooks, components)
- JavaScript everywhere - Leverage existing web knowledge and potentially share code
- Expo advantages:
    - Excellent DX with instant updates via Expo G
    - OTA (Over-The-Air) updates - update multiple times daily without app store approval
    - Easy testing/deployment - share via QR code instantly
- Built-in offline/sync capabilities with libraries like WatermelonDB, AsyncStorage
- Mature ecosystem - More libraries, solutions for forms (react-hook-form), image handling, offline sync
- Styling familiarity - NativeWind (Tailwind for RN) available if desired
- Largest community - More Stack Overflow answers, tutorials, third-party packages  React Native

**Cons**  

- "Write once, debug everywhere" - Platform-specific quirks can emerge
- Native module dependencies - Some libraries require ejecting from Expo
- Performance ceiling - Bridge architecture can be limiting (though improving with New Architecture)
- Not truly "like React" - No DOM, different components (<View> vs <div>), layout differences  ---

### Flutter

Pros  

- Consistent UI - Same rendering engine across platforms, fewer platform quirks
- Better performance - Direct compilation to native code, no bridge
- Hot reload - Excellent DX during development
- Web deployment
    - Can deploy as PWA from same codebase (though quality varies)
- Growing momentum - Strong backing from Google, improving ecosystem  Flutter -

Cons  

- Steeper learning curve - Dart is a new language; different paradigm (widgets vs components)
- Team reskilling required - None of your devs know Flutter/Dart
- Smaller ecosystem - Fewer packages for offline sync, forms compared to JS ecosystem
- Update friction - Traditional app store deployment (no equivalent to Expo's OTA updates by default)
- No existing code reuse - Can't leverage React knowledge or any existing JS/TS code
- Web deployment caveat - Flutter web still has limitations (SEO, size, performance)

### Developer summary

With this list in hand we had a first review, **leaning toward React Native**:

- OTA updates are a "killing" feature for us. Due to our deployment mode, being able to push updates without waiting for the App/Play Store validation is critical
- Flutter's pro about performance and consistent UI are mostly irrelevant to us.

This being said, several "downside" of Flutter were also irrelevant to us (we don't mind learning a new languages, and code reuse is not high on our current list).

### Plot twist: the AI fight back

As a joke, one of our colleague decided to feed the context and the Claude answer to another AI, asking it to play the "Devils Advocate" feedback.

It did find several good pieces:

- [Shorebird](https://shorebird.dev/) allow sort of OTA update in a Flutter app
- It mentioned several other edges such as having a "battery included" form system

even so, it pointed that going for Flutter was probably a good idea if we wanted Native look or were manipulating a lot of medias - problems that we don't have nor expect.

So we kept our initial choice.

## Summary

We're going for React Native, probably with some packages we already use (react hook form and NativeWind for Tailwind like styling) - with an external coach/expert to help us make some of the remaining choices, including our offline architecture.

I guess I'll be able to write a conclusion in a few months - even if as usual, we'll never know what would have happened with the other choice.


