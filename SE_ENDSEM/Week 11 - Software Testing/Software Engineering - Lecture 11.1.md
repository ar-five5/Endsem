# Software Engineering - Lecture 11.1

## Slide 1: Software Engineering(CS3201)Software Testing

Avinash

## Slide 2: Objectives

Understand the different stages of testing from 'testing during development' to 'acceptance testing by system customers'
Understand techniques to help choose test cases
Understand 'Test First Development'
Understand Component testing, System testing and Release testing
2
Software Engineering

## Slide 3: Introduction

Intention of testing – show that program does what it is supposed to do, and discover program defects
When you test software, you execute program using artificial data
When you test software, you are trying to do two things:
  - Demonstrate to developer and customer that the software meets its requirements (called validation testing)
  - Find inputs or input sequences where the behavior of the software is incorrect, undesirable, or does not conform to its specification (called defect testing)
Edgar Dijkstra: "Testing can only show the presence of errors, not their absence"
3
Software Engineering

## Slide 4: Introduction

4
Software Engineering
Defect testing is not about seeing if the system works with bad input. It's about checking if the system handles bad input correctly without breaking

## Slide 5: Introduction

Verification vs. Validation:
  - Validation – are we building the right product?
  - Verification – are we building the product right?
  - Software verification is the process of checking that the software is built correctly, according to specification, following the right steps
  - Software validation is the process of ensuring that the software meets the customer’s expectations. It goes beyond checking conformance with the specification
  - Verification is checking if we follow all steps in the software recipe, validation is tasting the food for goodness (yum) once it is prepared
V&V help establish a confidence in the software, that it is "fit for purpose"
5
Software Engineering

## Slide 6: Introduction

What determines amount of confidence in a system? (how confident you need to be about a software before releasing it)
  - Software purpose: More critical the software, more important the reliability, higher the confidence needed
  - User expectations: Prior experiences with older versions of software, or similar software, can set up user expectations in current software, and greater the expectations, greater is the confidence needed
  - Marketing environment: Environmental factors, for instance, how quickly you want to release the software to market, the price the customer is willing to pay for a product, etc.
6
Software Engineering

## Slide 7: Introduction

As well as software testing, V&V may involve software inspections and reviews
These are "static" V&V techniques, no need to execute the system
Inspections mostly focus on software code, and on other readable representations of the software – requirements specification or design models
Advantages of inspection and reviews:
  - Testing can mask or hide errors (especially side effects) which reviews catch
  - Incomplete versions of the system can be inspected without additional costs
  - Broader qualities of the software can be tested – standards, portability, maintainability
Fagan (1976) reported that 60% defects can be caught in reviews, CleanRoom process (Prowell et.al 1999) claimed 90% can be caught
7
Software Engineering

## Slide 8: Introduction

Typically, commercial software systems go through three stages of testing:
  - Development testing: Testing during development to discover bugs and defects
  - Release testing: Separate testing team tests the complete version of the system before it is released to users
  - User testing: Users or potential users test the system in their own environment (Acceptance testing is one type of formal user testing)
In practice, testing also involves a combination of manual and automated testing
8
Software Engineering

## Slide 9

Development Testing
9
Software Engineering

## Slide 10: Development testing

Testing activities carried out by the team developing the system
Three stages:
  - Unit testing: Where individual program units or object classes are tested
  - Component testing: Individual units integrated to form components. Component testing should focus on testing the component interfaces that provide access to the component functions
  - System testing: Some or all of the components in a system are integrated and the system is tested as a whole
Development testing is primarily defect testing where the aim is to discover bugs in the system (therefore, sometimes interleaved with debugging)
10
Software Engineering

## Slide 11: Unit testing

Testing individual units – like methods or object classes
Methods or functions are the simplest kinds of units
Call methods with all possible parameters
In object testing, test all operations associated with the object; set and check the value of all attributes associated with the object; and put the object into all possible states. This means that you should simulate all events that cause a state change
  - Example: In the weather station application, consider 'Weather Station' object; for this object, you can check if it goes through all states of the state chart diagram: Configure -> Running -> Collecting -> Running -> Summarizing
  - Each state is nothing but a certain value(s) an attribute(s) of an object holds at some point (another way of seeing testing of all possible states)
11
Software Engineering

## Slide 12: Unit testing

How will you write test cases to unit test the following object class?
Note: Generally, you test methods in isolation, but sometimes, methods need to be tested in sequence (to test reconfigure(), you will have to call shutdown() first)
12
Software Engineering

## Slide 13: Unit testing - Automated

