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

# 9. What is Software Testing? What is the role of a Software Tester? Compare Black Box and White Box Testing.

#### Software Testing

- Software testing is a process of identifying the correctness of software by considering its all attributes (Reliability, Scalability, Portability, Re-usability, Usability) and evaluating the execution of software components to find the software bugs or errors or defects.
- Testing is mandatory because it will be a dangerous situation if the software fails any of time due to lack of testing.
- So, without testing software cannot be deployed to the end user.

#### Role of a Software Tester

- Software Testers are responsible for the quality of software development and deployment
- They are involved in performing automated and manual tests to ensure the software created by developers is fit for purpose. 
- Some of the duties include analysis of software, and systems, mitigate risk and prevent software issues.
- Provide timely solutions
- Provide support and documentation
- collaborate closely with other team members and departments
- execute all levels of testing (System, Integration, and Regression)

#### Black Box and White Box Testing

| S. No. | Black Box Testing                                                                                                                   | White Box Testing                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.     | It is a way of software testing in which the internal structure or the program or the code is hidden and nothing is known about it. | It is a way of testing the software in which the tester has knowledge about the internal structure or the code or the program of the software. |
| 2.     | Implementation of code is not needed for black box testing.                                                                         | Code implementation is necessary for white box testing.                                                                                        |
| 3.     | It is mostly done by software testers.                                                                                              | It is mostly done by software developers.                                                                                                      |
| 4.     | No knowledge of implementation is needed.                                                                                           | Knowledge of implementation is required.                                                                                                       |
| 5.     | It can be referred to as outer or external software testing.                                                                        | It is the inner or the internal software testing.                                                                                              |
| 6.     | It is a functional test of the software.                                                                                            | It is a structural test of the software.                                                                                                       |
| 7.     | This testing can be initiated based on the requirement specifications document.                                                     | This type of testing of software is started after a detail design document.                                                                    |
| 8.     | No knowledge of programming is required.                                                                                            | It is mandatory to have knowledge of programming.                                                                                              |
| 9.     | It is the behavior testing of the software.                                                                                         | It is the logic testing of the software.                                                                                                       |
| 10.    | It is applicable to the higher levels of testing of software.                                                                       | It is generally applicable to the lower levels of software testing.                                                                            |
| 11.    | It is also called closed testing.                                                                                                   | It is also called as clear box testing.                                                                                                        |
| 12.    | It is least time consuming.                                                                                                         | It is most time consuming.                                                                                                                     |
| 13.    | It is not suitable or preferred for algorithm testing.                                                                              | It is suitable for algorithm testing.                                                                                                          |
| 14.    | Can be done by trial and error ways and methods.                                                                                    | Data domains along with inner or internal boundaries can be better tested.                                                                     |
| 15.    | Example: Search something on google by using keywords                                                                               | Example: By input to check and verify loops                                                                                                    |
| 16.    | Black-box test design techniques- Decision table testing All-pairs testing Equivalence partitioning Error guessing                  | White-box test design techniques- Control flow testing Data flow testing Branch testing                                                        |
| 17.    | Types of Black Box Testing:  Functional Testing  Non-functional testing  Regression Testing                                         | Types of White Box Testing:  Path Testing  Loop Testing  Condition testing                                                                     |
| 18.    | It is less exhaustive as compared to white box testing.                                                                             | It is comparatively more exhaustive than black box testing.                                                                                    |

# 10. Distinguish between verification & validation. 

| Verification                                                                           | Validation                                                                                      |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| It includes checking documents, design, codes and programs.                            | It includes testing and validating the actual product.                                          |
| Verification is the static testing.                                                    | Validation is the dynamic testing.                                                              |
| It does not include the execution of the code.                                         | It includes the execution of the code.                                                          |
| Methods used in verification are reviews, walkthroughs, inspections and desk-checking. | Methods used in validation are Black Box Testing, White Box Testing and non-functional testing. |
| It checks whether the software conforms to specifications or not.                      | It checks whether the software meets the requirements and expectations of a customer or not.    |
| It can find the bugs in the early stage of the development.                            | It can only find the bugs that could not be found by the verification process.                  |
| The goal of verification is application and software architecture and specification.   | The goal of validation is an actual product.                                                    |
| Quality assurance team does verification.                                              | Validation is executed on software code with the help of testing team.                          |
| It comes before validation.                                                            | It comes after verification.                                                                    |
| It consists of checking of documents/files and is performed by human.                  | It consists of execution of program and is performed by computer.                               |

# 11. Agile vs DevOps

