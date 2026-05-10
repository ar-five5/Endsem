# Software Engineering - Lecture 4.1

## Slide 1: Software Engineering(CS3201)CMMI

Avinash

## Slide 2: Why is Software Development difficult?

Communication
  - Between customer and  developer
    - Poor problem definition is largest cause of failed software projects
  - Within development team
    - More people = more communication, new programmers need training
Project characteristics
  - Novelty (but hey, this is welcome! Right?)
  - Changing requirements
  - 5 x cost during development (bug fixes, refactoring, etc.)
  - Up to 100 x cost during maintenance (production bugs, legacy software maintenance)
  - Hardware/software configuration (running software on various platforms)
  - Security requirements (more ubiquitous, more security concerns)
  - Real time requirements (more stringent constraints)
  - Reliability requirements
2
Software Engineering

## Slide 3: Process and Process Maturity

Software Process
Set of activities, methods, practices, and transformations (things converted as part of process) that people use to develop and maintain software and the associated products (e.g., project plans, design documents, code, test cases, user manuals)
Examples: Waterfall model, Incremental model, Agile methods, etc.
Software Process Maturity (how good is process of software dev?)
  - Defines to what extent an organizations' processes are mature (how good)
  - "Describes the range of expected results that can be achieved by following a software process" (better the process, more likely to predict results)
  - Means of predicting the most likely outcomes to be expected from the next software project the organization undertakes – standard procedure bring predictability
  - In simpler words – how good a team is at delivering high quality software
3
Software Engineering

## Slide 4: Introduction – Process Areas and succinct summary of all the slides in this lecture

So far, we have seen SDLC (Process) and SDLC phases
Now we look at process areas
Process areas are the building blocks of CMMI (coming next)
Each process area defines a specific organizational feature
Example: Project planning is a process area which focuses on how well a project is planned – estimate making, scheduling, resource allocation, etc.
Think of it this way, a Process Area can be a skill (time management for exam prep.), Capability is how good you are at that skill, and Maturity is how good is your overall process/ method to learning
4
Software Engineering

## Slide 5

Capability Maturity Model Integration (CMMI)
5
Software Engineering

## Slide 6: CMMI – Introduction (A café cum library)

