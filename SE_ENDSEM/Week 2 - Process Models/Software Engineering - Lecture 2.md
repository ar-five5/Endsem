# Software Engineering - Lecture 2

## Slide 1: Software Engineering(CS3201)Process Models

Avinash

## Slide 2: Software Process

2
Software Engineering
:Design Phase:
Software Design:
High-level Design – Define modular components (classes, interfaces), Define data structures
Detailed Design – how reach component works internally (functions/ interfaces, etc.), tables designed, Algorithm and logic design, sequence and interaction design, constraints
:Definition Phase: (Specification)
Requirements Definition and Analysis:
Developer must understand – Application Domain, Required Functionality, Required Performance, User Interface  (might require one or several meetings with client)
Project Planning – Allocate resources, Estimate costs, Define work tasks, Define schedule
System Analysis – Allocate system resources to hardware, software, users, etc.
:Development Phase:
Coding:
Develop code for each module, Unit Testing
Integration:
Combine modules, System Testing

## Slide 3: Software Process

3
Software Engineering
:Software Evolution: (Maintenance)
Correction – Fix Software defects
Adaptation – Accommodate changes and new features (and new company policy)
Enhancements – new features
Prevention – Identify areas to improve software and make it more maintainable
:Validation:
Requirements Analysis and Test Case development, Test Case Execution and Defect Tracking
Types - System Integration Testing (how software interacts with other software); User Acceptance Testing (tests if it works as per user req.); Quality Assurance Testing (meets quality standards)
:Umbrella Activities:
Reviews – Assure Quality (Documents review, Code review, etc.)
Documentation – Improves communication across teams and maintainability
Version Control – Track changes
Configuration Management – track of various versions and associated documentation

## Slide 4: Software Process

4
Software Engineering
Hans Van Vliet, 3rd Ed.

## Slide 5: Software Engineering Fundamentals

5
Software Engineering
Some fundamental principles apply to all types of Software system, irrespective of the development techniques used:
  - Systems should be developed using a managed and understood development process. Of course, different types of processes are used for different types of software
  - Dependability and performance are important for all types of system
  - Understanding and managing the software specification and requirements (what the software should do) are important
  - When appropriate, you should reuse software that has already been developed rather than write new software

## Slide 6: Case study 3 – A wilderness weather station

Classwork
Role play (tentative) – Mimic the people involved and the artefacts needed throughout the entire software lifecycle towards delivery of efficient working product
6
Software Engineering

## Slide 7: Case study 3 – A wilderness weather station

7
Software Engineering
UML Package Diagram showing the systems in the Software, where each system is a collection of components – for instance, classes.

## Slide 8: Case study 3 – A wilderness weather station

The weather station system: This system is responsible for collecting weather data, carrying out some initial data processing, and transmitting it to the data management system
The data management and archiving system: This system collects the data from all of the wilderness weather stations, carries out data processing and analysis, and archives the data in a form that can be retrieved by other systems, such as weather forecasting systems
The station maintenance system: This system can communicate by satellite with all wilderness weather stations to monitor the health of these systems and provide reports of problems. It can update the embedded software in these systems. In the event of system problems, this system can also be used to remotely control weather station
8
Software Engineering

## Slide 9: Case study 3 – A wilderness weather station

Requirements:
People involved – Primary stakeholders (Project Sponsors, End users); Secondary stakeholders (Regulatory authorities, Local community representatives); Technical team (Project Manager, Systems Architect, Hardware Engineers, Software Developers, Network Engineers, Data Analysts); Operations specialists (Deployment and Maintenance teams, IT security); Cross Discipline experts (Environmental scientists, GIS experts)
Use documents, mockups, prototypes, user stories, etc. to aid communication. Can have a requirements gathering workshop (with agenda, objective and plan in place to draw up requirements)
9
Software Engineering

## Slide 10: Case study 3 – A wilderness weather station

Design:
People involved – Core Design team (System Architect, hardware engineers, software engineers – backend developer, frontend developer, network engineers, data analysts, UI/UX designers), Support team (Project manager, environmental scientists, deployment and maintenance teams, IT security team)
By now, I think you are able to appreciate or get a flavor of what goes into software development on a large scale
10
Software Engineering

## Slide 11: Case study 3 – A wilderness weather station

Now let's look at testing (an example to give a better idea)
Testing:
  - Unit Testing: Individual components like sensor readings, transmission, storage
  - Integration Testing: How sensors interact with each other and server
  - System Testing: Deploy in controlled environment and test end-to-end
  - Performance Testing: Performance under stress (high loads)
  - Field Testing: Deploy prototype in real world and test
  - Failover and Recovery Testing: Simulate failures to see how system deals with failure (how it recovers from a power failure, for instance)
