# Chapter 1: Design Concepts

Software can be either:
- Like a biosystem where each cell communicates with other cells without knowing what they're made of or how they work internally
- Like a mechanical clock, where moving one gear turns another in this monolithic piece of machinery

## Object Machinery

Complex systems are made of parts, and objects send messages that either request information or request an action be done.

Each object has its own responsibilities that it must fulfill in order for it to fulfill the needs of the application as a whole.
Examples:
- To fulfill a request, it holds a scripted response given some input
- Sometimes the responsibility of an object includes remembering certain facts so that it can use them to respond differently in the future.

We translate real world problems into objects that play a specific role in how things get done.
To manage the complexity of the real world we divvy behaviors into objects that play well-defined roles.

Success is measured by how clearly we invent a software reality that fits the real-world application, instead of how closely it resembels the actual real world.

Defined perspectives:
- The Application: A set of interacting Objects
- An Object: An implementation of one or more Roles
- A Role: A set of related responsibilities
- A Responsibility: An obligation to perform a task or know information
- A Collaboration: An interaction of Objects and/or Roles
- A Contract: An agreement outlining the terms of a Collaboration

## Roles

A role is a set of responsibilities that can be used interchangeably.

Objects that play the same role can be interchanged. 

DHL, FedEx, UPS all fulfill the same purpose of deliverying letters and packages. You choose from them according to the 
requirements of your package: If you need one-day shipping, the rate, if its valuable, flammable, etc etc.

What is the difference between an Object and a Role?
When a Role is always played by the same kind of object, the two are equivalent.
**But if more than one kind of Object can fulfill the same responsibilities in a particular context, a Role becomes a set of responsibilities that can be fulfilled in different ways.**

A role is a slot in the software machinery to be filled with an appropriate object as the program runs.


## Object Role Stereotypes

It is useful to oversimplify Objects and the Roles they play without their specifics so that we can reason about systems more easily.

We find these stereotypes to be useful:
- Information Holder: Knows and provides information
- Structurer: Maintains relationships between Objects and information about those relationships
- Service Provider: Performs work and, in general, offers computing services
- Coordinator: Reacts to events by delegating tasks to others
- Controller: Makes decisions and closely directs other's actions
- Interfacer: Transforms information and requests between distinct parts of our system

Once we assign and characterize an Object's role, its responsibilities will follow. An Object can also fit into more than one stereotype.

But if it fits more than one stereotype, is it playing more than one Role? 
Service Providers typically also hold information that it needs to provide its service. 
But it fits one Role because the responsibilities are all wrapped up together for the same "customers" to use.
But if it's serving two different types of clients, it is likely to be playing two roles.

Some objects are hard to stereotype because they fit into more than one category. How do you choose?
**You must decide what you want to emphasize.**

A Service Provider can look like an Interfacer depending on what context you're looking at it from. 
It okay to emphasize more than one aspect. There are blends of stereotypes, just as there are blends of emphasis.