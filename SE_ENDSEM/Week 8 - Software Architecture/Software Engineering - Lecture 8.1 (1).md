# Software Engineering - Lecture 8.1 (1)

## Slide 1: Software Engineering(CS3201)Architectural Design

Avinash

## Slide 2: Refinement in Design / Steps in design

High-level architecture (big picture)
  - This lecture (8.1) deals with high-level architecture primarily
Component-level design (breaking it down)
  - How components interact, Example: Component diagrams
Database design (where data is stored)
  - Type of DB (SQL vs. NoSQL), Example: ER diagrams
User interface design
  - How users interact with system? Examples: wireframes, use cases
API design (how components talk)
  - Front and back end communication, output: API documentation
Security and performance planning
2
Software Engineering

## Slide 3: Brainstorming (more in slide 14)

Is there a tried and tested formula / approach we can use to structure our project? (Architecture patterns)
Single or Distributed? (deployment impacts architecture)
Centralized or Distributed control? (impacts architecture)
How will we document plans? (UML, SDD,…)
Fundamental approach to solve the problem, should we go with monolithic? modular? Microservices?
The word that keeps repeating - 'Architecture'
3
Software Engineering

## Slide 4: Setting up the stage... for high level design

What is Software Architecture? What is Architectural Design?
Is it important? (otherwise, I would not be teaching it)
What decisions need to be taken when it comes to software architecture? (slide 14)
What are Architectural patterns? (the keyword is pattern)
What are Application Specific Architectural patterns? (certain patterns are linked to certain applications)
Why so many questions? Can we stop now please!
4
Software Engineering

## Slide 5

Architectural Design
5
Software Engineering

## Slide 6: Introduction

Architectural design: Organization and structure of a software system
Identifies the main structural components of a system and the relationships between them
Output of Architectural Design process: Architectural model
Even something as dynamic as Agile process aims to identify overall system architecture early into the project. Why? Because changes to Architecture is expensive (students, why is it expensive?)
6
Software Engineering

## Slide 7: System Architecture: A sample block diagram

Shows the components of a robotic packing system and the links between them
Informal model of architecture
Box = Component (can be decomposed into subcomponents)
Arrow = Direction of data or control signal flow
High-level picture of system structure
7
Software Engineering

## Slide 8: System Architecture: Levels of abstraction

Architecture in the small: Architecture of individual (??) programs ("concerned with how an individual program is decomposed into components" - Do not let SOM. confuse you, he means, very likely, an individual software system "this chapter is concerned with program architectures")
Architecture in the large: Architecture of complex enterprise systems that include other systems, programs, and program components ("can consist of or spread over several computers across different companies" - SOM. specifically means distributed systems)
8
Software Engineering

## Slide 9: System Architecture: Importance

Effects the performance, robustness, distribute-ability and maintainability of a system
Individual components implement functional requirements, but the system architecture influences non-functional requirements
"Non-functional requirements have the most significant effect on system's architecture" (Chen et al, 2013)
You can fulfill the same functional requirements by different architectures, but the non-functional requirements are impacted by different architectures
9
Software Engineering

## Slide 10: System Architecture: Advantages (Bass et. Al, 2012)

Stakeholder communication: Architecture is a high-level presentation of the system that may be used as a focus for discussion by a range of different stakeholders
System analysis: Making system architecture explicit early in the project leads to system analysis, and decisions have a profound effect on critical (non-functional) requirements like performance, reliability and such
Large-scale reuse: The system architecture is often the same for systems with similar requirements and so can support large-scale software reuse
10
Software Engineering

## Slide 11: System Architecture Model: Usage

The block diagram seen earlier does not show relationships between components or the externally visible properties of components (it is an example of a high-level system design)
Two ways in which an architectural model is used:
  - As a way of encouraging discussions by using a high-level system design
  - As a way of documenting architecture that has been designed (complete model showing different components, interfaces, connections)
11
Software Engineering

## Slide 12: System / Software Architecture definitions (Hans Van Vliet, pg. 281)

An early definition: "The architecture of a software system defines that system in terms of computational components and interactions among those components." (shaw et.al., 1995)
Recent definition: "The software architecture of a program or computing system is the structure or structures of the system, which comprise software elements, the externally visible properties of those elements, and the relationships among them." (Bass et.al., 2003)
Also, software architecture can have different views (just like your system models had different views, based on different perspectives)
12
Software Engineering

## Slide 13: Software Architecture and SDLC (Hans Van Vliet,pg. 283)

Software life cycle a) without and b) with explicit attention to software architecture
13
Software Engineering
In traditional models there is no balancing of functional and quality requirements. Once the functional requirements are agreed upon, development proceeds and it is assumed that quality requirements can be met.If it turns out that the quality requirements cannot be met, the project gets into trouble. Deadlines slip, functionality is skipped, more hardware is bought, etc.
In process models that include a software architecture phase, there is a balancing of functional and quality requirements at an early stage