Unit testing can be automated, and should be automated, wherever possible
An automated test (generally) has three parts:
  - A setup part, where you initialize the system with the test case, namely, the inputs and expected outputs
  - A call part, where you call the object or method to be tested
  - An assertion part, where you compare the result of the call with the expected result. If the assertion evaluates to true, the test has been successful; if false, then it has failed
Example: JUnit framework in Java
13
Software Engineering

## Slide 14: Unit testing – Automated Example using JUnit

14
Software Engineering
public class Calculator {
public int add(int a, int b) {
return a + b;
}
}
import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;
public class CalculatorTest {
@Test
public void testAddition() {
Calculator calc = new Calculator();
int result = calc.add(2, 3);
assertEquals(5, result);  // Assertion: Expected 5
}
}

## Slide 15: Unit testing – Test case objectives

Testing is expensive and time consuming, so make sure you choose effective unit test cases
Effective unit test cases?
  - Should show that, when used as expected, the component does what it is expected to do
  - If there are any defects, they should be revealed
Therefore, you should design two types of test cases:
  - Those having normal/ expected data and reflect normal working
  - Testing experiences where common problems arise. You can use abnormal inputs here for testing (to see if they are properly handled and do not crash system)
15
Software Engineering

## Slide 16: Unit testing – Strategies to choose test cases

Two strategies for choosing test cases:
  - Partition testing: Identify groups of inputs that have similar characteristics and are processed the same way
  - Guideline-based testing: Follow guidelines to prepare test cases. The guidelines are developed in the basis of prior experience
Equivalence partitioning of test cases – Identify equivalence partitions for the set of possible inputs, then for each equivalence partition, represent it by one input test case (instead of testing for all possible inputs within an equivalence partition)
There may or may not be a 1:1 mapping between an input and output equivalence partition
16
Software Engineering

## Slide 17: Unit testing – Equivalence partitions

17
Software Engineering
An equivalence partition of data is a set within which all members share similar data characteristics

## Slide 18: Unit testing – Equivalence partitions

Example:
  - Let's say you have a form that accepts ages 18 to 60
  - You can divide this into three input equivalent partitions
    - Ages < 18   (members of this partition: 17, 16, 15, …, 12, …)
    - Ages >= 18 && Ages <= 60 (members of this partition: 30, 25, 28, …., 55, 59, 50, …)
    - Ages > 60 (members of this partition: 65, 70, 63, 72, 80, 90, 92, …)
  - The corresponding output equivalence partitions would then be
    - Valid (when age is between 18 and 60)
    - Invalid (when age is greater than 60 or less than 18)
18
Software Engineering

## Slide 19: Unit testing – Equivalence partitions

Once you have identified a set of partitions, you choose test cases from each of these partitions
A good rule of thumb for test-case selection is to choose test cases on the boundaries of the partitions, plus cases close to the midpoint of the partition
You identify partitions by using the program specification (in previous example, we used program specification) or user documentation and/ or from experience
Using specification of a system to identify equivalence partitions is called black-box testing
When using code of the program to find other possible tests, it is called white box testing (refer slide 33 and beyond)
19
Software Engineering

## Slide 20: Unit testing – Equivalence partitions

20
Software Engineering
Example: A program specification states that the program accepts four to ten inputs which are five-digit integers greater than 10,000.

## Slide 21: Unit testing – Guideline based testing

Guidelines encapsulate knowledge of what kinds of test cases are effective for discovering errors
For example, when you are testing programs with sequences, arrays, or lists, guidelines that could help reveal defects include:
  - Test software with sequences that have only a single value
  - Use different sequences of different sizes in different tests
  - Derive tests so that the first, middle, and last elements of the sequence are accessed. This approach reveals problems at partition boundaries
Whittaker (2009) suggests some general guidelines:
  - Choose inputs that force the system to generate all error messages
  - Design inputs that cause input buffers to overflow
  - Repeat the same input or series of inputs numerous times
  - Force invalid outputs to be generated
  - Force computation results to be too large or too small.
21
Software Engineering

## Slide 22: Component Testing

Components – several interacting objects (through interfaces)
Therefore, focus is on testing whether the interfaces work as per specification
Assume that testing of individual objects is complete
22
Software Engineering

## Slide 23: Component Testing

Assume that components A, B, and C have been integrated to create a larger component or subsystem
The test cases are not applied to the individual components but rather to the interface of the composite component created by combining these components
23
Software Engineering

## Slide 24: Component Testing

