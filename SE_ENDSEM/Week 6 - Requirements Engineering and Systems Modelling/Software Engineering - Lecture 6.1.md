# Software Engineering - Lecture 6.1

## Slide 1: Software Engineering(CS3201)Requirements Engineering

Avinash

## Slide 2

Requirements Engineering
2
Software Engineering

## Slide 3: Introduction

Involves three key activities
  - Requirements Elicitation (and Analysis)
  - Requirements Specification
  - Requirements Validation
Requirements Elicitation: Discovering requirements by interacting with stakeholders
Requirements Specification: Converting requirements to standard form
Requirements Validation: Checking whether the requirements define what the customer wants
3
Software Engineering

## Slide 4: Introduction

The output of the RE process is a system requirements document
4
Software Engineering

## Slide 5: Introduction

5
Software Engineering

## Slide 6: Introduction

The time and effort devoted to each activity in each iteration depends on the type of system being developed and the budget
Early in the process – more effort on understanding high level business, non-functional and user requirements
Later in the process – more effort on eliciting and understanding the non-functional requirements and system requirements
Spiral allows development in different levels of detail
Number of iterations can vary, and can exit spiral at any stage (once you think you have gathered sufficient, and sufficient level, of requirements)
6
Software Engineering

## Slide 7: Introduction

Sometimes, Agile development can be used instead of prototyping so that the requirements and the system implementation are developed together (feedback and refinement)
In virtually all systems, requirements change
  - People develop a better understanding of what they want
  - Organization buying the system changes
  - Modifications are made to the system’s hardware, software, and organizational environment
Changes must be managed to understand the impact on other requirements and the cost and system implications of making the change (we will look into this in requirements management)
7
Software Engineering

## Slide 8: Business Requirements Specification??Example

A Business Requirement Specification (BRS) is like defining the vision and goals for the Student Portal before getting into technical details
It answers the big questions
It answers:
  - Why is the system needed? (To improve efficiency in student services)
  - Who benefits? (Students, professors, administrators)
  - What should the system do? (Provide self-service, course management, messaging, etc.)
8
Software Engineering

## Slide 9: Feasibility study

Technical feasibility:
  - Can it be developed using existing technology
    - Does the university (or business) have the necessary hardware/software infrastructure?
    - Are the proposed features (e.g., AI-based student score predictions) technically achievable?
    - Can existing university databases integrate with the new portal?
Economic feasibility (Cost-benefit analysis):
  - Is the project financially practical?
    - What is the estimated budget for development and maintenance?
    - Will the benefits (e.g., improved efficiency, reduced manual work) outweigh the costs?
    - Can the university afford the necessary infrastructure upgrades?
9
Software Engineering

## Slide 10: Feasibility study

Legal and Compliance:
  - Does the system comply with relevant laws and regulations? (data storage and privacy laws, for example)
Operation feasibility:
  - Will users (students, professors, administrators) accept and use the system?
    - How will students register and access their courses?
    - Will professors be comfortable with online grading and communication?
    - Will training be needed for users?
Schedule feasibility:
  - Can the system be developed within the given time frame?
    - How long will it take to build, test, and deploy?
    - Are there critical deadlines (e.g., before the next semester begins)?
10
Software Engineering

## Slide 11: Requirements Elicitation

Aim:
  - Understand the new system needed / wanted
  - Understand the stakeholder work (needed for the following point)
  - How the new system will support/ improve the work
Software Engineers work with stakeholders to find out:
  - Application domain (where the application is to be used – university, hotel, etc.)
  - Work activities (general everyday tasks at work-place, some involve existing system, some manual)
  - Services and System features needed (functional requirements)
  - Required performance (non-functional requirements)
  - Hardware constraints
11
Software Engineering

## Slide 12: Requirements Elicitation

Challenges (of eliciting requirements from stakeholders):
  - Stakeholders do not know what they want from the system (except in most general terms)
  - Stakeholders express requirements in their own way (and with their own implicit knowledge of their own work)
  - Different stakeholders express requirements in different ways (requirements engineers then must check for commonality and resolve conflict)
  - The economic and business environment in which the analysis takes place is dynamic (importance and priority of requirements may change, new requirements may emerge)
12
Software Engineering

## Slide 13: Requirements Elicitation challenges - Examples

