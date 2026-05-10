# Software Engineering - Lecture 4.2

## Slide 1: Software Engineering(CS3201)Software Requirements

Avinash

## Slide 2: Introduction

The Requirements for a system are the descriptions of the services that a system should provide and the constraints on its operation
Requirements reflect the needs of customers
The process of finding out, analyzing, documenting and checking (the feasibility) of these services and constraints is called requirements engineering (RE)
The term 'requirement' is not used consistently in the industry
  - Sometimes, it is a high-level, abstract statement of service
  - Other times, it can be a detailed and formal definition of a system function
Both these types of requirement specification may be the 'Requirements document' for a system
These two types of requirements are distinguished using the terms user requirements and system requirements
2
Software Engineering

## Slide 3: User Requirements and System Requirements

User Requirements
User requirements are statements, in a natural language plus diagrams, of what services the system is expected to provide to system users and the constraints (under which it should operate)
System Requirements
  - System requirements are more detailed descriptions of the software system’s functions, services, and operational constraints. The system requirements document (sometimes called a functional specification) should define exactly what is to be implemented
Different kind of requirements are needed for different kinds of readers (Customers and managers speak one language, dev other)
3
Software Engineering

## Slide 4: Example: User and System Requirements

4
Software Engineering

## Slide 5: Example 2: User and System requirements (Sustainable shopping app)

5
Software Engineering
User Requirements
1. Barcode Scanning: The user should be able to scan a product barcode and see its sustainability rating.
2. Sustainability Information: The user should be able to see environmental impact details of a product (carbon footprint, recyclability, ethical sourcing).
3. Eco-Friendly Alternatives: The app should suggest more sustainable alternatives for scanned products.
4. Bill Analysis: The user should be able to upload or scan a supermarket bill and get an ecological footprint summary.
5. Personal Impact Tracking: The user should be able to track their sustainability score over time.
System Requirements
Barcode Scanning:
SR1.1: The system shall allow users to scan EAN-13 and UPC-A barcodes using the mobile device camera.
SR1.2: The system shall retrieve product data from the sustainability database within 3 seconds of a successful scan.
SR1.3: If the barcode is not found, the system shall display “Product not available in database.”
Sustainability information:
SR2.1: The system shall display:
Carbon footprint (kg CO₂ equivalent per unit)
Packaging recyclability percentage
Ethical sourcing score (1–10 scale)
SR2.2: The system shall show a sustainability rating on a 0–100 scale.

## Slide 6: System stakeholders

The different types of document readers (managers, clients, developers, etc.) are examples of system stakeholders
System stakeholders include anyone who is affected by the system in some way and so anyone who has a legitimate interest in it or is impacted by it
6
Software Engineering

## Slide 7: Example: Stakeholders for Mentcare

Patients whose information is recorded and relatives of these patients
Doctors who are responsible for assessing and treating patients
Nurses who coordinate the consultations with doctors and administer some treatments
Medical receptionists who manage patients’ appointments
IT staff who are responsible for installing and maintaining the system
A medical ethics manager who must ensure that the system meets current ethical guidelines for patient care (confidentiality, informed consent, etc.)
Health care managers who obtain management information from the system
Medical records staff who are responsible for ensuring that system information can be maintained and preserved, and that record keeping procedures have been properly implemented
7
Software Engineering

## Slide 8: Example: Stakeholders for Sustainable Shopping App

End users/ app users  who install and use the app (primary stakeholders)
Supermarkets who integrate their catalog with the app
Sustainability data providers who provide sustainable ratings data
App owners/ Product team who designed the app
Technology providers who provide third party bar code scanning API
Advertisers & partners who showcase their sustainable products using our app
Society and environment who are benefited by people using the app (these are the indirect stakeholders)
8
Software Engineering

## Slide 9: Requirements Engineering

Requirements engineering is usually presented as the first stage of the software engineering process
Before committing to system development, a preliminary understanding of requirements is needed to form a high-level view of system functionality and benefits, enabling informed decision-making about feasibility and investment.
These may then be considered in a feasibility study, which tries to assess whether or not the system is technically and financially feasible
Help decide whether to procure or develop (or drop) the system
9
Software Engineering

## Slide 10: Requirements Engineering - breakdown

Understand the Needs → Talk to users & stakeholders to know what they want
Define Requirements → Clearly describe what the system should do
Check Feasibility → Ask whether requirements are realistic & achievable?
Document Everything → Write down the requirements in a structured way
Manage Changes → Update requirements if needs change during development (even waterfall allows change, but change is controlled, expensive, formal and time consuming)
10
Software Engineering

## Slide 11: Feasibility Studies

"A feasibility study is a short, focused study that should take place early in the RE process. It should answer three key questions: (1) Does the system contribute to the overall objectives of the organization? (2) Can the system be implemented within schedule and budget using current technology? and (3) Can the system be integrated with other systems that are used? If the answer to any of these questions is no, you should probably not go ahead with the project."
Sommerville (Software Engineering, web sections) - feasibility study
11
Software Engineering

## Slide 12

Functional and Non-functional Requirements
12
Software Engineering

## Slide 13: Introduction

Software system requirements are often classified as functional or non-functional requirements
  - Functional Requirements: These are statements of services the system should provide, how the system should react to particular inputs, and how the system should behave in particular situations. In some cases, the functional requirements may also explicitly state what the system should not do
  - Non-functional Requirements: These are constraints on the services or functions offered by the system. They include timing constraints, constraints on the development process, and constraints imposed by standards. Non-functional requirements often apply to the system as a whole rather than individual system features or services
13
Software Engineering