There are different types of interfaces between components (and therefore, different type of interface errors may occur):
  - Parameter interfaces: Data or function reference passed from one component to another
  - Shared Memory interfaces: A block of memory is shared between components
  - Procedural interfaces: Set of procedures in one component that can be called by another component
  - Message Passing interfaces: Component requests service from another component by passing a message to it
24
Software Engineering
// Procedural Interface:
bool authenticateUser(string username, string password);
// Parameter Interface:
username: must be a non-empty string, 5-20 characters
password: must be a string, minimum 8 characters

## Slide 25: Component Testing – Interface errors

Interface errors are one of the most common type of errors in complex systems (Lutz 1993)
Three class of errors:
  - Interface misuse: Error in use of interface, usually in the form of wrong parameter passed, incorrect parameter order, incorrect parameter number
  - Interface misunderstanding: Calling component misunderstands the specification or interface of called component (example: binary search method maybe called on an unordered array – because of an assumption that method will first sort before applying binary search)
  - Timing errors: Happens in real time systems that use shared memory or message passing where the producer and consumer operate at different speeds (you saw this in Operating Systems class)
25
Software Engineering

## Slide 26: Component Testing – General guidelines

Identify calls to external component. Design tests such that values of parameters to external components are at extreme ends of ranges
When passing pointers across interfaces, test against NULL pointer
When calling a component through procedures, design tests to deliberately fail the component
Use stress testing in message passing systems
When components interact via shared memory, design tests that vary the order in which the components are activated (call consumer component first, then producer component)
26
Software Engineering

## Slide 27: Component Testing – Closing points

Testing for interfaces might get tricky because some faults manifest only in unusual conditions (example: Called object implements fixed length queue, whereas calling object assumes infinite length queue). This error can only be caught during queue overflow
Faults in one object may be detected only when some other object behaves in an unexpected way
Sometimes it is better to use inspections and reviews rather than testing to look for interface errors
27
Software Engineering

## Slide 28: System Testing

System testing during development involves integrating components to create a version of the system and then testing the integrated system
Checks that components are compatible, interact correctly, and transfer the right data at the right time across their interfaces
Overlaps with component testing, but with 2 differences:
  - Reusable components that have been separately developed, and off-the-shelf systems may be integrated with newly developed components. The complete system is then tested
  - Components developed by different sub teams maybe integrated at this stage
Systems have emergent behavior; some functionality becomes evident only after final system has been put together
28
Software Engineering

## Slide 29: System Testing

Because of its focus on interactions, use case-based testing is an effective approach to system testing
Several components or objects normally implement each use case in the system
Testing the use case forces these interactions to occur
And which diagram shows implementation, or interaction of objects in a use case? A sequence diagram!
If you have developed a sequence diagram to model the use case implementation, you can see the objects that are involved in the interaction to decide on how to test
29
Software Engineering

## Slide 30: System Testing

30
Software Engineering

## Slide 31: System Testing

The sequence diagram can help develop test cases, shows the inputs required and the outputs expected
The previous diagram is simple (in that it does not show exceptions)
A complete scenario/ use case test takes these exceptions into account and ensure they are correctly handled
31
Software Engineering

## Slide 32: System Testing

Exhaustive testing is difficult, and therefore, most companies have policies (or experience) to help decide which subset of test cases need to be performed. An example can be as:
  - All system functions that are accessed through menus should be tested.
  - Combinations of functions (e.g., text formatting) that are accessed through the same menu must be tested.
  - Where user input is provided, all functions must be tested with both correct and incorrect input
32
Software Engineering

## Slide 33: White Box Testing (a kind of Unit testing)

Guarantee that all independent paths within a module have been exercised (or tested) at least once
Exercise (or test) all logical decisions on their true and false sides
Execute all loops at their boundaries and within their operational bounds
Exercise (or test) internal data structures to ensure their validity
33
Software Engineering

## Slide 34: White Box Testing

Statement coverage: Exercise every statement at least once
Branch/decision coverage: Exercise every branch at least once
Path coverage: Exercise every path at least once
INSTEAD OF THESE THREE, MORE EFFICIENT – BASIS PATH TESTING
Condition testing: Test all individual boolean conditions inside compound condition
Data flow testing: Check variables properly defined and used
Loop testing: Check loop function at common and boundary conditions
Why need Condition, data flow and loop testing, when we already have basis path testing? - question to students
34
Software Engineering

## Slide 35: White Box Testing: Examples

