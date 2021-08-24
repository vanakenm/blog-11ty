---
title: "My problem with NoSQL"
date: "2021-08-25"
tags: [SQL, Database, rant]
decription: It's all fun until you actually want to use the data
permalink: posts/{{ title | slug }}.html
---

I've had to work with several "NoSQL" databases those last months (I'm here speaking of using let's say Mongo or Apache Jena as the main storage of your application, not things such as having a cache in Redis) - and I don't get it.

My main problem is that, well, data *has a structure* and not having to worry about it is super fun - until you want to do something meaningful with it. Students have names and first names, Orders have a OrderItems that have quantity and prices, etc - and generally if they don't, Bad Things happen. I'd ever go as far as "not only is most 'real world' data structured, it also tend to be relational".

So if the structure is not managed by the database, it will need to be managed somewhere else - either in the application (possibly via an ODM like Mongoose or Djongo, probably via specific validations) or worse even in the UI. I don't know many applications where the end users wants to deal with unstructured data on their side. We tend to name stuff we show on the screen and organise it a bit so that it make sense for the person using the application.

My feeling is a sort of eternal cycle of:

- This is wonderful we can make our database evolve so fast, everything is getting in!
- Cool we can accept users even without emails - schemaless FTW, no migration needed!
- Doh looks like our last mailing did not go well as half of our users had no email at all
- Let's add some validation for this not to happen again
- Also would be good to check that each user is properly linked to an account via this "account_id" field we added
- ...

In other words: what feels (for a very limited amount of time) as a blessing become a curse really fast, ending up into some kind of partial, erronous, inefficient custom reiplementation of a relational model.

I'm going back to PostgreSQL.