# Software Engineering - Lecture 5

## Slide 1: Software Engineering(CS3201)Software Requirements

Avinash

## Slide 2

Functional and Non-functional Requirements
2
Software Engineering

## Slide 3: Introduction (formal definition)

Software system requirements are often classified as functional or non-functional requirements
  - Functional Requirements: These are statements of services the system should provide, how the system should react to particular inputs, and how the system should behave in particular situations. In some cases, the functional requirements may also explicitly state what the system should not do
  - Non-functional Requirements: These are constraints on the services or functions offered /imposed by the environment. They include timing constraints, constraints on the development process, and constraints imposed by standards. Non-functional requirements often apply to the system as a whole rather than individual system features or services
3
Software Engineering
Constraint (noun): a limitation or restriction

## Slide 4: Functional Requirements

Functional requirements (of a system) describe what the system should do
Functional requirements depend on:
  - The kind of software being developed (cannot have 7" LED screen UI on an embedded insulin delivery application)
  - Expected users (An app for senior citizens should have icons accordingly)
  - Organizational approach (User stories vs. SRS, IEEE 830 (SRS) vs. Custom, etc.)
Functional requirements can be expressed either as user or system requirements (depending on the granularity of expression)
Therefore, functional requirements can be one of two types:
  - Functional user requirements
  - Functional system requirements
4
Software Engineering

## Slide 5: Functional Requirements

When expressed as user requirements, functional requirements should be written in natural language
Functional system requirements expand the user requirements and are written for system developers (describe the system functions, their inputs and outputs, and exceptions in detail)
Note: Functional user requirements can vary in level of level of detail. Example:
  - A user shall be able to search the appointments lists for all clinics
  - The system shall generate each day, for each clinic, a list of patients who are expected to attend appointments that day
  - Each staff member using the system shall be uniquely identified by his or her eight-digit employee number
5
Software Engineering

## Slide 6: Requirements this and requirements that!!

Requirements: Can be user (more generic) or system (more specific)
Example:
  - User Requirement: We need a login page where users enter their credentials and login
  - System Requirement: The login page must consist of two textboxes, each of width 250 px and height 20 px. The password textbook should hide the characters using asterick. There should be a login button which when clicked checks the credentials entered in the two textboxes against a database, and while this happens, a loading icon must be displayed
6
Software Engineering

## Slide 7: Requirements this and requirements that!!

Requirements: Can be functional (express what software must do) or non-functional (not related to the software per se, but is a requirement of the ecosystem where the software runs)
"Ecosystem where the software runs"?!? An example: If you develop an application that is meant to automatically administer insulin, the non-functional requirement here is that the application must be reliable (another requirement can be that it use less energy)
7
Software Engineering

## Slide 8: Functional Requirements

You must have understood by now that different types of requirements have different levels of expressional granularity (let's call it that)
Due to this differences in expression, errors might creep in (check 'notes' of this slide for an example from textbook)
Imprecision in the requirements specification can lead to disputes between customers and software developers
Natural for a system developer to interpret an ambiguous requirement in a way that simplifies its implementation
8
Software Engineering

## Slide 9: Functional Requirements- Example on imprecision

"The system should allow users to book appointments."
Why is this a Problem?
  - What does "booking" mean? (One-click booking? Should it have a calendar view?)
  - What type of appointments? (Doctor, in person, consultancy?)
  - Can users cancel or reschedule?
  - Is there a limit on how many appointments a user can book?
  - Should users receive reminders? If yes, how? (Email, SMS, push notification?)
Better way - "The system shall allow users to book, cancel, and reschedule appointments through a calendar interface. Users will receive automated email and SMS reminders 24 hours before their appointment."
9
Software Engineering

## Slide 10: Functional Requirements

Key Takeaway: Imprecise requirements lead to mismatched expectations, rework, and disputes. Always be clear, detailed, and specific in functional requirements!
Ideally, the functional requirements specification of a system should be both complete and consistent
Completeness means that all services and information required by the user should be defined
Consistency means that requirements should not be contradictory
10
Software Engineering

## Slide 11: Functional Requirements

In practice, it is only possible to achieve requirements consistency and completeness for very small software systems
It is easy to make mistakes and omissions when writing specifications for large, complex systems
Additionally, large systems have many stakeholders, with different backgrounds and expectations
Stakeholders are likely to have different—and often inconsistent—needs
Inconsistencies may not be obvious when the requirements are originally specified, and the inconsistent requirements may only be discovered after deeper analysis or during system development
11
Software Engineering

## Slide 12: Functional Requirements – Example of inconsistent needs

E-commerce website:
Stakeholder 1: Marketing Team
  - Wants a one-click checkout option to make the purchasing process fast and seamless for customers.
  - Believes fewer steps = higher conversion rates and more sales.
Stakeholder 2: Finance & Security Team
  - Wants a multi-step verification process for payments, including OTP (one-time password) and CAPTCHA, to prevent fraud and chargebacks.
  - Prefers additional security, even if it makes the checkout process longer.
12
Software Engineering

## Slide 13: Non-functional requirements

Not directly concerned with the services needed / delivered by the system to users
Usually specify or constrain characteristics of the system as a whole
In simple words – Requirements enforced by the system/ environment
Examples:
  - Emergent system properties: Reliability, Response time, Memory use
  - Constraints on the system: I/O device capabilities, data representation
Non-functional requirements (ironically, because "non-functional") are more critical than functional requirements (you can drop a functional requirement if need be)
  - Example: A software for an aircraft must be reliable, a software for a body embedded insulin delivery system must consume less battery
13
Software Engineering

## Slide 14: Non-functional requirements

Possible to identify which system components implement specific functional requirements (e.g., a specific UI/UX tool is responsible for generating charts)
Not possible / or more difficult with non-functional requirements
The implementation of these non-functional requirements may be spread throughout the system, for two reasons:
  - Non-functional requirements may affect the overall architecture of a system rather than the individual components
  - An individual non-functional requirement, such as a security requirement, may generate several, related functional requirements (In addition, it may also generate requirements that constrain existing requirements)
14
Software Engineering

## Slide 15: Non-functional requirements

Nonfunctional requirements arise through user needs because of budget constraints, organizational policies, the need for interoperability with other software or hardware systems, or external factors such as safety regulations or privacy legislation
From the figure in the following slide, you can see that the non-functional requirements may come from required characteristics of the software (product requirements), the organization developing/using the software (organizational requirements), or external sources
15
Software Engineering

## Slide 16: Types of non-functional requirements

16
Software Engineering

## Slide 17: Non-functional requirements

Product requirements: "These requirements specify or constrain the runtime behavior of the software" (what even?!! Hmph!)
Requirements that are defined by the characteristics of the system (the system/ device/ environment the software should run on)
  - (System: Smart phone, Req: App must launch within 5 sec. of tap)
  - (System: Sensor node, Req: Must consume < 1 joule energy per day)
  - (System: Bank DB, Req: Finance records must not have round-off errors)
  - (System: Social Media server, Req: Must handle 1,000,000 concurrent users)
  - ...
These requirements focus on the system’s internal attributes, such as performance, security, usability, and reliability, which impact the user experience and system effectiveness
17
Software Engineering

## Slide 18: Non-functional requirements

Organizational requirements: "Broad system requirements derived from policies and procedures in the customer’s and developer’s organizations"
These requirements ensure that the product aligns with the company’s internal processes, business rules, regulatory compliance, and long-term goals
  - (System: Juno, Req: Must be compatible with existing payroll schema) - Business Process Alignment
  - (System: Student records, Req: Use AES256 algorithm) - Security policy
  - (System: Data center, Req: Must use at least 50% renewable energy by 2030)
  - (System: Juno, Req: Must support role-based access – Student, faculty) - This can be an example of a functional requirement as well; or a non-functional requirement that can lead to functional requirements
18
Software Engineering

## Slide 19: Non-functional requirements

External requirements: This broad heading covers all requirements that are derived from external factors (legal regulations, market conditions, customer expectations, environmental factors)
Beyond the direct control of organization but must be met
  - (System: Social Media App, Req: Must comply with GDPR in Europe) - Regulatory requirement
  - (System: Healthcare App, Req: Must comply with HIPAA in US) - Data protection and privacy laws
  - (System: Middle east travel guide, Req: Must support RTL text direction for Arabic) - Cultural considerations
  - (System: Cloud web app, Req: Must satisfy AWS security best practices) - External hosting constraints
  - (System: AI resume shortlisting, Req: AI must not exhibit gender or race bias) - Ethical requirements
  - (System: Card payment system, Requirement: Must comply with PCI DSS) - Regulatory and legal compliance
19
Software Engineering

## Slide 20: Examples of possible non-functional requirements for Mentcare (from textbook)

20
Software Engineering
Product requirement
  - The Mentcare system shall be available to all clinics during normal working hours (Mon–Fri, 08:30–17:30). Downtime within normal working hours shall not exceed 5 seconds in any one day
Organizational requirement
  - Users of the Mentcare system shall identify themselves using their health authority identity card
External requirement
  - The system shall implement patient privacy provisions as set out in HStan-03-2006-priv

## Slide 21: Example case study:Smart Home Automation System

A technology company wants to develop a Smart Home Automation System that allows users to control various smart devices (e.g., lights, thermostats, security cameras, and door locks) through a mobile app. The system should support voice commands, provide automation rules (e.g., turning off lights when no one is home), and send real-time notifications for security alerts
21
Software Engineering

## Slide 22: Example case study:Smart Home Automation System

Functional Requirements:
  - Device Control: Users should be able to remotely control smart devices (e.g., turn lights on/off, adjust thermostat temperature)
  - Voice Command Integration: The system should support voice assistants (e.g., Alexa, Google Assistant) for hands-free control
  - Automation Rules: Users can create automation routines, such as setting lights to turn on at sunset or locking doors at bedtime
  - Security Alerts & Notifications: The system should send real-time alerts if security sensors detect unusual activity (e.g., motion detected while the house is empty)
  - Multi-User Access: Homeowners can grant access to family members with different permission levels (e.g., full control vs. limited control)
22
Software Engineering

## Slide 23: Example case study:Smart Home Automation System

Non-Functional Requirements:
  - Reliability: The system should work 24/7 with minimal downtime, ensuring devices remain accessible at all times
  - Security: Data transmissions must be end-to-end encrypted to prevent hacking or unauthorized access
  - Scalability: The system should support adding new devices without affecting performance
  - Latency: Commands should be executed within 2 seconds of user input to ensure responsiveness
  - Compatibility: The system should be compatible with at least 80% of smart home devices available on the market
23
Software Engineering

## Slide 24: Non-functional requirements

Goals proposed can be generic and difficult to quantify an objectively check
Customers find it difficult to translate goals to measurable requirements
Non-functional requirements can conflict and interact with other functional and non-functional requirements
It can be difficult to separate functional and non-functional requirements sometimes
However, you should, highlight requirements that are clearly related to emergent system properties (performance or reliability) - You can do this by putting them in a separate section of the requirements document or by distinguishing them, in some way, from other system requirements
Non-functional requirements such as reliability, safety, and confidentiality requirements are particularly important for critical systems
24
Software Engineering

## Slide 25: Non-functional requirements – possible metrics

25
Software Engineering

## Slide 26: Differentiate between functional and non-functional

Sometimes, it is difficult to differentiate between functional and non-functional requirements. Here are possible hacks
What vs. How:
  - Functional Requirements (WHAT the system should do): These describe specific tasks, actions, or operations the system must perform
  - Non-Functional Requirements (HOW the system should perform): These describe the quality, constraints, and system behavior
26
Software Engineering

## Slide 27: What vs. How - Example

Online Banking System:
Functional Requirements (WHAT the system should do)
  - The system shall allow users to transfer money between accounts.
  - Users can reset their password via email verification.
Non-Functional Requirements (HOW the system should perform)
  - The system must process transactions within 2 seconds. (Performance)
  - The system must be available 99.9% of the time. (Availability)
  - All sensitive data must be encrypted. (Security)
27
Software Engineering

## Slide 28: Differentiate between functional and non-functional

Another Hack (perhaps): "Can You Code It?"
  - Functional Requirements: Can be directly coded."A user can log in with a username and password."
  - Non-Functional Requirements: Are about quality, not code."The system should be user-friendly." (This is a guideline, not a function)
Quick Test to Check:
  - Does it describe a feature? It is Functional
  - Does it describe performance, security, usability, or constraints? It is Non-Functional
28
Software Engineering

## Slide 29

Requirements Specification
29
Software Engineering

## Slide 30: Introduction

Requirements specification is the process of writing down the user and system requirements in a requirements document
Should be clear, unambiguous, easy to understand, complete, and consistent (difficult to achieve in practice)
User requirements are almost always written in natural language supplemented by appropriate diagrams and tables in the requirements document
System requirements may also be written in natural language, but other notations based on forms (predefined structure), graphical, or mathematical system models can also be used
30
Software Engineering

## Slide 31: Notations for writing System Requirements

31
Software Engineering

## Slide 32: Natural language specification Guidelines (SOM. Pg. 122)

Invent a (basic) standard format and ensure that all requirement definitions adhere to that format
Wherever possible, you should write the requirement in one or two sentences of natural language
Use language consistently to distinguish between mandatory and desirable (usage of "shall" and "should")
Use text highlighting to pick out key parts
Avoid the use of jargon, abbreviations, and acronyms
Include rationale where possible. The rationale should explain why the requirement has been included and who proposed the requirement
32
Software Engineering

## Slide 33: Structured Specification

Structured natural language: Requirements are written in a standard way rather than as free-form text
Still uses natural language BUT brings in a structure / template (ensuring uniformity)
These specifications may use programming language constructs to show alternatives and iteration
May structure your template around objects (data) manipulated, functions performed, events processed (and so on)
Variability in specification is reduced
May use tables and other graphical models, if extra information is needed (tables are especially useful when there are multiple possible alternative actions)
33
Software Engineering

## Slide 34: Information to be included in structured format

A description of the function or entity being specified.
A description of its inputs and the origin of these inputs.
A description of its outputs and the destination of these outputs.
Information needed for the computation or other entities in the system that are required (the “requires” part).
A description of the action to be taken.
If a functional approach is used, a precondition setting out what must be true before the function is called, and a postcondition specifying what is true after the function is called.
A description of the side effects (if any) of the operation.
34
Software Engineering

## Slide 35: Structured Specification

35
Software Engineering

## Slide 36: Structured Specification

36
Software Engineering

## Slide 37: Graphical Notation: Use cases

Will be covered in lab
37
Software Engineering

## Slide 38: Mathematical models

ResponseTime ≤ 2 seconds (Response time should be <= 2 seconds)
∀u(Login(u)⇒Registered(u)) (if user is logging in, they should be registered)
Marks⊆{0,1,2,...,100} (Marks can take values between 0-100)
S={Idle,Monitoring,Delivering,Alarm}, Glucose>Threshold⇒State=Delivering (if glucose is greater than threshold, move to the state deliver)
G(Glucose>180⇒F<5min DeliverInsulin)  (temporal logic)
38
Software Engineering

## Slide 39: Software Requirements Specification document

Official statement of what system developers should implement
May include both user requirements and system requirements
Essential when:
  - System (software) development is outsourced
  - Different teams develop different components
  - Detailed requirements analysis is mandatory
Places where it is not needed: Software first approach, quick prototypes, Agile development (user stories)
Still a good practice to have a condensed SRS, even when focused on short increments/ sprints, to keep track of overall system requirements
39
Software Engineering

## Slide 40: Users of SRS document

40
Software Engineering

## Slide 41: Software Requirements Specification document

Diversity of the users means this document can be a compromise
The level of detail of the document depends on the type of system being developed (critical vs. non-critical), and the development process used (many teams/ outsourcing vs. in-house, iterative)
One possible standard for SRS is IEEE 1998-830 (it is generic but can be adapted to specific uses)
41
Software Engineering

## Slide 42: Structure of SRS (as per IEEE 1998-830) SOM. pg. 128

42
Software Engineering

## Slide 43

Requirements Engineering
43
Software Engineering
