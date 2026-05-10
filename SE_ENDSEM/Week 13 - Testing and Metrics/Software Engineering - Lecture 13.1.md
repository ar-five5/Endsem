# Software Engineering - Lecture 13.1

## Slide 1: Software Engineering(CS3201)Software Testing

Avinash

## Slide 2: Objectives

Understand the different stages of testing from 'testing during development' to 'acceptance testing by system customers': Done
Understand techniques to help choose test cases: Done
Understand 'Test First Development': Done
Understand Component testing, System testing and Release testing
2
Software Engineering

## Slide 3: Recap

Refer Software Engineering – Lecture 12.1
3
Software Engineering

## Slide 4

Release Testing
4
Software Engineering

## Slide 5: Release Testing

Testing a particular 'release' of a system that is intended for use outside the development team
Generally, release is for customers / users
In complex projects, release can be for other development teams that are developing related software, or using your system as part of a larger project
Primary goal: Convince the supplier of system that it is good enough to be released as product or delivered to customer
Usually, black box testing where tests are derived from system specs
Another name is functional testing since the tester is only concerned with functionality and not implementation
5
Software Engineering

## Slide 6: Release Testing

Types
  - Requirements-based testing
  - Scenario testing
  - Performance testing
6
Software Engineering

## Slide 7: Requirements based testing

Remember good practice of requirements engineering? The requirements should be testable
Requirements based testing is an approach to test-case design where you consider each requirement and derive a set of tests for it
It is validation rather than defect testing
It is not necessary to have a 1:1 mapping between a requirement and a test case, you normally have to write several test cases to ensure coverage of a requirement
Good practice – Keep traceability records which link tests to specific requirements
7
Software Engineering

## Slide 8: Requirements based testing: Example

Mentcare system requirements:
  - If a patient is known to be allergic to any particular medication, then prescription of that medication shall result in a warning message being issued to the system user.
  - If a prescriber chooses to ignore an allergy warning, he or she shall provide a reason why this has been ignored
8
Software Engineering

## Slide 9: Requirements based testing: Example

Corresponding tests for requirements in previous slide:
  - Set up a patient record with no known allergies. Prescribe medication for allergies that are known to exist. Check that a warning message is not issued by the system
  - Set up a patient record with a known allergy. Prescribe the medication that the patient is allergic to and check that the warning is issued by the system
  - Set up a patient record in which allergies to two or more drugs are recorded. Prescribe both of these drugs separately and check that the correct warning for each drug is issued
  - Prescribe two drugs that the patient is allergic to. Check that two warnings are correctly issued
  - Prescribe a drug that issues a warning and overrule that warning. Check that the system requires the user to provide information explaining why the warning was overruled
9
Software Engineering

## Slide 10: Scenario testing

Devise typical usage scenarios and then develop test cases using these scenarios
Scenario is a story which describes one way in which system might be used
Scenarios must be realistic (credible), and should be easy to evaluate
10
Software Engineering

## Slide 11: Scenario testing: Example

11
Software Engineering

## Slide 12: Scenario testing: Example

The previous scenario tests a lot of features of the system:
  - Authentication by logging on to the system
  - Downloading and uploading of specified patient records to a laptop
  - Home visit scheduling
  - Encryption and decryption of patient records on a mobile device
  - Record retrieval and modification
  - Links with the drugs database that maintains side-effect information
  - The system for call prompting
12
Software Engineering

## Slide 13: Scenario testing: Example

If you are a release tester, you run through this scenario, playing the role of George and observing how the system behaves in response to different inputs
You may make deliberate mistakes (inputting the wrong key phrase to decode records, ...). This checks the response of the system to errors
Carefully note any problems that arise, including performance problems. If a system is too slow, this will change the way that it is used (example: if it takes too long to encrypt a record, then users who are short of time may skip this stage; if they then lose their laptop, an unauthorized person could then view the patient records)
In this approach, you are (usually) testing several requirements within the same scenario. Therefore, as well as checking individual requirements, you are also checking that combinations of requirements do not cause problems
13
Software Engineering

## Slide 14: Performance testing

Now that you have a complete system, you can also test for emergent properties, like performance and reliability
These tests ensure that the system can process its intended load
Involves running a series of tests while increasing load until the performance becomes unacceptable
Operational profile is a set of tests that reflect the actual nature of work the system performs (in other words, the relative frequency of the different operations the system performs). The goal is to simulate actual usage conditions and test appropriately (if task A is performed 90% of the time, test it the most)
Some say operational profile testing is not the best approach, and instead perform stress testing
  - Particularly relevant in network or distributed environments
  - Helps understand when degradation begins so you can add checks to proactively tackle it
14
Software Engineering

## Slide 15

User Testing
15
Software Engineering

## Slide 16: User Testing

Stage where users/ customers provide input on system testing
Can be formal or informal
User testing is essential, the user's working environment can have a major effect on the system's reliability, performance, usability and robustness
It is practically impossible for a developer to recreate the user's environment, and therefore user testing is necessary
Three types of User testing:
  - Alpha testing
  - Beta testing
  - Acceptance testing
16
Software Engineering

## Slide 17: Alpha testing

Selected group of software users work closely with the development team to test early software releases
Users and developers work together while the system is being developed
Generally used when developing software products or apps, but can also be used when developing custom software
Agile methods advocate user involvement early in the development process
17
Software Engineering

## Slide 18: Beta testing

Release of the software is made available to a larger group of users to allow them to experiment and to raise problems that they discover
Beta testers may be a selected group of customers who are early adopters of the system
Alternatively, it can also be made available to the public
Beta testing is mostly used for software products that are used in many different settings
18
Software Engineering

## Slide 19: Acceptance testing

Inherent part of custom system development
Customers test a system, using their own data, and decide if it should be accepted from the system developer
Acceptance implies that final payment should be made for the software
Six stages to acceptance testing process:
  - Define acceptance criteria
  - Plan acceptance testing
  - Derive acceptance tests
  - Run acceptance tests
  - Negotiate test results
  - Reject / Accept system
19
Software Engineering

## Slide 20: Difference between Beta testing and Acceptance testing

Beta testing focuses on identifying bugs and gathering feedback from a wider, more representative group of users in a real-world environment
Acceptance testing, on the other hand, is a more structured process where specific acceptance criteria are validated to ensure the product meets requirements before release
20
Software Engineering
