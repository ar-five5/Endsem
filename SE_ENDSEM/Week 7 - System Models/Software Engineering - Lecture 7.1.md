# Software Engineering - Lecture 7.1

## Slide 1: Software Engineering(CS3201)System Models

Avinash

## Slide 2: Recap

In last week's lectures, we looked at Context models and Structural models
Context model: Helps decide system boundaries, what is and what is not part of a system
Structural model: Helps display the organization of the system in terms of the components that make up the system and their relationships
Today, we will look at the remaining models (interaction and behavioral models)
2
Software Engineering

## Slide 3

System Models continued...
3
Software Engineering

## Slide 4: Interaction Models

All systems involve interaction of some kind
Types:
  - User interaction (involves user inputs and outputs)
  - Between system and environment (other systems)
  - Between components of a software system
Importance:
  - User interaction modeling is important as it helps identify user requirements – what user wants to achieve from interaction, how they will interact
  - Modeling system-to-system interaction highlights the communication problems that may arise – at the interface level
  - Modeling component interaction helps us understand if a proposed system structure is likely to deliver the required system performance and dependability – is your design good enough?
4
Software Engineering

## Slide 5: How modelling component interaction helps

Suppose the components on the university portal interact as follows, Web Interface => Student Service => Grades Service => Database
If every request goes through multiple services sequentially, the system might become slow when thousands of students check grades simultaneously after results are released
Modeling component interaction helps detect:
  - Bottlenecks (too many service calls)
  - Single points of failure
  - Slow database queries
  - Overloaded services during peak usage
5
Software Engineering

## Slide 6: Interaction Models

Two related approaches to interaction modeling
  - Use case modeling: Mostly used to model interactions between a system and external agents (human users or other systems)
  - Sequence diagrams: Model interactions between system components, although external agents may also be included
Both present interactions at a different level of detail (in case both are used to describe systems)
Details of the interactions involved in a high-level use case may be documented in a sequence diagram
6
Software Engineering

## Slide 7: Use Case Modeling

As seen on TV in lab
7
Software Engineering

## Slide 8: Sequence Diagrams

As seen on TV in lab
8
Software Engineering

## Slide 9: Behavioural Models

Models the dynamic behavior of a system as it is executing
Show what happens or what is supposed to happen when a system responds to a stimulus from its environment
The stimuli may be either data or events:
  - Availability of certain data triggers processing in the system
  - An event that triggers processing happens, events may or may not have associated data
Many business systems are data processing systems
By contrast, most real-time systems are event driven
9
Software Engineering

## Slide 10: Data-driven Modeling

Data-driven models show the sequence of actions involved in processing input data and generating an associated output
They show the sequence of actions that take place from an initial input being processed to the eventual output
Among the first graphical software models
Data-flow diagrams (DFDs) were among the first models (c. 1970s)
Tracking and documenting how data flows through a system helps understand what is going on in the process
Data-flow diagrams can be represented in the UML using the activity diagram type (more in SE lab)
10
Software Engineering

## Slide 11: Data-driven Modeling

You can see the processing steps, represented as activities (rounded rectangles), and the data flowing between these steps, represented as objects (rectangles)
11
Software Engineering

## Slide 12: Data-driven Modeling

An alternative way of showing the sequence of processing in a system is to use UML sequence diagrams (generally used to model interaction, "but with messages sent only left to right, they show sequential data processing")
12
Software Engineering

## Slide 13: Event-driven Modeling

Event-driven modeling shows how a system responds to external and internal events
Assumption: System has a finite number of states and that events (stimuli) may cause a transition from one state to another
This view of a system is particularly appropriate for real-time systems
The UML supports event-based modeling using state diagrams (more in SE lab)
State diagrams show system states and events that cause transitions from one state to another
They do not show the flow of data within the system but may include additional information on the computations carried out in each state
13
Software Engineering

## Slide 14: Event-driven Modeling

14
Software Engineering
In UML state diagrams, rounded rectangles represent system states. They may
include a brief description (following “do”) of the actions taken in that state. The
labeled arrows represent stimuli that force a transition from one state to another. You can indicate start and end states using filled circles, as in activity diagrams.

## Slide 15: Event-driven Modeling

15
Software Engineering
The problem with state-based modeling is that the number of possible states increases rapidly. For large system models, therefore, you need to hide detail in the models. One way to do this is by using the notion of a “superstate” that encapsulates a number of separate states.

## Slide 16: Event-driven Modeling

16
Software Engineering
State models of a system provide an overview of event processing, but you normally have to extend this with a more detailed description of the stimuli and the system states. You may use a table to list the states and events that stimulate state transitions along with a description of each state and event.

## Slide 17: Model-driven Engineering

Model-driven engineering (MDE) is an approach to software development whereby models rather than programs are the principal outputs of the development process (Brambilla, Cabot, and Wimmer 2012)
Model-driven engineering was developed from the idea of model-driven architecture (MDA) (proposed by the Object Management Group (OMG) as a new software development paradigm (Mellor, Scott, and Weise 2004))
MDA focuses on the design and implementation stages of software development, whereas MDE is ­ concerned with all aspects of the software engineering process
17
Software Engineering

## Slide 18: Model-driven Architecture

Use a subset of UML models to describe a system
Models are created at different level of abstraction
MDA recommends three types of abstract system models:
  - Computation Independent Model (CIM): High level business model that describes process without considering software details (example: flowchart or activity diagram)
  - Platform Independent Model (PIM): Defines architecture and logic without mentioning specific technology (example: class diagrams)
  - Platform Specific Model (PSM): Transform PIM into a platform specific implementation (example: Eclipse EMF (Eclipse Modeling Framework) – Generates Java code from UML models, Acceleo – Generates code from models using templates (supports Java, Python, PHP), AndroMDA – Converts UML into J2EE components)
18
Software Engineering
