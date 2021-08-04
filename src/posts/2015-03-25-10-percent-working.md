---
title:  "10% working is better than 80% not working"
date:   "2015-04-14"
tags: [code]
decription: Main goal for any program is first to run.
permalink: posts/{{ title | slug }}.html
---


For the last 9 weeks, I've been working with a session of [LeWagon Bootcamp](http://lewagon.org/program) students. I'm used to coach developers, but this was the first time in many years that I was coaching total beginners again, and that gave me new insights about the way we learn to program, and also on some typical problems people face when learning.

## They try to eat the whole problem in one bite

Like hungry little kids, when facing a programming problem, they try to figure out a full solution, in their head and/or in their code. And like little kids, the result is a lot of splashed food around, and not that much in the mouth.

This make little kids (and little programmers) angry, which means that the next bite become more and more complicated, until they give up in frustration.

## An example
One of the exercises from [LeWagon Bootcamp](http://lewagon.org/program) was to translate a text (several words/sentences) into "louchebem" - a slang used notably by parisian butchers a while ago. To "louchebemize" a word, you apply the following rules:

* Move the first syllable to the end if it starts with a consonant
* Add a "l" as first letter
* Add a "ji" suffix at the end
* One-letter words are kept "as is"
* Punctuation or other special characters (dots, quotes, commas, apostrophes...) needs to be kept "as is"

Our placeholder was something like:

{% highlight ruby %}
def louchebemize(text)
end
{% endhighlight %}

Our test harness required the ´louchebemize´ method to return the text in its new form.

As an example:

    louchebemize("Bonjour à tout le monde!")
    => "Ljourbonji à ltoutji lleji ldemonji!"

## What the students did

Starting on something that was a rather complex program (several rules/steps), most of the students attempted to implement the full transformation in one cut, resulting in a code with several errors.

The testing period was then quite painful, as multiple problems occured - from syntax to logic ones, making the debugging both complicated and frustrating.    

This was made even worse as the program itself was not running at all (due to invalid syntax).

## The problem

The main problem of this approach is that they were trying to figure the whole problem in their heads - and logically couldn't.

This leads to writing block and frustration - from a solution that they (rightfully) thought 80% right. Unfortunately, in programming, the devil is mostly in those 20%.

## A better way

Seeing this scenario happens again and again forced me to get back to the way I did create my own solution, and to see how to push them in the right direction (without simply helping on the debugging) -- *the interesting part in coaching is that the objective is not really to make the code run, but mostly to be sure that the next problem will be tackled better*.

I asked one student the logic he wanted to use, and he told me directly:

- I'll iterate on each word, then...
- Why don't you do that already? Just the loop.

### Looping

Quite logically, I was called again by the same student. His code looked like:

{% highlight ruby %}
def louchebemize(text)
  text.split(" ").each do |word|
    # ???
  end
end
{% endhighlight %}

- I've done it, but this is of course not working.
- Why don't you return the sentence already?
- It won't help - I did not do any transformation yet.
- Do it anyway.

A few minutes later:

{% highlight ruby %}
def louchebemize(text)
  louchebem_words = text.split(" ").map do |word|
    word
  end

  louchebem_words.join(" ")
end
{% endhighlight %}

*This was I call the 10%: the program is doing something, and most importantly, it is running* (outputting the text 'as is'). Should there be any mistakes in the loop, split or join logic, it would be easy to catch & fix - it is just 3 lines of code.

Funny part, the student initially was not really happy with this - it did not look to him that he had made any progress toward a solution. Yet.

- Looks good. Now you can start with the rules. For example, you could already add the suffix 'ji' to each word.
- Except the ones with only one letter?
- Disregard that for now - we'll add it after.

A few more minutes later:

{% highlight ruby %}
def louchebemize(text)
  louchebem_words = text.split(" ").map do |word|
    word + "ji"
  end

  louchebem_words.join(" ")
end
{% endhighlight %}

Again, this code is clearly not getting the right result, but:

1. It runs
2. It is one step further towards the solution

Several errors where actually found & fixed directly at that time by several students (like using an 'each' instead of a 'map').

We had to repeat this several times (for the one-letter word case, for adding the 'l', for moving the first syllable to the end), but once they were at this point, most of the students had learned something.

## Learnings

Altought this is nothing new for seasoned programmers, having to look back at the learning process was actually helpful for me too - I've made the same mistakes my students did several times during my career, and this may help me to do it less in the future.

Facing any but the most trivial problem, it's actually realizing that:

*It’s ok to write something that:*

- *does not solve the complete problem (just applying one of the required operations)*
- *does not take all cases in consideration (for example only working on the happy case)*

In other words: it is much better to have a solution that is returning something that you know is incomplete/false in a specific way that to have something that you think correct but will require a lot of debugging.