You just opened a new café (this was my friend's idea, I wanted a library, we came upon a compromise, as you can imagine, library cum café, nice quaint space to read and/ or munch, NOT TOGETHER) - that’s me and my friend (see picture)
Goal: Serve delicious food (the actual goal is to make people happy, and how does a café do that, with delicious food), run a smooth business
6
Software Engineering

## Slide 7: Café setting: CMMI Level 1: Initial (Chaotic)

No structured processes (cooking, billing, etc.), things are unpredictable
Some days, food tastes amazing; other days, it's terrible
Staff is confused—sometimes they follow recipes, sometimes they don’t
Orders get lost (forgotten, orally taken), and customer service is hit-or-miss (!!!)
Success depends on luck/chance and individual brilliance rather than a system
Your restaurant might make the best pizza one day, but the next day, it’s undercooked because there’s no set process for making it
7
Software Engineering

## Slide 8: Café setting: CMMI Level 2: Managed (Basic)

You create basic recipes and train staff to follow them.
You start tracking inventory, so you don’t run out of key ingredients.
Orders are written down properly, so they don’t get lost.
You monitor customer complaints and try to fix common issues.
Basic amount of book-keeping / planning/ specification/ process
Now we have documentation in place to do tasks
Now, every pizza is cooked at the same temperature for the same time, so customers get a consistent experience each time they visit
8
Software Engineering

## Slide 9: Café setting: CMMI Level 3: Defined (Standardized and Documented)

You document every recipe, cooking process, and cleaning routine
All employees are trained to follow the same procedures
You introduce quality checks, like tasting dishes before serving them
Your customer service team follows a script to handle complaints efficiently (script = standard)
Standard = documentation across all types of activities in the cafe
Even if a new chef joins, they can read the recipes and deliver the same quality food without guessing
9
Software Engineering

## Slide 10: Café setting: CMMI Level 4: Quantitatively Managed (Data-Driven Decisions)

You collect data on food preparation time, ingredient usage, and customer feedback
You analyze trends (e.g., "More customers order biryani on Fridays—let’s prepare more yogurt!")
You introduce performance metrics (e.g., "Our goal is to serve every customer in under 10 minutes") - stems from data you have
You notice that spicy dishes get lower ratings, so you adjust recipes slightly based on customer feedback
10
Software Engineering

## Slide 11: Café setting: CMMI Level 5: Optimizing (Continuous Improvement & Innovation)

You introduce new innovations (e.g., using AI to predict footfall and be ready accordingly)
You experiment with new recipes based on customer preferences
You implement a loyalty program to retain customers
You use feedback loops to constantly improve operations.
You test a vegan menu, get feedback, and refine it to attract new customers while keeping regulars happy
11
Software Engineering

## Slide 12: So... 1901 CMMI

These levels, what you just saw, these are nothing but your different CMMI Maturity levels
CMMI is a framework that helps an organization improve their processes, efficiency and quality
Originally developed for Software development, now used across various industries to enhance product delivery via following proper guidelines
IN SIMPLE WORDS – Tells what level of goodness you are at in developing software
When you are dealing with things on a large scale, "winging it" is not a good idea
12
Software Engineering

## Slide 13: CMMI 2 versus CMMI 3

A subtle but important thing at this point -
  - CMMI 2 also has documentation and so does CMMI 3. What is the difference?
  - In CMMI 2, the process is documented per project, whereas in CMMI 3, the processes are defined and standardized across the organization and not just a single project
13
Software Engineering

## Slide 14: Why is CMMI important?

Ensures consistent quality in products/services
Reduces errors, risks, and inefficiencies
Improves customer satisfaction
Helps organizations stay competitive
Enhances predictability in project execution
CMMI tells:
  - The ways in which a software development process can be good
  - How good the existing process (that is followed) is
  - How to improve processes, step by step
14
Software Engineering

## Slide 15: CMMI domains (where is it applied)

CMMI for Development (CMMI-DEV) – Software, product, and system development
CMMI for Services (CMMI-SVC) – Service delivery and management
CMMI for Acquisition (CMMI-ACQ) – Procurement and supply chain management
15
Software Engineering

## Slide 16: CMMI (a more formal introduction)* because textbook *

Developed by the Software Engineering Institute of the Carnegie Mellon University
A Software Process Improvement (SPI) Framework that describes the key elements of an effective software process
Describes an evolutionary improvement path for software organizations from an ad hoc, immature process to a mature, disciplined one (Levels 1 to 5)
Provides guidance on how to gain control of processes for developing and maintaining software and how to evolve toward a culture of software engineering and management excellence
16
Software Engineering

## Slide 17: CMMI (Pressman, pg. 828)

A comprehensive process meta-model that is dependent on a set of system and software engineering capabilities that should be present as organizations reach different levels of process capability and maturity
CMMI has 2 variants: Continuous and Staged
The CMMI represents a process meta-model in two different ways: (1) as a “continuous” model (built on "capability") and (2) as a “staged” model (built on "maturity")
17
Software Engineering
The café example was a staged model (maturity levels).

## Slide 18: Staged? Continous? (eh?)

Staged:
  - Focuses on the overall maturity of an organization (which level does the organization follow)
  - Organization progress level by level
  - All process areas (requirements planning, risk analysis, etc.) required at a particular level must be fulfilled for the overall maturity of an organization to be at that particular level
Continuous
  - Capability of individual process areas
  - Each process gets a capability level (0-5)
Next question: What are process areas?! (hint: check introductory slide)
18
Software Engineering

## Slide 19: What are process areas?

These are specific areas of software development work that CMMI focuses on
Examples:
  - Requirements Gathering
  - Project Planning
  - Configuration Management
  - Quality Assurance
  - Risk Management
Note: These are different from the phases in software development life cycle (Requirements – Design – Implementation – Validation)
19
Software Engineering

## Slide 20

Staged CMMI
20
Software Engineering

## Slide 21: Staged CMMI

This deals with Maturity rather than Capability
"To achieve a maturity level, the specific goals and practices associated with a set of process areas must be achieved"
"The continuous CMMI model defines the same process areas, goals, and practices as the staged model. The primary difference is that the staged model defines five maturity levels, rather than five capability levels."
Capability levels are against individual process areas, whereas maturity levels encompass all process areas that go into a process, and lead to product development
21
Software Engineering

## Slide 22: Relationship between process areas and maturity levels

22
Software Engineering
As you can see, each maturity level has certain process areas defined. If all the process areas in a particular level are implemented satisfactorily, then that maturity level is said to be achieved.
Note: An organization at maturity level 3 will implement all process areas mentioned in maturity levels 1, 2 and 3.

## Slide 23: CMMI Levels

23
Software Engineering
Image source: Hans Van Vliet

## Slide 24: CMMI Maturity Levels

Maturity level indicates how capable the overall process is:
1. Initial
2. Repeatable
3. Defined → officially labelled as CMMI Level 3
4. Managed
5. Optimizing → officially labelled as CMMI Level 5
24
Software Engineering
Overall process – Combination of all process areas (requirements, design, implementation, etc.) is the overall process.
These are the levels we saw earlier – in the café example!

## Slide 25: CMMI Level 1: Initial

Initial: The software process is characterized as ad hoc, and occasionally even chaotic. Few processes are defined, and success depends on individual effort
  - At this level, frequently have difficulty making commitments that the staff can meet with an orderly process
  - Products developed are often over budget and schedule
  - Wide variations in cost, schedule, functionality and quality targets
  - Much depends on individual effort and brilliance rather than a proper process
25
Software Engineering

## Slide 26: CMMI Level 2: Repeatable

Basic process management processes (planning, estimation, etc.) are established to track cost, schedule, and functionality. The necessary process discipline is in place to repeat earlier successes on projects with similar applications
  - Realistic project commitments based on results observed on previous projects
  - Software project standards are defined and faithfully followed
  - Processes may differ between projects
  - Process is disciplined
  - Earlier successes can be repeated
26
Software Engineering

## Slide 27: CMMI Level 3: Defined

The software process for both management and engineering activities is documented, standardized, and integrated into a standard software process for the organization. All projects use an approved, tailored version of the organization’s standard software process for developing and maintaining software
By standard, what we mean is that now we have a set of pre agreed upon processes that are to be followed across all projects in the organization (the steps are standardized)
Processes (the things you do – requirements gathering, planning, etc.) are standardized across projects in the organization
27
Software Engineering

## Slide 28: CMMI Level 4: Managed

Detailed measures of the software process and product quality are collected. Both the software process and products are quantitatively understood and controlled
  - Narrowing the variation in process performance to fall within acceptable quantitative bounds
  - When known limits are exceeded, corrective action can be taken
  - Quantifiable and predictable
  - Since data is collected, this data is then used to predict trends in process and product quality
  - Data is also used to improve process
28
Software Engineering

## Slide 29: CMMI Level 5: Optimizing

Continuous process improvement is enabled by quantitative feedback from the process and from piloting innovative ideas and technologies
Data on process effectiveness used for cost benefit analysis of new technologies and proposed process change
29
Software Engineering

## Slide 30

Continuous CMMI
30
Software Engineering

## Slide 31: Continuous CMMI

The continuous CMMI meta-model (fancy word for framework) describes a process in two dimensions
Each process area is formally assessed against specific goals and practices and is rated according to the following capability levels
31
Software Engineering

## Slide 32: Continuous CMMI (These levels define capability)

Level 0: Incomplete — The process area (e.g., requirements management) is either not performed or does not achieve all goals and objectives defined by the CMMI for level 1 capability for the process area
Level 1: Performed— All of the specific goals of the process area (as defined by the CMMI) have been satisfied. Work tasks required to produce defined work products are being conducted
Level 2: Managed— All capability level 1 criteria have been satisfied. In addition, all work associated with the process area conforms to an organizationally defined policy; all people doing the work have access to adequate resources to get the job done; stakeholders are actively involved, all work tasks and work products are monitored, controlled, and reviewed
32
Software Engineering

## Slide 33: Continuous CMMI

Level 3: Defined— All capability level 2 criteria have been achieved. In addition, the process is “tailored from the organization’s set of standard processes according to the organization’s tailoring guidelines, and contributes work products, measures, and other process-improvement information to the organizational process assets”
Level 4: Quantitatively managed — All capability level 3 criteria have been achieved. In addition, the process area is controlled and improved using measurement and quantitative assessment. “Quantitative objectives for quality and process performance are established and used as criteria in managing the process”
Level 5: Optimized— All capability level 4 criteria have been achieved. In addition, the process area is adapted and optimized using quantitative (statistical) means to meet changing customer needs and to continually improve the efficacy of the process area under consideration
33
Software Engineering

## Slide 34: Continuous CMMI defines each process area in terms of specific goals

34
Software Engineering
Example goals for a process area, in this case, the process area is 'Project Planning'.
See a more elaborate example on 'Project planning' here: CMMI_Project_Planning_Capability_Example.docx

## Slide 35: The C in CMMI - Capability

Capability refers to the level of performance a specific process area can achieve within an organization
  - Process Area – Requirements gathering, etc.
It measures how well a process is defined, managed, and optimized to produce predictable and high-quality results (each process area can have its own results; requirements phase will lead to SRS, for eg.)
An organization can be good in certain process areas and not so good in some other process areas (from introductory analogy, you can be good in time management, but bad at listening to class)
Capability versus Maturity - Capability is measured at the individual process level, unlike maturity, which is assessed at the organizational level (overall process level)
35
Software Engineering
Like Maturity, Capability is also defined in terms of different levels.

## Slide 36: The M in CMMI - Maturity

Helps improve software process performance
  - Better results (product) achieved by following a software process
Software Process Maturity (how good (=mature) is your process?)
  - Extent to which a specific process is explicitly defined, managed, measured, controlled and effective
  - Indicates good practices in process and consistency with which they are applied in projects throughout the organization
Product Vs Process debate
36
Software Engineering
Note: Maturity is measured at an organizational level, at a level where all the steps (process) can be evaluated.

## Slide 37: Why measure software process?

Obtain data that helps us to better control
  - Schedule
  - Cost
  - Quality of software products
You can’t improve something that you can’t measure
Benefits of measurement:
  - Quantitatively expressing requirements, goals, and acceptance criteria
  - Monitoring progress and anticipating problems
  - Quantifying tradeoffs used in allocating resources
  - Predicting schedule, cost and quality
37
Software Engineering

## Slide 38

38
Software Engineering
Image source: https://sprinto.com/blog/compliance-memes/https://www.memecreator.org/meme/agile-scrum-or-cmmi-8/
Closing Point:
Understand difference between:
Process and Process Areas
Capability and Maturity