## Slide 14: Architectural Design decisions

14
Software Engineering

## Slide 15: Architectural views

Two uses of Architectural models:
  - Encourage discussions on system
  - Help with detailed system design
Two issues relevant in both uses:
  - What views and perspectives are useful when designing and documenting a system's architecture?
  - What notation should be used for describing models?
Impossible to show all relevant architecture information (what components? how they interact? etc.) in one diagram
We will need different perspectives at different times
Therefore, we have multiple views of software architecture
15
Software Engineering

## Slide 16: Architectural views (more disturbing than the eye of Sauron?)

16
Software Engineering

## Slide 17: Architectural views

4 fundamental architectural views:
  - Logical view: Shows key abstractions as objects or object classes (helps relate requirements to entities)
  - Process view: Shows interacting processes at system runtime (gives idea of non-functional characteristics like performance and availability)
  - Development view: Shows breakdown of software into components
  - Physical view: Shows system hardware and how software components are distributed across processors
Hofmeister et al. (Hofmeister, Nord, and Soni 2000) suggest the use of similar views but add to this the notion of a conceptual view
Conceptual view: Abstract system view, basis for decomposing high-level requirements into more detailed specifications
17
Software Engineering

## Slide 18: Architectural views

18
Software Engineering
Logical View:
Focus: Functionality
Describes the system's key components, their responsibilities, and interactions from a developer’s perspective.
Often represented using class diagrams, sequence diagrams, or ER diagrams.
Example: In an e-commerce app, this view would show modules like "User Management," "Product Catalog," and "Order Processing."
Development View (Implementation view)
Focus: Code structure and organization
Describes the system's module structure, libraries, and components to help developers manage source code.
Uses package diagrams, component    diagrams, or folder structures.
Example: The e-commerce app might have different repositories for frontend, backend, and database schemas. They will be shown as a folder structure where different components are specified.

## Slide 19: Architectural views

19
Software Engineering
Process View:
Focus: Runtime behavior and concurrency
Describes how threads, processes, and communication mechanisms work to achieve performance, scalability, and fault tolerance.
Often represented using sequence diagrams, activity diagrams, or deployment diagrams.
Example: How requests from multiple users are handled in parallel in the e-commerce app.
Physical View:
Focus: Infrastructure and hardware
Describes how the software is deployed across servers, networks, or cloud environments.
Uses deployment diagrams or infrastructure diagrams.
Example: The e-commerce app might be deployed on AWS with multiple microservices.

## Slide 20: Architectural views

Differing views (I mean opinions) on whether UML should be used for describing/ documenting software architectures
Lange et al., 2006, surveyed and found that UML was applied many a times, in an informal way
However, UML is of most use when documenting an architecture in detail – Somerville, pg. 175
Some researchers (Bass et al., 2012) propose using ADLs to describe architectures – not a very widespread opinion
Informal models, and notations, like UML, remain most used ways of documenting architecture
For more of what Sommerville has to say, read pg. 175; for what I have to say, attend class on 18.3.2026
20
Software Engineering

## Slide 21

Architectural Patterns
21
Software Engineering

## Slide 22: Introduction

Pattern (English) - "a repeated decorative design", "standard", "model", "arrangement", "structure" (all repeatable)
Pattern as a way of presenting, sharing, reusing knowledge of software systems
Patterns may be described in a standard way using a mixture of narrative description and diagrams
But what is a pattern (in a software/ system sense?)
22
Software Engineering

## Slide 23: Architectural Patterns

Abstract description of good practice
Tried and tested (successful) system organizations (on different systems and environments)
Architectural pattern, therefore, "should describe a system organization that has been successful in previous systems"
Should include details of when it is proper to use the pattern, details of strengths and weaknesses of the pattern
Used in high level design
Based on requirements and nature of project, choose an arch. pattern
23
Software Engineering

## Slide 24: Model-View-Controller: A sample pattern

24
Software Engineering

## Slide 25: Model-View-Controller: A sample pattern

25
Software Engineering
Organization of a Model-View-Controller system
Note: Use login of a website as an example to explain this architectural pattern.

## Slide 26: Model-View-Controller: A sample pattern

26
Software Engineering
Web application architecture using the Model-View-Controller pattern

## Slide 27: Layered Architecture

Separation and independence - fundamental to architectural design – since they allow changes to be localized
MVC, seen previously, allows separate elements in a system, which can be changed independently
The Layered Architecture is another architectural pattern that allows separation and independence
27
Software Engineering

## Slide 28: Layered Architecture

System functionality organized into layers
Each layer relies only (depends) on the layer beneath it
Each layer can communicate with adjacent layers only
Allows incremental development, changeable and portable
If a layer interface changes, only the adjacent layer is affected
Can help localize machine dependencies, therefore portable across platforms
The number of layers is arbitrary
28
Software Engineering