13
Software Engineering
#1: Stakeholders don't know what they want (except in general terms)
"We need a system where students can register for courses"
Can they edit (add/ drop)? Prerequisites? What if some course is full? Are there limits?
#2: Stakeholders express requirements in their own way (with own implicit knowledge)
"We need a system that supports a curved grading policy." - Professor X
What is curved – bell curve? Linear scaling? Professor assumes everyone understands grading policy, and is on the same grading policy
#3: Different stakeholders express requirements in different ways
Students want an easy way to reset forgotten passwords via email.
IT security staff want a strict, multi-step authentication process to prevent hacking.
#4: The economic and business environment in which the analysis takes place is dynamic
The system should support credit and debit card payments.
Within 6 months, market trends indicate the usage of UPI. Somewhere down the line, cryptocurrency starts becoming prevalent, need to incorporate all these changes

## Slide 14: Requirements Elicitation

14
Software Engineering

## Slide 15: Requirements Elicitation

Requirements discovery and understanding: This is the process of interacting with stakeholders of the system to discover their requirements
Requirements classification and organization: This activity takes the unstructured collection of requirements; groups related requirements and organizes them into coherent clusters.
15
Software Engineering

## Slide 16: Requirements Elicitation

Requirements prioritization and negotiation: Inevitably, when multiple stakeholders are involved, requirements will conflict. This activity is concerned with prioritizing requirements and finding and resolving requirements conflicts
Requirements documentation: The requirements are documented and input into the next round of the spiral. An early draft of the software requirements documents may be produced
16
Software Engineering

## Slide 17: Requirements Elicitation Techniques

Requirements elicitation involves meeting stakeholders (of different kinds) to discover information about the proposed system
This can be supplanted with knowledge of existing systems and information from documents
Two fundamental approaches to elicit requirements:
  - Interviewing – talk to people about what they do
  - Observation or Ethnography – watch people at their job
You should use a mix of interviewing and observation – thereby derive requirements – which is then the basis for further discussion / work
17
Software Engineering

## Slide 18: Interviewing

Formal and/or informal interviews with system stakeholders
Puts questions to stakeholders about the system they currently use and the system to be developed
Interviews are of two types:
  - Closed: Stakeholders answer a predefined set of questions
  - Open: No predefined agenda. Requirements engineering team explore a range of issues with stakeholders to understand the needs
Interviews with stakeholders are normally a mixture of both
Completely open ended usually do not work well, ask some questions to get started and keep the focus
18
Software Engineering

## Slide 19: Interviewing

Interviews are useful, however, unless you have a prototype, it is hard to expect stakeholders to provide specific and detailed requirements
Eliciting domain knowledge can be difficult:
  - Application specialists use jargon specific to their work
  - Some domain can be so familiar that stakeholders find it either difficult to explain or think of it as so fundamental or commonsense that they do not mention it
Interviews are also not effective when trying to elicit knowledge about organizational requirements and constraints (subtle power relationships might exist, people might follow processes that are not explicitly mentioned on paper)
People are generally reluctant to discuss political and organizational issues
19
Software Engineering

## Slide 20: Interviewing

To be an effective interviewer:
  - You should be open-minded, avoid preconceived ideas about the requirements
  - Prompt the interviewee by using spring-board questions (open ended questions that stimulate thinking), or by using something akin to a prototype ("tell me what you want" does not usually work)
Therefore, information from interviews is used along with other information from documentation describing business processes, user observations and developer experience.
20
Software Engineering

## Slide 21: Spring-board questions: examples

What problems do you currently face with the existing system?
Can you walk me through a typical day using the current process?
What frustrates you the most?
What happens when something goes wrong?
If this system failed, what would be the biggest impact?
21
Software Engineering

## Slide 22: Ethnography

Software systems do not exist in isolation
Used in a social and organizational setting, and therefore, requirements maybe generated or constrained by the environment
"Ethnography is an observational technique that can be used to understand operational processes and help derive requirements for software to support these processes"
A requirements engineer will immerse their selves in the working environment to observe and understand
Ethnography therefore helps discover implicit system requirements (your organizational non-functional requirements) - reflecting the way the people work in reality, rather than the formal process on paper
22
Software Engineering

## Slide 23: Okay, let us use an example to understand the previous slide better

23
Software Engineering
Systems do not exist in isolation:The system is not just a barcode scanner
It is used in supermarkets who might have policy for phone usage, and with sometimes limited connectivity. Therefore, it has to deal with store policy, and work gracefully in poor internet connection.
Used in a social and organizational setting:
Crowded stores, cashier in a hurry, response time should be fast.
Role of Ethnography:
Instead of asking "would you use sustainability ratings?"
Observe users in the supermarket (in a non-creepy way) to understand how they behave. You visit a supermarket and observe shoppers, how they pick products, whether they even read labels, do they spend time comparing products?
Immersing in the work environment – check customers, maybe speak to a couple of them, speak to the cashier, etc.

