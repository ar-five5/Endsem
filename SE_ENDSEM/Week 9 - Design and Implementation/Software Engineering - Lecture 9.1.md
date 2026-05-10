# Software Engineering - Lecture 9.1

## Slide 1: Software Engineering(CS3201)Design and ImplementationMISSION: Save Earth 🚀

Avinash

## Slide 2: Recap (design classes so far)

Architectural design – Organization and structure of software
System Architecture – Example (MVC etc.), Levels of abstraction (arch of small vs large), Importance and Advantages
Architectural design decisions (the questions that need to be asked to select the right architecture patterns)
Architectural views – showing design from various perspectives
Architectural patterns – standard reusable design architectures
2
Software Engineering
TEXTBOOK THEORY
NOTE: Slides marked ‘TEXTBOOK THEORY’ are based on textbook chapters. Marked such for easy reference before preparation for exam!

## Slide 3: You wake up…

A spaceship in deep space
You wake up alone… alarms blaring… you have no memory… and you must design a system to save earth
Today you are not students, but engineers on a failing spaceship, systems failing around you
There are no instructions on what is to be done
This is exactly how software with bad design feels like
3
Software Engineering

## Slide 4: What is Design and what is Implementation?

Architectural pattern deals with how the spaceship is organized
Design pattern concerns with how individual components communicate
Implementation deals with fixing and running the system in space
Bad design means you, earth’s last hope, dies
4
Software Engineering

## Slide 5: System is the spaceship

A system is a collection of components (spaceship is the system architecture)
Communication, Life support, Navigation are all components of the spaceship
Each module must work independently and interact with one or more components to get the job done (design patterns)
If life support stops, does navigation also stop working? No (why? Modular design/ layered design)
5
Software Engineering

## Slide 6: Introduction

Design – a creative process (?) where you identify components and their relationships
Implementation – realizing the design as a program
A design language like UML is more appropriate when using object oriented based development
Less appropriate (useful) when developing using off the shelf components
Dynamically typed languages (like Python) do not enforce type, making it less rigorous – some say this makes design less apt (SOM.), however, I believe it puts the onus on us to follow design carefully?
6
Software Engineering
TEXTBOOK THEORY

## Slide 7: Design Steps

Context
Architecture
Objects
UML Models
Interfaces
7
Software Engineering

## Slide 8

Object Oriented Design using UML
8
Software Engineering

## Slide 9: Introduction