## Slide 29: Layered Architecture

29
Software Engineering

## Slide 30: Layered Architecture

30
Software Engineering

## Slide 31: Repository Architecture

Describes how a set of interacting components can share data
Systems that use a large amount of data are organized around a shared database or repository
Used by systems where data is generated by one component and used by another
Repository is passive and control the responsibility of components using the repository
"black board" model triggers components when particular data becomes available
31
Software Engineering

## Slide 32: Repository Architecture – Simpler words?

Repository Architecture is a software design pattern where:
  - multiple system components interact with a centralized data store (repository)
  - The repository acts as a shared knowledge base that different modules access to store, retrieve, and update data
This pattern is useful when multiple subsystems need a common data source and helps in data consistency, integration, and scalability.
32
Software Engineering

## Slide 33: Repository Architecture

33
Software Engineering

## Slide 34: Repository Architecture

34
Software Engineering

## Slide 35: Repository Architecture – A more relatable example: GitHub

Central Repository (GitHub Server): Acts as a shared storage where developers push and pull code
Multiple Clients (Developers, Teams, CI/CD Pipelines): Developers interact with the repository using Git commands (clone, commit, push, pull)
Decentralized Contributions: Developers work on local copies (branches), make changes, and synchronize with the central repository
Data Consistency: GitHub ensures that the latest changes are available for all contributors
35
Software Engineering

## Slide 36: Client Server Architecture

Commonly used organization for distributed systems
System organized as a set of services (and associated servers), and clients that access and use that services
Major components of this architecture:
  - Set of servers that offer services to other components
  - A set of clients that call on the services offered by the servers
  - A network that allows the clients to access the servers
Generally considered for distributed, a logical model of independent services can be implemented on a single computer
Again, the important benefit is separation and independence (modularity)
36
Software Engineering

## Slide 37: Client Server Architecture

Clients should know available servers (and services) and a way to access them (for eg., RPC using HTTP request-reply protocol)
Server need not keep identity of clients, or number of clients connected
Example:
  - Multi-user, web-based system for providing film and photograph library
Biggest advantage: It is a distributed architecture
37
Software Engineering

## Slide 38: Client Server Architecture

38
Software Engineering

## Slide 39: Client Server Architecture

39
Software Engineering

## Slide 40: Pipe and Filter Architecture

Model of the runtime organization of a system (where functional transformations process their inputs and produce outputs)
Data moves from one process step to another and is transformed in the process
These process steps may execute sequentially or in parallel
Data can be transformed item by item or in a batch
Name comes from unix where processes can be linked using pipes
A variant of this architecture was used since computers were first used for automatic data processing – sequential processing of batch data – the classic batch (sequential) processing
Best suited for batch and embedded systems (because of limited user interaction)
40
Software Engineering

## Slide 41: Pipe and Filter Architecture

41
Software Engineering

## Slide 42: Pipe and Filter Architecture

42
Software Engineering

## Slide 43: Various patterns have overlapping features, how do I differentiate? T.T

43
Software Engineering

## Slide 44: Various patterns have overlapping features, how do I differentiate? T.T

44
Software Engineering

## Slide 45: When to use which? T.T

45
Software Engineering

## Slide 46: Closing thoughts

Other architectures are available:
  - Microservice based architecture
  - Peer-to-peer architecture
  - Event-Driven Architecture
  - …
Look them up, Sommerville doesn't discuss them, but I will, time permitting
46
Software Engineering

## Slide 47: An example: University portal

Functional requirements:
  - Students can login.
  - Students can view grades.
  - Students can view attendance.
  - Faculty can upload grades.
  - Admin can manage users.
All these functional requirements can be implemented using any architectural pattern
However, different architecture patterns impact non-functional requirements in different ways
47
Software Engineering

## Slide 48: An example: University portal

Consider using the simplest architecture, Monolithic architecture (all modules (login, grades, attendance, admin) run inside one application and one database.)
48
Software Engineering

## Slide 49: An example: University portal

Consider MVC (separation of application into three different logical layers, model-view-controller)
Example flow: Student clicks View Grades => Controller => Model => View displays results
49
Software Engineering

## Slide 50: An example: University portal

Consider client-server
Example flow: Student app => request grades => server processes => results returned.
50
Software Engineering

## Slide 51: An example: University portal

Consider layered (3 layers, presentation for UI, business layer for processing grades and other logic, and data layer to access database)
Example flow: Student UI => Business logic => Database => response returned.
51
Software Engineering

## Slide 52: An example: University portal

Consider microservices  (each module is a separate service, and the services communicate using APIs)
Example flow: Student UI => Business logic => Database => response returned.
52
Software Engineering

## Slide 53: Comparison across architectures

53
Software Engineering
