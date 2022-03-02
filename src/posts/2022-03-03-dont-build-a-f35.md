---
title: "Don't build a F35"
date: "2022-03-03"
tags: [tech]
decription: Solutions for everyone tend to satisfy no one
permalink: posts/{{ title | slug }}.html
---

## The setup

Someone inside BigCorp (which can be a private company but also a public one or a part of an institution, governement, etc - what matters is that it's big) Bob, a manager stumble into a massive efficiency: team blue is considering building a task tracker (or an accounting software, or a security one, or whatever productivity tool is needed there - let's call this $SOFTWARE) - while team red already has one / is already building one.

Listening only to his courage and righteous fury facing this obvious misuse of company resources - building the same thing twice inside the same company ! - Bob quickly gets into team blue meeting:

- You don't need to build this - team red has one already, you can use theirs !
- But our need are not the same - we're not sure what they are building is good for us ?
- No worries - my cursory look tells me you need the same thing - and I'll discuss with team red to make sure to take into account your needs

Being thorough, Bob also barges into team red meeting room:

- Good news! $SOFTWARE will also be used by team blue!
- But $SOFTWARE is just currently being built - and we have a long list of features that we need already
- It's ok - their needs are almost the same

His job done, Bob retire to his meditation room - and thus a F35 is born.

## The F35

I'm no expert in weapons - but the story of the F35 as I understand it is mostly as follow. The US Military is made of several branches - Air Force, Army, Navy being the three biggest. Someone realized one day that if Air Force had planes (which make sense), the Navy also had planes - and so had the Army. Worse - all branches had different planes and were ordering them separately.

Thus came the logical idea - let's build a plane that is going to be able to fit the needs of everyone - so the whole US Military could use the same.

What happened is a a very, very long process - as a plane able to fulfill all branches specification was something very complex (and let's face it, combat planes are not simple things already) - that means also very costly, that finally gave birth to a plane that was:

- Less good in dogfights than the FA/18 (The Air Force current fighter)
- Less good to kill thanks than the A10 (The Army tank killer fighter)
- Not really good at landing on a boat (something the Navy cares about)

Ie - while being widely more expensive, it was actually worse than every plane it wanted to replace.

This in turn led to the miliarty produce "versions" of the F35 - specialized for a role or another one - again on a very inflated budget.

In other words - the plane for everyone ended up being a costly thing no one really wanted (they got it anyway, and us too in Europe, but still).

## The F35 Fallacy

There are several fallacies at play here:

- Duplication are inherently evil
- Grouping effort will lead to a better/more efficient software

This misjudge a lot of context - especially in big companies. 

### If it looks the same it is the same

Most task tracking software looks the same from afar - until you get into the details. Maybe team red uses very specific tasks but with no order (they operate in an area with strong autonomy) - while team blue needs to respect very specific processes. Maybe team red love transparency and boards where everything can be seen by everyone while team blue is actually in HR and require strict permissions.

### Adding some simple features won't hurt

So we have different needs - it's ok, we can add those to the software - the core is the same, it should not impact it much. Except most software tend to be late already (and overbudget, but let's focus on what impact our users). Adding "one more thing" especially when not taken into account from the start may actually delay it significaantly - to the furor of team red users that were promised it and are now facing delays for reasons completly unrelated to their needs.

Delays will come from the development time - but also from additionnal test needed, maybe integrations, etc.

### The software will be better for everyone in the end

Finally the software will be "done" (as much as a software ever is, but let put that part aside too). At least it will be better for everyone. Except it most probably won't - cramming the features means some will be "in the face" of users that don't need them. Or (as the F35) it will be generic and hence require a huge level of customization by each team to adjust the way it work to the way they work.

Use cases that were suppsoed to be "simple" will turn into multi screen wizard or dashboard with dozens of levels and gears to manage to get a result.

### And they were happy ever after

Assuming the software somehow manages to get out - then there is the rest of its life - with probably competing use cases or priorities at every corner.

### Results

The result of this "cost efficient" approach is probably going to be a massive spend, large delays and worse of all - furious users.

## Some lessons

The general lessons here are:

- Things that looks the same are not always the same - so in doubt, look closer. The devil tends to be in the details
- Disturbing one audience for the sake of another will probably not end well - make sure everyone is indeed better with the deal, and evaluate planning impacts
- Small, targeted software have a far better chance to be useful (and hence - used) to their intended audience than large generic ones.
- (apparent) Duplication may not be the end of the world. If the cases are indeed close enough, maybe some integration can progressively be built to ensure interop - until maybe the use case can be merged down the line ?

Next time you feel that people are duplicating work - make sure it is the case and that the duplication is actually hurting - you'll realize that autonomy may be a bigger benefit than normalisation or cost cutting.