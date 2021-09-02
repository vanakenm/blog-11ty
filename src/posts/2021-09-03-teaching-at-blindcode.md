---
title: "Teaching React to blind students"
date: "2021-09-03"
tags: [coaching, accessibility]
decription: Why I did it and why you should too
permalink: posts/{{ title | slug }}.html
---

Due to a network effect (network matters - I'll blog about that another day), I was given the opportunity to give a small React Native course to a motivated group of blind students thanks to [Eqla](https://eqla.be/)'s [Blind Code](https://eqla.be/nouvelles-technologies/blindcode/) program. While I'm not new to coaching and teaching, this was clearly a first for me and probably my most personal experience with accessibility so far.

So I was both eager and a bit afraid about the experience - which ended up being one of my best teaching experience of those last years.

What I learned - in no specific order:

- Teaching code to blind students is much less different than teaching any group of juniors than you may think
- While I was not used to working with blind students... they were quite used to work with non blind teachers. The first thing they told me was "We're used to that - we're going to help you, no worries".
- Blind people use "see" in figurative ways all the time (ex: "do you see what I mean") - so you can too, it's not ableist or offensive by any means
- Screenreaders are not limited to text to speech feature - they also provide for example alternate navigation options (for example to go from link to link or tabs to tabs on a webpage)
- Using screensharing and remote access to help them debug their mistakes gave me a better view of the way they interact with the computer, roughly:
  - Screen readers allows them to get whatever in the screen read to them. Alternatives exists (Braille displays).
  - Fun fact, most of them have their screen reader at 1.5 or 2x speed - you get tired of listening to all links on a page
  - They either type (I'm not looking to my keyboard either, why should they need it?) with a echo system or dictate
  - Keyboard shortcuts are obviously critical
- I had to replace my usual way of "explaining things while I type them with my screen sharing open" - this means dictacting more code, alternating between the exact dictation and the explanations that goes with it. React is a bit of a mess in that regard due to the abuse of symbols (<>?:{}()[]...).
- Any interactive command line is a mess (for example `expo init myapp`) - but generally alternative exists to pass params directly (`expo init -t blank myapp` in this case) - once I got that I just looked always for those kind of commands.

On the "fun facts":

- Using a combination of shortcuts, screen readers and braille displays, I've seen several of them navigate code as fast as I can
- While we were working with https://opendata.bruxelles.be/ (a site with all open datasets from the city of Brussels where I live) one of the students exclaimed "This site is far too crowded - it's difficult to navigate". That's exactly what I thought too - so when it's bad it's bad for everyone - but worse for disabled people.
- I would be ready to bet some money that I could have some of them work (at junior positions) for companies and that people would need some time to realize they are blind (in this "remote new world" that we have nowadays).

I really think this experience will have me approach accessibility better in my future missions.

So thanks to Harielle from Eqla for trusting me with this and mostly to Sophie, Bruno, Matthieu, Simon, Isaac, Mounir, Yves and Ibrahim for their energy and the warm welcome they gave me.