35
Software Engineering
Loop Testing:
for (i = 0; i < n; i++)
Test this for n = 0 (loop skipped), n = 1 (loop checked once), n = typical and n = MAX
Data flow testing:
x = 10;   // definition
if (y > 5)   // use of y (but y not defined)
print(x);
Problem: y used before definition.
Other problems that can be caught – defined but never used, redefined
Condition Testing:
if (A > 10 || B < 5)
Even if branch testing passes, individual condition checks might hide bugs. Therefore, condition testing ensures all conditions are checked.

## Slide 36: White Box Testing: Questions to students

Why do we need Basis Path testing when we already have Path testing?
Why do we need Condition testing, data flow testing and loop testing when we already have Basis Path testing?
Apply your coding knowledge/ skills to think it over and let me know in the next class. It might not be as easy as you think it is
36
Software Engineering

## Slide 37: Basis Path Testing

Ensure every linearly independent path in a program is tested at least once
Based on flow graphs (or control flow graphs) and helps in achieving 100% branch coverage
Benefits:
  - Ensures all decision outcomes are tested
  - Helps identify untested parts of code
  - Complements other testing methods like integration testing
When to Use
  - Small to medium-sized functions or methods with clear logic
  - Especially effective for critical or error-prone code blocks
37
Software Engineering

## Slide 38: Basis Path Testing: Core components

Control Flow Graph:
A graphical representation of all paths that might be traversed through a program during its execution.
  - Nodes: Represent statement or groups of statements.
  - Edges: Represent flow of control between nodes.
Cyclometric Complexity
  - A metric that helps determine the number of independent paths through the program
  - Formula:
    - V(G)=E−N+2
    - Where:
    - E: Number of edges
    - N: Number of nodes
  - You can also calculate it by counting decision points:
    - V(G)=Number of decision nodes+1
38
Software Engineering

## Slide 39: Basis Path Testing: Core components

Independent Paths:
  - A path that introduces at least one new edge not included in any other paths
39
Software Engineering

## Slide 40: Basis Path Testing: Example

MAX = AIF B > A
THEN IF B > C
THEN MAX = B
ELSE MAX = C
END IF
END IF
PRINT MAX
40
Software Engineering
Note: This is just a pseudo code snippet. The example shows that basis path testing is focused on testing code, but not necessarily the LOGIC of the code. However, it is understood/ assumed (rightly) that the programmer, while using basis path testing, will identify errors in logic (if any).

## Slide 41: Basis Path Testing: Example

(1) MAX = A
(2) IF B > A
(3)  THEN IF B > C
(4)   THEN MAX = B
(5)   ELSE MAX = C
(6)  END IF
(7) END IF
(8) PRINT MAX
41
Software Engineering

## Slide 42: Basis Path Testing: Cyclometric complexity of example

Decision nodes: 2
So, V(G)=2+1=3 V(G) = 3
Other formula, V(G) = E – N + 2 = 9 – 8 + 2 = 3
Here are 3 possible independent paths through the program:
B <= A
B > A and B > C
B > A and B < C
42
Software Engineering

## Slide 43: Basis Path Testing: Design Test cases for paths

Inputs (a,b,c) = 5,3,1, Expected output = 5, Path 1
Inputs (a,b,c) = 5,7,3, Expected output = 7, Path 2
Inputs (a,b,c) = 1,3,5, Expected output = 5, Path 3
43
Software Engineering

## Slide 44

Test-Driven Development
44
Software Engineering

## Slide 45: Introduction

An approach to development that interleaves testing and code development
You develop code incrementally, along with a set of tests for that increment
You do not work on the next increment until the code you developed passes all its tests
45
Software Engineering

## Slide 46: Test-Driven Development: Steps

Start by identifying the increment of functionality that is required. This should normally be small and implementable in a few lines of code
Write a test for this functionality and implement it as an automated test. This means that the test can be executed and will report whether or not it has passed or failed
Run the test, along with all other tests that have been implemented. Initially, you have not implemented the functionality so the new test will fail. This is deliberate as it shows that the test adds something to the test set
Then implement the functionality and re-run the test. This may involve refactoring existing code to improve it and add new code to what’s already there
Once all tests run successfully, you move on to implementing the next chunk of functionality
46
Software Engineering

## Slide 47: Test-Driven Development

Automated testing environment is useful for TTD. That way, code developed in small increments can be tested faster
TTD helps write better code (you need to understand what is needed to clearly write test cases, and to understand something clearly is to code it better)
Other advantages:
  - Code coverage
  - Regression testing
  - Simplified debugging
  - System documentation
TTD is of most use when developing new software
47
Software Engineering

## Slide 48

Release and User Testing
48
Software Engineering
