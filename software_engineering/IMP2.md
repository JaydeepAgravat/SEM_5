# 1. Which are the Software quality standards? Explain any one.

- Quality: developed product meets it’s specification.
- List of Quality Standards:
1. ISO 9000
2. CMM
3. Six Sigma

#### CMM (Capability Maturity Model)
- To determine an organization’s current state of process maturity, the SEI (Software Engineering Institute) uses an assessment that results in a five point grading scheme
- The grading scheme determines compliance with a capability maturity model (CMM) that defines key activities required at different levels of process maturity
- The SEI approach establishes five process maturity levels that are defined in the following manner

###### Level 1: Initial
- The software process is characterized as ad hoc and occasionally
- Few processes are defined and success depends on individual effort
###### Level 2: Repeatable
- Basic project management processes are established to track cost, schedule, and functionality.
- The necessary process discipline is in place to repeat earlier successes on Project
###### Level 3: Defined
- The software process for both management and engineering activities is documented, standardized and integrated
- This level includes all characteristics defined for level 2
###### Level 4: Managed
- Detailed measures of the software process and product quality are collected
- This level includes all characteristics defined for level 3
###### Level 5: Optimizing
- Continuous process improvement is enabled by quantitative feedback from the process and from testing innovative ideas and technologies
- This level includes all characteristics defined for level 4

<img src="http://www.gtu-paper-solution.com/upload/2160701/W2017/Q4B_OR.png" width=50%>

# 2. RMMM

<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/software_engineering/SE_IMG/1.png" width=50%>
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/software_engineering/SE_IMG/2.png" width=50%>
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/software_engineering/SE_IMG/3.png" width=50%>
<img src="https://github.com/JaydeepAgravat/SEM_5/blob/main/software_engineering/SE_IMG/4.png" width=50%>

# 3. What is the importance of user interface? Discuss user interface design rules.

### User interface
- User interface is the front-end application view to which user interacts in order to use the software.
- The software becomes more popular if its user interface is:
1. Attractive
2. Simple to use
3. Responsive in short time
4. Clear to understand
5. Consistent on all interface screens
- There are two types of User Interface:
1. Command Line Interface: 
2. Graphical User Interface:

### Importance of user interface
1. Attracting and acquiring new customers
2. A boost in customer retention 
3. Lower customer support expenses
4. Lower costs for development
5. Higher customer satisfaction

### User interface design rules

1. Place the User in Control
- Define interaction modes in a way that does not force a user into unnecessary or undesired
- Provide for flexible interaction.
- Allow user interaction to be interruptible and undoable.
- Streamline interaction as skill levels advance and allow the interaction to be customized.
- Hide technical internals from the casual user.
- Design for direct interaction with objects that appear on the screen.

2. Reduce the User’s Memory Load
- Reduce demand on short-term memory.
- Establish meaningful defaults.
- Define shortcuts that are intuitive.
- The visual layout of the interface should be based on a real-world metaphor.
- Disclose information in a progressive fashion.

3. Make the Interface Consistent
- Allow the user to put the current task into a meaningful context.
- Maintain consistency across a family of applications.
- If past interactive models have created user expectations, do not make changes unless there is a compelling reason to do so.

# 4. What is SRS? What are the key elements of it? What are the qualities of a good SRS?

### SRS

- A software requirements specification (SRS) is a comprehensive summary of software that needs to be developed. 
- It contains all the requirements, whether they are functional or non-functional.

### key elements of SRS

- Functional requirements
- System requirements
- Technical requirements
- Constraint
- Assumptions
- Criteria of acceptance

### Qualities of a good SRS

1. Correctness: 
- User review is used to ensure the correctness of requirements stated in the SRS. 
- SRS is said to be correct if it covers all the requirements that are actually expected from the system. 
 

2. Completeness: 
- Completeness of SRS indicates every sense of completion including the numbering of all the pages, resolving the to be determined parts to as much extent as possible as well as covering all the functional and non-functional requirements properly. 
 

3. Consistency: 
- Requirements in SRS are said to be consistent if there are no conflicts between any set of requirements. 
- Examples of conflict include differences in terminologies used at separate places, logical conflicts like time period of report generation, etc. 
 

4. Unambiguousness: 
- A SRS is said to be unambiguous if all the requirements stated have only 1 interpretation. 
- Some of the ways to prevent unambiguousness include the use of modelling techniques like ER diagrams, proper reviews and buddy checks, etc. 
 

5. Ranking for importance and stability: 
- There should a criterion to classify the requirements as less or more important or more specifically as desirable or essential.
-  An identifier mark can be used with every requirement to indicate its rank or stability. 
 

6. Modifiability: 
- SRS should be made as modifiable as possible and should be capable of easily accepting changes to the system to some extent.
-  Modifications should be properly indexed and cross-referenced. 
 

7. Verifiability: 
- A SRS is verifiable if there exists a specific technique to quantifiably measure the extent to which every requirement is met by the system. 
- For example, a requirement starting that the system must be user-friendly is not verifiable and listing such requirements should be avoided. 
 

8. Traceability: 
- One should be able to trace a requirement to design component and then to code segment in the program. 
- Similarly, one should be able to trace a requirement to the corresponding test cases. 
 

9. Design Independence: 
- There should be an option to choose from multiple design alternatives for the final system. 
- More specifically, the SRS should not include any implementation details. 
 

10. Testability: 
- A SRS should be written in such a way that it is easy to generate test cases and test plans from the document. 
 

11. Understandable by the customer: 
- An end user maybe an expert in his/her specific domain but might not be an expert in computer science.
- Hence, the use of formal notations and symbols should be avoided to as much extent as possible. 
- The language should be kept easy and clear. 
 

12. Right level of abstraction: 
- If the SRS is written for the requirements phase, the details should be explained explicitly.
-  Whereas, for a feasibility study, fewer details can be used. Hence, the level of abstraction varies according to the purpose of the SRS. 






