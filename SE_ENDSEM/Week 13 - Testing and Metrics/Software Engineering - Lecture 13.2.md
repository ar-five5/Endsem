# Software Engineering - Lecture 13.2

## Slide 1: Software Engineering(CS3201)Product and Process Metrics

Avinash

## Slide 2: Objectives

Brief introduction on Product metrics
Brief introduction on Process metrics
2
Software Engineering

## Slide 3

Product Metrics
3
Software Engineering

## Slide 4: Introduction

Metrics help quantify software quality attributes like reliability, maintainability, usability, and performance
Without metrics, subjectivity and bias creep in
Can make better decisions on release readiness, maintenance
Metrics like cyclometric complexity can help find out issues early in the work cycle (helps find out complex code – less readable, less maintainable, more prone to errors)
Metrics like LOC help predicting effort and cost (remember COCOMO?)
Metrics, in short, turn subjective analysis into actionable insights
4
Software Engineering

## Slide 5: Software Quality Metrics

These assess the overall quality of the software
  - Functionality: Feature completeness, correctness, interoperability
    - Defined by ISO/IEC 25010
    - Completeness – Requirements coverage (%); Correctness – Passed functional test cases (%); Interoperability – Interface Compatibility (%) = (Interfaces Working Correctly / Total Interfaces) × 100, Standards Compliance Rate (%) = (Supported Standards / Required Standards) × 100
  - Reliability: Mean Time Between Failures (MTBF), failure rate, system uptime
    - MTBF = Total operating time / number of failures
    - Failure Rate = No. of failures / total time of operation (or system uptime)
  - Usability: Time to learn, user error rate, user satisfaction score
    - Time to learn – how to make it objective?
    - Time to learn – define proficiency goal ("view Grades using JUNO"), select representative new users, use screen recordings and time tracking tools to see how much time users take for the task, calculate average time to perform task across all tested users
    - User Satisfaction Score – Use a likert scale (1 to 5) or Net promoter scale (0 to 10), measure ratings give across scale (example: In survey, 60 chose 5, 20 chose 4, 10 chose 3, 10 chose 2 and 0 chose 1 – then USS = (60+20)/100)
5
Software Engineering

## Slide 6: Software Quality Metrics

These assess the overall quality of the software
  - Efficiency: Response time, throughput, CPU/memory usage
    - You have seen these in Operating Systems course
  - Maintainability: Cyclomatic complexity, modularity, ease of change
    - Cyclometric complexity = E – N + 2  (or) number of decision nodes + 1
    - Modularity – number of modules, fan in and fan out
    - Fan in: Number of modules that call or depend on a particular module
    - Fan out: Number of modules that a given module calls (or depends on)
  - Portability: Installation success rate, adaptability across platforms
    - Defined under ISO/IEC 25010
    - Success Rate = number of successful installations/total installation attempts
    - Adaptability across platforms = platforms successfully deployed on/targeted platforms
    - What is a platform? A combination of OS (Linux, Windows, …), device type (Laptop, Smartphone, …), architecture (x86, x64, ARM), browser environment (Chrome, Firefox, …), runtime environment (JavaVM, .NET, Node.js,…)
6
Software Engineering

## Slide 7: Metrics for Analysis Models

Used during the requirements and analysis phase to measure complexity and correctness
  - Function Points (FP): Measures the size of software based on inputs, outputs, files (accessed to get the task done) - why am I showing a code based ex.?
7
Software Engineering
# Simple login function
def login(username, password):
stored_users = {"alice": "pass123", "bob": "qwerty"}
if username in stored_users and stored_users[username] == password:   return "Login Successful"
else:        return "Invalid Credentials"
External Input (EI): Username and Password – Count (1); Complexity (Low); Weight (3)
External Output (EO): Messages returned – Count (1); Complexity (Low); Weight (4)
Internal logic file (ILF): Stored user credentials – Count (1); Complexity (Low); Weight (7)
Unadjusted Function Points (UFP) = (1*3)+(1*4)+(1*7) = 14
Note: Weights are assigned on the basis of the type of component

## Slide 8: Metrics for Analysis Models