## Slide 24: Ethnography

Ethnography is particularly effective for discovering two types of requirements:
  - Requirements derived from the way in which people actually work
  - Requirements derived from cooperation and awareness of other people’s activities
Ethnography can be combined with the development of a system prototype (ethnography informs development of prototype so fewer prototype cycles are needed)
Ethnography is helpful to understand existing systems, but this understanding does not always help with innovation. Innovation is particularly relevant for new product development (Nokia vs. Apple)
24
Software Engineering

## Slide 25: Ethnography, Stories and Scenarios

Ethnography is a research method, while stories and scenarios are tools used to describe findings from ethnographic studies
Comparison:
  - Ethnographic research: Observing real users in their actual environment to understand their behaviors, culture, and workflows (provides rich information of how people interact with systems)
  - Story: Narratives that describe real or hypothetical user experiences (helps makes ethnographic finding more relatable and easier to communicate)
  - Scenario: Hypothetical situations that describe how a system will be used in real life (this ensures system meets user needs)
25
Software Engineering

## Slide 26: Ethnography, Stories and Scenarios

Ethnography is a research method, while stories and scenarios are tools used to describe findings from ethnographic studies
Student portal example:
  - Ethnographic research: A researcher observes how students currently register for courses, take notes on the difficulties they face, and interviews them about their frustrations
  - Story: "XYZ, a third-year student, logs into the student portal to register for courses. The system crashes just as he selects his final course, and he must start over. Frustrated, he tries again late at night when fewer students are online."
  - Scenario: See next slide
26
Software Engineering

## Slide 27

27
Software Engineering
Scenario Name: Peak-Time Course Enrollment
Primary Actor: Student
Precondition:
Registration portal is open.
Thousands of students are logged in simultaneously.
Main Flow of Events:
Student logs into the Student Portal.
Student navigates to the Course Registration page.
Student selects desired elective courses.
Student clicks “Enroll.”
The system processes the enrollment request.
The system confirms successful registration within 2 seconds.
The updated course list is displayed to the student.
System Behavior Requirements (Implicit in Scenario):
The system must support high concurrent users (e.g., 5000+).
The system response time must remain under acceptable limits (e.g., ≤ 2 seconds).
The system must not crash or freeze.
No data inconsistency should occur.
Postcondition:
Student is successfully enrolled in selected courses.
Database records are updated correctly.
System remains operational for other users.

## Slide 28: Stories and Scenarios

Real-life examples are easier to relate than abstract descriptions
People might not be able to tell you system requirements, however, they might find it easier to describe how they handle a particular situation or imagine things they might do on a new system
Stories and scenarios capture this kind of information
"Stories and scenarios are essentially the same" (description of how the system can be used for a particular task) – what people do, what information they use and produce, what systems they use in this process
Difference – Stories are written as narrative text (high-level description), Scenarios are usually structured with specific information
28
Software Engineering

## Slide 29: Stories and Scenarios

Stories can be thought of as setting out the "big picture", and then parts of stories can then be developed in more detail and represented as scenarios
29
Software Engineering

## Slide 30: Story

These stories can then be shared as a wiki or something to get feedback from a wider range of stakeholders
Useful to get information from a wider community than we could realistically interview
These high-level stories do not go into detail about a system, but they can be developed into more specific scenarios. Scenarios are descriptions of example user interaction sessions
30
Software Engineering

## Slide 31: Scenario

A scenario starts with an outline of the interaction
A scenario may include:
  - A description of what the system and users expect when the scenario starts
  - A description of the normal flow of events in the scenario
  - A description of what can go wrong and how resulting problems can be handled
  - Information about other activities that might be going on at the same time
  - A description of the system state when the scenario ends
31
Software Engineering

## Slide 32: Scenario: Example (Textbook)

32
Software Engineering

## Slide 33: Scenario: Example

Check the Additional handout that goes along with this week's lecture
Scenario Example.docx
33
Software Engineering

## Slide 34

Requirements Specification
34
Software Engineering

## Slide 35: Recap

