# 1. What is the importance of SQA? Discuss SQA activities.

#### SQA

- Software quality assurance (often called quality management) is an umbrella activity that is applied throughout the software process.
- It is planned and systematic pattern of activities necessary to provide high degree of confidence in the quality of a product.
- Software quality assurance (SQA) encompasses:
  1. An SQA process.
  2. Specific quality assurance and quality control tasks.
  3. Effective software engineering practice.
  4. Control of all software work products and the changes made to them.
  5. A procedure to ensure compliance with software development standards.
  6. Measurement and reporting mechanisms.


#### Importance of SQA

1. SQA produces high quality software. 
2. High quality application saves time and cost. 
3. SQA is beneficial for better reliability. 
4. SQA is beneficial in the condition of no maintenance for a long time. 
5. High quality commercial software increase market share of company. 
6. Improving the process of creating software. 
7. Improves the quality of the software. 

#### SQA Activities

1. Prepare an SQA plan for a project
2. Participate in the development of the project’s software process description
3. Review software engineering activities to verify compliance with the defined software process
4. Audit designated software work products to verify compliance with those defined as part of the software process
5. Ensure that deviations in software work and work products are documented and handled according to a documented procedure.
6. Records any noncompliance and reports to senior management

# 2. Reverse Engineering

- Software Reverse Engineering is a process of recovering the design, requirement specifications and functions of a product from an analysis of its code.
- The purpose of reverse engineering is to facilitate the maintenance work by improving the understandability of a system and to produce the necessary documents for a legacy system. 

#### Reverse Engineering Goals: 

- Cope with Complexity.
- Recover lost information.
- Detect side effects.
- Synthesise higher abstraction.
- Facilitate Reuse.

#### Steps of Software Reverse Engineering: 

- Collection Information: 
- Examining the information: 
- Extracting the structure: 
- Recording the functionality: 
- Recording data flow: 
- Recording control flow: 
- Review extracted design: 
- Generate documentation: 
 
#### Reverse Engineering Tools:

- CIAO and CIA: 
- Rigi
- Bunch
- GEN++
- PBS

# 3. What is DevOps? How it works? What are the DevOps principles & best practices?

#### DevOps

- DevOps is a software development methodology that improves the collaboration between developers and operations teams using various automation tools.
- These automation tools are implemented using various stages which are a part of the DevOps Lifecycle.
- DevOps bridges the gap between the operation team & development team, which generally used to work in isolation with another.
- The main aim of DevOps is to provide continuous & high-quality delivery of the software by making shortening SDLC

#### How DevOps Works?

- The DevOps Lifecycle divides the SDLC lifecycle into the following stages:
1. Continuous Development:
2. Continuous Integration:
3. Continuous Deployment:
4. Continuous Testing:
5. Continuous Monitoring:
6. Continuos operations
7. Continuos Feedback

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20220103162635/11.PNG">

#### Devops Practices

1. Process automation
2. Continuous Integration (CI)
3. Continuous Delivery (CD)
4. Continuous Deployment
5. Infrastructure as code
6. Microservices
7. Configuration management and many more.

#### Devops Principles

- DevOps principles guide how to organize a DevOps environment.

1. Incremental Releases
2. Automation
3. DevOps Pipeline
4. Continuous Integration
5. Continuous Delivery
6. Continuous Monitoring
7. Feedback Sharing
8. Version Control
9. Collaboration

# 4. Write short note on Version Control. 

- Version control systems are a category of software tools that helps in recording changes made to files by keeping a track of modifications done in the code. 

- **Example** : Git, Helix core, Microsoft TFS,


#### Types of Version Control Systems: 

1. Local Version Control Systems
2. Centralized Version Control Systems
3. Distributed Version Control Systems

#### Purpose of Version Control: 

- Multiple people can work simultaneously on a single project.
- It integrates the work that is done simultaneously by different members of the team
- Version control provides access to the historical versions of a project.
- It can be easily known when, why, and by whom any part of a file was edited.

#### Benefits of the version control system:

- Enhances the project development speed by providing efficient collaboration.
- Reduce possibilities of errors through traceability to every small change.
- Informs us about Who, What, When, Why changes have been made.
- Helps in recovery in case of any disaster or contingent situation.