| S. No. | Agile                                                                                                                                                                                                                                                                                                                   | DevOps                                                                                                                                                                       |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.     | It started in the year 2001.                                                                                                                                                                                                                                                                                            | It started in the year 2007.                                                                                                                                                 |
| 2.     | Invented by John Kern, and Martin Fowler.                                                                                                                                                                                                                                                                               | Invented by John Allspaw and Paul Hammond at Flickr, and the Phoenix Project by Gene Kim.                                                                                    |
| 3.     | Agile is a method for creating software.                                                                                                                                                                                                                                                                                | It is not related to software development. Instead, the software that is used by DevOps is pre-built, dependable, and simple to deploy.                                      |
| 4.     | An advancement and administration approach.                                                                                                                                                                                                                                                                             | Typically a conclusion of administration related to designing.                                                                                                               |
| 5.     | The agile handle centers on consistent changes.                                                                                                                                                                                                                                                                         | DevOps centers on steady testing and conveyance.                                                                                                                             |
| 6.     | A few of the finest steps embraced in Agile are recorded underneath – 1. Backlog Building 2.Sprint advancement                                                                                                                                                                                                          | DevOps to have a few best hones that ease the method – 1. Focus on specialized greatness. 2. Collaborate straightforwardly with clients and join their feedback.             |
| 7.     | Agile relates generally to the way advancement is carried of, any division of the company can be spry in its hones. This may be accomplished through preparation.                                                                                                                                                       | DevOps centers more on program arrangement choosing the foremost dependable and most secure course.                                                                          |
| 8.     | All the group individuals working in a spry hone have a wide assortment of comparable ability sets. This is often one of the points of interest of having such a group since within the time of requirement any of the group individuals can loan help instead of holding up for the group leads or any pro impedances. | DevOps features a diverse approach and is very viable, most of the time it takes after “Divide and Conquer”. Work partitioned among the improvement and operation groups.    |
| 9.     | Spry accepts “smaller and concise”. Littler the group superior it would be to convey with fewer complexities.                                                                                                                                                                                                           | DevOps, on the other hand, accepts that “bigger is better”.                                                                                                                  |
| 10.    | Since Agile groups are brief, a foreordained sum of time is there which are sprints. Tough, it happens that a sprint has endured longer than a month but regularly a week long.                                                                                                                                         | DevOps, on the other hand, prioritizes reliabilities. It is since of this behavior that they can center on a long-term plan that minimizes commerce’s unsettling influences. |
| 11.    | A big team for your project is not required.                                                                                                                                                                                                                                                                            | It demands collaboration among different teams for the completion of work.                                                                                                   |
| 12.    | Some of the Tools-     Bugzilla JIRA  Kanboard and more.                                                                                                                                                                                                                                                                | Some of the Tools-  Puppet Ansible AWS Chef team City OpenStack and more.                                                                                                    |
| 13.    | It is suitable for managing complex projects in any department.                                                                                                                                                                                                                                                         | It centers on the complete engineering process.                                                                                                                              |
| 14.    | It does not focus on the automation.                                                                                                                                                                                                                                                                                    | It focusses on automation.                                                                                                                                                   |
| 15.    | Working system gets more significance in Agile than documentation.                                                                                                                                                                                                                                                      | The process documentation is significant in DevOps.                                                                                                                          |

# 12. Component-Based Software Engineering.

- Component-based software engineering (CBSE) is a process that emphasizes the design and construction of
computer-based systems using reusable software “components.”
- CBSE seems quite similar to conventional or object-oriented software engineering.
- The process begins when a software team establishes requirements for the system to be built using
conventional requirements elicitation techniques.

#### Activities

1. Component qualification.
- System requirements and architecture define the components that will be required.
- Reusable components (whether COTS or in-house) are normally identified by the characteristics of their
interfaces.
2. Component adaptation.
- Software architecture represents design patterns that are composed of components
(units of functionality), connections, and coordination.
- In essence the architecture defines the design rules for all components, identifying modes of connection and
coordination.
3. Component composition.
- Architectural style again plays a key role in the way in which software components are integrated to form a working system.
4. Component update.
- When systems are implemented with COTS components, update is complicated by the imposition of a third party (i.e., the organization that developed the reusable component may be outside the
Immediate control of the software engineering organization).

#### Various Components

1. Component
- a nontrivial, nearly independent, and replaceable part of a system that fulfills a clear function in
the context of a well-defined architecture.
2. Run-time software component
- a dynamic bindable package of one or more programs managed as a unit and accessed through documented interfaces that can be discovered in run time.
3. Software component
- a unit of composition with contractually specified and explicit context dependencies only.
4. Business component
- the software implementation of an “autonomous” business concept or business process.
5. Qualified components
- assessed by software engineers to ensure that not only functionality, but performance, reliability, usability, and other quality factors follow to the requirements of the system or
product to be built.
6. Adapted components
- adapted to modify (also called mask or wrap) unwanted or undesirable characteristics.
7. Assembled components
- integrated into an architectural style and interconnected with an appropriate infrastructure that allows the components to be coordinated and managed effectively.
8. Updated components
- replacing existing software as new versions of components become available.

# 13. Write short note on Six Sigma standard. 

- Six Sigma is the process of producing high and improved quality output. 
- This can be done in two phases – identification and elimination. - - The cause of defects is identified and appropriate elimination is done which reduces variation in whole processes.
- To achieve six sigma a process must not produce more than 3.4 defects per million opportunities.
- 5 Sigma -> 230 defects per million
- 4 Sigma -> 6210 defects per million

#### Characteristics of Six Sigma
1. Statistical Quality Control
2. Methodical Approach
3. Fact and Data-Based Approach
4. Project and Objective-Based Focus
5. Customer Focus
6. Teamwork Approach to Quality Management

#### Six Sigma Methodologies

- Six sigma have two methodologies.
1. DMAIC (Define, Measure, Analyze, Improve, Control)
- Define: Define the problem or process to improve upon related to the customer and goals
- Measure: How can you measure this process in a systematic way?
- Analyze: Analyze the process or problem and identify the way in which it can be improved. What are the root causes of problems within the process? 
- Improve: Once you know the causes of the problems, present solutions for them and implement them
- Control: Utilize Statistical Process Control to continuously measure your results and ensure you are improving Several Software Packages available to assist in measuring yield, defects per million opportunities, etc.

2. DMADV: (Define, Measure, Analyze, Design, Verify)
- Define, Measure and analyze are similar to above method.
- Design: Avoid root causes of defects and meet the customer requirements.
- Verify: To verify the process, compare the process with the standard plan and find differences.
 
