# Software Engineering - Lecture 3

## Slide 1: Software Engineering(CS3201)Agile Methodologies

Avinash

## Slide 2: Some artefacts (for course project)

Statement of Work Template: Available here
2
Software Engineering

## Slide 3

Process Models... continued
3
Software Engineering

## Slide 4: Agile Software Development (Process)

Agile Processes (Agile methods)
  - Extreme Programming
  - Scrum
  - DSDM (Refer Pressman, pg. 79)
4
Software Engineering

## Slide 5: Introduction

Businesses now operate in a global, rapidly changing environment
Rapid software development and delivery is therefore the most critical requirement for most business systems
In a changing environment, it is impossible to derive a complete set of stable software requirements
It may only be after a system has been delivered and users gain experience with it that the real requirements become clear
As the requirements change or as requirements problems are discovered, the system design or implementation has to be reworked
Conventional waterfall or specification-based process usually becomes a lengthy one
5
Software Engineering

## Slide 6: Introduction

For some types of software, such as safety-critical control systems, where a complete analysis of the system is essential, this plan-driven approach is the right one
For fast moving businesses, by the time the software is available for use, the original reason for its procurement may have changed so radically that the software is effectively useless
Therefore, for business systems in particular, development processes that focus on rapid software development and delivery are essential
Agile methods are designed to produce useful software quickly
6
Software Engineering

## Slide 7: Agile Method characteristics

The processes of specification, design and implementation are interleaved. There is no detailed system specification, and design documentation is minimized or generated automatically (by using certain tools)
User requirements document is an outline definition of the most important characteristics of the system
System is developed in a series of increments. End users and other stakeholders involved in specifying and evaluating each increment
Extensive tool support is used to support the development process (examples: Automated testing tools, configuration management, system integration)
7
Software Engineering

## Slide 8: Agile Methods

Incremental development methods
Increments are small, and, typically, new releases of the system are created and made available to customers every two or three weeks
Customers involved in development - rapid feedback on changing requirements
Minimize documentation by using informal communications rather than formal meetings with written documents
Consider design and implementation to be the central activities
8
Software Engineering

## Slide 9: Agile Method vs. Plan based methods

9
Software Engineering
In plan-based development, iterations happen within phases / activities
In Agile, iterations happen across phases / activities
Possible to use agile practices along with plan based processes

## Slide 10: Agile Methods vs. Plan based methods

Plan based software development
  - Came from a software engineering community that was responsible for developing large, long-lived software systems such as aerospace or government systems
  - Usually large teams across different companies
  - Time: Might take even 10 years from initial plan to deployment
  - Overhead in planning but justified by system criticality and coordination
Agile:
  - For small and medium businesses, overhead in plan-based approach dominates actual software development process
  - Focus on software, requirements change as software develops
  - Deliver working software quickly, new and changed requirements in future iterations
  - Agile Manifesto
10
Software Engineering

## Slide 11: Change costs as a function of time:Agile vs. Plan based

11
Software Engineering

## Slide 12: Principles of Agile Methods (Som., pg. 76)

12
Software Engineering

## Slide 13: Agile Methods: Usage

Agile methods have been particularly successful for two kinds of system development:
  - Product development where a software company is developing a small or medium-sized product for sale. Virtually all software products and apps are now developed using an agile approach
  - Custom system development within an organization, where there is a clear commitment from the customer to become involved in the development process and where there are few external stakeholders and regulations that affect the software
Agile methodology works (best) when the software itself is a stand-alone system rather than tightly integrated with other systems being developed at the same time. Consequently, there is no need to coordinate parallel development streams
13
Software Engineering

## Slide 14: Agile Manifesto

"We are uncovering better ways of developing software by doing it and helping others do it. Through this work we have come to value:
  - Individuals and interactions over processes and tools
  - Working software over comprehensive documentation
  - Customer collaboration over contract negotiation
  - Responding to change over following a plan
That is, while there is value in the items on the right, we value the items on the left more."
14
Software Engineering

## Slide 15: Agile Methods

Extreme Programming (XP)
Scrum
DSDM
15
Software Engineering

## Slide 16: Extreme Programming (XP)

Most significant approach to changing software development culture
Pushing recognized software good practices (such as iterative development) to the extreme (An example of extreme: Several new versions of a system may be developed by different programmers, integrated, and tested in a day)
16
Software Engineering

## Slide 17: Extreme Programming (XP)

In XP:
  - Requirements are expressed as scenarios (called user stories)
  - Implemented directly as a series of tasks
  - Programmers work in pairs and develop tests for each task before writing the code
  - All tests must be successfully executed when new code is integrated into the system
  - There is a short time gap between releases of the system
17
Software Engineering

## Slide 18: XP Process