# 5. Re-engineering.

- When we need to update the software to keep it to the current market, without impacting its functionality, it is called software re-engineering.
- It is a process where the design of software is changed and programs are re-written
- Legacy software cannot keep tuning with the latest technology available in the market
  - For example, initially UNIX was developed in assembly language. When language C came into existence, UNIX was re-engineered in C, because working in assembly language was difficult.
- Other than this, sometimes programmers notice that few parts of software need more maintenance than others and they also need re-engineering.
- Decide what to re-engineer.
  - Is it whole software or a part of it?
- Perform Reverse Engineering, in order to obtain specifications of existing software
- Restructure Program if required
  - For example, changing function-oriented programs into object-oriented programs and re-structure data as required
- Apply Forward engineering concepts in order to get re-engineered software

# 6. Explain Formal Technical Review.

- A formal technical review (FTR) is a software quality control activity performed by software engineers (and others).

#### The objectives of an FTR are:
1. To uncover errors in function, logic, or implementation; for any representation of the software
2. To verify that the software under review meets its requirements
3. To ensure that the software has been represented according to predefined standards
4. To achieve software that is developed in a uniform manner
5. To make projects more manageable

- During the FTR,
  - a reviewer (the recorder) actively records all issues that have been raised
- These are summarized at the end of the review meeting, and a reviewed issues list is produced
- In addition, a formal technical review summary report is completed

# 7. Cohesion & Coupling

- A good software design implies clean decomposition of the problem into
modules, and the neat arrangement of these modules in a hierarchy.

- The primary characteristics of neat module decomposition are
high cohesion and low coupling.

#### Cohesion

- Cohesion is a measure of the degree to which the elements of the module are functionally related.
- A good software will have high Cohesion. 
- Cohesion is an indication of the relative functional
strength of a module.
- A cohesive module performs a single task, requiring
little interaction with other components.
- A module having high cohesion and low coupling is
said to be functionally independent of other modules.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/cohesion.png">

#### Coupling

-  Coupling is the measure of the degree of interdependence between the modules.
- A good software will have low coupling. 
- If two modules interchange large amounts of data, then they are highly interdependent.
- The degree of coupling between two modules depends on their interface complexity.
- The interface complexity is basically determined by the number of types of parameters that are interchanged while invoking the functions of the module.
- A module having high cohesion and low coupling is said to be functionally independent of other modules.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/coupling.png">

| Cohesion                                                | Coupling                                                 |
|---------------------------------------------------------|----------------------------------------------------------|
| Cohesion is the concept of intra-module.                | Coupling is the concept of inter-module.                 |
| Cohesion represents the relationship within a module.   | Coupling represents the relationships between modules.   |
| Increasing cohesion is good for software.               | Increasing coupling is avoided for software.             |
| Cohesion represents the functional strength of modules. | Coupling represents the independence among modules.      |
| Highly cohesive gives the best software.                | Whereas loosely coupling gives the best software.        |
| In cohesion, the module focuses on a single thing.      | In coupling, modules are connected to the other modules. |

# 8. State the difference between procedural Design and Object Oriented Design.

|                                                      Procedural Oriented Design                                                     |                                                                             Object Oriented Design                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| The basic abstractions, which are given to the user, are real world functions.                                                      | The basic abstractions are not the real world functions but are the data abstraction where the real world entities are represented.                                            |
| Functions are grouped together by which a higher level function is Page on obtained.an eg of this technique isSA/SD.                | Functions are grouped together on the basis of the data they operate since the classes are associated with their methods.                                                      |
| In this appproach the state information is often represented in a centralized shared memory.                                        | In this approach the state information is not represented in a centralized memory but is implemented or distributed among the objects of the system.                           |
| we decompose in function/procedure level                                                                                            | we decompose in class level                                                                                                                                                    |
| Top down Approach                                                                                                                   | Bottom up approach                                                                                                                                                             |
| It views system as Black Box that performs high level function and later decompose it detailed function so to be mapped to modules. | Object-oriented design is the discipline of defining the objects and their interactions to solve a problem that was identified and documented during object-oriented analysis. |
| Begins by considering the use case diagrams and Scenarios.                                                                          | Begins by identifying objects and classes                                                                                                                                      |




