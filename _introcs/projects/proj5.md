---
layout: project
course: introcs

number: 5
title: Final Project
due: 2016-06-08
turnin: #
forum: #

rubric:
  total: 60
  design:
    criteria:
       - criterion: Brainstorming
         value: 2
       - criterion: Project Pitches
         value: 6
       - criterion: Scenarios
         value: 6
       - criterion: Implementation Plan
         value: 6
       - criterion: Exit tickets are completed daily throughout project
         value: 2
    total: 22
  implementation:
    criteria:
        - criterion: Program is well-documented	and shows good style
          value: 4
        - criterion: Program uses SNAP elements effectively, including all required elements
          value: 6
        - criterion: Project is appropriately complex and creative
          value: 12
        - criterion: Final product meets all requirements and goals laid out in spec
          value: 16
    total: 38
---
### Overview
During this course, you have learned a huge amount about computer science and programming in general, and SNAP in particular.  In this project, you will put all of that knowledge, along with some new skills you will develop around design, planning, and project management, to build a relatively large and complex application that _you_ choose.  You can create almost anything you want and should ultimately produce a project that is interesting, useful, and challenging.

### Project Phases
This project will be significantly larger in scope than any of your previous assignments, so there will be more design and planning than before.  More importantly, though, rather than be given a well-defined specification, _YOU_ will be setting the requirements for your project by coming up with an idea, fleshing out the details, and defining the steps necessary to complete your program.
<p />
To help you through this process, there will be several steps to this project.  You must complete **all** of the steps **in order** for your project to be successful.  In fact, roughly _a third_ of your grade will be based not on how well your program works, but on how well you completed the design and planning process.
<p />
The phases of the project will be:

1. _Brainstorming_ - coming up with as many possible project ideas as you can
2. _Pitching_ - choosing a few ideas and developing a short description of what the project will entail
3. _Scenario Definition_ - listing out the features the project will need and what they will look like
4. _Specification_ - fleshing out all the specifics of how the project will work
5. _Development_ - writing the code for your project by following the spec and schedule created in the previous steps

### Progress Tracking
In phase iv, you will complete a [Final Project Development Plan]({{site.baseurl}}/introcs/Final Project Development Plan.docx).  This document will be your guides in the development phase and will help you stay on track and aware of your progress.  Throughout the development phase of the project, you will be expected to keep your spec and plan up-to-date and make adjustments as you get ahead or behind, as requirements change, or as tasks or features get reprioritized.  At the end of each coding day, your spec should be updated to reflect the current state of your project.  

At the conclusion of the planning day of the project, you should submit your brainstorming and planning documents to Canvas here: [https://canvas.instructure.com/courses/1001373/assignments/4780751](https://canvas.instructure.com/courses/1001373/assignments/4780751).

### Implementation Requirements

#### Complexity and Creativity
Your final project should be sufficiently complex and large-scale to push your limits as a programmer, but not so sophisticated that you are not able to complete it in the time allotted.  The complexity in your project should come from the _design_ and the _algorithms_ and not from the _code_.  (That is, you cannot meet the complexity requirement simply by writing a lot of code.  Your code must be challenging or interesting in some meaningful way.)  In addition, you should not add complexity by introducing peripheral elements, such as graphics or sound effects.  (Your program can certainly have these, but they will not be considered in determining the projects complexity.)
<p />
In addition, one of the main goals of this project is to allow you to unleash your creativity and allow you to create something of interest to you.  To achieve this, your project must show some level of creativity or personalization that makes it your own.  Simply creating your own version of some existing application will not fully meet this requirement.
<p />
For both the complexity and creativity requirements, you should talk to the instructors early and often to ensure your project is in line with our expectations.

#### Documentation and Style
As with all previous projects, your program must be well-written, well-documented, and readable.  Writing code with good style is always a good idea, but in a project of this size and scope, following style guidelines will help you keep your thoughts organized and make it easier to keep track of your progress, pick up where you left off each day, and find and fix bugs.  In particular, though this is certainly not a comprehensive list, pay attention to the following:

* organizing your scripts so that they can be read and comprehended easily
* giving your sprites, variables, lists, and custom blocks descriptive and meaningful names
* using the right type of variable (global, local, sprite) for each situation
* including comments to describe the structure of your program and track your progress
* avoiding redundancy with good use of loops, custom blocks, and/or lists
* practicing good procedural decomposition and abstraction
        
#### Required SNAP Elements
In order to show that you have fully mastered all the skills from the course, you project must include at least the following:

* a clear way to start the program, and clear prompts or instructions for any user interaction
* an least one loop, variable, custom block, and list, and more as necessary or appropriate
  * each these must be used correctly and meaningfully-- creating a list that contains  a single element just to meet this requirement will not earn points
* at least one user interaction
  * this can be prompting for information using ask, responding to key presses or mouse movements, or any other action that keeps the user involved