We covered the various ways in which Requirements can be specified in the previous Lecture (refer Lecture 5)
In the following couple of slides, we present, in brief, candidate structure for the SRS
Note that the IEEE 830 – 1998 standard for the SRS allows room for customization (in certain sections of the document), and merely proposes an outline (which you will see in the following slides)
35
Software Engineering

## Slide 36: Software Requirements Specification (PRE., pg. 136)

36
Software Engineering

## Slide 37: Software Requirements Specification – IEEE 830(Hans Van Vliet, pg. 231)

37
Software Engineering

## Slide 38: Software Requirements Specification – IEEE 830(Hans Van Vliet)

Refer pg. 232 to pg.234 for a brief example of the fields of the SRS (using a library system)
38
Software Engineering

## Slide 39

Requirements Validation
39
Software Engineering

## Slide 40: Introduction

"Process of checking that requirements define [capture the essence of] the system that the customer really wants"
Essence – meets customer expectations and goals, apart from being clear and feasible
Can overlap with elicitation and analysis, as it is concerned with finding problems with the requirements
Critically important since errors in requirements document can lead to extensive rework
40
Software Engineering

## Slide 41: Checks in Requirements validation

Validity checks: These check that the requirements reflect the real needs of system users
Consistency checks: Requirements in the document should not conflict
Completeness checks: The requirements document should include requirements that define all functions and the constraints
Realism checks: (by using knowledge of existing tech.,) ensure that system can be implemented in time and budget constraints
Verifiability: System requirements should always be written so that they are verifiable
41
Software Engineering

## Slide 42: Checks in Requirements validation - Example

Validity Check:
  - Does the student portal actually help students register for courses in a way that matches their real needs and expectations? (simply: does it do what it is supposed to do)
Consistency Check:
  - If one requirement states that students can reset their password via email, another requirement should not say that password resets are only possible through the IT helpdesk
Completeness Check:
  - The student portal requirements should include course registration, fee payment, grade viewing, and any necessary constraints (e.g., prerequisite enforcement)
Realism Check:
  - A requirement that says "The student portal should process 1 million registrations per second" is unrealistic given the university’s current infrastructure and budget
Verifiability Check:
  - The system should allow students to reset their password within 5 minutes of requesting a reset link (this can be tested and measured)
42
Software Engineering

## Slide 43: Requirements validation techniques

Requirements reviews: The requirements are analyzed systematically by a team of reviewers who check for errors and inconsistencies
Prototyping: This involves developing an executable model of a system and using this with end-users and customers to see if it meets their needs and expectations (stakeholders use prototype and feedback changes to requirements, if any)
Test-case generation: Requirements should be testable. If the tests for the requirements are devised as part of the validation process, this often reveals requirements problems. If a test is difficult or impossible to design, this usually means that the requirements will be difficult to implement and should be reconsidered. Developing tests from the user requirements before any code is written is an integral part of test-driven development.
43
Software Engineering

## Slide 44: How does test case generation help with requirements validation?

Confirms Functional Coverage
  - Each test case is designed based on a requirement. One to one mapping. If test cases cover all requirements, it confirms that the system meets the intended functionality.
Identifies Missing or Ambiguous Requirements
  - If a test case cannot be created for a requirement, it may indicate ambiguity or missing details.
  - Example: If a requirement states, "The system should allow users to reset their password," but does not specify constraints (e.g., password complexity rules), test case generation will highlight this gap.
Detects Incorrect or Conflicting Requirements
  - If a test case fails, it could mean the requirement is incorrect, unrealistic, or conflicting with another requirement.
  - Example: One requirement says, "Users must be logged in to view reports," but another says, "Users can access reports without logging in." Test cases will reveal this inconsistency
  - Example: One requirement says, "Students must be able to register for any course at any time, without any restrictions." Here the test case might reveal that the requirement is incorrect since universities allow registration at start of semester
44
Software Engineering

## Slide 45: How does test case generation help with requirements validation?

Ensures Testability of Requirements
  - If a requirement cannot be tested, it may be too vague or non-measurable.
  - Example: "The system should be user-friendly." This is subjective and cannot be directly tested, so it needs clearer criteria like "The system should load within 2 seconds."
Validates Business Logic and User Scenarios
  - Test cases simulate real-world usage to check if the system aligns with business needs and user expectations
  - Example: A test case simulates students accessing their grades to verify that only authorized students can view them, or only authorized professor(s) can assign and publish grades. This way, the test case ensures that business logic and user scenarios are satisfied
45
Software Engineering

## Slide 46

Requirements Management
46
Software Engineering