Object oriented system – set of interacting objects, that maintain their own state/ data and provide operations on that state (using methods), to fulfill an objective
We design classes and their relationships, when design is realized at runtime, objects are created out of these class definitions
Changes to class (objects) should not affect other classes (objects) in a system
To develop system design (in OOP): (already saw this in slide #7)
  - Understand context and external interactions
  - Design system architecture
  - Identify principal objects
  - Develop design models
  - Specify interfaces
9
Software Engineering
TEXTBOOK THEORY

## Slide 10: Step 1: System context and Interactions

First stage – understand what your system should do, and its relation to the external environment
System context models are complementary – shows both structure (using simple block diagram and association) and interaction (using use cases)
10
Software Engineering
TEXTBOOK THEORY

## Slide 11: System context for a weather station

Shows the components of a weather station system and the links between them
Informal model of architecture
Box = Component (can be decomposed into subcomponents)
Association – relationship between components
High-level picture of system structure
11
Software Engineering
TEXTBOOK THEORY

## Slide 12: Use cases for Weather Station

12
Software Engineering
TEXTBOOK THEORY

## Slide 13: Use case description for Weather Station

13
Software Engineering
TEXTBOOK THEORY

## Slide 14: Step 2: System Architecture (previous lecture)

You understand the components, how they interact with environment (people and other systems) - call this X
Using X, principles of architecture design (modularity, decoupling, etc.), and domain knowledge (file download app has several users requesting similar service), you then need to design system architecture
May use a particular architectural pattern (like layered or client-server) to organize the components of your system (and their interactions)
Finally the design pattern (how components interact to one another or events) - In the following example (weather station), a "listener model" is followed (this is an example of an event-based design pattern – components listen and react to specific events)
14
Software Engineering
TEXTBOOK THEORY

## Slide 15: System Architecture – Weather station

Composed of independent subsystems
Easy to support different configurations because sender and receiver do not have to address one another
15
Software Engineering
TEXTBOOK THEORY

## Slide 16: Step 3: Object class identification

By this stage (in design process), you should have an idea of the essential objects in your system
As system understanding develops, you understand objects needed (which can and will be later refined)
16
Software Engineering
TEXTBOOK THEORY

## Slide 17: Object class identification

Some approaches to identify objects:
  - Grammatical analysis of natural language description of the system, where objects and attributes are nouns, and operations / services / interfaces / methods are verbs
  - Objects are tangible entities (student, faculty, etc.), roles such as admin, interactions such as meetings, locations such as offices or classrooms
  - Scenario analysis – Take various usage scenarios one by one, and identify the required objects (what objects and interactions take place during withdrawal of money from ATM – lab example)
17
Software Engineering
TEXTBOOK THEORY

## Slide 18: Object class identification

In practice, use several knowledge sources to discover objects
Apart from object identification in previous slide, you may have to design "implementation objects", that are used to provide services – searching database (here search is an abstract operation, providing a service of searching database, and yet it can be converted to an object)
Your tangible hardware can become objects too
18
Software Engineering
TEXTBOOK THEORY

## Slide 19: Object class identification

19
Software Engineering
TEXTBOOK THEORY

## Slide 20: Object class identification

Knowledge of application domain can be used to identify objects, attributes and services
  - Weather stations are located in remote places and include instruments whose functioning can go wrong. This implies that we need attributes and operations to check the proper functioning of the system
  - Many remote weather stations, so each station needs a unique identifier
  - Weather stations can be installed at different times, and hence have different instruments, therefore each system should be uniquely identified, and might need a database table containing information of all instruments in use
You may also identify a hierarchy in objects, and apply generalization (all instrument classes can have 'Instrument' superclass)
20
Software Engineering
TEXTBOOK THEORY

## Slide 21: Object class identification: Game time!

What objects exist in a spaceship?
_________________
_________________
_________________
Turn objects into spaceship entities: ‘OxygenSystem’ class can have a method say generateOxygen()
21
Software Engineering

## Slide 22: Step 4: Design Model

Stage 4 – show objects/ classes, and relationships and interactions between these entities
Abstract but at the same time, detailed enough for programmers to make implementation decisions
Plan based development usually requires more detailed design model
UML supports two kinds of design model:
  - Structural models: Static structure of the system
  - Dynamic models: dynamic structure and runtime interactions
Three UML model types:
  - Subsystem model: logical grouping of objects into systems and subsystems
  - Sequence model: shows sequence of object interactions
  - State machine model: shows how objects change in response to events
22
Software Engineering
TEXTBOOK THEORY

## Slide 23: Step 5: Interface Specification

Specifies the interfaces between the components identified by design
Important since it enables parallel implementation of objects/ subsystems
Once interface is specified, it is assumed that the person developing the particular object/ component/ subsystem will provide the specified interfaces
Specified in UML in notation similar to class diagram, however, there is no attributes section
UML stereotype <<interface>> is used to indicate interfaces
Include operations to access and update data
As data is hidden, it can be changed without affecting object behavior, and code is more maintainable
23
Software Engineering
TEXTBOOK THEORY

## Slide 24: Interface Specification

24
Software Engineering
TEXTBOOK THEORY

## Slide 25

Design Patterns
25
Software Engineering
TEXTBOOK THEORY

## Slide 26: Design Patterns

Certain common patterns of building design that are effective
Pattern is a description of the problem and the solution
A well-tried solution to a common problem
Apart from being tested solution to common problems, they have become a vocabulary for talking about a design (you can explain your design by mentioning your design pattern)
Four essential elements to design patterns
  - A name
  - A description of the problem area
  - A solution description
  - A statement of consequences (results and tradeoffs of applying this pattern)
26
Software Engineering
TEXTBOOK THEORY

## Slide 27: Design Patterns: Sample

27
Software Engineering
TEXTBOOK THEORY

## Slide 28: Design Patterns: Sample

28
Software Engineering
TEXTBOOK THEORY

## Slide 29: Design pattern: Back to our spaceship

Observer pattern: Sensors notify and alert the ship
  - Grace doesn’t constantly ask Rocky if he is there? He just listens, he reacts to any signal sent by Rocky
Singleton: Only one main control system on the ship! You do not want TWO captains issuing commands on the ship
Architectural pattern – spaceship blueprint
Design pattern – how buttons and controls work
29
Software Engineering

## Slide 30: Difference between design and arch. pattern?

30
Software Engineering

## Slide 31: Design pattern: Back to our spaceship

Forget the 3 textbooks, just check this site out for everything related to Design patterns:
  - https://refactoring.guru/design-patterns
Example: Observer pattern
  - https://refactoring.guru/design-patterns/observer
31
Software Engineering

## Slide 32

Implementation Issues
32
Software Engineering
TEXTBOOK THEORY

## Slide 33: Implementation Issues

Reuse: Can Grace reuse existing tools or must he build them from scratch?
Configuration Management: What if settings are configured wrong? Incorrect Oxygen levels?
Host-target development: Testing on earth while planning for the mission versus Testing in deep space where the system should do what it is supposed to do
33
Software Engineering

## Slide 34: Summary

<<ToDo: Insert image of summary written down on board in class>>
34
Software Engineering

## Slide 35

Open-source Development
35
Software Engineering