Planning:
  - XP Release Planning
    - Identify requirements in the form of stories
    - Prioritize them
    - Group them into releases.
  - XP Iteration Planning
    - Each iteration delivers a group of stories
    - Estimate project velocity (total number of story points, estimate of number of work done)
    - Plan the overall project deadline based on the velocity (possible from 2nd iteration onwards)
18
Software Engineering

## Slide 19: XP Process

Design:
  - Build Task cards
  - Build Class-Responsibility-Collaborator (CRC) cards
  - CRC cards identify and organize the object-oriented classes
  - Create prototypes to address difficult designs
  - Prototype is called spike solution
Coding:
  - Develop test cases first.
  - Programmers code with test cases in view
  - Pair programming
  - Ensures real time problem solving and quality assurance
  - Code is integrated at the end of the day with that of others
19
Software Engineering

## Slide 20: XP Process

Testing:
  - Focus on XP acceptance tests also called customer tests
  - Acceptance tests are derived from user stories
  - Verification and Validation
    - Building the product right Vs building the right product
Release:
  - Software increment decided (what features are to be implemented in the next iteration are decided)
  - Velocity computed (helps plan for the next release)
20
Software Engineering

## Slide 21: XP ComponentsStory

21
Software Engineering
In the Extreme Programming (XP) process model, a story (also known as a user story) is a short, simple description of a feature or functionality that the system should provide. It’s written from the perspective of the end user or customer and focuses on what the user wants to achieve rather than how it will be implemented.

## Slide 22: XP Components: Story

The common template is:
“As a [type of user], I want [an action or feature] so that [desired outcome].”
Examples (Sustainable Shopping Assistant App):
Barcode Scanning:
  - "As a shopper, I want to scan a product’s barcode so that I can instantly see its sustainability rating."
Eco-Friendly Suggestions:
  - "As a conscious consumer, I want to receive eco-friendly product suggestions based on my purchases so that I can make more sustainable choices."
Carbon Footprint Analysis:
  - "As a user, I want to upload my supermarket bills so that the app can analyze my ecological footprint."
22
Software Engineering

## Slide 23: XP ComponentsTask cards

23
Software Engineering
In Extreme Programming (XP), task cards are used to break down user stories into smaller, manageable units of work called tasks. While user stories describe what the user wants, task cards focus on how to implement those features from a technical perspective.

## Slide 24: XP Process Components – Task cards

Key Characteristics of Task Cards:
Implementation-Focused:
  - Each task card describes a specific technical activity needed to complete a user story.
  - Example: “Design the database schema for storing product sustainability data.”
Small and Manageable:
  - Tasks should be small enough to be completed within a few hours to a day.
  - This makes tracking progress easier during iterations.
Linked to User Stories:
  - Every task card is associated with a specific user story, ensuring that all technical work directly contributes to delivering user value.
Written by Developers:
  - Unlike user stories, which are often written by customers or product owners, task cards are usually created by the development team during iteration planning
24
Software Engineering

## Slide 25: Example: Sustainable Shopping Assistant App

User Story:
"As a shopper, I want to scan a product’s barcode so that I can instantly see its sustainability rating."
Associated Task Cards:
Integrate Barcode Scanner API
  - Set up the barcode scanning library and test device compatibility.
  - Estimate: 4 hours
Develop UI for Scanning Screen
  - Design and implement the screen where users scan barcodes.
  - Estimate: 3 hours
Connect Scanner to Database
  - Ensure scanned barcodes fetch sustainability data from the database.
  - Estimate: 5 hours
Implement Error Handling for Invalid Barcodes
  - Display appropriate messages when a barcode isn’t recognized.
  - Estimate: 2 hours
25
Software Engineering

## Slide 26: XP Process Components – Velocity

Key Aspects of Velocity:
Definition:
  - Velocity represents the sum of effort estimates (usually in story points, ideal days, or hours) for all the user stories or tasks that a team completes in an iteration
  - It reflects the team’s productivity and capacity
How It's Measured:
  - At the end of each iteration, the team adds up the effort estimates of fully completed work items
  - For example, if a team completes stories worth 20, 15, and 10 story points, their velocity for that iteration is 45 story points
26
Software Engineering

## Slide 27: XP Process Components – Velocity example

Example (Sustainable Shopping Assistant App):
Iteration 1:
  - Barcode Scanner Feature (8 story points) ✔
  - Product Sustainability Database (13 story points) ✔
  - Eco-Friendly Product Suggestions (5 story points) ❌ (not completed)
Velocity: 8 + 13 = 21 story points for Iteration 1
For a full example, refer here
27
Software Engineering

## Slide 28: XP Process Components – CRC cards

Key Components of CRC Cards:
Class:
  - Represents an object or entity in the system.
  - The name of the class is written at the top of the card.
  - Example: Product, User, Order.
Responsibilities:
  - Defines what the class is supposed to do—its duties, behaviors, or functions.
  - Example: For a Product class, responsibilities could be "calculate price with discount" or "update stock quantity."