## Slide 47: Introduction

The requirements for large software systems are always changing
Due to "wicked" problems - problems that cannot be completely defined (example in next slide)
During the software development process, the stakeholders’ understanding of the problem is constantly changing
Once a system has been installed and is regularly used, new requirements inevitably emerge (sometimes this is due to omission in original requirements) - oft stated gaming example in class
Also, changes to system requirements may also arise because of changes to the business environment (see slide 49)
47
Software Engineering

## Slide 48: Feeling a little … wicked

Requirement: "A university wants to implement a Dynamic Student Feedback System in a university portal"
Hard to define! Why? Student expectations, faculty preferences, university policies are evolving
  - Initially – End of semester feedback
  - Then – students request removal of forced feedback (having to provide feedback for profs who do not teach them)
  - Then – Some course faculty consider real-time mid semester feedback
  - Then – Administration says bias and misuse might happen with dynamic feedback (but then faculty says no problem, we will have moderation)
  - Then – Admin says why not have AI based sentiment analysis, but privacy regulations come in the way (can you really take something shared discreetly and in privacy and feed it to a system?)
These shifting needs make it difficult to finalize a stable set of requirements, leading to continuous modifications in the system
48
Software Engineering

## Slide 49: Changes in Business Environment

The business and technical environment of the system always changes after installation. New hardware may be introduced and existing hardware updated (new OS has packages which are incompatible with software). Business priorities may change (use cisco webex instead of messenger)
The people who pay for a system and the users of that system are rarely the same people
Large systems usually have a diverse stakeholder community, with stakeholders having different requirements
49
Software Engineering

## Slide 50: Requirements Management

As requirements are evolving, you need to keep track of individual requirements and maintain links between dependent requirements so that you can assess the impact of requirements changes
Requirements management: "Formal process for making change proposals and linking these to system requirements"
This process of “requirements management” should start as soon as a draft version of the requirements document is available
In many cases, users prioritize change
Users are not necessarily the best people to decide if the change is worth it (cost effective)
Therefore, independent authority, who balances needs of all stakeholders, should decide on which changes need to be accepted
50
Software Engineering

## Slide 51: Requirements Management: Example

In a university portal
  - Initially - course registration system allows students to enroll in courses based on prerequisites
  - Then - university introduces a waitlist feature, requiring changes to enrollment logic (wait for a while before finalizing courses)
  - Then - administrators request automated prerequisite overrides for exceptional cases, impacting both the registration and waitlist modules
To manage these evolving requirements, developers maintain traceability links between related requirements, ensuring that changes in prerequisite handling do not break waitlist logic or grade verification rules. This tracking helps assess the impact of changes, preventing unintended disruptions in the system
51
Software Engineering

## Slide 52: Requirements Management Planning

Requirements management planning: Answers the question – how will you manage evolving requirements?
During the planning stage (within RE), decide on:
  - Requirements identification: Each requirement should have a unique ID so it can be tracked with respect to other requirements
  - Change management process: Set of activities that assess the impact and cost of changes (slide 55)
  - Traceability policies: Policies define the relationships between each requirement and between the requirements and the system design (slide 53)
  - Tool support: Since this task can get tricky, you can decide on what tools to use for automation support before starting requirements planning
52
Software Engineering

## Slide 53: Traceability policies

Help manage requirements changes by linking related features to ensure consistency
A well-defined traceability policy ensures that any modification in a requirement is tracked and assessed across all dependent requirements, preventing inconsistencies
Example policy: Use a traceability matrix
By maintaining traceability matrices, developers can evaluate the impact of the change
53
Software Engineering

## Slide 54: Example: From Grades to Pass / Fail

54
Software Engineering

## Slide 55: Change Management Process

Ensures that modifications to a system are evaluated, approved, and implemented without disrupting existing functionality
Three stages:
  - Problem Analysis and Change Specification: Problem or change proposal analyzed for validity. Might go back to requestor for more specific change request or dropping change request
  - Change Analysis and Costing: Effect assessed using traceability information. Cost in terms of changes to requirement document, design and implementation (if need be). At end of this phase, final call taken to go ahead with requirement change or not
  - Change implementation: Requirements document, and where necessary, design and implementation are modified (any project artefacts should be so made that changes do not incur extensive rewriting or reorganization)
55
Software Engineering

## Slide 56

Prioritizing Requirements
56
Software Engineering

## Slide 57: Introduction

