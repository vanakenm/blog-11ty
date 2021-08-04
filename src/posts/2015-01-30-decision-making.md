---
title:  "Decision Making"
date:   "2015-01-30"
tags: [process]
decription: Decisions matter in every team. What matters too is how fast we can take them.
permalink: posts/{{ title | slug }}.html
---

Decisions are an integral part of a development's team work. Whether it is about priorities, methodologies, tools to use, we always have to settle on something. This is even more true for startups, where all the business and financials decisions are added to the pure development ones.

## My decision process evaluation (only) rule

I've worked in many environment, from [PullReview](http://pullreview.com)'s two-man structure to very large companies. I've seen a lot of teams with a lot of different ways to reach decisions. I don't think there is a good one, but I do think there is some bad ones. Whatever way you pick, it should respect a single and simple rule:

<em>Your process should allow you to reach a decision in a specific amount of time.</em>

The "amount of time" being dependant on the decision to take - some things are of much more importance than others, but should be fixed in advance as much as possible:

- "So, we have two options for our Continuous Integration, let's take 30 minutes together to discuss the pros & cons and pick one"
- "We need to have our next release content fixed before Monday"

## Some process that succeed...

Some process that do follow that rule:

### Dictatorship

A <em>Dictatorship</em> happens when a specific person take the decision at the end of the allocated time. The reason can be hierarchical, but that's just one among a lot of others.

Altough the word is somewhat pejorative, I've no qualm with Dictatorship, especially if it is linked to some kind of skill. As an example, if we do have to take a decision regarding the servers with the team, I'll tend to let the sysadmin take the decision. I'll contribute to the discussion and expect to be listened to, but I'll bow to the person with the most knowledge. 

Another Dictatorship option is to let the person that is doing the discussed task (or that will do it) decide.

This means that the Dictator can be various persons, depending of the context. What matters is that the context (and so the Dictator) is clear to everyone.

### Democracy

A <em>Democracy</em> is when at the end of the allocated time, the stakeholders vote. The decision with the highest number of vote get implemented.

I did not see the Democracy implemented a lot, except in Scrum processes' retrospectives, but it is following my unique rule. The caveats are that the "diktat of the majority" may lead to strange situations. 

I remember discussing the way the knowledge was shared between developers inside the team. At the end, there was two opinions: use a "everyone pick the first story on the pile" approach versus a "each developer nominate and train a specific backup for his/her projects". The second option was the leader in the votes, even if no developer in the team actually voted for it - we were outvoted by non-coding team members on a subject specific to coding.

### Throwing a dice

Probably a far fetched example, but throwing a dice is a valid decision strategy regarding the unique rule. Probably a bad one, but probably better than the options below.

## ...and some that do not

### Consensus

A <em>Consensus</em> require all the stakeholders to agree for the decision to be taken. In practice, it means giving everry person a veto, so that no decision will be taken until everyone agree - which requires a non-predictive amount of time that increase very quickly with the number of persons involved.

### Delay/Delegate

A <em>Delay</em> happens when at the end of the allocated time, the decision is delayed to another date (often to another meeting actually). A <em>Delegate</em> happens when the decision power is transferred to another person at the end of the allocated time.

None of those can garantee a decision in a specific amount of time, so they should be avoided at all costs. Despite this, they are actually pretty common.

## We have rules for the cases that don't work

Something I heard a lot is: "you should first try to agree together before coming to this sort of process". Fact is, I do. You don't need rules for the cases that work. <em>You need them for the cases that don't</em>. If you agree from the start, then you don't need a process on that case, and that's good.

## Conclusion

As one our our advisors said to us at PullReview:

"<em>Your problem is that you still think there is good and bad decisions, while there is just the decisions you take and those you don't.</em>"

This means that your company/team has to take decisions. If you want those to be taken (and you should!), be sure to 

* allocate a specific amount of time to each (5 minutes is a perfectly reasonable time to take most decision)
* timebox the interventions if needed (ie, don't let someone talk for 15 minutes if you have 5 persons in the room and 30 minutes to decide)
* be transparent about the rule used to take the decision
* try to limit the number of people involved