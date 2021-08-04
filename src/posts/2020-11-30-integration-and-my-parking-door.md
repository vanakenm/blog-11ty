---
title: "Integration and my parking door"
date: "2020-11-23"
tags: [integration]
decription: My parking door is an integrated system - with the associated problems
permalink: posts/{{ title | slug }}.html
---

I've been looking to explain a bit what **integration** means for developers - the kind of answer I've to give following exchanges like this:

- Those are separated systems
- Let's make an integration between them!

Last week gave me a nice example - my parking door.

## The Parking Door

I've recently moved to a new appartment in the middle of Brussels. Being a new building, it has a mandatory parking (public parking space is in short supply in Brussels) - but as the building are quite narrow, it was impossible to build a ramp.

Instead, we have a "car elevator" so that cars can enter the parking at street level, go down with the elevator and then park in the underground parking.

I actually don't own a car, but I'm using the parking for my e-bike, so I've been using it quite a lot.

Here is a little schema about how it works:

![Car Elevator](/images/car-elevator.png)

## The problem

So - this is a typical example of a clever solution to a set of constraints:

- We have to have a parking
- We don't have the space for the usual solution (the ramp)
- We need this to not cost an arm and a leg

Now car elevators (at minimum small ones like this) are rather unusual - so we're a bit into new territory.

The good news is that the two main pieces exists:

- Doors than can open and close with a remote control
- Elevators able to manage "heavy" weights

The bad news is that we now have a **system** made of two independent pieces.

## The specification

So there is a certain number of rules that the system need to respect:

- The street door can only open if the elevator is a street level (don't want the car to run into a hole)
- The parking door can only open if the elevator is at parking level
- The elevator can only move if both doors are closed
- No door can close if a car is below one
- The elevator can't move if something is too close to either door

## The problems

The first thing I learned when I arrived in the building was that "getting in and out the parking is not simple" - we also got a two pages guide about thow to manage that system.

Two weeks in, while the systems mostly seems to work, you see things getting weird once in a while:

- The street door almost got on the car of a visitor
- If one of the door does not close or open completely, the whole system become unresponsive - effecively blocking the elevator, possibly with the street door open.
- When this happen, a combination of actions + waiting time generally ends up in the door closing, and the system resuming normal behavior
- No one is clear on what that combination of actions is
- The street door did fall on the car of another tenant

Now again - the providers for both the doors & the elevator looks like decent companies knowing what they do. Individually, they probably work.

## What about integration

This simple example showcase a good set of elements to have in mind when talking about "integration":

- Having two independant, working systems does not means the integration part will work as well (or at all)
- Integration often "leaks" to the end user in the form of a set of disjointed interfaces resulting in a poor user experience
- Having two systems "talk with each other" is not a given - especially if those systems have not be created with that purpose
- The more complex the integration, the more source of bugs
- Even if the integration "works" (achieve expected result) it will most probably be awkward to the user (the two remote controls - or in software, having to log separately in two systems)
- Bugs are especially probably with complex interaction depending on the state of each sub-systems

## Conclusion

This does not means we should never use any integration, more that it comes at a cost - in budget or frustration for the end user.

In several recent cases, proposing a single system (even with significantly less features than what the combined system could provide) was actually in the end a better solution.

As someone said recently "Integration are more like organ transplant than lego blocks" - so use it with care.