Collaborators:
  - Lists other classes that this class interacts with to fulfill its responsibilities.
  - Example: A ShoppingCart class might collaborate with the Product and Payment classes
28
Software Engineering

## Slide 29: XP Process Components – Pair Programming

Pair Programming is a core practice in Extreme Programming (XP) where two developers work together at one workstation to write code. It’s designed to improve code quality, encourage collaboration, and enhance problem-solving through real-time feedback and shared knowledge
Details (2-page handout) of pair programming: here
29
Software Engineering

## Slide 30: XP Process Components – Test case description

In Extreme Programming (XP), test cases are an integral part of the development process, especially because XP heavily relies on Test-Driven Development (TDD). Test cases in XP are often written before the actual code to ensure that the code meets the desired requirements and behaves as expected.
Details (2-page handout) of pair programming: here
30
Software Engineering

## Slide 31: XP Components:Test casedescription

31
Software Engineering

## Slide 32: XP Release Cycle

32
Software Engineering
Note (my 2 cents): The term 'release' here is slightly confusing. Release generally consists of multiple iterations, where each iteration is a phase where some part of the product is built. You can think of an iteration as an increment. Therefore, read 'release' as 'iteration' in this graph.

## Slide 33: XP Practices

33
Software Engineering

## Slide 34: XP Practices

34
Software Engineering

## Slide 35: XP Closing thoughts

In practice, the application of Extreme Programming as originally proposed has proved to be more difficult than anticipated
It cannot be readily integrated with the management practices and culture of most businesses. Therefore, companies adopting agile methods pick and choose those XP practices that are most appropriate for their way of working
Sometimes these are incorporated into their own development processes but, more commonly, they are used in conjunction with a management focused agile method such as Scrum (Rubin 2013).
35
Software Engineering

## Slide 36

Scrum
36
Software Engineering

## Slide 37: Agile Project Management.. Scrum.. Introduction

In any software business, managers need to know what is going on and whether a project is likely to meet its objectives (and deliver the project on time)
Plan-driven approaches to software development evolved to meet this need
XP based approaches do not cater to the point above
A plan-based approach requires a manager to have a stable view of everything that must be developed and the development processes
The informal nature of early agile methods clashed with the business requirement for visibility
While this can and does work for small companies developing software, it is inappropriate for larger companies
37
Software Engineering

## Slide 38: Agile Project Management.. Scrum.. Introduction

To address the issues mentioned in the previous slide(s), Scrum agile method was developed
Scrum developed to "provide a framework for organizing agile projects and, to some extent at least, provide external visibility of what is going on"
Therefore, it is called a plan-based agile approach
Developers of scrum wished to make it clear that is not a method for project management in the conventional sense, therefore, you have new terminology (which you will see in due course)
Scrum follows the principles of Agile development, however,
It provides a framework for Agile Project Organization, and does not mandate specific practices (like pair programming, for instance) - meaning, can be integrated more easily with existing company policies
38
Software Engineering

## Slide 39: SCRUMptious? Whet your appetite up to some study?

Where do we start? Let's start at the very beginning... In the beginning, there was a need to eat... food... it started simple enough, foraging for small animals, plants... Hit Fast Forward 2 million years... priorities have changed, we start with the 'Product Backlog'
'Product backlog' - The input to the scrum process
Product backlog is a list of to-do items that are needed for the product
Okay, this is not working, let me try another approach – let's look at an image explaining the overall scrum ideology
39
Software Engineering

## Slide 40: Scrum process flow (Pressman, pg. 78)

40
Software Engineering

## Slide 41: SCRUM – Setting the environment

Roles – Product owner, Scrum Master, Team
Ceremonies – Sprint planning, Sprint review, Sprint retrospective, Daily Scrum meeting
Artifacts – Product backlog, Sprint backlog, Burndown chart
41
Software Engineering
A lot of  sprinting around! Very healthy!
A sprint is nothing but a period (of time), where some pre-defined tasks are completed.
Some people tend to use the term 'Sprint Meeting', however, in reality, there is no 'sprint meeting' and instead sprint planning (what to do in a sprint), sprint review (what did we build) and sprint retrospective (how did we build, how was our process) are various meetings that happen during a sprint.

## Slide 42: SCRUM – Roles

Product Owner:
    - Defines product features, release date and content, responsible for profitability of product (ROI), prioritize features, create product backlog
    - Primary Point of Contact with the customer (and represents the customer)
Scrum Master:
    - Represents management side (and what do managers do – ensure productivity, following of practices, coordination and cooperation)
Scrum Team:
    - 5 - 10 people (typically), Cross functional (Each member provides a variety of skills - QA, Programmers, UI designers, etc.), Members should be full time (usually), highly collaborative, empowered (team members have the authority to make decisions), transparent (work in the open and understood across all in the team)
