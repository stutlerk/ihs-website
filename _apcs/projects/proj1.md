---
layout: project
course: apcs

number: 1
title: Fraction Calculator
due: 2015-12-16
turnin: #
forum: #

checkpoints:
  - title: Checkpoint 1 - Parsing Input
    date: 2015-12-01
    value: 10%
    description: main() creates a Scanner and reads one line of input; produceAnswer() breaks a single line of input into the relevant three parts, stores each part in a variable, and returns the second operand
  - title: Checkpoint 2 - Driver and Fractions
    date: 2015-12-07
    value: 10%
    description: 'main() includes the driver loop, repeatedly accepting input and calling produceAnswer() until the user types "quit"; produceAnswer() parses each operand into three parts-- a whole portion, a numerator, and a denominator-- and returns a String describing the second operand, formatted as "whole: <whole part> numerator: <numerator> denominator: <denominator>" (e.g. if the second operand is 3_5/8, produceAnswer() returns "whole: 3 numerator: 5 denominator: 8")'
    
rubric:
  total: 40
  behavior:
    criteria:
      - criterion: Program greets user on startup and displays a goodbye message on termination
        value: 1
      - criterion: Typing "quit" ends the program regardless of case
        value: 1
      - criterion: Program repeatedly prompts the user for an expression
        value: 1
      - criterion: Program is able to parse each line of input into three parts (value, operator, value)
        value: 2
      - criterion: Program is able to parse each fraction value into three parts (whole, numerator, denominator)
        value: 3
      - criterion: Program is able to handle integers, proper fractions, improper fractions, and mixed numbers, both positive and negative
        value: 4
      - criterion: Program output is in proper format
        value: 2
      - criterion: Output is a mixed fraction in lowest terms
        value: 4
      - criterion: Multiplication and division work correctly
        value: 3
      - criterion: Addition and subtraction work correctly
        value: 4
    total: 25
  implementation:
    criteria:
      - criterion: main is a concise summary of program behavior
        value: 1
      - criterion: produceAnswer is implemented as required
        value: 2
      - criterion: Program uses good procedural decomposition, including parameters and return values
        value: 2
      - criterion: Program is well-documented and uses good style
        value: 2
      - criterion: Checkpoint 1
        value: 4
      - criterion: Checkpoint 2
        value: 4
    total: 15
---
### Overview
Modern computers are capable of an incredibly varied set of operations and behaviors, from analyzing data to playing movies to supporting complex three-dimensional games.  At the core of all these programs, however, is the central talent of computers—- performing mathematical operations.  We will utilize this basic skill to implement a calculator program that will perform a variety of operations on fractions.

### Behavior

#### Input
Input will be in the form of a **value**, followed by an **operators**, followed by another **value** (e.g. "1/2 * 3/8").  Values and operators will be separated by a single space, and neither values nor operators will contain any spaces.  Input values may be in the form of mixed fractions, proper fractions, improper fractions, or integers.  Fractional input values need not necessarily be in lowest terms.  The numerator and denominator of a fraction will be separated by a forward slash (/).  The integer and fraction parts of a mixed fraction will be separated by an underscore (_) (e.g. "1_3/4" is one and three fourths, while "13/4" is thirteen fourths).

The calculator will support the four basic arithmetic operations: addition (+), subraction (-), multiplication (*), and division (/).  Note that the symbol for division is the same as the symbol that separates the numerator and denominator of a fraction.

#### Output
The program should output the result of the calculation to the screen.  Output should be in the form of the **expression**, and **equals sign**, and the **result** (e.g. "1/2 * 3/8 = 3/16").  The input values should be echoed in the output exactly as they were given, but the result should be an integer, proper fraction, or mixed number in lowest terms (e.g. 3/4 instead of 6/8 and 1_1/2 instead of 3/2).  The result of an operation should _never_ be an improper fraction.

#### Main Driver Loop
Your program should begin by welcoming the user to the program.  Then, it should enter a "driver loop" that executes the various steps of the program repeatedly until the user chooses to exit.  Your driver loop will operate as follows:

- Ask for an expression (see "Input" above).
- If the user typed "quit", exit the program.  
- Otherwise, evaluate the expression.
- Echo the expression that was input and print the result (see "Output" above).
- Ask for another expression and repeat.

The program should continue through this loop until the user types "quit."  You should ignore case when checking the input (i.e. "quit," "QUIT," "Quit," and "qUiT," among others, should all end the program).  Once the user types quit, the program should print a goodbye message and terminate.

### Implementation Details

#### Code Organization
Your code must conform to the following requirements in the implementation:

- Your file must be named "FractionCalculator.java".
- Your main method must represent a concise summary of the behavior of your program, and must only contain the main driver loop.  Your main method should use a Scanner to receive input and should call produceAnswer (see below) with that input and print the result according to the specification.
- Your program must include a method with the following prototype: 
```
public static String produceAnswer(String input)
```
This method should take a single line of user input as its parameter (e.g. "1/2 * 3/4"), perform the indicated calculation, and return the result as a String (e.g. "3/8").  _This method should NOT print anything!_ 

#### Unit Testing
You will be provided with a suite of unit tests to run against your program.  In order to receive full credit for any checkpoint or the final submission, your program must pass ALL relevant unit tests.  Note that these tests are not exhaustive, so passing all the tests does not guarantee any particular grade.  Details on importing and running the tests in jGRASP will be provided soon.

#### Extra Credit
You may earn extra credit by implementing additional features beyond those that are required.  Point values for extra credit features will be solely at my discretion and will be determined based on creativity and difficulty of implementation.  **No extra credit will be awarded for features that break required functionality, and points will still be lost for failing to meet requirements.**  It is HIGHLY recommended that you not attempt extra credit work until your project is fully complete.  Extra credit will be capped at 10% of the total project value.

Possible extra credit features include (but are not limited to):

- Detecting and issuing error messages for invalid input
- Adding additional operations
- Handling multiple operations at once (e.g  3 + 4 * 5)
  - More extra credit for doing this and respecting order of operations!

Note that your extra credit work must not cause any of your unit tests to fail or otherwise cause the program functionality to change.  In other words, your extra credit features must not require the user to change their behavior to use the program properly-- you must simply add additional, optional features.



  