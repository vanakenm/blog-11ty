---
title: "Picking a blog engine in 2021"
date: "2021-08-09"
tags: [blog]
decription: It's all about choices and it's not that easy
permalink: posts/{{ title | slug }}.html
---

Getting back to a more varied freelance role made me want to blog again. As a good procrastinator, I decided I first needed to give my blog a lifting - toward something simpler both visually and for me to manage.

In my ideal imaginary world, I'd just put some words down and be down with it - with minimal overhead. My current Jekyll setting was working but a bit cumbersome so I started a review of "what to use as a blog in 2021 as a developer that does not want to tinker nor host". This proven be more complicated that I expected:

- [Medium](medium.com): A winner on the "zero-config", but Medium general model concerns me and I've seen them paywall free content. So, no.
- [Wordpress](wordpress.com): I did consider that one more than I'm willing to say - thinking of the "Wordpress.com" part (I don't want to host it either). I finally found something before going there, so that's good.
- [Ghost](https://ghost.org/): Looks way too elaborate for what I need - "Turn your audience into a business" looks a bit too ambitious for me.
- [Micro Blog](micro.blog): I really wanted to like that one. Looked perfect for me, so I went with it... before getting so many errors with weird messages when moving my content there that I had to just delete everything and look for something else.
- [Eleventy](https://www.11ty.dev/): This what worked for me in the end. Some detail below.

So to be complete, this is using Elventy with a theme/starter called [Eleventy Duo](https://github.com/yinkakun/eleventy-duo) created by [Yinkakun](https://github.com/yinkakun) (thanks!). The setup include an easy and free way to deploy on [Netlify](https://www.netlify.com/) and even a link to [Forestry](https://forestry.io/) - a web UI that can even commit to GitHub.

Thanks to Netlify's [redirect capabilities](https://docs.netlify.com/routing/redirects/#syntax-for-the-redirects-file) I was able to keep my old urls working.

In a nutshell this gives me what I need:

- A ui to edit/post if I want to use it
- A git repo back end so I can move again if needed
- Markdown document as content (I love markdown)
- A free deploy on Netlify
- A nice simple theme with most of the required bricks in place (RSS feed, links, pages & posts...)


I'm quite happy of the result for a couple of hours of work altogether. So now I 'just' have to get content here again I assume.