In most cases, not all requirements can be realized, so we have to make a selection of requirements which need to be realized first / on priority
57
Software Engineering

## Slide 58: Triage

Triage in requirements prioritization refers to the process of evaluating, categorizing, and ranking requirements based on their importance, urgency, and feasibility—similar to how medical triage prioritizes patients based on the severity of their condition
Why triage?
  - Projects often have limited resources, time, and budget, so some requirements need to be fulfilled before others
  - Triage helps identify the most critical requirements to work on first
58
Software Engineering

## Slide 59: Triage – How it works

Critical (Must-Have) – These are essential for the system to function. Without them, the project fails or does not deliver its core value.
  - Example: A student portal must allow students to register for courses.
Important (Should-Have) – Highly desirable but not immediately essential. These can be added in later phases or releases.
  - Example: A student portal should allow students to receive notifications when a waitlisted course becomes available.
Optional (Nice-to-Have) – Enhancements that improve user experience, not urgent/ critical, can be postponed or removed
  - Example: A chatbot assistant for answering student FAQs within the portal.
59
Software Engineering

## Slide 60: Triage – Example using student portal

60
Software Engineering

## Slide 61: MoSCoW (Hans Van Vliet, pg. 226)

Distinguishes four types of requirements:
  - Must haves: These are top priority requirements (ones that definitely need to be realized in order to make system acceptable to customer)
  - Should haves: Not strictly mandatory (but highly desirable) - important but not show stoppers
  - Could haves: If time allows, these requirements will be realized (in practice, they usually won't) - desirable but low priority
  - Won't haves: These requirements will not be realized in the present version (they are recorded though. They will/ might be considered again for a next version of the system) - low value, high cost (in terms or time or budget)
"MoSCoW assumes that requirements can be ordered along a single axis, and that realizing more requirements yields more satisfied customers (reality is more complex)" - this is where Kano comes
61
Software Engineering

## Slide 62: MoSCoW: In simpler terms

Distinguishes four types of requirements:
  - Must haves: Essential requirements; system will fail without them
  - Should haves: Important but not critical; workaround may exist
  - Could haves: Desirable features if time permits
  - Won't haves: Not included in the current version
Example:
62
Software Engineering

## Slide 63: How to prioritize using MoSCoW?

List all requirements
  - Identify key features & functions
Assess impact & dependencies
  - Can the system work without it?
Categorize each requirement
  - Based on business needs & feasibility
Get stakeholder agreement
  - Ensure alignment with all (most) stakeholders
Adjust based on project constraints
  - Budget, time, and resources.
63
Software Engineering

## Slide 64: Kano model (Hans Van Vliet, pg. 226)

Preferences classified into five categories:
  - Attractive: More satisfied if these requirements are met, but not less satisfied if they are not
  - Must-be: Will be dissatisfied if these requirements are not met (but will not be overly happy if they are met)
  - One-dimensional: Satisfaction is proportional to how many of these requirements are being met
  - Indifferent: Customer does not really care about these requirements
  - Reverse: Customer's judgement of the requirements is the opposite of what the analyst thought a priori
  - Questionable: Customer's preferences are not clear
64
Software Engineering

## Slide 65: Kano model (Hans Van Vliet, pg. 226)

65
Software Engineering
The way customers value the Attractive,
Must-be and One-dimensional categories of requirements is depicted in figure.
This figure shows that offering attractive, so called killer features, is what will really excite your customers.
"Our task is not to provide every button and pull-down menu enhancement that our
customers ask for, but to invent a completely new way of working -- one that will thrill and amaze them." - (Robertson, 2002)

## Slide 66: Kano (put another way)

Focuses on customer satisfaction rather than just importance
Think of it this way:
Satisfaction behavior:
66
Software Engineering

## Slide 67: Kano (example – student portal)

Basic Requirement
  - Student must be able to login
Performance Requirement
  - Faster login response time
Excitement Requirement
  - AI assistant suggesting courses
67
Software Engineering

## Slide 68: Comparison of the three models

68
Software Engineering

## Slide 69: Which model to choose?

69
Software Engineering
Based on stakeholder involvement
Rule of thumb
Based on Project Type
Based on goal

## Slide 70: Further reading / browsing (if interested)

NLP for Requirements Engineering (NLP4RE) - ACM Journal Survey Article
Summary of the first workshop of NLP4RE - IEEE Journal
Requirements elicitation using Generative AI based NLP tools – Conference Article
Requirements Engineering – Springer Journal
70
Software Engineering