Used during the requirements and analysis phase to measure complexity and correctness
  - Use Case Metrics: Estimate software size, effort and complexity based on use cases
    - Number of actors
    - Number of use cases
    - Number of interactions
  - Requirements Stability Index: Measures how often requirements change over time
  - Completeness and Consistency: Checks for missing, ambiguous, or contradictory requirements
8
Software Engineering

## Slide 9: Metrics for Design Models

These assess the quality of Software design (architecture and UML)
  - Design Size: Total number of classes/modules
  - Fan-In / Fan-Out: Number of modules calling (fan-in) and called by (fan-out) a given module
  - Cohesion (LCOM - Lack of Cohesion of Methods): Measures how related the methods of a class are
    - LCOM = No. of method pairs that do not share data – no. of method pairs that share data
    - Method pairs? Two methods are pairs if they operate on same set of attributes
  - Coupling (CBO - Coupling Between Objects): Indicates dependency between classes
    - CBO = Number of classes that a class is coupled with (coupled with? Means relies on other class)
  - Depth of Inheritance Tree (DIT): Measures the inheritance levels of a class
  - Number of Children (NOC): Measures the number of subclasses a class has
9
Software Engineering

## Slide 10: Metrics for Source Code

These evaluate the source code itself, post implementation
  - Lines of Code (LOC): Total number of lines in the source code.
  - Comment Density: Ratio of comment lines to total code lines.
  - Cyclomatic Complexity: Number of independent paths through the code (lower is better)
  - Halstead Metrics:
    - Program length
    - Vocabulary
    - Volume
    - Effort
  - Code Churn: Number of lines added, changed, or deleted over time
10
Software Engineering

## Slide 11: Metrics for Source Code

These evaluate the source code itself, post implementation
  - Halstead Metrics (example)
11
Software Engineering
// Sample code snippet
x = 10;  y = 20;
sum = x + y;
// Operators: =, +
// Operands: x, 10, y, 20, sum
// nₒ (Unique Operators) = 2 (=, +)
// nₑ (Unique Operands) = 5 (x, 10, y, 20, sum)
// Nₒ (Total Operators) = 4 (=, =, +, =)
// Nₑ (Total Operands) = 7 (x, 10, y, 20, sum, x, y)
// Now, based on these values, calculate things like program length = total operators + total operands, vocabulary = unique operators + unique operands, volume = program length * log2(vocabulary), difficulty = n0/2 * Ne/ne, Effort = volume * difficulty, time = effort/18

## Slide 12: Metrics for Testing

Used to assess the quality and effectiveness of testing process
  - Test Coverage:
    - Statement coverage
    - Branch coverage
    - Path coverage
  - Defect Density: Number of defects per 1,000 lines of code (KLOC)
  - Defect Removal Efficiency (DRE): Bugs fixed before release / Total bugs (pre + post release)
  - Test Case Effectiveness: % of test cases that successfully detect defects
  - Mean Time to Detect (MTTD): Average time to discover a defect after code deployment
    - Time deployed / defects discovered post deployment
  - Mean Time to Repair (MTTR): Average time taken to fix a defect
    - Total downtime / total software failures
12
Software Engineering

## Slide 13: Metrics for Maintenance

These help track the maintainability and performance of the system post deployment
  - Mean Time Between Failures (MTBF): Average time between failures
  - Change Request Frequency: Number of change requests received over time
  - Maintenance Effort: Total person-hours spent on bug fixes and updates
  - Rework Percentage: Proportion of total effort spent on redoing faulty code
13
Software Engineering

## Slide 14

Process Metrics
14
Software Engineering

## Slide 15: Introduction

Process metrics are quantitative measures used to evaluate how well the software development process is performing. They provide insights into productivity, quality, effort, time, and efficiency of the development activities
15
Software Engineering

## Slide 16: Importance

Process Improvement: Identify bottlenecks and inefficiencies in workflows (e.g., excessive rework or delays)
Predictability: Enable better estimations of time, cost, and resources in future projects
Quality Assurance and continuous improvement: Early tracking of process performance helps find issues and optimize specific development phases
Risk Management: Reveal high-risk areas (e.g., volatile requirements)
Accountability and Transparency: Provide objective evidence of process performance, thereby track performance of different stakeholders working on software development
Enhances customer satisfaction
16
Software Engineering

## Slide 17: A few examples

17
Software Engineering