11
Software Engineering

## Slide 12: Case study 3 – A wilderness weather station

Document showcasing a structured approach needed to designing, implementing and deploying the wilderness weather station: See here
12
Software Engineering

## Slide 13: Summary of Software Engineering Process

Requirements Analysis
Design
Coding / Implementation
Validation / Testing
Maintenance
13
Software Engineering

## Slide 14: Maintenance

"A family friend retired after being a COBOL programmer for 30 years. About two years after his retirement, a company came to him and said, 'Name your salary,' and he requested around $1.5 million/year. He was hired on the spot and still works there.“
"Pick an obscure programming language, write lots of important code, and don’t comment or document anything.“
14
Software Engineering
Source: https://www.buzzfeed.com/andyneuenschwander/people-are-sharing-what-their-wealthiest-friend-does-for

## Slide 15: Software Engineering Costs

15
Software Engineering
Figure source: SE CS3204, Raghu Kisore, MEC, 2024

## Slide 16

Process Models
16
Software Engineering

## Slide 17: Generic Process Models / Process Flows (Refer Pressman, pg. 33)

17
Software Engineering
!!! Though Pressman uses the term Process flows, I would you rather NOT USE the term Process flow, since it can be misunderstood for 'flow or usage pattern of a software'. !!!

## Slide 18: Generic Process Models / Process Flows (Refer Pressman, pg. 33)

18
Software Engineering

## Slide 19: Software Engineering Process Models

As explained earlier, a software process model (sometimes called a Software Development Life Cycle or SDLC model) is a simplified representation of a software process
In this section, we introduce a number of very general process models (sometimes called process paradigms) and present these from an architectural perspective. That is, we see the framework of the process but not the details of process activities
These can be thought of as process frameworks, and can be extended and adapted to create more specific software engineering processes
There is no universal process model which works for all kinds of software development
19
Software Engineering

## Slide 20: Software Engineering Process Models

Types:
  - The waterfall model: This takes the fundamental process activities of specification, development, validation, and evolution and represents them as separate process phases such as requirements specification, software design, implementation, and testing
  - Incremental development: This approach interleaves the activities of specification, development, and validation. The system is developed as a series of versions (increments), with each version adding functionality to the previous version
  - Integration and configuration: This approach relies on the availability of reusable components or systems. The system development process focuses on configuring these components for use in a new setting and integrating them into a system
20
Software Engineering

## Slide 21: Software Engineering Process Models

Many practical software projects tend to combine the best bits from different general models (previous slide)
Attempts have also been made to come up with an universal process model, the best known among these is the Rational Unified Process – RUP
RUP can be modified in different ways such that can resemble any of the general models
Adopted by some companies, notably IBM, but not widespread
21
Software Engineering

## Slide 22: Waterfall Model (Refer Sommerville, pg. 47)

Derived from large military systems engineering
Plan driven process – you plan and schedule in advance
Stages of Waterfall model directly reflect the fundamental software engineering activities
Result of each phase is one or more documents which are “signed off” (approved). The next phase does not start until the previous phase completes
This approach works better for hardware solutions, but is not practical (at least in most cases) for software solutions
22
Software Engineering

## Slide 23: Waterfall Model

23
Software Engineering

## Slide 24: Waterfall Model

Drawbacks:
  - Sequential flow from stage to stage rarely possible, especially hard to envisage the end product in the requirements analysis stage
  - No option to come back and modify, forces teams to freeze prematurely at different stages
When to use:
  - Only in situations where – Requirements well understood, Technology is stable, No ambiguity at any stage
Example usage:
  - Embedded Systems
  - Critical Systems
24
Software Engineering

## Slide 25: Incremental Development (Refer Sommerville, pg. 49)

Incremental development is based on the idea of developing an initial implementation, getting feedback from users and others, and evolving the software through several versions until the required system has been developed
Therefore, here, specification, development and validation are interleaved, rather than separate, with rapid feedback across activities
Incremental development reflects the way that we solve problems. We rarely work out a complete problem solution in advance but move toward a solution in a series of steps, backtracking when we realize that we have made a mistake. By developing the software incrementally, it is cheaper and easier to make changes in the software as it is being developed
25
Software Engineering

## Slide 26: Incremental Model (Refer Pressman, pg. 43)

26
Software Engineering

## Slide 27: Incremental Development

Major advantages over waterfall:
  - Cost of implementing requirements changes is reduced
  - Easier to get customer feedback on tangible work (customer can give better feedback on a working prototype than on a set of documents)
  - Early delivery and deployment of “useful” software is possible, customers gain value faster from the software
