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

## Roles, Responsibilities, and Collaborations

An application is a system of responsibilities that are assigned to roles. Roles collaborate with eachother in order to 
carry out its responsibilities. A good application is structured to effectively fulfill these responsibilities.

We invent objects, assigning responsibilities to them for doing/holding things, and they work together to fulfill the 
application's larger responsibilities.

One object may need help from another object. Objects work together in concert in order to fulfill the application's
responsibilities. We also must design these collaborations. 
**Design is an iterative and incremental process of envisioning objects and their responsibilities and inventing flexible collaborations within small neighborhoods**

**The services that an object holds and the info that an object provides define how it behaves alongside other objects**.
**An object embodies a set of roles with a designated set of responsibilities**

Objects collaborate by sending requests and receiving replies.

An object can be more intelligent if it does something with what it knows. The more it knows, the less its client needs to
know in order to use it.
Blending stereotypes makes things easier to use. That way, clients can focus on their problem and not on the details.

Collaborating objects must establish contracts with one another. The protocol to communicate, only use certain services,
provide the appropriate info, use under certain conditions, handle the concequences, etc.

The fewer demands an object makes, the easier it is to use them. If an object constantly needs the help of other objects, 
it is hard to use. The more demands it can fulfill, the more useful it is. Though we must balance requirements and the 
demands those requirements place on the object's neighbors.