42
Software Engineering
For more on Product Owner and Scrum Master, refer
What is a scrum master and their responsibilities?

## Slide 43: SCRUM – Artifacts

Product Backlog:
  - "The product backlog is a dynamic, prioritized list of all the features, functions, requirements, enhancements, and fixes necessary for a project."
  - "product backlog helps prioritize and organize project requirements"
  - The list is prioritized by Product Owner
  - Usually the list consists of story-based work ("let the user search") and task-based work ("we should handle exceptions")
  - Usually created before the 'Sprint planning' meeting
  - Can be changed and re-prioritized before each Sprint Planning
  - More can be found here: Product and Sprint Backlog
43
Software Engineering

## Slide 44: SCRUM – Artifacts

Sprint Backlog:
  - It is a curated list of items the development team commits to completing during a sprint
  - Breaks down the selected product backlog into actionable tasks that can be taken in a sprint
  - Also helps provide a clear sprint plan
  - Sprint backlog is usually created during the 'Sprint Planning' meeting
  - Is flexible and allows change – can add new tasks to meet goals, remove unnecessary tasks
  - Can be updated only by the scrum team
  - More can be found here: Product and Sprint Backlog
44
Software Engineering

## Slide 45: SCRUM – Artifacts

An example of Product backlog and Sprint backlog (the tasks under a product backlog):
1. Redesign the checkout page (Product backlog)
  - Task 1.1: Conduct user research to identify pain points (Assigned: User experience researcher, eight hours)
  - Task 1.2: Create wireframes (Assigned: UI designer, 16 hours)
  - Task 1.3: Develop frontend code (Assigned: Frontend developer, 24 hours)
  - Task 1.4: Integrate with backend (Assigned: Backend developer, 16 hours)
  - Task 1.5: Conduct usability testing (Assigned: QA engineer, eight hours)
45
Software Engineering

## Slide 46: SCRUM – Artifacts

Differences between product and sprint backlogs
46
Software Engineering

## Slide 47: SCRUM – Artifacts

Sprint burn down chart
  - Depicts the total Sprint Backlog hours remaining per day
  - Shows the estimated amount of time to release
  - Ideally should burn down to zero to the end of the Sprint
  - Is usually not a straight line
47
Software Engineering

## Slide 48: SCRUM – Ceremonies

Sprint Planning:
  - 1st Part:
    - Participants: Product Owner, Scrum Master, Scrum Team
    - Creating Product Backlog
    - Determining the Sprint Goal
  - 2nd Part:
    - Participants: Scrum Master, Scrum Team
    - Creating Sprint Backlog
The whole team is involved in selecting which of the highest priority items they believe can be completed
To make these estimates, they use the velocity attained in previous sprints, that is, how much of the backlog could be covered in a single sprint
This leads to the creation of a sprint backlog—the work to be done during that sprint
48
Software Engineering

## Slide 49: SCRUM – Ceremonies

Sprint:
  - A month-long iteration, during which is a product functionality is implemented (SOM. says 2-4 weeks)
  - NO outside influence can interfere with the Scrum team during the Sprint
  - Each Sprint begins with the Daily Scrum Meeting (which then happens every day)
  - Note: Sprints are never extended to take account of unfinished work
  - Items that cannot be completed are returned to the product backlog
49
Software Engineering

## Slide 50: SCRUM – Ceremonies

Daily Scrum Meeting:
  - Parameters – Daily, 15-minutes, Stand-up (also called a Huddle), Not for problem solving
  - Three questions:
    - What did you do yesterday?
    - What will you do today?
    - What obstacles are in your way?
  - Is NOT:
    - a problem-solving session (though sometimes discussions on problems do happen)
    - a way to collect information about WHO is behind the schedule
  - Is:
    - meeting in which team members make  commitments to each other and to the Scrum Master
    - a good way for a scrum master to keep track of the work going on
50
Software Engineering

## Slide 51: SCRUM – Ceremonies

Sprint Review:
  - Team presents what it accomplished during the sprint
  - Typically takes the form of a demo of new features or underlying architecture
  - Informal: 2-hour prep time rule
  - Participants:
    - Customers
    - Management
    - Product Owner
    - Other engineers
Sprint Retrospective Meetings:
  - Scrum team only
  - Feedback meeting (Start, stop, continue)
51
Software Engineering

## Slide 52: Scrum sprint cycle (SOM., pg. 86)

52
Software Engineering

## Slide 53: What people like about scrum? (SOM., pg. 87)

The product is broken down into a set of manageable and understandable chunks
Unstable requirements do not hold up progress
The whole team has visibility of everything
Customers see on-time delivery of increments and gain feedback on how the product works
Trust between customers and developers is established
53
Software Engineering

## Slide 54

Thank you!
54
Software Engineering