Drawbacks (managerial):
  - Process not visible, therefore difficult to track (and since versions are developed quickly, it is not viable to produce documents for every version)
  - System structure tends to degrade as new features are added (however, agile methods suggest that you regularly refactor, i.e., improve and restructure, the software
27
Software Engineering

## Slide 28: Integration and Configuration (re-use)(Refer Sommerville, pg. 52)

Informally, there is some amount of software reuse always (regardless of process type)
Reuse-oriented approaches rely on a base of reusable software components and an integrating framework
Three types of software components are frequently reused: Stand-alone application systems, collection of objects as part of a component or package, web services developed following some standard and can be accessed by remote invocation over the Internet
28
Software Engineering

## Slide 29: Integration and Configuration (re-use)

29
Software Engineering

## Slide 30: Integration and Configuration (re-use)

Stages:
  - Requirements Specification: Initial requirements proposed. These do not have to be elaborated in detail but should include brief descriptions of essential requirements and desirable system features
  - Software discovery and evaluation: A search is made for components and systems that provide the functionality required. Candidate components and systems are evaluated
  - Requirements refinement: During this stage, the requirements are refined using information about the reusable components and applications that have been discovered
  - Application system configuration: If an off-the-shelf application system that meets the requirements is available, it may then be configured for use to create new system
  - Component adaptation and integration: If there is no off-the-shelf system, individual reusable components may be modified, then integrated to create the system
30
Software Engineering

## Slide 31: Examples on each of the process models

Sample software engineering examples utilizing each of the three process models can be found here: Additional handouts
31
Software Engineering

## Slide 32: Additional Models (based on the 3 paradigms)

V model
Evolutionary Process Models
  - Prototyping Model
  - Spiral Model
32
Software Engineering

## Slide 33: V Model (Refer Pressman, pg. 42)

33
Software Engineering
Wait, what is happening here?!
Just look at the left arm (or leg) of the V, and it is nothing but your simple waterfall model.
The right arm (or leg) of the V symbolizes the fact that the V model focuses on testing artefacts produced at every single stage / phase of project lifecycle.
Do other models not focus on testing? How is V different?
It integrates testing ALONGSIDE each phase of process lifecycle.
How do you test requirements modelling?Here, testing does not happen in a conventional sense, rather you do something like requirements review, where documents are verified across all stakeholders. You could also start developing test cases and work on Requirements Traceability Matrix (RTM)

## Slide 34: Prototyping Model (Refer Pressman, pg. 45)

34
Software Engineering
Oi! Whats happening here?! Is this life? (maybe it is, maybe it isn't – refer Parminedes and Neitzsche)
Okay, so coming back, prototyping involves building a quick prototype (simple version of software), to gather ideas and feedback, and get a consensus on the product before building it in detail.
General life cycle of a prototype:
-Understand the Basics
-Build a simple version (prototype)
-Get feedback
-Improve the prototype
-Build the final product
One gray area in this process is what one can do with the prototype? Do we build on top of it, or build the final product from scratch. In my experience, prototypes do not follow rigor while building, and then it becomes risky to build final product on top of prototype (but that is just my 2 cents)

## Slide 35: Spiral Model (Refer Pressman, pg. 45)

35
Software Engineering
Okay, now what? A vinyl?
Then how it is different from incremental?
Here, there is a lot of focus on risk analysis and management.
Think of it as baking a cake? First build the base, if it tastes okay, add a layer on top of it, and so on. Unlike prototyping, every intermediate product is well executed and follows engineering rigor.
Building software step by step, focusing on reducing risks and improving the product as you go. It’s like combining planning, building, and testing in small loops (or spirals) until the software is finished. Each loop adds more details and features to the software
The crucial difference between this model and the others is that here, 'Risk Analysis' happens in 'Planning' stage
Risk analysis is the process of identifying, evaluating, and prioritizing potential problems or uncertainties in a project to minimize their impact.

## Slide 36: Selecting a process model (Pressman pg. 47)

36
Software Engineering

## Slide 37: Selecting a process model (Pressman pg. 50)

37
Software Engineering

## Slide 38: Agile Processes

Next set of slides
38
Software Engineering

## Slide 39: Cue cards: Which Software Process to use

39
Software Engineering
Waterfall model: Best for projects with clear requirements, fixed scope and predictable timelines.
Iterative Model: Suitable for complex projects where requirements may change during development, allowing for incremental refinement.
Spiral Model: Used for high-risk projects where thorough risk assessment and mitigation are crucial.
V-model: Emphasizes rigorous testing at each development phase, ensuring high quality software.
Agile Model: Ideal for projects with evolving requirements, frequent customer feedback, and a need for flexibility.
I & C Model: When system can be built using reusable components, when time is critical, requirements are well defined, and minimal custom development.

## Slide 40

Thank you!
40
Software Engineering
