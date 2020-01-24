**Introduction**

The Test Strategy for the PPR project aims to lay the appropriate QA and Test management foundation by implementing the tools, processes and governance to support the release plan for PPR.

The agile nature of the project set up will be reflected in:
-   Approach
-   Goals
-   Techniques
-   Technology use
-   Planning

This approach does not preclude us from applying a level of rigor and good testing practices to this project. In fact, agile projects if done well are often more rigorous and consistent in approach.

For our project we are working with a set of Testing Principles, which contain good (some would say best) practices for QA and testing.

1.1 Content

The Test Strategy addresses the following topics in detail:
-   Risks, Dependencies, Assumptions, and Constraints
-   Test Process Introduction
-   Detailed Test Strategies
-   Unit Test Strategy
-   Integration Test Strategy
-   Functional Test Strategy
-   System Test Strategy
-   User Acceptance Test Strategy
-   Smoke Test Strategy
-   Regression Test Strategy
-   Performance Test Strategy
-   Security Test Strategy
-   Test Automation Strategy
-   Management Strategies
-   Test Data Strategy
-   Defect Management Strategy
-   Test Results Strategy
-   Progress Reporting Strategy
-   Readiness, Exit, Suspension and Resumption Criteria
-   Definition of Done for Testing
-   Test Environmental Needs
-   Test Tool Needs
-   Responsibilities, Staffing, and Training Needs
-   Continuous Improvement Process (CIP)

1.2 Key Scope Statements

-   The Test Strategy describes an approach for QA and Testing
    > activities during the project with the intent to provide a
    > foundation and guidance for future process improvement and
    > alignment at PPR.

-   Test planning will commence ASAP and focused test plans will be implemented on a Sprint by Sprint basis.
-   Test plans will continue to evolve throughout the life of the PPR project. 

Risks, Dependencies, Assumptions and Constraints

Dependencies

  ** **   **Dependency Between**   **Potential Impact of Dependency**   **Owners**
  ------- ------------------------ ------------------------------------ ------------
  1                                                                      
  2                                                                      
  3                                                                      

Assumptions

  ** **   **Assumption to be proven**                                                                                                                                                                                                                                                           **Impact of Assumption being incorrect**   **Status**   **Owners**
  ------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------ ------------ ------------
  1       BCGov will be able to supply business testing resources For UAT                                                                                                                                                                                                                       Schedule, Quality                                        
  2       Technical Environment(s) will be available in time, in order to set up test automation tools chains, test management tools and process automation                                                                                                                                     Schedule, Capability, Quality, Coverage                  
  3       PPR Project Testing resources will be available for 100% available time during sprints - after/In between sprints an availability of at least 50% is assumed                                                                                                                          Schedule, Coverage, Quality                              
  4       PPR Testing resources will be scheduled in for a minimum 24 effort hours a week, during sprints up to 35 hours per week might be required.                                                                                                                                            Schedule                                                 
  5       PPR Testing resources (Project and UAT) will need to be trained in testing fundamentals, Agile process, test process, tools, defect management.                                                                                                                                       Preparation                                              
  6       PPR Testing resources will start the on boarding and training process as soon as possible in order to be fully ready for phase 2.                                                                                                                                                     Schedule, Preparation                                    
  7       The on boarding for the Business Testers will be similar but not identical to the testing resources                                                                                                                                                                                   Schedule, Preparation                                    
  8       The start of the on boarding for the Business Testers will happen mid-July 2019                                                                                                                                                                                                       Schedule, Preparation                                    
  9       User Experience Focus Groups: This activity is the responsibility of PPR and will involve engaging with the member community to obtain their feedback on the new solution. These sessions will start once several pieces of functionality have been developed and can demonstrated.   Schedule, Coverage, Quality                              

Constraints

  ** **   **Constraints**       **Impact of Constraint on testing effort**                                                                                                                   **Owners**   **Update**
  ------- --------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------ ------------ ------------------------------------------------------------------------------------------------------------------
  1       Sprint Duration       Length of the sprint and therefore the available time for testing will has us timebox the testing activities and potentially generating new backlog items.                A significant portion of testing/regression testing from the previous Sprint is not scheduled in the new Sprint.
  2       Tester Availability   Testers will have less than 100% availability due to matrix and leave demands. This could constrain us to 24 plannable effort hours per week.                              
  3                                                                                                                                                                                                        

 

 

 

Test Process in an Agile Context

June 24, 2019

3:00 PM

![Machine generated alternative text: Planning Design Development Start
Planning • Define scope and boundaries for development Implementation
Testing Design • Articulate scope into detailed requirements required to
deliver functionality Development • Translate requirements into code
Testing • Validate that developed system addresses requirements • Finish
Implementation Deploy to production environment
](media/image1.png){width="7.35625in" height="4.1305555555555555in"}

As PPR has adopted the agile software development paradigm, testing
processes have to evolve accordingly.

The key characteristics of agile testing will align with the key
characteristics of agile development:

-   Working closely with developers, business analysts, testers and
    > other stakeholders.

-   Testers are an integrated part of agile team.

-   Testing on an ongoing basis during sprints and not at the end of
    > project.

-   Focus on test automation.

-   Shorter test and release cycles.

An agile context would perhaps suggest foregoing any process. This is
not the case. What we will be doing is using \"just enough\" process and
guidelines to add value to the cooperation during the sprints.

In the following chapters we describe a set of processes to guide our
approach. It is certain that these processes will evolve during the
first few sprints until the best fit for PPR is found.

 

 

Test Process Introduction

June 24, 2019

3:01 PM

Testing Pyramid

Testing for PPR is represented below.

![Machine generated alternative text: User Acceptance Testing Automated
Testing Exploratory Testing Manual Testing Unit/lntegration Testing
](media/image2.png){width="6.790972222222222in"
height="3.973611111111111in"}

 

The pyramid gives an indication of the relative importance of the
different test activities and the dependencies. We\'ll discuss this
pyramid from the bottom upwards.

First Layer
-----------

The basis for all testing is intensive unit testing (and integration
testing) by CGI that is executed during development. Unit testing has
the potential of eradicating most of the easy to find defects and many
more complex ones. As almost every defect found after unit testing needs
about the same amount of time in documentation, discussion and tracking,
it would make sense to clear out the \"easy\" defects as soon as
possible. It has been proven in practice and widely documented that a
solid unit test effort has the largest impact on overall solution
quality.

Unit testing is the sturdy foundation for our testing pyramid.

Second Layer
------------

The next layer is a trifecta of 3 types of testing:

-   Exploratory testing

-   Manual testing

-   Automated Testing

Both Exploratory Testing and Manual (Functional) Testing are pre-cursors
for Automated Testing. They are the main mechanisms to obtain test ideas
and identify regression test scenarios that can be (should be)
automated.

As the pyramid indicates, automated testing will grow in scope during
the sprint and exploratory testing and manual testing will shrink in
scope. At the end of the sprint, the objective is that no more manual or
exploratory tests are required for the Sprint\'s deliverables.

Third layer
-----------

User Acceptance testing follows the previous activities and build on the
information already obtained. Contrary to popular belief, user
acceptance testing is not so much a testing activity as a
verification/confirmation one. The activities in user acceptance are
complementary to the previous testing activities and not a repeat.
 The verification and validation of fit to business and ability to
support the business processes (be it the application ones or the manual
ones) will lead to the ability to answer the question: \"Would this new
solution be able to support us and our members in the work that we need
to do?\".

Test Processes

After the Test Initiation each of the test activities contains the
following processes:

-   Test Planning

-   Test Design

-   Test Execution

-   Defect Management

-   Test Closure

These process are described to provide guidance to the team(s). It is
expected that processes will change, mature and otherwise evolve during
the course of the sprints and the project.

 

 

Test Initiation Process

June 24, 2019

3:01 PM

Test Initiation is the first stage of software testing life-cycle
process. In this stage, the Test Strategy information will be created.
This is a business level document which informs the Managers, Developers
and Testers about the testing process, the approach and direction. 

RASCI

  **Roles**                        **Responsible**   **Approves/Accountable**   **Supports**   **Consulted**   **Informed**
  -------------------------------- ----------------- -------------------------- -------------- --------------- --------------
  **Test Lead**                    X                                                                            
  **Test Analyst (Agile)**                                                                     X                
  **Business Tester**                                                                          X                
  **Test Automation Specialist**                                                               X                
  **Business Analyst**                                                                         X                
  **Business Lead**                                                                            X                
  **Developer**                                                                                                 X
  **Developer Lead**                                                                           X                
  **Solution Architect**                                                                       X                
  **Release Manager**                                                                           X               
  **Project Manager**                                X                                                          
  **Client/Sponsor**                                 X                                                          

Objectives

-   Create clarity and direction on:

-   Test processes

-   Approach

-   Planned Test activities

-   Resource requirements

-   Tools and infrastructure

-   Obtain client approval

Description

During the test initiation process we consult, discuss and review. Since
the agile approach is new to BCPC, it makes sense to spend time upfront
thinking about the ramifications for testing.

We need to find the balance between:

-   Project Goals

-   Constraints

-   Existing practices/knowledge

-   Efficiency

The test initiation for PPR will yield a large amount of guidance that
at this phase seems to be needed. The actual project experience will
adjust to what is actually needed and used. Still we are stating a clear
starting point to develop understanding and to obtain agreement.

**Steps**

  **Step**               **Participant(s)**                                        **Description**
  ---------------------- --------------------------------------------------------- -----------------------------------------------------------------
  Investigation          Test Lead                                                 Understanding scope, constraints, existing guidance, objectives
  Consultation           Test Lead, Client, Business, Testers                      Clarifying, discussing approach
  Creation of strategy   Test Lead                                                 Writing the actual Test Strategy
  Review                 Test Lead, Business, Client, Testers, Project Team, CGI   Broad review leading up to be ready for approval.
  Approval               Client/Sponsor                                            Based on endorsements obtained from the review process.

 

 

Test Planning Process

June 24, 2019

3:02 PM

Test Planning determines the scope, approach, resources and schedule of
testing activities within the sprint.

Test planning is essential in:

-   ensuring testing identifies and reveals as many errors in the
    > software as possible

-   bringing software to an acceptable level of quality

-   giving efficiency regarding scope, budgetary and scheduling
    > limitations.

 

Test planning spans our Test Initiation, Test Planning and Test
Design processes. Detailed Test plans will be created at Sprint planning
time before and refined during the sprint.

RASCI

  **Roles**                        **Responsible**   **Approves/Accountable**   **Supports**   **Consulted**   **Informed**
  -------------------------------- ----------------- -------------------------- -------------- --------------- --------------
  **Test Lead**                    X                                                                            
  **Test Analyst (Agile)**                                                                     X                
  **Business Tester**                                                                          X                
  **Test Automation Specialist**                                                               X                
  **Business Analyst**                                                                                         X 
  **Business Lead**                                                                            X                
  **Developer**                                                                                                 X
  **Developer Lead**                                                                           X                
  **Solution Architect**                                                                                       X 
  **Release Manager**                                                                           X               
  **Project Manager**                                X                                                          
  **Client/Sponsor**                                                                           X                

Objective

-   Define Scope

-   Define Test Approach (based on the Test Strategy set out here)

-   Define resource needs

-   Create schedule

Description

The following describes a largely common approach to the test planning
process but supplemented with the agile project context.

Test planning will not be just an activity at the beginning of the
sprint, it will have to be part of the agile planning and re-planning
process. It is therefore important to identify what can be planned
upfront and where we need to be agile.

**High-level Test Planning**

This is the activity that describes the \"who, what, when, where, and
how\" of the test. Test plans can be developed at a variety of levels,
for instance for a whole project, a sprint or even a specific testing
activity in a sprint. The high-level test plan will show which functions
and quality attributes of the application are to be tested. In the PPR
Project, we create test plans per Sprint.

**Planning Tasks**

+-------+--------------+--------------+--------------+--------------+
| ** ** | **Task**     | **D          | **Outcome**  | **           |
|       |              | escription** |              |  Frequency** |
+=======+==============+==============+==============+==============+
| 1     | Define Test  | Determines   | Clearly      | Before the   |
|       | Objectives   | at a high    | delineated   | Sprint       |
|       |              | level what   | objectives   | starts,      |
|       |              | is to be     | which can be | typically in |
|       |              | tested. This | reviewed and | pre-sprint   |
|       |              | is based on  | c            | planning.    |
|       |              | defined      | ommunicated. | But          |
|       |              |  requirement |              | objectives   |
|       |              | s/acceptance |              | may need to  |
|       |              | criteria,    |              | be adjusted  |
|       |              | no           |              | when changes |
|       |              | n-functional |              | to sprint    |
|       |              | r            |              | scope and    |
|       |              | equirements, |              | objectives   |
|       |              | business     |              | are needed.  |
|       |              | events and   |              |              |
|       |              | processes.   |              | The          |
|       |              |              |              | definition   |
|       |              |              |              | of the       |
|       |              |              |              | objectives   |
|       |              | Risk         |              | will be      |
|       |              | Analysis     |              | subject to   |
|       |              | will play a  |              | review       |
|       |              | role during  |              | during the   |
|       |              | the          |              | in-sprint    |
|       |              | id           |              | planning     |
|       |              | entification |              | exercises.   |
|       |              | of the       |              |              |
|       |              | objectives.  |              |              |
|       |              | With regards |              |              |
|       |              | to           |              |              |
|       |              | th           |              |              |
|       |              | e acceptance |              |              |
|       |              | crit         |              |              |
|       |              | eria testing |              |              |
|       |              | we follow    |              |              |
|       |              | the risk and |              |              |
|       |              | priority     |              |              |
|       |              | settings     |              |              |
|       |              | from the     |              |              |
|       |              | business     |              |              |
|       |              | team.        |              |              |
|       |              |              |              |              |
|       |              | Additional   |              |              |
|       |              | test         |              |              |
|       |              | objectives   |              |              |
|       |              | are related  |              |              |
|       |              | to:          |              |              |
|       |              |              |              |              |
|       |              | -   Test     |              |              |
|       |              |              |              |              |
|       |              | > Automation |              |              |
|       |              |              |              |              |
|       |              | -   Test     |              |              |
|       |              |     > Data   |              |              |
|       |              |              |              |              |
|       |              | > Management |              |              |
|       |              |              |              |              |
|       |              | -   System   |              |              |
|       |              |     > Test,  |              |              |
|       |              |              |              |              |
|       |              |   > Security |              |              |
|       |              |     > Test   |              |              |
|       |              |     > etc.   |              |              |
+-------+--------------+--------------+--------------+--------------+
| 2     | Identify     | Fine tune    | Dependable   | Pre-Sprint   |
|       | Needed       | the          | resource     | during the   |
|       | Resources    | resources    | planning     | planning.    |
|       |              | needed for   |              | Resource     |
|       |              | the sprint.  |              | usage will   |
|       |              | The general  |              | be reviewed  |
|       |              | requirement  |              | at the end   |
|       |              | has been     |              | of each      |
|       |              | documented   |              | sprint to    |
|       |              | in the Test  |              | see if any   |
|       |              | Strategy but |              | adjustments  |
|       |              | since no     |              | need to be   |
|       |              | sprint is    |              | made.        |
|       |              | exactly the  |              |              |
|       |              | same, the    |              |              |
|       |              | resource     |              |              |
|       |              | requirements |              |              |
|       |              | needs to be  |              |              |
|       |              | revisited on |              |              |
|       |              | a sprint by  |              |              |
|       |              | sprint       |              |              |
|       |              | basis.       |              |              |
+-------+--------------+--------------+--------------+--------------+
| 3     | Plan Test    | Determine    | Prepared     | Pre-Sprint   |
|       | Environment  | where we     | environment  | during the   |
|       |              | will test    |              | planning.    |
|       |              | and what     |              | Environment  |
|       |              | needs to be  |              | usage will   |
|       |              | available in |              | be reviewed  |
|       |              | the          |              | at the end   |
|       |              | environment. |              | of each      |
|       |              | Every sprint |              | sprint to    |
|       |              | will have    |              | see if any   |
|       |              | different or |              | adjustments  |
|       |              | increased    |              | need to be   |
|       |              | requirements |              | made.        |
|       |              | and would    |              |              |
|       |              | require a    |              |              |
|       |              | review       |              |              |
|       |              | upfront to   |              |              |
|       |              | make sure    |              |              |
|       |              | that the     |              |              |
|       |              | testers can  |              |              |
|       |              | start their  |              |              |
|       |              | work.        |              |              |
+-------+--------------+--------------+--------------+--------------+
| 4     | Define Test  | Based on     | High level   | First cut at |
|       | Proce        | scope and    | organi       | pre-Sprint   |
|       | dures/Suites | objectives   | zation/scope | during the   |
|       |              | we will plan | of our       | planning.    |
|       |              | the test     | testing      | The final    |
|       |              | procedures.  |              | cut during   |
|       |              |              |              | the first    |
|       |              |              |              | week of the  |
|       |              |              |              | Sprint.      |
|       |              | In our test  |              |              |
|       |              | management   |              |              |
|       |              | tool, we     |              |              |
|       |              | will use the |              |              |
|       |              | test suite   |              |              |
|       |              | concept to   |              |              |
|       |              | capture      |              |              |
|       |              | this.        |              |              |
+-------+--------------+--------------+--------------+--------------+
| 5     | Identify     | We identify  | Specific     | Developed    |
|       | Functions to | the          | id           | starting     |
|       | be Tested    | functions to | entification | with the     |
|       |              | be tested by | of           | sprint but   |
|       |              | reviewing    | application  | will most    |
|       |              | our test     | and system   | likely       |
|       |              | base         | functions    | change       |
|       |              | (do          | that will be | depending on |
|       |              | cumentation, | tested       | changes      |
|       |              | discussion   |              |              |
|       |              | etc.) and    |              |              |
|       |              | map the      |              |              |
|       |              | functions to |              |              |
|       |              | be tested to |              |              |
|       |              | our test     |              |              |
|       |              | suites       |              |              |
+-------+--------------+--------------+--------------+--------------+
| 6     | Identify     | We identify  | Specific     | Developed    |
|       | Interfaces   | the          | id           | starting     |
|       | to be Tested | interfaces   | entification | with the     |
|       |              | to be tested | of           | sprint but   |
|       |              | by reviewing | interfaces   | will most    |
|       |              | our test     | and          | likely       |
|       |              | base         | integration  | change       |
|       |              | (technical   | points that  | depending on |
|       |              | do           | will be      | changes      |
|       |              | cumentation) | tested       |              |
|       |              | and map the  |              |              |
|       |              | interfaces   |              |              |
|       |              | to be tested |              |              |
|       |              | to our test  |              |              |
|       |              | suites       |              |              |
+-------+--------------+--------------+--------------+--------------+
| 7     | Write Test   | Individual   | Test         | These will   |
|       | Scripts /    | scripts and  | S            | be           |
|       | Define Tests | tests cases  | cripts/Cases | developed,   |
|       | Cases /      | will be      | and          | maintained   |
|       | Define       | written. A   | exploratory  | and pruned   |
|       | Exploratory  | test case is | testing      | during the   |
|       | Testing      | the lowest   | sessions     | sprint.      |
|       | sessions     | level of     | which are    |              |
|       |              | test that is | ready to be  |              |
|       |              | intended to  | executed     |              |
|       |              | test one     |              |              |
|       |              | thing and    |              |              |
|       |              | one thing    |              |              |
|       |              | only.        |              |              |
|       |              |              |              |              |
|       |              |              |              |              |
|       |              |              |              |              |
|       |              | During this  |              |              |
|       |              | exercise we  |              |              |
|       |              | will also    |              |              |
|       |              | i            |              |              |
|       |              | dentify test |              |              |
|       |              | automation   |              |              |
|       |              |  candidates. |              |              |
+-------+--------------+--------------+--------------+--------------+
| 8     | Design Test  | Every test   | Test data is | This will be |
|       | Data         | case needs   | identified   | developed,   |
|       |              | test data,   | and/or       | maintained   |
|       |              | this data is | created      | and pruned   |
|       |              | either       |              | during the   |
|       |              | identified   |              | sprint.      |
|       |              | in the       |              |              |
|       |              | already      |              |              |
|       |              | present data |              |              |
|       |              | or needs to  |              |              |
|       |              | be created   |              |              |
|       |              | from scratch |              |              |
+-------+--------------+--------------+--------------+--------------+
| 9     | Build Test   | The Test     | Traceability | This will be |
|       | Matrix       | requirement  | matrix is    | developed,   |
|       |              | coverage     | present and  | maintained   |
|       |              | matrix is    | will allow   | and pruned   |
|       |              | build up     | for          | during the   |
|       |              | during the   | management   | sprint.      |
|       |              | definition   | of progress  |              |
|       |              | of the       | and coverage |              |
|       |              | suites, and  |              |              |
|       |              | the          |              |              |
|       |              | individual   |              |              |
|       |              | test         |              |              |
|       |              | sc           |              |              |
|       |              | ripts/cases. |              |              |
|       |              | The          |              |              |
|       |              | integration  |              |              |
|       |              | between JIR  |              |              |
|       |              | A and Zephyr |              |              |
|       |              | and the      |              |              |
|       |              | project\'s   |              |              |
|       |              | practice to  |              |              |
|       |              | capture      |              |              |
|       |              | requirements |              |              |
|       |              | and          |              |              |
|       |              | acceptance   |              |              |
|       |              | criteria     |              |              |
|       |              | allows the   |              |              |
|       |              | project to   |              |              |
|       |              | build up     |              |              |
|       |              | such a       |              |              |
|       |              | matrix in an |              |              |
|       |              | efficient    |              |              |
|       |              | way as it is |              |              |
|       |              | a natural    |              |              |
|       |              | outcome of   |              |              |
|       |              | the way we   |              |              |
|       |              | work with    |              |              |
|       |              | our tools.   |              |              |
+-------+--------------+--------------+--------------+--------------+
| 10    | Determine    | Based on     | Defined      | First cut at |
|       | Test         | test         | schedule     | pre-Sprint   |
|       | Schedules    | objectives,  | will allow   | during the   |
|       |              | planned      | us to start  | planning.    |
|       |              | availability | the effort   | The test     |
|       |              | of testable  | with         | schedule     |
|       |              | fu           | reasonable   | will be      |
|       |              | nctionality, | confidence.  | subject to   |
|       |              | resources,   |              | review and   |
|       |              | test data    |              | change       |
|       |              | and test     |              | during the   |
|       |              | design       |              | in-sprint    |
|       |              | readiness,   |              | planning     |
|       |              | we will      |              | exercises.   |
|       |              | create our   |              |              |
|       |              | initial test |              |              |
|       |              | schedule.    |              |              |
+-------+--------------+--------------+--------------+--------------+

 

 

Test Design Process

June 24, 2019

3:02 PM

-   Test design is the act of creating and writing test suites for
    > testing a software.

> Designing efficient tests is an analytic process that requires
> information, skills, communication, a critical eye and an awareness of
> constraints and risks.
>
> RASCI

  **Roles**                        **Responsible**   **Approves/Accountable**   **Supports**   **Consulted**   **Informed**
  -------------------------------- ----------------- -------------------------- -------------- --------------- --------------
  **Test Lead**                                      X                                                          
  **Test Analyst (Agile)**          X                                                                           
  **Business Tester**               X                                                                           
  **Test Automation Specialist**    X                                                                           
  **Business Analyst**                                                          X                               
  **Business Lead**                                                             X                               
  **Developer**                     X                                                                           
  **Developer Lead**                                  X                                                         
  **Solution Architect**                                                                                       X
  **Release Manager**                                                                                          X
  **Project Manager**                                                                                          X
  **Client/Sponsor**                                                                           X                

> Objective

-   Obtain efficient test cases

-   Obtain full coverage for all functionality and processes with Test
    > cases

-   Obtain a basis for test automation

> Description
>
> Testing software is a real challenge, because there are so many types
> of test cases that come in so many different shapes and sizes. The
> truth is, there is no "one size fits all" method for software testing.
> Our project lends itself to a more casual, exploratory approach, where
> agile test cases are helpful. But with our strong test automation
> drive and with an eye for existing practices at PPR, we will design
> test cases that will combine the exploratory testing, manual test case
> and test automation aspects.
>
> Documenting software test cases is required when you have to conform
> to specific business rules. The project may have legal compliance
> requirements, or there may even be contractual obligations to provide
> documentary evidence of exactly what you tested. In that scenario, you
> obviously need detailed test cases. The PPR application will be in use
> for years, a set of well-thought-out agile test cases will provide
> value for money because they'll be reused again and again. They will
> even form the basis for automated tests. 
>
> **Challenges of Test Design in an Agile Environment**
>
> In cases where the project team is adopting an agile approach
> (i.e. features are designed in an iterative fashion) there is no clear
> picture for the application during any one sprint. Generally we find
> that the initial goal at the start of development changes as backlogs
> are revised (i.e. the sprint requirements change). Writing a lot of
> agile test cases then is going to be less effective because you'll
> have to rewrite them completely within a few builds. You might opt for
> a checklist approach instead and combine exploratory testing with a
> simple list of compatibility requirements that don't need to be
> spelled out in full. It may even be possible for testers simply to
> refer to the original user stories that informed the design or talk
> directly to the customer to find a basis for their testing.
>
> In PPR, we will adopt a hybrid approach where much of the actual
> business design, user stories and acceptance criteria have been
> developed and reviewed before the Sprint. This will allow testing to
> leverage the created information to help with the test design.
>
> **Test Basis**
>
> The test basis is the information available (or to be acquired) that
> we base our tests on.
>
> For PPR our test base is:

-   Project scope as defined by our product owner

-   User Stories, see Epics, Features & User Stories

-   Acceptance Criteria (part of the user stories), see Epics, Features
    > & User Stories

-   Non-functional requirements

-   Discussions and decisions on the above captured in JIRA

-   Feedback from SME\'s, Business Analysts, Architects and technical
    > specialists

-   Testers\' insight and experience with PPR business processes

-   Good testing practices

-   Constraints, Risks and Changes

-   Creativity and the drive to create efficient tests

> **Test Case Design**
>
> Test case design is based on:

-   The stated, explicit requirements for the feature

-   The unstated, implied requirements

-   The expected behavior of the feature

-   The constraints imposed on the behavior of that feature

> **Test Case Design Techniques**
>
> Of all the test case design techniques which are available, the most
> effective for the PPR project are:

-   Specification-based technique.  This technique derives test cases
    > from the documented specifications of the system's behavior.

-   Functional analysis (functional specification-based testing).

-   Sampling techniques.  These techniques identify small samples of
    > high-potential test cases from large populations of possible
    > conditions.

-   Equivalence

-   Boundary value (BV)

-   Combinatorial methods, such as pair-wise and n-wise testing

-   Experience-based techniques.  These techniques utilize the testers'
    > and others' experience, either with the system under test or in
    > prior similar situations. 

-   Exploratory testing

-   User scenarios

-   Checklists

-   Risk analysis and prioritization.

> **Process**
>
> Test Design approach is indicated by the following steps:

  ** **   **Activity**                                  **Technique Used**                                        **Description**
  ------- --------------------------------------------- --------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  1       Test Basis Analysis                           Review documentation and other test basis artifacts.      This activity identifies gaps, generates questions and develops a initial understanding.
  2       First Identification of major test areas      Sprint Scope/Schedule, Risk Analysis and prioritization   Reviewing schedule and planned scope of work for the Sprint, the major areas of interest can be identified.
  3       Test Idea generation                          Risk Analysis                                             Initial series of test ideas, exploratory sessions and application of other techniques are identified.
  4       Drafting of test cases/exploratory sessions   All previously obtained information is used               The high level test case and suites (groups of test cases that belong to the same logical group) are created. Also this is the time when we plan our sessions for exploratory sessions
  5       Adding detail to test cases                   All design techniques                                     Using the appropriate test design technique, test cases will be expanded and added to.
  6       Identify test steps for each test case        Review of the actual functionality                        If needed, test steps will be added to the test case. In the project we will minimize this step as test steps typically are very labor-intensive and add very little value.
  7       Identify candidacy for test automation        See Test Automation Strategy                              At an early stage we label test cases as test automation candidates. We make sure that the test case contains enough information for automation scripting to commence.
  8       Review Test Cases                             Peer review                                               Peer review is a powerful technique and is very appropriate in a agile project.
  9       Consolidate Test Cases in Test Suites         Functional Analysis and Risk Analysis                     Test cases are grouped in logical block.

> These steps will be repeated several times based on the following
> triggers:

-   New design becomes available

-   A change to design invalidates previous test design

-   Scope changes

-   Bug Fixes

> **Test Case Rating**
>
> Test case rating or priority setting is important for the following
> reasons:

-   It focuses the testers on those tests that will make the most
    > difference

-   It will allow for better and more efficient re-planning

-   It helps with the tester workload assignment

-   It greatly helps the team to achieve working (and verified)
    > functionality

-   It will allow for test automation candidates selection

> Rating a test case is about rating the aspect of the function that the
> test case intends to test. We can obtain much of our guidance from how
> the user stories have been rated. Critical-rated user stories will
> elevate the rating for the associated test cases.
>
> Here are the risk/priority attributes that we take into consideration
> when rating our test cases:

  **Aspect to be Tested is**         **Description**                                                                                                                                                                          **High**                                                                            **Medium**                                                                          **Low**
  ---------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------- ----------------------------------------------------------------------------------- --------------------------------------------------------------------------
  Frequently tested by other tests   Aspects that are tested many times are often navigational tests, login etc.                                                                                                              Rate if tested more than 3 times in other tests                                     Rate if tested more than 0 but lower or equal than 3                                Rate if not tested yet
  Well understood                    Aspects that are clear to the tester because sufficient documentation/guidance is present                                                                                                Rate if completely understood                                                       Rate if some questions are still outstanding                                        Rate if none of the questions are answered or the answers remain unclear
  Mission-Critical                   Aspects that are mission-critical, without this functioning the solution would not be viable. Guidance for this rating attribute can be obtained from the User Story priority setting.   Rate if the solution would not be viable                                            Rate where the solution would be impeded but workarounds could be available         Rate when the aspect is a nice-to-have for the solution
  Risky                              Aspects that pose is risk to the business, security, confidentially, finance etc.                                                                                                        Rate if one or more high/critical risks are identified                              Rate if one or more medium risks are identified                                     Rate if no or only low risks are identified
  Used Frequently                    Aspects that are used frequently.                                                                                                                                                        Rate if used multiple times per user session                                        Rate if used only once per user session                                             Rate if only used occasionally
  Complex                            Aspects that are complex, have many business rules, calculations, need to be precise etc.                                                                                                Rate if contains calculations, more than 3 decisions, validations or data updates   Rate if contains calculations, more than 1 decisions, validations or data updates   Rate if contains no calculations, decisions, validations or data updates
  is dependent or has dependencies   Aspects that require other components or functionalities to be present in order to function. Or aspects that other functionality is dependent on.                                        Rate if there are multiple dependencies that are needed to operate                  Rate if there is one dependency that is needed to operate                           Rate if there are no dependencies

> The following spreadsheet utility is used to obtain guidance for our
> test case rating. This has been created for consistency sake and its
> value will be evaluated after Sprint 1.
>
> The rating that the spreadsheet will come up with is the
> standard *test case priority* setting in Zephyr.  (TBD)

  **Test Case Priority**   **Description**
  ------------------------ ------------------------------------------------------------------------------------------------------------------------
  **Test Case Priority**   **Description**
  1-Don\'t Test            No need to test, this would apply to test cases that were maybe introduced at a time where not all details were clear.
  2-Maybe                  Can be included in the test runs, but would be one of the first to be dropped if time and scope demands a reduction.
  3-If Time                Typical candidate be included in the test runs, but could be de-scoped.
  4-Must be Tested         Mandatory to test, key functionality or higher risk test case. Would typically not be de-scoped even under pressure.
  5-Critical               Mandatory. Without this test case the risk exists that critical functionality is not working correctly.

>  
>
>  

  **Test Case Priority Analysis**                                                                   
  ---------------------------------- ------------ ------------ --------- --------- ----------- --- ------------------
                                     **Rating**                                                     
  **Aspect to be Tested**            **High**     **Medium**   **Low**   **N/A**                    
  Frequently tested by other tests                                                 0                
  Well understood                                                                  0                
  Mission-Critical                                                                 0                
  Risky                                                                            0                
  Used Frequently                                                                  0                
  Complex                                                                          0                
  is dependent or has dependencies                                                 0                
  **Test Case Priority Guidance**                                                  **\#N/A**        
                                                                                               1   1-Don\'t Test
                                                                                               2   2-Maybe
                                                                                               3   3-If Time
                                                                                               4   4-Must be Tested
                                                                                               5   5-Critical

> Test Case Rating Review
>
> The ratings can be changed after review at the end of every Sprint or
> when ever it is deemed needed. As test case rating is a tool, we need
> to make sure that we keep our tool sharp and relevant.

 

 

Test Execution Process

June 24, 2019

3:03 PM

Test execution is the process of executing the code (running the
application) and comparing the expected and actual results.

 

RASCI

  **Roles**                        **Responsible**   **Approves/Accountable**   **Supports**   **Consulted**   **Informed**
  -------------------------------- ----------------- -------------------------- -------------- --------------- --------------
  **Test Lead**                                      X                                                          
  **Test Analyst (Agile)**          X                                                                           
  **Business Tester**               X                                                                           
  **Test Automation Specialist**    X                                                                           
  **Business Analyst**                                                          X                               
  **Business Lead**                                                                                             
  **Developer**                     X                                                                           
  **Developer Lead**                                  X                                                         
  **Solution Architect**                                                                                       X
  **Release Manager**                                                           X                              X
  **Project Manager**                                                                                          X
  **Client/Sponsor**                                                                           X                

Objective

-   Obtain application Quality Status information

-   Find defects

-   Verify and Validate the solution

* **V & V***

*Verification - "Have we built the product right?" and Validation -
"Have we built the right product?" *

Description

In the project there are 5 groups/mechanisms involved with test
execution. They are:

1.  Developers - Manual/Automated Unit Test on their workstation
    > (iValua)

2.  Agile Testers - Manual and Exploratory Tests in the TEST environment

3.  Test Automation Specialist - Automated functional testing in the
    > TEST environment

4.  User Acceptance Testers - UAT in the TEST environment

**Automated Test Execution Process**

The process is described in the following chart that shows the different
systems, activities and parties involved:

**tbd**

**The Manual Test Execution Process**

The manual and exploratory test execution steps are as follows:

  **Activity**                           **When/Frequency**                                                                                                                                                                                                                      **Participant**
  -------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------
  Manual Unit Testing                    All throughout the development process.                                                                                                                                                                                                 Developer
  Manual Testing of defined test cases   Once a targeted functionality becomes available. This will need to be repeated in case of defects and changes. The manual tests will be transformed into automated tests and the necessity for a tester to run the test will go away.   Agile Testers
  Exploratory Testing                    Once a targeted functionality becomes initially available. The exact exploratory test will not be repeated, but variations on it can be in case of changes. Exploratory testing is also meant to generate ideas for test automation.    Agile Testers
  User Acceptance Testing                In the last 7 work days of the Sprint and close to the release date, user acceptance testers will manually execute their test cases and scenarios. In case of defects, they would need to repeat.                                       Tester/Business Analyst

**Requirements for Test Execution**

 For manual test execution, the following needs to present:

-   Targeted functionality is available in the TEST or STAGING
    > environment

-   Test Cases are ready or a Exploratory Test Session has been defined

-   Test Cases have been assigned and the go ahead has been given by the
    > test lead

-   Test Data is present/identified

> For automated test execution, the following needs to present:

-   Targeted functionality is available in the TEST environment

-   Automated Unit Test and/or Functional Test Scripts have been
    > created, debugged and incorporated into the test framework

-   Test Data is present/identified

-   The automated test execution run is cleared to go by test lead 

 

 

Defect Management Process

June 24, 2019

3:03 PM

RASCI

  **Roles**                        **Responsible**   **Approves/Accountable**   **Supports**   **Consulted**   **Informed**
  -------------------------------- ----------------- -------------------------- -------------- --------------- --------------
  **Test Lead**                                      X                                                          
  **Test Analyst (Agile)**          X                                                                           
  **Business Tester**               X                                                                           
  **Test Automation Specialist**    X                                                                           
  **Business Analyst**              X                                                                           
  **Business Lead**                 X                                                                           
  **Developer**                     X                                                                           
  **Developer Lead**                X                                                                           
  **Solution Architect**                                                        X                               
  **Release Manager**              X                                                                           X
  **Project Manager**                                                           X                               
  **Client/Sponsor**                                                                                           X

Objective

Define the defect management process to support efficient handling and
documentation of defects found during sprints.

Description

Documented defects are the main output of the testing team, it is this
information that will allow the team to achieve its goals and identify
anything that might need to be added to the backlog.

Defect reports need to be:

-   Objective

-   Factual

-   Concise

-   Complete

-   Precise

Defect reports will need to stand the test of time and geographic
distance as not all defects will be fixed immediately, we need to
provide full context, discussion and details. In other words the defect
description should be actionable.

Our tool set (JIRA) allows for configuration of the defect management
workflow that will support consistent tracking and reportability.

Defect Management Workflow

![](media/image3.png){width="9.738888888888889in"
height="7.530555555555556in"}

 

 

+----------+----------+----------+----------+----------+----------+
| **Step** | **       | **Tran   | **R      | **Descr  | **Action |
|          | Status** | sition** | esulting | iption** | By**     |
|          |          |          | Status** |          |          |
+==========+==========+==========+==========+==========+==========+
| **Open** | Open     |          |          | Opening  | Anybody, |
|          |          |          |          | of a new | but      |
|          |          |          |          | Defect   | mainly   |
|          |          |          |          |          | testers  |
+----------+----------+----------+----------+----------+----------+
| ** **    | Open     | Ready    | In       | Once the | The      |
|          |          | For      | Review   | defect   | defect   |
|          |          | Review   |          | has been | reporter |
|          |          |          |          | do       |          |
|          |          |          |          | cumented |          |
|          |          |          |          | it will  |          |
|          |          |          |          | be       |          |
|          |          |          |          | s        |          |
|          |          |          |          | ubmitted |          |
|          |          |          |          | for      |          |
|          |          |          |          | review.  |          |
|          |          |          |          | No       |          |
|          |          |          |          | action   |          |
|          |          |          |          | on the   |          |
|          |          |          |          | defect   |          |
|          |          |          |          | will     |          |
|          |          |          |          | happen   |          |
|          |          |          |          | until it |          |
|          |          |          |          | is       |          |
|          |          |          |          | labeled  |          |
|          |          |          |          | \"Ready  |          |
|          |          |          |          | for      |          |
|          |          |          |          | R        |          |
|          |          |          |          | eview\", |          |
|          |          |          |          | this     |          |
|          |          |          |          | will     |          |
|          |          |          |          | allow    |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | reporter |          |
|          |          |          |          | to       |          |
|          |          |          |          | collect  |          |
|          |          |          |          | all the  |          |
|          |          |          |          | n        |          |
|          |          |          |          | ecessary |          |
|          |          |          |          | info     |          |
|          |          |          |          | rmation. |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Open     | Close    | Closed   | If it    | The      |
|          |          |          |          | turns    | defect   |
|          |          |          |          | out that | author   |
|          |          |          |          | the      | or test  |
|          |          |          |          | defect   | lead.    |
|          |          |          |          | wasn\'t  |          |
|          |          |          |          | a defect |          |
|          |          |          |          | or it    |          |
|          |          |          |          | was a    |          |
|          |          |          |          | du       |          |
|          |          |          |          | plicate, |          |
|          |          |          |          | misunder |          |
|          |          |          |          | standing |          |
|          |          |          |          | etc. the |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | closed   |          |
|          |          |          |          | imme     |          |
|          |          |          |          | diately. |          |
|          |          |          |          | Int      |          |
|          |          |          |          | eresting |          |
|          |          |          |          | to note  |          |
|          |          |          |          | is that  |          |
|          |          |          |          | we are   |          |
|          |          |          |          | not      |          |
|          |          |          |          | deleting |          |
|          |          |          |          | any      |          |
|          |          |          |          | defects  |          |
|          |          |          |          | as even  |          |
|          |          |          |          | the fact |          |
|          |          |          |          | of       |          |
|          |          |          |          | quickly  |          |
|          |          |          |          | closed   |          |
|          |          |          |          | defects  |          |
|          |          |          |          | is       |          |
|          |          |          |          | int      |          |
|          |          |          |          | eresting |          |
|          |          |          |          | and      |          |
|          |          |          |          | might    |          |
|          |          |          |          | feed     |          |
|          |          |          |          | into the |          |
|          |          |          |          | Sprint   |          |
|          |          |          |          | Retros   |          |
|          |          |          |          | pective. |          |
+----------+----------+----------+----------+----------+----------+
| **       | In       |          |          | During   | Test     |
| Review** | Review   |          |          | review   | Lead     |
|          |          |          |          | the test |          |
|          |          |          |          | lead     |          |
|          |          |          |          | does a   |          |
|          |          |          |          | quality  |          |
|          |          |          |          | and a    |          |
|          |          |          |          | quick    |          |
|          |          |          |          | sanity   |          |
|          |          |          |          | check on |          |
|          |          |          |          | the      |          |
|          |          |          |          | created  |          |
|          |          |          |          | defect   |          |
|          |          |          |          | report.  |          |
|          |          |          |          | A        |          |
|          |          |          |          | typical  |          |
|          |          |          |          | review   |          |
|          |          |          |          | does not |          |
|          |          |          |          | take a   |          |
|          |          |          |          | lot of   |          |
|          |          |          |          | time and |          |
|          |          |          |          | the test |          |
|          |          |          |          | lead     |          |
|          |          |          |          | will be  |          |
|          |          |          |          | able to  |          |
|          |          |          |          | do those |          |
|          |          |          |          | in mere  |          |
|          |          |          |          | seconds. |          |
|          |          |          |          |          |          |
|          |          |          |          | This QA  |          |
|          |          |          |          | gate     |          |
|          |          |          |          | ensures  |          |
|          |          |          |          | that an  |          |
|          |          |          |          | ac       |          |
|          |          |          |          | tionable |          |
|          |          |          |          | defect   |          |
|          |          |          |          | report   |          |
|          |          |          |          | is       |          |
|          |          |          |          | f        |          |
|          |          |          |          | orwarded |          |
|          |          |          |          | and will |          |
|          |          |          |          | cut down |          |
|          |          |          |          | on       |          |
|          |          |          |          | unn      |          |
|          |          |          |          | ecessary |          |
|          |          |          |          | back and |          |
|          |          |          |          | forth    |          |
|          |          |          |          | commu    |          |
|          |          |          |          | nication |          |
|          |          |          |          | between  |          |
|          |          |          |          | reporter |          |
|          |          |          |          | and      |          |
|          |          |          |          | de       |          |
|          |          |          |          | veloper. |          |
|          |          |          |          | With our |          |
|          |          |          |          | o        |          |
|          |          |          |          | ff-shore |          |
|          |          |          |          | dev      |          |
|          |          |          |          | elopment |          |
|          |          |          |          | group    |          |
|          |          |          |          | this is  |          |
|          |          |          |          | es       |          |
|          |          |          |          | sential. |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | In       | Return   | Open     | If the   | Test     |
|          | Review   | to       |          | defect   | Lead     |
|          |          | Reporter |          | report   |          |
|          |          |          |          | is found |          |
|          |          |          |          | lacking  |          |
|          |          |          |          | or       |          |
|          |          |          |          | in-ac    |          |
|          |          |          |          | tionable |          |
|          |          |          |          | it is    |          |
|          |          |          |          | returned |          |
|          |          |          |          | to the   |          |
|          |          |          |          | reporter |          |
|          |          |          |          | with the |          |
|          |          |          |          | request  |          |
|          |          |          |          | to       |          |
|          |          |          |          | update   |          |
|          |          |          |          | the      |          |
|          |          |          |          | info     |          |
|          |          |          |          | rmation. |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | In       | Ready    | Triage   | If the   | Test     |
|          | Review   | for      |          | test     | Lead     |
|          |          | Triage   |          | lead     |          |
|          |          |          |          | find the |          |
|          |          |          |          | defect   |          |
|          |          |          |          | report   |          |
|          |          |          |          | in good  |          |
|          |          |          |          | state,   |          |
|          |          |          |          | it can   |          |
|          |          |          |          | be       |          |
|          |          |          |          | tran     |          |
|          |          |          |          | sitioned |          |
|          |          |          |          | to the   |          |
|          |          |          |          | defect   |          |
|          |          |          |          | triage.  |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | In       | Close    | Closed   | If it    | Test     |
|          | Review   |          |          | turns    | Lead     |
|          |          |          |          | out that |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | wasn\'t  |          |
|          |          |          |          | a defect |          |
|          |          |          |          | or it    |          |
|          |          |          |          | was a    |          |
|          |          |          |          | du       |          |
|          |          |          |          | plicate, |          |
|          |          |          |          | misunder |          |
|          |          |          |          | standing |          |
|          |          |          |          | etc. the |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | closed.  |          |
+----------+----------+----------+----------+----------+----------+
| **       | Triage   |          |          | The      | Sprint   |
| Triage** |          |          |          | triage   | Team     |
|          |          |          |          | process  | Leads    |
|          |          |          |          | is meant |          |
|          |          |          |          | to       |          |
|          |          |          |          | discuss  |          |
|          |          |          |          | the      |          |
|          |          |          |          | course   |          |
|          |          |          |          | of       |          |
|          |          |          |          | action   |          |
|          |          |          |          | for      |          |
|          |          |          |          | defects  |          |
|          |          |          |          | that     |          |
|          |          |          |          | have     |          |
|          |          |          |          | just     |          |
|          |          |          |          | been     |          |
|          |          |          |          | r        |          |
|          |          |          |          | eported. |          |
|          |          |          |          | This is  |          |
|          |          |          |          | the      |          |
|          |          |          |          | process  |          |
|          |          |          |          | in which |          |
|          |          |          |          | the team |          |
|          |          |          |          | agrees   |          |
|          |          |          |          | on       |          |
|          |          |          |          | priority |          |
|          |          |          |          | for      |          |
|          |          |          |          | fixing   |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect.  |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Triage   | Complete | Triage   | During   | Test     |
|          |          | Triage   | C        | th       | Lead,    |
|          |          |          | ompleted | e Triage | Team     |
|          |          |          |          | mee      |          |
|          |          |          |          | ting the |          |
|          |          |          |          | inf      |          |
|          |          |          |          | ormation |          |
|          |          |          |          | is       |          |
|          |          |          |          | c        |          |
|          |          |          |          | ollected |          |
|          |          |          |          | to       |          |
|          |          |          |          | compete  |          |
|          |          |          |          | the      |          |
|          |          |          |          | triage   |          |
|          |          |          |          | for the  |          |
|          |          |          |          | issue.   |          |
|          |          |          |          | This     |          |
|          |          |          |          | d        |          |
|          |          |          |          | ocuments |          |
|          |          |          |          | de       |          |
|          |          |          |          | cisions, |          |
|          |          |          |          | assi     |          |
|          |          |          |          | gnments, |          |
|          |          |          |          | pri      |          |
|          |          |          |          | orities, |          |
|          |          |          |          | business |          |
|          |          |          |          | value    |          |
|          |          |          |          | etc.     |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Triage   | Assign   | Waiting  | Once the | Test     |
|          |          | to Fix   | for Fix  | triage   | Lead,    |
|          |          |          |          | is       | Team     |
|          |          |          |          | co       |          |
|          |          |          |          | mpleted, |          |
|          |          |          |          | valid    |          |
|          |          |          |          | defects  |          |
|          |          |          |          | that     |          |
|          |          |          |          | need to  |          |
|          |          |          |          | be fixed |          |
|          |          |          |          | will be  |          |
|          |          |          |          | assigned |          |
|          |          |          |          | to the   |          |
|          |          |          |          | Dev.     |          |
|          |          |          |          | Lead.    |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Triage   | Defer    | Deferred | If the   | Team     |
|          |          |          |          | defect   |          |
|          |          |          |          | is       |          |
|          |          |          |          | deemed   |          |
|          |          |          |          | out of   |          |
|          |          |          |          | scope    |          |
|          |          |          |          | for this |          |
|          |          |          |          | sprint   |          |
|          |          |          |          | but      |          |
|          |          |          |          | valid it |          |
|          |          |          |          | will be  |          |
|          |          |          |          | deferred |          |
|          |          |          |          | and will |          |
|          |          |          |          | end up   |          |
|          |          |          |          | on the   |          |
|          |          |          |          | backlog  |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Triage   | Close    | Closed   | If it    | Test     |
|          |          |          |          | turns    | Lead,    |
|          |          |          |          | out that | Team     |
|          |          |          |          | the      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | wasn\'t  |          |
|          |          |          |          | a defect |          |
|          |          |          |          | or it    |          |
|          |          |          |          | was a    |          |
|          |          |          |          | du       |          |
|          |          |          |          | plicate, |          |
|          |          |          |          | misunder |          |
|          |          |          |          | standing |          |
|          |          |          |          | etc. the |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | closed.  |          |
+----------+----------+----------+----------+----------+----------+
| **Assign | Waiting  |          |          | The      | Dev.     |
| to Fix** | for Fix  |          |          | defect   | Lead     |
|          |          |          |          | has been |          |
|          |          |          |          | assigned |          |
|          |          |          |          | to the   |          |
|          |          |          |          | Dev.     |          |
|          |          |          |          | Lead     |          |
|          |          |          |          | into the |          |
|          |          |          |          | fix      |          |
|          |          |          |          | queue    |          |
|          |          |          |          | for      |          |
|          |          |          |          | ass      |          |
|          |          |          |          | ignment. |          |
|          |          |          |          | After    |          |
|          |          |          |          | the      |          |
|          |          |          |          | ass      |          |
|          |          |          |          | ignment, |          |
|          |          |          |          | the      |          |
|          |          |          |          | d        |          |
|          |          |          |          | eveloper |          |
|          |          |          |          | sees the |          |
|          |          |          |          | defect   |          |
|          |          |          |          | in his   |          |
|          |          |          |          | task     |          |
|          |          |          |          | list.    |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Waiting  | Start    | In       | The      | D        |
|          | for Fix  | Work     | Progress | d        | eveloper |
|          |          |          |          | eveloper |          |
|          |          |          |          | starts   |          |
|          |          |          |          | work on  |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect,  |          |
|          |          |          |          | the \"In |          |
|          |          |          |          | Pr       |          |
|          |          |          |          | ogress\" |          |
|          |          |          |          | status   |          |
|          |          |          |          | i        |          |
|          |          |          |          | ndicates |          |
|          |          |          |          | to the   |          |
|          |          |          |          | dev lead |          |
|          |          |          |          | that the |          |
|          |          |          |          | d        |          |
|          |          |          |          | eveloper |          |
|          |          |          |          | is busy. |          |
+----------+----------+----------+----------+----------+----------+
| **       | In       |          |          | The      | D        |
| Fixing** | Progress |          |          | d        | eveloper |
|          |          |          |          | eveloper |          |
|          |          |          |          | starts   |          |
|          |          |          |          | the work |          |
|          |          |          |          | on       |          |
|          |          |          |          | fixing   |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect.  |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | In       | Finish   | Ready    | Once the | D        |
|          | Progress | Work     | for      | d        | eveloper |
|          |          |          | Va       | eveloper |          |
|          |          |          | lidation | is       |          |
|          |          |          |          | f        |          |
|          |          |          |          | inished, |          |
|          |          |          |          | he       |          |
|          |          |          |          | d        |          |
|          |          |          |          | ocuments |          |
|          |          |          |          | the fix  |          |
|          |          |          |          | and      |          |
|          |          |          |          | updates  |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | report.  |          |
|          |          |          |          | The      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | is now   |          |
|          |          |          |          | ready    |          |
|          |          |          |          | for      |          |
|          |          |          |          | va       |          |
|          |          |          |          | lidation |          |
|          |          |          |          | by       |          |
|          |          |          |          | testing  |          |
|          |          |          |          | (or the  |          |
|          |          |          |          | re       |          |
|          |          |          |          | porter). |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | In       | Back to  | Assign   | If the   | D        |
|          | Progress | Fix      | to Fix   | d        | eveloper |
|          |          | Queue    |          | eveloper |          |
|          |          |          |          | has too  |          |
|          |          |          |          | much     |          |
|          |          |          |          | work on  |          |
|          |          |          |          | his      |          |
|          |          |          |          | plate or |          |
|          |          |          |          | finds    |          |
|          |          |          |          | that     |          |
|          |          |          |          | this     |          |
|          |          |          |          | defect   |          |
|          |          |          |          | is not   |          |
|          |          |          |          | his, the |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | assigned |          |
|          |          |          |          | back to  |          |
|          |          |          |          | the Dev. |          |
|          |          |          |          | lead for |          |
|          |          |          |          | re-ass   |          |
|          |          |          |          | ignment. |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | In       | Return   | Triage   | If new   | D        |
|          | Progress | to       |          | inf      | eveloper |
|          |          | Triage   |          | ormation |          |
|          |          |          |          | emerges  |          |
|          |          |          |          | on the   |          |
|          |          |          |          | defect   |          |
|          |          |          |          | that     |          |
|          |          |          |          | would    |          |
|          |          |          |          | require  |          |
|          |          |          |          | the      |          |
|          |          |          |          | team\'s  |          |
|          |          |          |          | input    |          |
|          |          |          |          | and      |          |
|          |          |          |          | ass      |          |
|          |          |          |          | essment, |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | send     |          |
|          |          |          |          | back to  |          |
|          |          |          |          | triage.  |          |
|          |          |          |          |          |          |
|          |          |          |          | Reasons  |          |
|          |          |          |          | could    |          |
|          |          |          |          | be:      |          |
|          |          |          |          | Signi    |          |
|          |          |          |          | ficantly |          |
|          |          |          |          | more     |          |
|          |          |          |          | risk,    |          |
|          |          |          |          | missed   |          |
|          |          |          |          | requi    |          |
|          |          |          |          | rements, |          |
|          |          |          |          | defect   |          |
|          |          |          |          | exposes  |          |
|          |          |          |          | more     |          |
|          |          |          |          | issues   |          |
|          |          |          |          | etc.     |          |
+----------+----------+----------+----------+----------+----------+
| **Ready  | Ready    |          |          | The      | Test     |
| for      | for      |          |          | defect   | Lead     |
| Vali     | Va       |          |          | is now   |          |
| dation** | lidation |          |          | ready to |          |
|          |          |          |          | be       |          |
|          |          |          |          | assigned |          |
|          |          |          |          | to a     |          |
|          |          |          |          | tester   |          |
|          |          |          |          | (        |          |
|          |          |          |          | reporter |          |
|          |          |          |          | of       |          |
|          |          |          |          | defect)  |          |
|          |          |          |          | to       |          |
|          |          |          |          | validate |          |
|          |          |          |          | that the |          |
|          |          |          |          | issue    |          |
|          |          |          |          | was      |          |
|          |          |          |          | dealt    |          |
|          |          |          |          | with     |          |
|          |          |          |          | co       |          |
|          |          |          |          | rrectly. |          |
|          |          |          |          | This     |          |
|          |          |          |          | step is  |          |
|          |          |          |          | i        |          |
|          |          |          |          | mportant |          |
|          |          |          |          | because  |          |
|          |          |          |          | the test |          |
|          |          |          |          | env      |          |
|          |          |          |          | ironment |          |
|          |          |          |          | co       |          |
|          |          |          |          | ntaining |          |
|          |          |          |          | the fix  |          |
|          |          |          |          | might    |          |
|          |          |          |          | not be   |          |
|          |          |          |          | a        |          |
|          |          |          |          | vailable |          |
|          |          |          |          | just     |          |
|          |          |          |          | yet.     |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Ready    | Assign   | Va       | The      | Test     |
|          | for      | for      | lidating | as       | Lead     |
|          | Va       | Va       |          | signment |          |
|          | lidation | lidation |          | to the   |          |
|          |          |          |          | tester   |          |
|          |          |          |          | (re      |          |
|          |          |          |          | porting) |          |
|          |          |          |          | will be  |          |
|          |          |          |          | t        |          |
|          |          |          |          | riggered |          |
|          |          |          |          | by the   |          |
|          |          |          |          | avai     |          |
|          |          |          |          | lability |          |
|          |          |          |          | of the   |          |
|          |          |          |          | test     |          |
|          |          |          |          | env      |          |
|          |          |          |          | ironment |          |
|          |          |          |          | co       |          |
|          |          |          |          | ntaining |          |
|          |          |          |          | the fix. |          |
|          |          |          |          | And even |          |
|          |          |          |          | though   |          |
|          |          |          |          | we build |          |
|          |          |          |          | new      |          |
|          |          |          |          | versions |          |
|          |          |          |          | conti    |          |
|          |          |          |          | nuously, |          |
|          |          |          |          | a        |          |
|          |          |          |          | cons     |          |
|          |          |          |          | olidated |          |
|          |          |          |          | new      |          |
|          |          |          |          | version  |          |
|          |          |          |          | for QA   |          |
|          |          |          |          | will not |          |
|          |          |          |          | be       |          |
|          |          |          |          | a        |          |
|          |          |          |          | vailable |          |
|          |          |          |          | as       |          |
|          |          |          |          | fre      |          |
|          |          |          |          | quently. |          |
+----------+----------+----------+----------+----------+----------+
| **Vali   | Va       |          |          | During   | Tester   |
| dating** | lidating |          |          | the      |          |
|          |          |          |          | va       |          |
|          |          |          |          | lidating |          |
|          |          |          |          | step,    |          |
|          |          |          |          | the      |          |
|          |          |          |          | tester   |          |
|          |          |          |          | will     |          |
|          |          |          |          | validate |          |
|          |          |          |          | the      |          |
|          |          |          |          | fixed    |          |
|          |          |          |          | defect.  |          |
|          |          |          |          | The      |          |
|          |          |          |          | tester   |          |
|          |          |          |          | would    |          |
|          |          |          |          | only     |          |
|          |          |          |          | start    |          |
|          |          |          |          | the      |          |
|          |          |          |          | va       |          |
|          |          |          |          | lidation |          |
|          |          |          |          | if the   |          |
|          |          |          |          | defect   |          |
|          |          |          |          | was      |          |
|          |          |          |          | assigned |          |
|          |          |          |          | to him.  |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Va       | Pass     | Closed   | If the   | Tester   |
|          | lidating |          |          | defect   |          |
|          |          |          |          | fix was  |          |
|          |          |          |          | correct, |          |
|          |          |          |          | the      |          |
|          |          |          |          | tester   |          |
|          |          |          |          | will     |          |
|          |          |          |          | indicate |          |
|          |          |          |          | \        |          |
|          |          |          |          | "Pass\". |          |
|          |          |          |          | This     |          |
|          |          |          |          | will     |          |
|          |          |          |          | autom    |          |
|          |          |          |          | atically |          |
|          |          |          |          | close    |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect.  |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Va       | Fail     | Assign   | If the   | Tester   |
|          | lidating |          | to Fix   | defect   |          |
|          |          |          |          | fix was  |          |
|          |          |          |          | not      |          |
|          |          |          |          | correct, |          |
|          |          |          |          | the      |          |
|          |          |          |          | tester   |          |
|          |          |          |          | will     |          |
|          |          |          |          | indicate |          |
|          |          |          |          | \"Fail\" |          |
|          |          |          |          | and the  |          |
|          |          |          |          | defect   |          |
|          |          |          |          | will     |          |
|          |          |          |          | autom    |          |
|          |          |          |          | atically |          |
|          |          |          |          | be       |          |
|          |          |          |          | assigned |          |
|          |          |          |          | back to  |          |
|          |          |          |          | the Dev. |          |
|          |          |          |          | lead in  |          |
|          |          |          |          | status   |          |
|          |          |          |          | \"Assign |          |
|          |          |          |          | to Fix\" |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Va       | Return   | Triage   | If new   | Tester   |
|          | lidating | to       |          | inf      |          |
|          |          | Triage   |          | ormation |          |
|          |          |          |          | emerges  |          |
|          |          |          |          | on the   |          |
|          |          |          |          | defect   |          |
|          |          |          |          | that     |          |
|          |          |          |          | would    |          |
|          |          |          |          | require  |          |
|          |          |          |          | the      |          |
|          |          |          |          | team\'s  |          |
|          |          |          |          | input    |          |
|          |          |          |          | and      |          |
|          |          |          |          | ass      |          |
|          |          |          |          | essment, |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | send     |          |
|          |          |          |          | back to  |          |
|          |          |          |          | triage.  |          |
|          |          |          |          |          |          |
|          |          |          |          | Reasons  |          |
|          |          |          |          | could    |          |
|          |          |          |          | be:      |          |
|          |          |          |          | Signi    |          |
|          |          |          |          | ficantly |          |
|          |          |          |          | more     |          |
|          |          |          |          | risk,    |          |
|          |          |          |          | missed   |          |
|          |          |          |          | requi    |          |
|          |          |          |          | rements, |          |
|          |          |          |          | defect   |          |
|          |          |          |          | exposes  |          |
|          |          |          |          | more     |          |
|          |          |          |          | issues   |          |
|          |          |          |          | etc.     |          |
+----------+----------+----------+----------+----------+----------+
| *        | Deferred |          |          | An       | Test     |
| *Defer** |          |          |          | out-     | Lead,    |
|          |          |          |          | of-scope | Team     |
|          |          |          |          | defect   |          |
|          |          |          |          | will be  |          |
|          |          |          |          | labelled |          |
|          |          |          |          | \"De     |          |
|          |          |          |          | ferred\" |          |
|          |          |          |          | in order |          |
|          |          |          |          | to be    |          |
|          |          |          |          | reviewed |          |
|          |          |          |          | at a     |          |
|          |          |          |          | later    |          |
|          |          |          |          | time.    |          |
|          |          |          |          | Deferral |          |
|          |          |          |          | only     |          |
|          |          |          |          | happens  |          |
|          |          |          |          | during   |          |
|          |          |          |          | the      |          |
|          |          |          |          | triage   |          |
|          |          |          |          | and is   |          |
|          |          |          |          | t        |          |
|          |          |          |          | herefore |          |
|          |          |          |          | a        |          |
|          |          |          |          | combined |          |
|          |          |          |          | decision |          |
|          |          |          |          | of the   |          |
|          |          |          |          | team.    |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Deferred | R        | Triage   | Once the | Test     |
|          |          | e-Assess |          | time is  | Lead,    |
|          |          |          |          | there, a | Team     |
|          |          |          |          | deferred |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | brought  |          |
|          |          |          |          | back     |          |
|          |          |          |          | into the |          |
|          |          |          |          | process  |          |
|          |          |          |          | by       |          |
|          |          |          |          | re-a     |          |
|          |          |          |          | ssessing |          |
|          |          |          |          | in       |          |
|          |          |          |          | triage.  |          |
+----------+----------+----------+----------+----------+----------+
| **R      | R        |          |          | A        | Tester/  |
| e-Open** | e-opened |          |          | formerly | Reporter |
|          |          |          |          | closed   |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | r        |          |
|          |          |          |          | e-opened |          |
|          |          |          |          | if the   |          |
|          |          |          |          | same     |          |
|          |          |          |          | c        |          |
|          |          |          |          | ondition |          |
|          |          |          |          | appears  |          |
|          |          |          |          | again.   |          |
|          |          |          |          | This     |          |
|          |          |          |          | defect   |          |
|          |          |          |          | will     |          |
|          |          |          |          | then be  |          |
|          |          |          |          | co       |          |
|          |          |          |          | nsidered |          |
|          |          |          |          | in the   |          |
|          |          |          |          | same     |          |
|          |          |          |          | fashion  |          |
|          |          |          |          | as a     |          |
|          |          |          |          | brand    |          |
|          |          |          |          | new      |          |
|          |          |          |          | defect.  |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | R        | Close    | Closed   | If it    | Tester/  |
|          | e-opened |          |          | turns    | Reporter |
|          |          |          |          | out that |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | wasn\'t  |          |
|          |          |          |          | a defect |          |
|          |          |          |          | or it    |          |
|          |          |          |          | was a    |          |
|          |          |          |          | du       |          |
|          |          |          |          | plicate, |          |
|          |          |          |          | misunder |          |
|          |          |          |          | standing |          |
|          |          |          |          | etc. the |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | closed.  |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | R        | Ready    | In       | Once the | Tester/  |
|          | e-opened | for      | Review   | defect   | Reporter |
|          |          | Review   |          | has been |          |
|          |          |          |          | updated  |          |
|          |          |          |          | it will  |          |
|          |          |          |          | be       |          |
|          |          |          |          | s        |          |
|          |          |          |          | ubmitted |          |
|          |          |          |          | for      |          |
|          |          |          |          | review.  |          |
|          |          |          |          | No       |          |
|          |          |          |          | action   |          |
|          |          |          |          | on the   |          |
|          |          |          |          | defect   |          |
|          |          |          |          | will     |          |
|          |          |          |          | happen   |          |
|          |          |          |          | until it |          |
|          |          |          |          | is       |          |
|          |          |          |          | labeled  |          |
|          |          |          |          | \"Ready  |          |
|          |          |          |          | for      |          |
|          |          |          |          | R        |          |
|          |          |          |          | eview\", |          |
|          |          |          |          | this     |          |
|          |          |          |          | will     |          |
|          |          |          |          | allow    |          |
|          |          |          |          | the      |          |
|          |          |          |          | defect   |          |
|          |          |          |          | reporter |          |
|          |          |          |          | to       |          |
|          |          |          |          | collect  |          |
|          |          |          |          | all the  |          |
|          |          |          |          | n        |          |
|          |          |          |          | ecessary |          |
|          |          |          |          | info     |          |
|          |          |          |          | rmation. |          |
+----------+----------+----------+----------+----------+----------+
| *        | Closed   |          |          | A defect | Team     |
| *Close** |          |          |          | can be   |          |
|          |          |          |          | closed   |          |
|          |          |          |          | because  |          |
|          |          |          |          | it       |          |
|          |          |          |          | passed   |          |
|          |          |          |          | va       |          |
|          |          |          |          | lidation |          |
|          |          |          |          | or for a |          |
|          |          |          |          | variety  |          |
|          |          |          |          | of other |          |
|          |          |          |          | reasons. |          |
+----------+----------+----------+----------+----------+----------+
| ** **    | Closed   | Re-Open  | R        | A        | Tester/  |
|          |          |          | e-opened | formerly | Reporter |
|          |          |          |          | closed   |          |
|          |          |          |          | defect   |          |
|          |          |          |          | can be   |          |
|          |          |          |          | r        |          |
|          |          |          |          | e-opened |          |
|          |          |          |          | if the   |          |
|          |          |          |          | same     |          |
|          |          |          |          | c        |          |
|          |          |          |          | ondition |          |
|          |          |          |          | appears  |          |
|          |          |          |          | again.   |          |
|          |          |          |          | This     |          |
|          |          |          |          | defect   |          |
|          |          |          |          | will     |          |
|          |          |          |          | then be  |          |
|          |          |          |          | co       |          |
|          |          |          |          | nsidered |          |
|          |          |          |          | in the   |          |
|          |          |          |          | same     |          |
|          |          |          |          | fashion  |          |
|          |          |          |          | as a     |          |
|          |          |          |          | brand    |          |
|          |          |          |          | new      |          |
|          |          |          |          | defect.  |          |
+----------+----------+----------+----------+----------+----------+

**Output**

Managed defects.

 

 

Defect Triage Meeting Guidelines

June 24, 2019

3:03 PM

A defect triage is a meeting/review initiated by the Test Lead/Scrum
Master and attended by the leads. The objective of the meeting is to
prioritize and track the defects to be addressed, ensuring timely and
accurate resolution.  The triage will also be the time where testers
readiness for the new build is communicated.

Frequency

A Defect Triage should be held as needed during the sprints. The
frequency and the number of occurrences will vary, but is typically
based on:

-   the number of defects being reported,

-   the overall sprint schedule and

-   the current status of the sprint.

Scope of the meeting

The defects that will be discussed are all the defects which have the
status "Triage".  

At the Defect Triage, each defect should be discussed; even those that
are rated at a lower severity or ones that are deemed "simple".

Common Triage Meeting Guidelines

-   The Test Lead/Scrum Master makes sure the right people are present.
    > Nota Bene: Not all are needed all the time!

-   Test Lead determines when the meeting is held. *Do not hold meetings
    > because they are on the calendar if you have nothing to discuss!*

-   The Test Lead facilitates the meeting.

-   The Test Lead documents the decisions in JIRA during the meeting.

-   An efficient triage meeting should take no longer than 30 minutes
    > and should be finished as soon as possible.

-   Participants actively and respectfully contribute.

-   The Defect Triage is not intended to solve defects. Common rule of
    > thumb: If you need more than 2-3 minutes to decide on priority and
    > assignment, it needs to be assigned for clarification.

-   The priority of defects to be discussed are:

1.  "Failed" Validation

2.  Defects that have new information provided to them

3.  Returned to Triage from Development of Validation

4.  Re-assessed defects (previously deferred)

5.  Re-opened defects

6.  New defects in order of descending severity

-   The triage meeting will also discuss readiness of testing for the
    > new build.

Agenda for a Triage Meeting

**Introduction (2 minutes)**

-   Flag any burning, immediate action needed, defects that impact test
    > and development progress.

-   Bring up list on screen sorted by priority of discussion.

**Review defect by defect (no longer than 2-3 minutes per defect)**

> **Determine:**

1.  Validity of defect. (Invalid will close the defect)

2.  In scope or out of scope? (Out of scope will result in Deferral)

3.  Completeness/clarity of information

> **Complete Triage (JIRA Transition) by obtaining input from
> participants**

1.  Review Symptom/Severity for correctness (Reporter has already
    > entered this)

2.  Review Product Status for correctness (Reporter has already entered
    > this)

3.  Discuss Business Value

4.  Set Priority

5.  Determine the Fix Versions (The version in which this defect needs
    > to be fixed)

6.  Determine the Due Date

7.  Add a comment if necessary

8.  Review Priority again to make sure that that it is indeed correct.

> **Obtain agreement from the participants**

1.  Update Status and Assignment

> **Next defect....**

**Discuss Testing's readiness for the next build. (5 minutes)**

-   Test Lead indicates status of current test cycle.

-   Dev. Lead reports on readiness of Dev. to produce a new build.

-   Agree build deployment date/schedule.

ROLES & RESPONSIBILITIES of individuals in Defect Triage

> **1. Project Manager**

-   Assists in the prioritization of the defects

-   Deals with or escalates scoping defects.

> **2. Business Lead/Product Owner**

-   Assists in the prioritization of the defects.

-   Assists in setting the Business Value of the defect.

-   Deals with or escalates business scoping defects.

> **3. Test Lead/Scrum Master**

-   Assists in the prioritization of the defects

-   Calls the Defect Triage

-   Manages defects in JIRA

-   Discusses the arrival of the next build for Testing

-   Escalates Testing defects

-   Explains the findings on each defect being presented

> **4. Development Lead(CGI)**

-   Assists in the prioritization of the defects

-   Escalates development defects to PM

-   Discusses the delivery date of next build to Testing

-   Explains the level of complexity and the risk associated with each
    > defect being presented at the Defect Triage

-   Assigns the defects to the appropriate developer

-   Team is aligned on the severity and priority of defects discussed
    > during the Defect Triage

 

 

Test Closure Process

June 24, 2019

3:04 PM

RASCI

  **Roles**                  **Responsible**   **Approves/Accountable**   **Supports**   **Consulted**   **Informed**
  -------------------------- ----------------- -------------------------- -------------- --------------- --------------
  **Test Lead**              X                                                                            
  **Business Lead**                                                        X                              
  **Developer Lead**                                                       X                              
  **Release Manager**                                                      X                              
  **Auditor**                                                                                            X
  **Project Manager**                          X                                                          
  **Product Owner/Client**                                                                               X

Objective

Determine \"done-ness\".

Wrap up the sprint\'s testing effort, consolidate results and report on
outcome.

Pre-requisites

**Before** closing the sprint test we determine if:

1.  We meet our definition of done (DoD) for testing

2.  Testing has been performed against test plan(s)

3.  All test cases are mapped to requirements

4.  All test cases have been executed unless known and agreed upon

5.  All defects have been addressed

Description

During the project, every sprint will go through a test closure. In the
test closure we determine that we are indeed finished and what
activities are still outstanding to secure our test artifacts and
results.

Any outstanding work items will need to be discussed and decided upon.

The decision can be one of the following:

-   Deal with it in the last phase of the sprint

-   Put on the backlog for future sprint incorporation 

-   Determine that the item is no longer necessary

**After** closing the sprint test we:

1.  Collect the lessons learned and suggested process improvements for
    > the **Sprint Retrospective**

2.  Evaluate our test estimation accuracy

3.  Conduct a defect trend analysis

4.  Archive/consolidate all relevant test collateral, including:

    a.  Test plan(s)

    b.  Test case(s)

    c.  Test report(s)

    d.  Test data

    e.  Relevant emails

Output: Test Closure Report

The Test Closure Report is input to the **Sprint Review.** 

This report provides the following details:

-   Outstanding Risks and Issues

-   Action Plan for open work items

-   Statistics on:

    -   Defects found

    -   Defects fixed

    -   Open Defects

    -   Open Defects by Severity and Priority

    -   Postponed defects (backlog)

    -   Test Passes/Fails

    -   Not-run test cases

    -   Blocked test cases

 

 

 

Detailed Test Strategies

June 25, 2019

9:34 AM

This chapter contains the individual test strategies for the different
test activities and techniques to be deployed in the PPR project.

Not all of these strategies will be deployed equally or with the same
width of implementation. The info-graphic below gives a high level
impression of the relative importance and therefore focus.

Rated from 0-10 on each category, the different activities are rated as
follows:

\<\<Detailed Test Strategies - Spreadsheet.xlsx\>\>

  ** **                         **Frequency**   **Impact On Quality**   **Business Importance**   **Operational Importance**   **Project Success factor**   **SUM Total**   **Rank**
  ----------------------------- --------------- ----------------------- ------------------------- ---------------------------- ---------------------------- --------------- ----------
  **Unit Testing**              0               0                       0                         0                            0                            **0**           10
  **Functional Testing**        10              10                      9                         5                            10                           **44**          1
  **Test Automation**           1               1                       3                         8                            4                            **17**          7
  **System Testing**            2               3                       4                         8                            5                            **22**          5.5
  **Regression Testing**        9               2                       8                         8                            8                            **35**          3.5
  **Smoke Testing**             10              1                       1                         8                            2                            **22**          5.5
  **Integration Testing**       5               8                       8                         6                            8                            **35**          3.5
  **User Acceptance Testing**   6               2                       10                        8                            10                           **36**          2
  **Security Testing**          1               1                       5                         8                            1                            **16**          8
  **Performance Testing**       1               1                       4                         8                            1                            **15**          9

 

 

 

Unit Test Strategy

June 25, 2019

9:44 AM

This section has been added for information only as Unit Testing for PPR
is not implemented as traditional Unit Testing. However, the
developers/configurators do have activities that could be characterized
as \"Developer Testing\". Many of the concepts shown below would still
apply to that activity.

Definition 

 A unit test, as Agile teams understand the term, is a short program
fragment written and maintained by the developers on the product team,
which exercises some narrow part of the product\'s source code and
checks the results. 

Unit testing is guided by the following principle:

 

**Unit Testing Principle**

**Basic assumption(s):**

-   All modules/functions/components/interfaces need to be Unit tested
    > by the developer.

-   Unit tests need to be re-usable.

-   Unit tests need to cover design specification requirements.

-   Unit Tests need to be implemented as automated tests.

**Test Principle:**

-   Developers will create a unit test design for each component they
    > produce.

-   Unit Test design is documented and stored for re-use and reference.

Objectives

Unit Testing aims to:

-   Find defects which may get created by the programmer while
    > developing the software.

-   Gain confidence in and provide information about the level of
    > quality.

-   Prevent defects being passed on to the next activity.

Expected Benefits

-   A team relying on automated unit tests can expect to reap some of
    > the benefits of test-driven development, in particular a decrease
    > in defect rates.

-   Early and frequent testing is a pattern common to successful
    > delivery of working software.

-   Continuous Integration can only succeed when there is a solid basis
    > of automated unit tests .

 

**To Note**

Agile has led to a strong emphasis, among developers, on the use of
automated checking procedures, and this has tended to marginalize other
forms of testing, in particular that done by professional testers. Yet
this work (which some Agile teams call \"exploratory\" testing) is no
less important in an Agile context.

Responsibilities

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead                                    X                
  Test Analyst (Agile)                                          
  Business Tester                                               
  Test Automation Specialist                   X                
  Business Analyst                                              
  Business Lead                                                 
  Developer                    X                                
  Developer Lead                       X                        
  Solution Architect                                   X        
  Release Manager                              X                
  Auditor                                                       
  Project Manager                                              X

Unit testing is the responsibility of the development team.

Scope

**Unit, Component and Module Test Scope**

In Agile projects the test scope is determined by the content of each
sprint. Each user story in the sprint will consist of one or more
software components, units and or modules and these will have one or
(typically) more unit tests each.

Approach

This section provides an overview of the test approach that will be
undertaken for Unit Testing. 

In the early eighties, IBM did a lot of research on the value of Unit
Testing and found that it was capable of finding at least 60% of all
defects that a project could encounter. The more striking number was
that this could be done for a fraction of the cost and with minimal
disruption to the delivery of the project. This notion is at the core of
the practice in agile projects to have a focus on unit testing and
particularly automated unit testing. 

In general terms we want unit testing to be:

-   Rigorous

-   Consistent

-   Repeatable

-   Dependable

**Rigorous**

Leave no stone unturned, all pieces of code will be:

-   Reviewed.

-   Covered by means of automated unit tests that will test all
    > sequences, iterations and decisions, not only to test if they work
    > but also if they react correctly in error situations.\
    > **Positive and Negative Tests\
    > **In Unit testing we aim to have at least 80% negative tests (test
    > that should fail) and 20% positive tests (test that should
    > succeed). The philosophy behind this is that errors typically
    > cluster around exceptions, \"this will never happen\", domain
    > issues, boundary problems etc.

-   Exposed to as many data/usage variations as possible. Testing and
    > therefore also Unit testing is largely a combinatorial problem,
    > Variations are potentially hard to test as they often are too
    > many. By deploying techniques like code coverage, pair-wise
    > testing and risk analysis we can focus on achieving best value for
    > our efforts balancing coverage with variability.

**Consistent**

Effectiveness of the automated unit tests is greatly enhanced when:

-   They get executed whenever the code changes

-   They are part of every code build and roll out process

-   They conform to minimum levels of coverage and complexity

-   They are reviewed for consistency

-   They are kept up-to-date when the code changes

**Repeatable**

Most value will be obtained from unit tests when they are repeatable at
any time. This requires that they are set up, in such a fashion that
they can run independently of the phase of the project or the activity.

This repeatability requires the unit tests to have the following
characteristics:

-   They need to be modular

-   They need specific unit test data

-   They need to be isolated from the rest of the system

**Dependable**

Unit tests that repeatedly yield believable results can be depended on
when assessing the quality of the code base.

Dependable unit tests are obtained by making each test independent to
all the others. Any given behaviour should be specified in one and only
one test. Otherwise if that behaviour changes later, multiple tests have
to be changed.

The corollaries of this rule include: 

-   **No unnecessary assertions**

> It's counterproductive to Assert() anything that's also asserted by
> another test: it just increases the frequency of pointless failures
> without improving unit test coverage one bit.  *Have only one logical
> assertion per test*. 

-   **Test only one code unit at a time **

> The architecture must support testing units (i.e., classes or very
> small groups of classes) independently, not all chained together. This
> will avoid overlap between tests. 

-   **Mock out all external services and state **

> Otherwise, behaviour in those external services overlaps multiple
> tests, and state data means that different unit tests can influence
> each other's outcome. 

-   **Avoid unnecessary preconditions **

> Avoid having common setup code that runs at the beginning of lots of
> unrelated tests. Otherwise, it's unclear what assumptions each test
> relies on.

-   **Don't unit-test configuration settings **

> By definition, the configuration settings aren't part of any unit of
> code. 

-   **Name unit tests clearly and consistently **

> Avoid non-descriptive unit tests names such as Purchase() or
> OutOfStock(). Maintenance is hard if it is unclear what we need to
> maintain.

Test Design

For our unit test design we will be deploying multiple techniques and
approaches in order to maximize our effectiveness.

  **Technique**                 **Description**
  ----------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------
  Path Coverage Analysis        Analysis of the paths through the code that can be executed and making sure that the unit tests account for every path
  Peer Review                   A peer review adds value by providing a set of fresh eyes on the code that can generate more testing ideas and better quality testing ideas
  Analysis of requirements      The code needs to meet the requirement or acceptance criteria that are defined.
  Review of flow charts         Developing an understanding of the overall flow of the functionality
  Standards review              Coding, database usage and iValua development standards need to be followed
  Decision Logic review         Review of decision tables, defined validations and external validation mechanisms
  Review of Data Structures     Developing an insight of where data resides and how it is interconnected
  Review of common interfaces   Understanding the common interfaces to iValua, the back end systems and external interfaces (like address complete)

The unit testing deliverables of the test design stage include unit test
scripts, mock objects, and test data. These deliverables will be
uploaded in the version control system and subsequently connected to the
delivered code units/components.

Test Execution

The outcome of a unit test is binary: either \"pass\" if the program\'s
behavior is consistent with the recorded expectations, or \"fail\"
otherwise. Developers will typically write a large number of unit tests
(corresponding to a large number of program behaviors of interest),
called a \"test suite\". 

Unit tests will first be executed on the developers workstation as part
of the development process. Once development is deemed done, the code is
updated in the version control system and the changes will be
incorporated in the automated build and unit test process that will run
multiple times a day.

Data Requirements

 As per definition in Test Data Strategy unit testing requires the
following types of test data: 

  **Usage**                            **Environment**         **Type of Test Data**   **User**
  ------------------------------------ ----------------------- ----------------------- ----------------------
  Unit Testing/Integration Testing     Developer Workstation   Purposely created       Developer
  Automated Unit/Integration testing   Build/Integration       Purposely created       Automated CI process

 In Test Environments Needs we have defined which environments will be
required to have the unit test data:

+----------+----------+----------+----------+----------+----------+
| **Type   | **       | **       | **In     | **Who**  | **Descr  |
| of       | Environm | Database | tegrated |          | iption** |
| T        | ent(s)** | In       | with     |          |          |
| esting** |          | stance** | Back     |          |          |
|          |          |          | end**    |          |          |
+==========+==========+==========+==========+==========+==========+
| Unit     | Dev.     | Local    | No       | De       | A        |
| Testing  | Work     | D        |          | velopers | utomated |
|          | station, | atabase, |          |          | Unit     |
|          | B        |          |          |          | tests    |
|          | uild/Int | Build    |          |          | are      |
|          | egration | Database |          |          | d        |
|          | Env      |          |          |          | eveloped |
|          | ironment |          |          |          | by the   |
|          |          |          |          |          | de       |
|          |          |          |          |          | velopers |
|          |          |          |          |          | on their |
|          |          |          |          |          | own      |
|          |          |          |          |          | wor      |
|          |          |          |          |          | kstation |
|          |          |          |          |          | and      |
|          |          |          |          |          | these    |
|          |          |          |          |          | test     |
|          |          |          |          |          | scripts  |
|          |          |          |          |          | get      |
|          |          |          |          |          | s        |
|          |          |          |          |          | ubmitted |
|          |          |          |          |          | with the |
|          |          |          |          |          | code     |
|          |          |          |          |          | they     |
|          |          |          |          |          | created. |
|          |          |          |          |          | Subs     |
|          |          |          |          |          | equently |
|          |          |          |          |          | the unit |
|          |          |          |          |          | tests    |
|          |          |          |          |          | will be  |
|          |          |          |          |          | executed |
|          |          |          |          |          | during   |
|          |          |          |          |          | the      |
|          |          |          |          |          | co       |
|          |          |          |          |          | ntinuous |
|          |          |          |          |          | int      |
|          |          |          |          |          | egration |
|          |          |          |          |          | process. |
+----------+----------+----------+----------+----------+----------+

Test data for unit testing needs to be:

-   For one unit only, independent from other data. If dependencies are
    > there, the data needs to be provided as part of the unit test and
    > not assumed to be available

-   Comprehensive in support for the unit test(s) and all its variants

If these requirements are met, a truly effective automated unit test
solution can be brought into place. If the requirements are *not* met,
it is very likely that the automated test solution will require
significant maintenance and upkeep in later sprints effectively negating
the benefits that automated unit testing can bring.

 

 

Integration Test Strategy

June 25, 2019

9:44 AM

> This section provides an overview of the test approach that will be
> undertaken for Integration Testing. In unit testing we are testing the
> individual components, which are then combined in large building
> blocks or assemblages. By frequently testing potential interactions
> (good or bad), the team will position itself to quickly deal with any
> issues found. 
>
> The term \"integration testing\" is used to mean three different
> things:

-   **A sub-assembly test**: an interim level of testing, part of the
    > way between unit testing and system testing of the fully
    > integrated system.  The Integration Test Strategy is oriented
    > primarily towards sub-assembly testing, but also addresses the
    > other two types of integration testing.

-   **Smoke Test (or build verification test)**: a quick test of an
    > integrated sub-assembly or complete system, just to confirm that
    > all components are present and are connected together correctly. 
    > The build verification test usually is not as intensive as a
    > sub-assembly test.  The build process is a series of steps in
    > which the components are compiled and linked together to form an
    > executable system (or subsystem).  In large complex systems, many
    > steps may be needed to build a system, and there can be several
    > build verification tests as interim checkpoints to ensure that the
    > build process is proceeding correctly.

-   **An end-to-end test (or System Integration Test)**, usually
    > performed on an entire system, where one feature is tested \"end
    > to end\" through the system, without the distraction of other
    > features or other simultaneous demands on the system.

> In all the above three types of integration tests, the objective is to
> ensure that components link and work together.  The focus is on the
> effectiveness of functional interactions and compatibility at the
> interfaces.  Integration testing is an interim level of testing that
> occurs between unit testing and systems testing, and where groupings
> of components are tested. 
>
> Definition
>
> Testing performed to expose defects in the interfaces and in the
> interactions between integrated components or systems.
>
> Objectives

-   Verify whether all the components/unit within assemblages interact
    > correctly, for example across procedure calls or processes. 

-   Verify the \"building blocks\" and add verified assemblages are
    > added to a verified base which is then used to support the
    > integration testing of further assemblages.

-   Verify interactions with external systems.

> Expected Benefits

-   Individual system components work correctly with each other on the
    > iValua platform

-   External functionality works as expected

-   REST-full layer operates according to specification

> Responsibilities
>
> [RASCI
> Legend](onenote:RASCI%20Legend.one#section-id={75397548-6BE0-46FB-80CC-551FBC2B6C97}&end&base-path=https://citz.sp.gov.bc.ca/sites/Shared/Project/BidR/BCBid/CONTRACT%20%20SCHEDULE/Testing/Resources/Testing%20Notes)

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead                                    X                
  Test Analyst (Agile)                         X                
  Business Tester                                               
  Test Automation Specialist                   X                
  Business Analyst                                              
  Business Lead                                                 
  Developer                    X                                
  Developer Lead                       X                        
  Solution Architect                                           X
  Release Manager                                              X
  Project Manager                                              X

> Scope
>
> Full System Integration will be tested during System(-Integration)
> Testing.
>
> Approach
>
> Integration tests are related to Unit tests and we\'ll use the same
> mechanism and approach to test.
>
> With integration tests we expand the scope of the test to include
> multiple components. During unit testing we want to isolate the
> component, in integration testing we want to have the unit connect to
> and work with other components. For this type of integration testing,
> the structure of the unit test scripts can be re-purposed and updated
> to reflect that actual data and results are coming back from the
> components it is integrated with.
>
> Test Design
>
> Test Design approach follows the Unit Test approach. As stated above,
> integration testing is performed to ensure that the units operate
> correctly when they are combined together, as parts in a working (but
> perhaps incomplete) application.  Integration testing usually proceeds
> from small subassemblies, containing only a few components, to larger
> ones containing many components.  Large complex products can go
> through many repetitive build-and-test cycles before they are fully
> integrated.
>
> Test Execution
>
> Execution will follow the same path and frequency of the automated
> unit tests.
>
> Data Requirements
>
>  As per definition in Test Data Strategy integration testing requires
> the following types of test data: 

  **Usage**                            **Environment**         **Type of Test Data**   **User**
  ------------------------------------ ----------------------- ----------------------- ----------------------
  Unit Testing/Integration Testing     Developer Workstation   Purposely created       Developer
  Automated Unit/Integration testing   Build/Integration       Purposely created       Automated CI process
  System Integration Testing           TEST                    Purposely Created       BA, Tester

>  
>
>  In Test Environments Needs we have defined which environments will be
> required to have the unit test data:

  **Type of Testing**          **Environment(s)**   **Integrated with Back end**   **Who**                        **Description**
  ---------------------------- -------------------- ------------------------------ ------------------------------ -----------------
  Integration Testing          Integration Test      Yes                           Developers                      
  System Integration Testing   TEST                 Yes                            BA, Tester, Business Testers    

 

 

Functional Test Strategy

June 25, 2019

10:45 AM

This section provides an overview of the test approach for Functional
Testing.

Functional testing is a large testing effort in our project. Functional
tests tend to answer the questions like "can the user do this?" or "does
this particular feature work?".

Definition

Testing based on an analysis of the specification of the functionality
of a component or system. 

In functional testing the testing of the functions of component or
system is done. It refers to activities that verify a specific action or
function of the code. This is typically described in a requirements
specification or in a functional specification. For PPR we use the
Acceptance Criteria (not to be confused with user acceptance criteria),
as our test cases.

Objectives

-   The main objective of functional testing is to verify that each
    > function of the software application operates in accordance with
    > the written acceptance (requirement) specifications.

```{=html}
<!-- -->
```
-   Functional testing is to verify whether your product meets
    > the *intended* functional acceptance criteria mentioned in your
    > user story documentation.

 

**Challenges in an Agile project**

In a traditional projects, (highly) detailed requirements are considered
the main guidance for test development. In an agile project, detailed
requirements are typically not available. Test ideas/case therefore will
be developed by consultation, reviewing other materials like the user
stories, technical specification etc. This process of discovery will
yield questions, issues and observations that will feed back into the
project.

Expected Benefits

-   Acceptance Criteria are verified

-   Functionality of the solution  is verified

-   Basic usability is ensured

-   Defects are found

Responsibilities

 

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead                            X                        
  Test Analyst (Agile)         X                                
  Business Tester                                              X 
  Test Automation Specialist                   X                
  Business Analyst                                     X        
  Business Lead                                         X       
  Developer                                    X                
  Developer Lead                                                X
  Solution Architect                                            
  Release Manager                                               X
  Subject Matter Expert                                 X       
  Auditor                                                      X
  Project Manager                                               X

Scope

Since a sprint works on a limited and different scope at the time, the
actual scope for functional testing can vary. The following list would
be our typical tests.

Functional Testing typically includes the following:

-   Functional Acceptance Criteria

-   Business Process

-   Application Behavior

-   Navigation

-   Field/Screen Element behavior

-   Validations

-   Data Entry

-   Limits and Boundaries

-   Buttons, check boxes, radio buttons

-   Basic functionality

-   Login/Logout

-   Data Search, Creation, Retrieval, Changing and deletion

-   Start/Stop of application page

-   Web specific tests

-   Security role validation (basic at this stage)

-   Negative Tests

-   Web Content and configuration

Approach

Testing functionality can be done from two perspectives:

-   **Requirement-based testing: **In this type of testing the
    > acceptance criteria (requirements) are prioritized and accordingly
    > the tests follow that prioritization. This will ensure that the
    > most important and most critical tests are included in the testing
    > effort.

-   **Business-process-based testing: **In this type of testing the
    > scenarios involved in the day-to-day business use of the system
    > are described. It uses the knowledge of the business
    > processes.** **For example, a personnel and payroll system may
    > have the business process along the lines of: someone joins the
    > company, employee is paid on the regular basis and employee
    > finally leaves the company.

> For PPR we deploy both perspectives to functionality testing. However,
> the emphasis will be initially on requirements-based testing (we would
> also include checklists, web standards etc.). Business process testing
> will come after the requirements have been tested and basic
> functionality is deemed acceptable. This approach is used to focus the
> testing effort.

Test Design

Our test design consists of the following high level categories of test
cases:

-   Functionality: This is the most straight forward category, where we
    > take each piece of the application and test it individually. 

-   Scenarios: We take the user scenarios and run them in order to
    > review the behavior of the system. 

-   Negative tests: We think of all possible things that a user may do
    > wrong in the system and make sure that a correct indication is
    > displayed and no permanent damage is done to the system or its
    > data.

-   Date dependent Tests: PPR is date dependent and a specific category
    > of test cases is necessary

### Test Case Design Techniques

Of all the test case design techniques which are available, the most
effective for the functional testing are:

-   Specification-based techniques.  This technique derives test cases
    > from the documented specifications of the system's behavior. This
    > includes the following design techniques:

-   Functional analysis (functional specification-based testing).

-   Sampling techniques.  These techniques identify small samples of
    > high-potential test cases from large populations of possible
    > conditions. This includes the following design techniques:

-   Equivalence Analysis

-   Boundary value (BV) Analysis

-   Combinatorial methods, such as pair-wise and n-wise testing

-   Experience-based techniques.  These techniques utilize the testers'
    > and others' experience, either with the system under test or in
    > prior similar situations. This includes the following design
    > techniques:

```{=html}
<!-- -->
```
-   Exploratory testing

```{=html}
<!-- -->
```
-   User scenarios

-   Checklists

-   Risk analysis and prioritization

**Checklists**

After each sprint the test team collects lessons learned and compiles
these into checklists for future reference when developing test cases.

Test Execution

Functional Testing is recognized as a separate activity that precedes
system and user acceptance testing (See below), however other test
activities below will also contain certain types of Functional tests.

+----------------------+----------------------+----------------------+
| **Test Activity**    | **Functional Test**  | **Participant**      |
+======================+======================+======================+
| Unit/Integration     | -   Screen/Object    | Developer            |
| Testing              |     > Behavior       |                      |
|                      |                      |                      |
|                      | -   Database         |                      |
|                      |     > functions      |                      |
|                      |                      |                      |
|                      | -   Navigation       |                      |
|                      |                      |                      |
|                      | -   Acceptance       |                      |
|                      |     > Criteria       |                      |
+----------------------+----------------------+----------------------+
| Functional Testing   | -   Functional       | Agile Testers, Test  |
|                      |     > Acceptance     | Automation           |
|                      |     > Criteria       | Specialist           |
|                      |                      |                      |
|                      | -   Business Process |                      |
|                      |                      |                      |
|                      | -   Application      |                      |
|                      |     > Behavior       |                      |
|                      |                      |                      |
|                      | -   Navigation       |                      |
|                      |                      |                      |
|                      | -   Field/Screen     |                      |
|                      |     > Element        |                      |
|                      |     > behavior       |                      |
|                      |                      |                      |
|                      | -   Validations      |                      |
|                      |                      |                      |
|                      | -   Data Entry       |                      |
|                      |                      |                      |
|                      | -   Limits and       |                      |
|                      |     > Boundaries     |                      |
|                      |                      |                      |
|                      | -   Buttons, check   |                      |
|                      |     > boxes, radio   |                      |
|                      |     > buttons        |                      |
|                      |                      |                      |
|                      | -   Basic            |                      |
|                      |     > functionality  |                      |
|                      |                      |                      |
|                      | -   Login/Logout     |                      |
|                      |                      |                      |
|                      | -   Data Search,     |                      |
|                      |     > Creation,      |                      |
|                      |     > Retrieval,     |                      |
|                      |     > Changing and   |                      |
|                      |     > deletion       |                      |
|                      |                      |                      |
|                      | -   Start/Stop of    |                      |
|                      |     > application    |                      |
|                      |     > page           |                      |
|                      |                      |                      |
|                      | -   Web specific     |                      |
|                      |     > tests          |                      |
|                      |                      |                      |
|                      | -   Security role    |                      |
|                      |     > validation     |                      |
|                      |     > (basic at this |                      |
|                      |     > stage)         |                      |
|                      |                      |                      |
|                      | -   Negative Tests   |                      |
|                      |                      |                      |
|                      | -   Web Content and  |                      |
|                      |     > configuration  |                      |
+----------------------+----------------------+----------------------+
| System Testing       | -   Business Process | Agile Tester         |
|                      |                      |                      |
|                      | -   Acceptance       |                      |
|                      |     > Criteria       |                      |
|                      |                      |                      |
|                      | -   Security Role    |                      |
|                      |     > validation     |                      |
+----------------------+----------------------+----------------------+
| User Acceptance      | -   Business Process | Tester/Business      |
| Testing              |                      | Analyst/Business     |
|                      |                      | Tester               |
+----------------------+----------------------+----------------------+

But the specific step of functional testing completely focuses on
functionality and making sure that system under test is in good enough
shape to continue with the next step: system testing.

Data Requirements

  **Usage**            **Environment**   **Type of Test Data**    **User**          **Comments**
  -------------------- ----------------- ------------------------ ----------------- --------------
  Functional Testing   DEV/TEST          Test Data + Valid IDIR   Testers (Agile)    

Infrastructure Requirements

 

+-------------+-------------+-------------+-------------+-------------+
| **Type of   | **Envir     | *           | **Who**     | **De        |
| Testing**   | onment(s)** | *Integrated |             | scription** |
|             |             | with Back   |             |             |
|             |             | end**       |             |             |
+=============+=============+=============+=============+=============+
| Functional  | DEV/TEST    | No          | Agile       | Functional  |
| Testing     |             |             | Testers     | Testing has |
|             |             |             |             | different   |
|             |             |             |             | aspects to  |
|             |             |             |             | it, first   |
|             |             |             |             | we\'ll have |
|             |             |             |             | the         |
|             |             |             |             | \'tr        |
|             |             |             |             | aditional\' |
|             |             |             |             | test cases  |
|             |             |             |             | and         |
|             |             |             |             | scripts,    |
|             |             |             |             | but we will |
|             |             |             |             | also engage |
|             |             |             |             | in          |
|             |             |             |             | exploratory |
|             |             |             |             | testing.    |
|             |             |             |             |             |
|             |             |             |             | This type   |
|             |             |             |             | of testing  |
|             |             |             |             | can         |
|             |             |             |             | co-exist    |
|             |             |             |             | with        |
|             |             |             |             | Automated   |
|             |             |             |             | Functional  |
|             |             |             |             | Testing as  |
|             |             |             |             | long as we  |
|             |             |             |             | keep a      |
|             |             |             |             | clear data  |
|             |             |             |             | separation  |
|             |             |             |             | between the |
|             |             |             |             | 2           |
|             |             |             |             | activities. |
+-------------+-------------+-------------+-------------+-------------+

 

 

Exploratory Testing Strategy

June 25, 2019

11:26 AM

This section provides an overview of the exploratory test approach for
the PPR project.

Exploratory testing is a style of software testing that emphasizes the
personal freedom and responsibility of the individual tester to
continually optimize the quality of his/her work by treating
test-related learning, test design, test execution, and test result
interpretation as mutually supportive activities that run in parallel
throughout the project. This completely aligns with the agile project
approach and has proven a very good fit for common agile scenarios like
change, refinements and course correction.

Definition

Exploratory testing is an approach to software testing that is concisely
described as simultaneous learning, test design and test execution. 

Objectives

-   Find defects quickly

-   React to quickly changing system

-   Define the basis for test automation and further exploratory test
    > sessions

-   Identify missed or unclear requirements

Expected Benefits

-   Less initial test preparation is needed

-   Important defects are found quickly

-   Test execution is more intellectually stimulating than execution of
    > scripted tests

-   Opens the possibility for deductive reasoning based on the results
    > of previous results

-   Exploration throughout testing continuously challenges the System
    > Under Test with new scenarios

Responsibilities

See Functional Test Strategy

Scope

While the software is being tested, the tester learns things that
together with experience and creativity generates new value-added tests
to run. Exploratory testing is often thought of as a black box testing
technique. Instead, those who have studied it consider it a test
approach that can be applied to any test technique, at any stage in the
development process. The key is not the test technique nor the item
being tested or reviewed; the key is the cognitive engagement of the
tester, and the tester\'s responsibility for managing his or her time.

The scope for exploratory testing is largely functional testing, but has
great benefit for business process testing as well.

Approach

*One of the criticisms of exploratory testing is that it can be purely
ad-hoc, uncontrolled, non-traceable. Indeed if the approach is left
undefined this would be a certainty. The answer to this is to instill a
lightweight process call Session-Based Test Management (SBTM), a method
for measuring and managing exploratory testing.*

***SBTM by James and Jon Bach***

 

**Description**

Exploratory testing is unscripted, unrehearsed testing. Its
effectiveness depends on several intangibles: the skill of the tester,
their intuition, their experience, and their ability to follow hunches.
But it\'s these intangibles that often confound test managers when it
comes to being accountable for the results. For example, at the end of
the day, when the manager asks for status from an exploratory tester,
they may get an answer like \"Oh, y\'know\... I tested some functions
here and there, just looking around.\" And even though the tester may
have filed several bugs, the manager may have no idea what they did to
find them. Even if the manager was skilled to ask the right questions
about what the tester did, the tester may have forgotten the details or
may not be able to describe their thinking out loud, on-the-fly.

We had this problem when doing exploratory testing for a client. We
wanted to be accountable for our work. We wanted to give status reports
that reflected what we actually did. We wanted to show that we could be
creative, skilled explorers, yet produce a detailed map of our travels.

**How it\'s done**

We invented Session-Based Test Management as a way to make those
intangibles more tangible. It can be thought of as structured
exploratory testing, which may seem like a contradiction-in-terms, but
\"structure\" does not mean the testing is pre-scripted. It means we
have a set of expectations for what kind of work will be done and how it
will be reported. As in a recording studio, this work is done in
\"sessions.\" Sessions range from 45 minutes to several hours, but no
matter the length, it is time spent testing against a charter for the
session. The nuts-and-bolts of sessions are described in further detail
in an **article** Jonathan Bach wrote for [STQE
magazine.](http://www.satisfice.com/articles/sbtm.pdf)

At the end of a session, the tester hands in a session report, tagged
with important information about what they did.

**Session metrics**

The session metrics are the primary means to express the status of the
exploratory test process. They contain the following elements:

-   Number of sessions completed

-   Number of problems found

-   Function areas covered

-   Percentage of session time spent setting up for testing

-   Percentage of session time spent testing

-   Percentage of session time spent investigating problems

**Debriefings**

At the end of each session, the tester and manager get together to talk
about it. We\'ve discovered that the value of SBTM relies on the ability
of the test manager to talk with the tester about the work that was
done, so to help the tester and manager make the most out of that
meeting (which takes about 15-20 minutes), we\'ve compiled
a checklist of questions.

**SBTM Approach**

**Mission**

The mission in Session Based Test Management identifies the purpose of
the session, helping to focus the session while still allowing for
exploration of the system under test. 

**Charter**

A charter is a goal or agenda for a test session. Charters are created
by the test team prior to the start of testing, but they may be added or
changed at any time. Often charters are created from a specification,
test plan, or by examining results from previous sessions. The charters
are stored and tracked in Zephyr.

**Session**

An uninterrupted period of time spent testing, ideally lasting 45
minutes to two hours. Each session is focused on a charter, but testers
can also explore new opportunities or issues during this time. The
tester creates and executes tests based on ideas, heuristics or whatever
frameworks to guide them and records their progress. This might be
through the use of written notes, video capture tools or by whatever
method as deemed appropriate by the tester.

**Session report**

The session report records the test session in Zephyr. This includes:

-   Charter

-   Area tested

-   Detailed notes on how testing was conducted

-   A list of any defects found

-   A list of issues (open questions, product or project concerns), in
    > JIRA

-   Any files/data the tester used or created to support their testing

-   Percentage of the session spent on the charter versus investigating
    > new opportunities

-   Percentage of the session spent on:

-   Testing - creating and executing tests

-   Bug investigation / reporting

-   Session setup or other non-testing activities

-   Session Start time and duration

Debrief

A debrief is a short discussion between the lead and tester (or testers)
about the session report. We use the acronym PROOF to help structure
this debriefing.

PROOF stands for:

-   **P**ast. What happened during the session?

-   **R**esults. What was achieved during the session?

-   **O**bstacles. What got in the way of good testing?

-   **O**utlook. What still needs to be done?

-   **F**eelings. How does the tester feel about all this?

Parsing results

With a standardized Session Report in Zephyr we have access to
aggregated data for reporting and metrics. This allows reporting on the
number of sessions per area or a breakdown of time spent on testing, bug
investigation, and setup / other activities.

Planning

Testers using session-based testing can adjust their testing daily to
fit the needs of the project. Charters can be added or dropped over time
as tests are executed and/or requirements change.

Test Design

Exploratory testing is test design on the fly, but that does not mean it
is random.

Most exploratory testing is driven by a set of simple heuristics (A
process or method enabling a person to discover or learn something for
themselves).

As testing is the process of asking questions of the solution. For
example, the following questions can be asked during exploratory test
sessions:

 

-   **Product**

    -   What is this product?

    -   What can I control and observe?

    -   What should I test?

-   **Tests**

    -   What would constitute a diversified and practical test strategy?

    -   How can I improve my understanding of how well or poorly this
        > product works?

    -   If there were an important problem here, how would I uncover it?

    -   What document to load? 

    -   Which button to push?

    -   What number to enter?

    -   How powerful is this test?

    -   What have I learned from this test that helps me perform
        > powerful new tests?

    -   What just happened? How do I examine that more closely?

-   **Problems**

    -   What quality criteria matter?

    -   What kinds of problems might I find in this product?

    -   Is what I see, here, a problem? If so, why?

    -   How important is this problem? Why should it be fixed?

Test Execution

Exploratory Tests can be executed during all test activities (except for
test automation) but will mostly be used by the agile testers and the
user acceptance testers.

Data Requirements

The data required is dependent on where the exploratory test is
executed. Please see Test Data Strategy for the different environments
and type of test data.

Infrastructure Requirements

The infrastructure required for exploratory testing is:

-   Test Environment

-   JIRA

-   Zephyr

 

 

System Test Strategy

June 25, 2019

9:44 AM

This section provides an overview of the test approach that will be
undertaken for System Testing. System testing occurs at 100%
integration, i.e., once all the components in the system planned for the
specific sprint have been integrated together. 

Definition

The process of testing an integrated system to verify that it meets
specified requirements.  During System Testing, the features and
requirements of the product as defined are tested.  Only after it has
been determined that the product meets a predetermined quality level,
should the product system integration testing begin. The integration of
systems and packages; interfaces to external organizations
(e.g. addressing integration with existing applications - purchased
packages and legacy, internally developed software - as well as
effective security, infrastructure, performance, and network
support/optimization) is tested.

Objectives

-   Verify the fully integrated system works correctly

-   Verify non-functional requirements specified for the system

-   Verify end-to-end functionality including all integration points

Expected Benefits

-   Correctly working and behaving system

-   System conforms to the non-functional requirements

-   System is proven ready for deployment

Responsibilities

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead                            X                        
  Test Analyst (Agile)         X                                
  Business Tester                              X                
  Test Automation Specialist                   X                
  Business Analyst                                     X        
  Business Lead                                        X        
  Developer                                    X                
  Developer Lead                                               X
  Solution Architect                                   X        
  Release Manager                              X                
  Project Manager                                              X

Scope

-   Business End-to-End testing: 

    -   *Testing a business process from its start through all steps
        > until a conclusion has been reached. This could involve
        > accessing multiple systems.*

-   System Integration testing

    -   *Testing the system\'s capability to operate and integrate with
        > other systems.*

-   Browser compatibility testing

    -   *Testing with the browsers that need to be supported.
        > See Browser/OS Matrix and *

-   Functional Testing

-   Usability testing

    -   *Testing system usability from a user\'s perspective.*

```{=html}
<!-- -->
```
-   Security testing (Roles and Access)

-   Exploratory testing

-   Regression testing

```{=html}
<!-- -->
```
-   Installation testing

    -   *Verification of the installation procedure for Staging and
        > Production.*

-   Recovery testing and failover testing

    -   *Testing forced failure of the system in a variety of ways to
        > verify that recovery is properly performed.*

-   Accessibility testing

    -   *Accessibility testing is a subset of usability testing where in
        > the users under consideration are people with all abilities
        > and disabilities.*

```{=html}
<!-- -->
```
-   Automated Testing

Approach

System Testing activities should only progress once it is established
that the system functions as intended. Functional Testing plays a major
role in this assessment. System testing also requires a fully integrated
system. For PPR that means that the functionality that is delivered in
the sprint is completely integrated with all components that it needs.
If not all components are available because they are planned for a later
sprint, full system integration testing for that functionality needs to
be planned for a later sprint.

Not all system testing scope will be able to be executed in the earlier
sprints. Some activities might simply be a waste of time if planned too
soon. The following table indicates the targeted tests in early sprints
(the first 5) and later sprints:

+----------------------------------+----------------------------------+
| **Activity**                     | **When**                         |
+==================================+==================================+
| Business End-to-End testing      | All Sprints                      |
|                                  |                                  |
|                                  |                                  |
+----------------------------------+----------------------------------+
| System Integration testing       | All Sprints                      |
+----------------------------------+----------------------------------+
| Browser compatibility testing    | Early Sprints for quick look,    |
|                                  | then final test at later sprints |
+----------------------------------+----------------------------------+
| Functional Testing               | Early Sprints                    |
+----------------------------------+----------------------------------+
| Usability testing                | Later Sprints, input from user   |
|                                  | experience sessions              |
+----------------------------------+----------------------------------+
| Security testing (Roles and      | Later Sprints                    |
| Access)                          |                                  |
+----------------------------------+----------------------------------+
| Exploratory testing              | All Sprints                      |
+----------------------------------+----------------------------------+
| Regression testing               | All Sprints                      |
+----------------------------------+----------------------------------+
| Installation testing             | Later Sprints                    |
+----------------------------------+----------------------------------+
| Recovery testing and failover    | Later Sprints                    |
| testing                          |                                  |
+----------------------------------+----------------------------------+
| Accessibility testing (TBD)      | Later Sprints                    |
+----------------------------------+----------------------------------+
| Automated Testing                | All Sprints                      |
+----------------------------------+----------------------------------+

A detailed plan per sprint indicates what is in scope for that sprint.

Test Design

Similar approach as with Functional Test Strategy. The design for System
Integration test differs in scope as we are evaluating the system
holistically and not on individual functionalities.

Test Execution

System Integration Testing will be executed by the agile testers. During
execution in the early sprints, user acceptance testers will be
operating in the same environment pursuing their acceptance testing
goals.

Data Requirements

  **Usage**                    **Environment**   **Type of Test Data**                                                                                     **User**      **Comments**
  ---------------------------- ----------------- --------------------------------------------------------------------------------------------------------- ------------- --------------
  System Integration Testing   TEST              Subset of masked data and purposely created test data, but using a different and stable subset of data.   All testing    

Infrastructure Requirements

+-------------+-------------+-------------+-------------+-------------+
| **Type of   | **Envir     | *           | **Who**     | **De        |
| Testing**   | onment(s)** | *Integrated |             | scription** |
|             |             | with Back   |             |             |
|             |             | end**       |             |             |
+=============+=============+=============+=============+=============+
| [System /   | TEST        | Yes         | Agile       | In this     |
| Intersystem |             |             | Testers     | environment |
| Te          |             |             |             | we will be  |
| sting](http |             |             |             | able to     |
| ://localhos |             |             |             | test the    |
| t:8090/disp |             |             |             | full end to |
| lay/TQA/5.4 |             |             |             | end         |
| +System+Tes |             |             |             | integration |
| t+Strategy) |             |             |             | including   |
|             |             |             |             | back end    |
|             |             |             |             | services.   |
+-------------+-------------+-------------+-------------+-------------+

 

 

User Acceptance Test Strategy

June 25, 2019

9:44 AM

This section provides an overview of the test approach that will be
undertaken for User Acceptance Testing (UAT). This process obtains
confirmation by Testers/Business Analysts, from the business, that a
system meets mutually agreed-upon requirements. 

Definition

Formal verification/validation with respect to user needs, requirements
and business processes conducted to determine whether or not a system
satisfies the acceptance criteria and to enable the user, customers or
other authorized entity to determine whether or not to accept the
system.

UAT is one of the final stages of a project and often occurs before a
client or customer accepts the new system.

Objectives

-   Verify that the user acceptance criteria are met

-   Verify that the system will serve its intended purpose.

-   Verify that the application is ready to be deployed

Expected Benefits

-   Compliance with the business requirements will be clear.

-   Functionality/business logic problems that earlier testing might
    > have missed will be identified.

-   Determination on how "done" the system is.

-   System ownership acceptance by the business.

-   Improve/establish confidence with the new solution.

Responsibilities

[RASCI
Legend](onenote:RASCI%20Legend.one#section-id={75397548-6BE0-46FB-80CC-551FBC2B6C97}&end&base-path=https://citz.sp.gov.bc.ca/sites/Shared/Project/BidR/BCBid/CONTRACT%20%20SCHEDULE/Testing/Resources/Testing%20Notes)

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead                                    X                
  Test Analyst (Agile)                         X                
  Business Tester              X                                
  Test Automation Specialist                   X                
  Business Analyst                             X                
  UAT Lead                             X                        
  Business Lead                                X                
  Developer                                    X                
  Developer Lead                                               X
  Solution Architect                                           X
  Release Manager                              X                
  Project Manager                                              X

Scope

UAT adds value to the test and validation process when it focuses on the
topics that have not been evaluated before with a user-centric focus.

UAT focuses on:

-   Business Process Validation

-   Business Scenario variations validation

-   Alignment with internal business processes

-   Validation of Portal Documentation and Content 

-   User Experience evaluation

-   Business Effectiveness assessment

-   Reporting validation

UAT does **not** need to focus on:

-   Technical correctness of functionality

-   Access Rules and implementation in the solution (a review would
    > still be welcome)

-   In-screen validations

In other words: All the testing that has been performed by the
developers and testers.

Approach

For PPR we distinguish between 3 different categories of activities
which could be characterized as UAT. These are:

1.  **Early Sprints Verification and Validation**: During the first
    > sprints, UAT related activities will be limited to verification
    > and validation based on user stories and functional acceptance
    > criteria. This activity also allows the UAT group a more gradual
    > introduction into the application, the testing work and the
    > requirements. These sessions will allow the UAT team to refine
    > their approach, engage with the team and start to give feedback.
    > During this, the team would not be required to create a formal UAT
    > approval. During the early sprints, the UAT testers will only be
    > participating for the last 7/8 working days of the sprint. 

2.  **Later Sprints UAT**: The last 3 Sprints, become more like a
    > regular, end-of-project, UAT. The UAT team has now prepared their
    > test cases and scenarios and is prepared to execute these. They
    > will also validate and re-test defect fixes on earlier found
    > issues. At the end of the last Sprint, the team will be in a
    > position to accept the solution. UAT during the later sprints will
    > be a one month full-time effort (full sprint length).

3.  **User Experience Focus Groups**: This activity is the
    > responsibility of PPR BA Team and will involve engaging with the
    > member community to obtain their feedback on the new solution.
    > These sessions will start once several pieces of functionality
    > have been developed and can demonstrated.

**Difference in the UAT experience between a traditional project and
PPR**

+----------------+----------------+----------------+----------------+
| ** **          | **Traditional  | **PPR**        | **PPR**        |
|                | Project**      |                |                |
|                |                | **During       | **Before       |
|                |                | Sprints**      | Release**      |
+================+================+================+================+
| **Readiness    | ** **          | ** **          | ** **          |
| for Test       |                |                |                |
| Design**       |                |                |                |
+----------------+----------------+----------------+----------------+
|                | Business       | User Stories   | User Stories   |
|                | Requirements   | and acceptance | and acceptance |
|                | are available  | criteria have  | criteria have  |
|                | and approved   | gone through   | largely        |
|                |                | reviews. They  | stabilized.    |
|                |                | can (and often | Changes in     |
|                |                | will) still    | scope,         |
|                |                | change. This   | functionality  |
|                |                | means that UAT | and objectives |
|                |                | testers will   | can still be   |
|                |                | potentially    | possible. UAT  |
|                |                | have to rework | testers have a |
|                |                | test design.   | more stable    |
|                |                | The user       | set of         |
|                |                | stories        | information to |
|                |                | targeted for   | base their     |
|                |                | delivery in    | tests and test |
|                |                | the sprint     | scenarios on.  |
|                |                | will be of a   |                |
|                |                | good-enough    |                |
|                |                | state to       |                |
|                |                | progress with  |                |
|                |                | test design.   |                |
+----------------+----------------+----------------+----------------+
| **Readiness    | ** **          | ** **          | ** **          |
| for            |                |                |                |
| Execution**    |                |                |                |
+----------------+----------------+----------------+----------------+
|                | Application is | Application is | Most of the    |
|                | fully          | only partly    | application    |
|                | developed      | developed,     | will be        |
|                |                | gaps are still | present and    |
|                |                | present.       | complete but   |
|                |                | Application    | the later      |
|                |                | might not yet  | sprints will   |
|                |                | be fully       | still add new  |
|                |                | integrated     | functionality. |
|                |                | with back-end  |                |
|                |                | or external    |                |
|                |                | services.      |                |
|                |                | Security,      |                |
|                |                | Roles etc. are |                |
|                |                | still at a     |                |
|                |                | development    |                |
|                |                | team level.    |                |
+----------------+----------------+----------------+----------------+
|                | Unit Testing,  | Unit and       | Most of the    |
|                | Integration    | Integration    | Unit and       |
|                | Testing &      | testing will   | Integration    |
|                | System Testing | be complete,   | testing will   |
|                | is completed   | but System     | be complete    |
|                |                | testing will   | and System     |
|                |                | happen in      | testing will   |
|                |                | parallel.      | be largely     |
|                |                |                | complete but   |
|                |                |                | not finalized. |
|                |                |                | UAT will need  |
|                |                |                | to happen in   |
|                |                |                | parallel.      |
+----------------+----------------+----------------+----------------+
|                | No             | There will be  | There will be  |
|                | Showstoppers,  | showstoppers   | showstoppers   |
|                | High, Medium   | and open       | and open       |
|                | defects from   | defects, but   | defects, but   |
|                | testing left   | towards the    | towards the    |
|                | open           | end of the     | end of the     |
|                |                | sprint they    | sprint they    |
|                |                | will be        | will be        |
|                |                | resolved (or   | resolved (or   |
|                |                | fixes will be  | fixes will be  |
|                |                | postponed)     | postponed). At |
|                |                |                | the end of the |
|                |                |                | sprint it is   |
|                |                |                | determined if  |
|                |                |                | any of the     |
|                |                |                | open items     |
|                |                |                | require        |
|                |                |                | re-planning or |
|                |                |                | deferral.      |
+----------------+----------------+----------------+----------------+
|                | Regression     | Regression     | Regression     |
|                | Testing has    | testing for    | will be        |
|                | completed      | the sprint     | ongoing, UAT   |
|                |                | will still be  | needs to be    |
|                |                | ongoing.       | executed in    |
|                |                |                | parallel.      |
+----------------+----------------+----------------+----------------+
|                | Staging is     | Staging is not | Staging will   |
|                | ready          | yet ready,     | be ready. Data |
|                |                | testing will   | for testing    |
|                |                | happen in the  | needs to be    |
|                |                | TEST           | identified in  |
|                |                | environment.   | Staging.       |
|                |                | Data for       |                |
|                |                | testing needs  |                |
|                |                | to be          |                |
|                |                | identified in  |                |
|                |                | TEST or needs  |                |
|                |                | to be created  |                |
|                |                | for the UAT    |                |
|                |                | team.          |                |
+----------------+----------------+----------------+----------------+
| **UAT Done**   | ** **          | ** **          | ** **          |
+----------------+----------------+----------------+----------------+
|                | All UAT Tests  | Work planned   | Work planned   |
|                | have been      | for the Sprint | for the Sprint |
|                | executed       | has been       | has been       |
|                |                | executed.      | executed and   |
|                |                |                | the UAT goals  |
|                |                |                | have been met. |
+----------------+----------------+----------------+----------------+
|                | No open        | No open        | No open        |
|                | issues/defects | issues, all    | issues, all    |
|                |                | issues are     | issues are     |
|                |                | closed or      | closed,        |
|                |                | deferred to a  | deferred to a  |
|                |                | next sprint.   | future round   |
|                |                |                | or considered  |
|                |                |                | acceptable.    |
+----------------+----------------+----------------+----------------+

Early involvement of UAT has significant benefits to the project as
user/business perspective is valuable and increases the success of the
project.

Test Design

Test design is a hybrid of standard test cases and exploratory sessions.
Exploratory sessions will be in focus for verification and validation in
the earlier Sprints to help with the higher levels of ongoing change. In
the later sprints, test cases will be used.

Exploratory sessions focus on:

-   Business End-to-End process

-   Business Process Variation

-   User Experience

-   Content and Document Validation

-   Reporting

Test Cases focus on:

-   Business End-to-End process

-   Business Process Variation

-   Business Process Alignment

-   Content and Document Validation

-   Reporting

Both Test Cases and exploratory sessions are recorded in the Zephyr test
management tool. Test cases will typically not contain detailed
navigational steps. UAT test design progress and status will be reported
by the Test Lead.

UAT test cases will be incorporated into the automated testing suite if
they prove to be viable automation candidates. With the multiple
iterations that the different sprint provide, this will help the UAT
testers focus on new tests and new exploratory sessions and not on
regression testing previously executed tests.

Test Execution

In the context of PPR we do have an extra challenge with regards to the
end users of the system. As some of our end users are not internal to
the organization, a different strategy was conceived to solicit their
input. This will be the User Experience Focus Groups that will be held
several times during the development of the PPR system. This activity
is **not** in scope for the core test team.

 

+----------------+----------------+----------------+----------------+
| **Activity**   | **When**       | **Who**        | **Re           |
|                |                |                | sponsibility** |
+================+================+================+================+
| Verification   | During Sprints | Business       | PPR Team       |
| and Validation | (last 7/       | Testers        |                |
|                |                |                |                |
|                | 8 days)        |                |                |
+----------------+----------------+----------------+----------------+
| UAT            | Before Release | Business       | PPR Team       |
| (              |                | Testers        |                |
| consolidation) |                |                |                |
+----------------+----------------+----------------+----------------+
| User           | 2/3 Times      | Typical        | PPR Team       |
| Experience     | during sprints | clients,       |                |
| Focus Groups   |                | suppliers,     |                |
|                |                | buyers         |                |
+----------------+----------------+----------------+----------------+

Data Requirements

  **Usage**                      **Environment**   **Type of Test Data**   **User**                  **Comments**
  ------------------------------ ----------------- ----------------------- ------------------------- -------------------------------------------------------------------------
  User Acceptance Testing        TEST              Test data               Business Analysts/Users    
  User Experience Focus Groups   TEST              Test data               Buyers/Suppliers          The team will facilitate access during the user experience focus groups

Infrastructure Requirements

  **Type of Testing**            **Environment(s)**   **Integrated with Back end**   **Who**                         **Description**
  ------------------------------ -------------------- ------------------------------ ------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  User Acceptance Testing        TEST                 Yes                            Testers (User/Business Focus)   The UAT will require a system that contains masked/de-identified production data. The staging environment will be close to an exact copy of production, providing the UAT testers with realistic experience.
  User Experience Focus Groups   TEST                 Yes                            Buyers/Suppliers                Temporary access to participating members will be provided.

 

 

Smoke Test Strategy

June 25, 2019

9:44 AM

This section provides an overview of the test approach that we will
deploy for Smoke Testing.  

A frequent characteristic of a smoke test is that it runs quickly, often
in the order of a few minutes, giving the benefit of quicker feedback
and faster turnaround than the running of full test suites which can
take hours or even days. Smoke testing performed on a particular build
is also known as a build verification test. A daily build and smoke test
is among industry best practices. Smoke testing is also done by testers
before accepting a build for further testing. Microsoft claims that
after code reviews, \"smoke testing is the most cost-effective method
for identifying and fixing defects in software\". 

One can perform smoke tests either manually or using an automated tool.
In the case of automated tools, the tests are often initiated by the
same process that generates the build itself.

 

***Smoke Test Origin***

*From the electronics industry: The term \"smoke test\" refers to
powering on a device simply to make sure it doesn\'t start smoking
(indicating a major problem).*

Definition

A subset of all defined/planned test cases that cover the main
functionality of a component or system, to ascertain that the most
crucial functions of a program work, but not bothering with finer
details.

Objectives

-   To assess if the installed application is operational

-   To prevent the team from wasting time on a non functional build

-   To quickly identify issues with a newly installed application

Expected Benefits

-   Save time and improve efficiency

-   As smoke tests are typically automated, they can be run as part of
    > the build and release process

-   Early detection of obvious issues

-   Prevention of wasted cycles because of releasing a non functional
    > build

Responsibilities

[RASCI
Legend](onenote:RASCI%20Legend.one#section-id={75397548-6BE0-46FB-80CC-551FBC2B6C97}&end&base-path=https://citz.sp.gov.bc.ca/sites/Shared/Project/BidR/BCBid/CONTRACT%20%20SCHEDULE/Testing/Resources/Testing%20Notes)

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead                            X                        
  Test Analyst (Agile)                         X                
  Business Tester                                               
  Test Automation Specialist   X                                
  Business Analyst                                              
  Business Lead                                                 
  Developer                                    X                
  Developer Lead                               X                
  Portal Architect                                              
  Release Manager                              X                
  Project Manager                                              X

Both the Test Lead and DevOps have a strong vested interest in a strong,
consistent and quick smoke test.

Scope

A good smoke test addresses the key capabilities of the provided build.
By verifying these key capabilities, we\'ll gain a good insight into the
configuration (and eventual problems) of the build.

The following table indicates the types of test, order and what
information we will be able to infer from the result.

+-------+----------+----------+----------+----------+----------+
| ** ** | **Test** | **Inf    | **Inf    | **Action | **       |
|       |          | ormation | ormation | needed** | Impact** |
|       |          | obtained | obtained |          |          |
|       |          | if**     | if**     | **if     |          |
|       |          |          |          | Failed** |          |
|       |          | **OK**   | **       |          |          |
|       |          |          | Failed** |          |          |
+=======+==========+==========+==========+==========+==========+
| 1     | Open URL | Web      | System   | I        | Testing  |
|       |          | portion  | is down  | mmediate | cannot   |
|       |          | of       |          | es       | proceed  |
|       |          | system   |          | calation |          |
|       |          | works,   |          | to fix   |          |
|       |          | un       |          |          |          |
|       |          | derlying |          |          |          |
|       |          | database |          |          |          |
|       |          | is       |          |          |          |
|       |          | c        |          |          |          |
|       |          | onnected |          |          |          |
+-------+----------+----------+----------+----------+----------+
| 2     | Log in   | Authen   | Authen   | I        | Testing  |
|       |          | tication | tication | mmediate | cannot   |
|       |          | m        | m        | es       | proceed  |
|       |          | echanism | echanism | calation |          |
|       |          | works    | is       | to fix   |          |
|       |          |          | bro      |          |          |
|       |          |          | ken/disc |          |          |
|       |          |          | onnected |          |          |
|       |          |          | or       |          |          |
|       |          |          | mis-co   |          |          |
|       |          |          | nfigured |          |          |
+-------+----------+----------+----------+----------+----------+
| 3     | Search   | Database | Portal   | Review   | Testing  |
|       | for      | is       | database | and fix  | cannot   |
|       | inf      | c        | and/or   | problem  | proceed  |
|       | ormation | onnected | search   |          |          |
|       | in the   | and      | m        |          |          |
|       | portal   | contains | echanism |          |          |
|       |          | se       | is       |          |          |
|       |          | archable | broke    |          |          |
|       |          | data     | n/mis-co |          |          |
|       |          |          | nfigured |          |          |
+-------+----------+----------+----------+----------+----------+
| 4     | Navigate | Funct    | Funct    | Review   | Testing  |
|       | to key   | ionality | ionality | and add  | can only |
|       | functi   | is       | is       | funct    | p        |
|       | onality, | present  | missing, | ionality | artially |
|       | most     | in the   | code was | to build | proceed  |
|       | i        | right    | not      |          | but will |
|       | mportant | l        | added or |          | be       |
|       | funct    | ocation, | confi    |          | hampered |
|       | ionality | code is  | guration |          |          |
|       | first    | present  | was not  |          |          |
|       |          |          | updated  |          |          |
|       |          |          | to point |          |          |
|       |          |          | to the   |          |          |
|       |          |          | new code |          |          |
+-------+----------+----------+----------+----------+----------+
| 5     | > Use    | Funct    | > Fails  | Review   | Testing  |
|       | > key    | ionality | > on:    | and fix  | can only |
|       | > funct  | b        |          | problem  | p        |
|       | ionality | asically | -        |          | artially |
|       | > in the | works.   |  Search: |          | proceed  |
|       | > f      | Back-end |     >    |          | but will |
|       | ollowing | is       | Database |          | be       |
|       | > order  | c        |     > or |          | hampered |
|       | > as     | onnected |     >    |          |          |
|       | > simple | and      | back-end |          |          |
|       | > as     | ope      |     >    |          |          |
|       | > p      | rational |  systems |          |          |
|       | ossible: |          |          |          |          |
|       |          |          |    > not |          |          |
|       | -        |          |     > c  |          |          |
|       |   Search |          | onnected |          |          |
|       |          |          |          |          |          |
|       | -        |          | -        |          |          |
|       |   Select |          |  Select: |          |          |
|       |          |          |          |          |          |
|       | -        |          |    > Inf |          |          |
|       |   Create |          | ormation |          |          |
|       |          |          |     >    |          |          |
|       | -        |          | selected |          |          |
|       |   Update |          |     > is |          |          |
|       |          |          |          |          |          |
|       | -        |          |    > not |          |          |
|       |   Delete |          |          |          |          |
|       |          |          | > shown, |          |          |
|       |          |          |     >    |          |          |
|       |          |          |  problem |          |          |
|       |          |          |     > in |          |          |
|       |          |          |          |          |          |
|       |          |          |  > funct |          |          |
|       |          |          | ionality |          |          |
|       |          |          |          |          |          |
|       |          |          | -   Crea |          |          |
|       |          |          | te: Data |          |          |
|       |          |          |     > is |          |          |
|       |          |          |          |          |          |
|       |          |          |    > not |          |          |
|       |          |          |     >    |          |          |
|       |          |          |  stored, |          |          |
|       |          |          |     >    |          |          |
|       |          |          | database |          |          |
|       |          |          |     > or |          |          |
|       |          |          |          |          |          |
|       |          |          | > rights |          |          |
|       |          |          |     >    |          |          |
|       |          |          |  problem |          |          |
|       |          |          |          |          |          |
|       |          |          | -        |          |          |
|       |          |          |  Update: |          |          |
|       |          |          |          |          |          |
|       |          |          |   > Data |          |          |
|       |          |          |     > is |          |          |
|       |          |          |          |          |          |
|       |          |          |    > not |          |          |
|       |          |          |     >    |          |          |
|       |          |          |  stored, |          |          |
|       |          |          |     >    |          |          |
|       |          |          | database |          |          |
|       |          |          |     > or |          |          |
|       |          |          |          |          |          |
|       |          |          | > rights |          |          |
|       |          |          |     >    |          |          |
|       |          |          |  problem |          |          |
|       |          |          |          |          |          |
|       |          |          | -        |          |          |
|       |          |          |  Delete: |          |          |
|       |          |          |     >    |          |          |
|       |          |          | Database |          |          |
|       |          |          |     > or |          |          |
|       |          |          |          |          |          |
|       |          |          | > rights |          |          |
|       |          |          |     >    |          |          |
|       |          |          |  problem |          |          |
|       |          |          |          |          |          |
|       |          |          | -   With |          |          |
|       |          |          |          |          |          |
|       |          |          |    > all |          |          |
|       |          |          |          |          |          |
|       |          |          |    > the |          |          |
|       |          |          |          |          |          |
|       |          |          | > above: |          |          |
|       |          |          |          |          |          |
|       |          |          |  > issue |          |          |
|       |          |          |          |          |          |
|       |          |          |   > with |          |          |
|       |          |          |     >    |          |          |
|       |          |          | back-end |          |          |
|       |          |          |     >    |          |          |
|       |          |          |  systems |          |          |
+-------+----------+----------+----------+----------+----------+
| 6     | Trigger  | External | External | Review   | Testing  |
|       | key      | systems  | systems  | and fix  | cannot   |
|       | int      | are up   | are      | problem  | proceed  |
|       | egration | and      | either   |          |          |
|       | points   | running  | down,    |          |          |
|       | with     | and      | not      |          |          |
|       | external | co       | c        |          |          |
|       | systems  | nfigured | onnected |          |          |
|       |          | c        | or not   |          |          |
|       |          | orrectly | co       |          |          |
|       |          |          | nfigured |          |          |
|       |          |          | c        |          |          |
|       |          |          | orrectly |          |          |
+-------+----------+----------+----------+----------+----------+

Typically a failed smoke test means that the build does not get accepted
into testing (or release) until the found issues have been addressed. A
failed smoke test is a critical priority item to address as following
activities are now halted.

Approach

We will start building our smoke test (both automated and manual checks)
as soon as code is built.

The smoke test will consist of:

-   Selected Unit and Integration Tests

-   Selected automated functional tests

-   Custom (smoke test only) automated tests and checks

-   Manual inspection

Smoke test has the following characteristics:

-   The duration will not be longer than 10 minutes, preferably shorter

-   It is highly repeatable as it build to avoid dependencies on
    > existing data, previous transaction etc.

-   It is to the point and superficial

-   It does not tell us anything about the quality of the functionality
    > (merely that it is there and seems to function)

-   It is mostly automated (as close to 100% as possible)

-   It will change based on demand, lessons learned, risk etc.

When new configuration is added to the build, we will:

-   Investigate what this code does and what minimally needs to work

-   Review the existing unit test scripts for candidacy for the smoke
    > test

-   Identify functional scripts that need to be created and build them

-   Integrate the new scripts into the smoke test

As part of the sprint end phase we will review the smoke test scripts to
make sure that we have the slimmest and most effective approach that can
be carried forward into the next sprint.

Test Design

See scope for the type of tests that we will have to design.

Characteristics of the tests are:

-   Simple: these are not major functional tests, these tests skim the
    > surface

-   Independent: each test should be able to run as an independent unit

-   Fast: each individual test should run no longer than a few seconds

-   Easy to understand: the test objective must be clear and easy to
    > understand

-   Automated: automation is essential for success

-   Parameterized: to provide flexibility in running them against a
    > variety of environments (like build, test, staging and production)

Test case aim to isolate:

-   Environmental Issues

-   Configuration issues

-   System Issues

-   Installation Issues

-   Inter-connectivity/integration issues

-   Build issues

-   Application Issues

Test Execution

The smoke tests will be executed:

-   As part of the build process and release process

-   Any time a build is placed in an environment

-   Any time any change is introduced in an environment (code,
    > configuration, system etc.)

A fully developed smoke test suite can also be (re-)used when the
application is released in production.

In that case, the following caveats must be taken into account:

-   Typically we would need to forego, writing, updating or deleting
    > information (unless specific test accounts are available for
    > exactly this purpose)

-   The smoke test will not be a replacement for the business user
    > production-ready check

Data Requirements

The smoke test would need test data that was already identified for the
existing re-purposed tests or will need to be created. See Test
Environments Needs

Infrastructure Requirements

Smoke test will utilize the QA Automation infrastructure.

 

 

Regression Test Strategy

June 25, 2019

9:44 AM

This section provides an overview of the test approach that will be
undertaken for Regression Testing. Automated regression testing is
essential to agile projects, with sprints moving forward rapidly and
with a searchlight focus on specific functionality, it is unlikely that
the team will have time to spend time regression testing previously
developed functionality. Test automation needs to fill that gap. 

Definition

Regression testing is a type of software testing that seeks to uncover
problems, or regressions, in existing functional and non-functional
areas of a system after changes such as enhancements, patches or
configuration changes, have been made to them.

Regression testing is guided by the following principle: 

 

> **Regression Test Principle**
>
> **Basic assumption(s):**

-   Systems need to be tested for regression errors after changes.

-   The scope of the regression test is dependent on risk.

> **Test Principle:**

-   Systems will be regression tested to mitigate risk on unintended
    > errors after changes.

-   Regression tests will be automated where appropriate.

Objectives

-   Ensure that defects have not been introduced or uncovered in
    > unchanged areas of the software, as a result of changes made

-   Create confidence in the solution by making sure that \"everything
    > still works\"

-   Through automation relieve the testers from manually running
    > regression tests

Expected Benefits

-   Confidence in the solution

-   Support the agile process

-   Build a regression test suite that can be used for the lifetime of
    > the solution

 

**Regression testing will not...**

-   Find new functionality defects

-   Find many defects

The effort versus effectivity in finding defects ratio is lopsided in
regression testing, which is often the reason why manual regression
testing is cut short, optimized or even ignored.

Responsibilities

[RASCI
Legend](onenote:RASCI%20Legend.one#section-id={75397548-6BE0-46FB-80CC-551FBC2B6C97}&end&base-path=https://citz.sp.gov.bc.ca/sites/Shared/Project/BidR/BCBid/CONTRACT%20%20SCHEDULE/Testing/Resources/Testing%20Notes)

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead                            X                        
  Test Analyst (Agile)                         X                
  Business Tester                              X                
  Test Automation Specialist   X                                
  Business Analyst                                     X        
  Business Lead                                        X        
  Developer                                            X        
  Developer Lead                                       X        
  Solution Architect                                   X        
  Release Manager                                              X
  Project Manager                                              X

Scope

The scope of regression testing is significantly larger than for smoke
testing. This does not mean that we\'ll (re-)test everything in our
regressions tests (automated or not), we want to be effective, frugal
and smart about our choice for the scope of our regression tests.

Guidelines for scope:

-   Focus on functionality and not design

-   Identify unique tests, do not repeat tests

-   Code changes are important but data changes (variations) need to be
    > considered too

-   Write regression tests for important bug fixes

See also the Test Design section for guidance on coverage.

Approach

Regression testing exists because of modifications to the application
code, system and configuration. But testing modifications involves more
than just regression testing.

How do we test a modification?  The answer is that four types of testing
are needed:

> **The unit test**, where the developer who is making the modification
> checks his or her work.  This testing concerns the internal changes to
> the source code, data structures, and stored data values. 
>
> **The modification test**, also called the localized change test. 
> This testing is done on the fully integrated, new version of the
> system, and it addresses only the modifications. It can be done by a
> black-box feature tester, and is driven by the change request or
> defect report which describes the intended change. In this phase, the
> goal is to test the direct modifications to the user features.  The
> externally visible changes are based on the internal changes to the
> source code, data structures, and stored data values, but these
> internal changes are usually hidden from the black-box feature
> testers.  The scope of this testing may include changes to the system
> and user documentation, impact on system performance, changes to
> system controls like password authentication, etc.
>
> **The regional impact test.**  This level of testing goes beyond
> checking the modification itself, and tests in the perceived
> high-impact region around the change.  The black-box feature tester
> needs to have some understanding of the system, what connects to what,
> in order to identify the likely high-impact region.  This testing is a
> compromise: it goes beyond testing just the modification, but falls
> far short of a full-blown regression test.  In this phase, the goal is
> to test the areas that are likely to be highly influenced by the
> change(s) , e.g., the immediate modules which directly call to, or are
> directly called by, the module that has been changed. 
>
> **The regression test.**  The regression test is broader than the
> modification test or the regional impact test, and its purpose is to
> find unintended and unforeseen side effects of the modification.  In
> regression testing, existing test cases are re-run in areas which
> should not have been affected by the modification, to see if they
> still work the same way as before.  Most regression testing is
> deliberately executed with the complete regression test suite, not
> just focused on where the modification has occurred. In this phase,
> the goal is to re-test the entire system after a change or set of
> changes, to ensure that features which were not intended to change
> still work the same way as before. This extensive re-test is needed if
> there is a concern about unintended side effects of the planed
> changes.  These side effects can include failures in parts of the
> system which seemingly are unrelated to the change, changes in the way
> features work, and the re-surfacing of old defects that supposedly had
> been eradicated.

**Who is responsible for each type of modification test?**

  **Type of Test**       **Responsible**                     **Manual/Automated?**
  ---------------------- ----------------------------------- ---------------------------------------------------------------------------------------
  Unit Test              Developer                           First manual but later automated as part of the automated unit test suite
  Modification Test      Tester                              Focus on manual, but potentially migrating into the automated regression test suite
  Regional Impact Test   Tester                              Focus on manual, but potentially migrating into the automated regression test suite
  Regression Test        Tester/Test Automation Specialist   Focus on automated testing, but individual test cases will start as manual test cases

**Steps**

The team will take the following steps to develop a regression test
suite. Please see Test Design for the categories of tests that will be
included in the regression test suite.

1.  Analyze requirements and develop tests for business criticality,
    > complexity and frequent use. These tests will be marked as
    > regression test candidates.

2.  Review (on an ongoing basis, basically every build) new and updated
    > functionality and configuration. This will most likely result in
    > tests that need to be added to the suite

3.  Identify critical defects, test fails and bad fixes for inclusion

4.  From the exploratory testing sessions identify regression test
    > candidates

5.  Document and first manual test all new tests

6.  Automate identified tests and include them in the automated testing
    > suite

7.  Run the automated regression test suite

8.  Review results and investigate and escalate any found issues

On a regular basis:

-   Review suite effectiveness

-   Add new tests

-   Optimize execution

Test Design

In the design of our regression test suite we have to consider
criticality, time available and the amount of value/comfort the tests
add. An inclusion of all the tests that the test team has developed is
typically not a very efficient way of structuring the regression test.
The risk is that a lot of time will be spend on designing/automating
tests that add very little value.

We use the following guideline to determine the **minimal** degree of
coverage in our regression test:

  **Category**                                 **Degree of Coverage**   **Description**
  -------------------------------------------- ------------------------ --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Smoke test                                   100%                     A smoke test as the start of a regression test suite is highly advisable, we will re-use smoke test artifacts.
  Test cases which have failed in the past                              It is good practice to include \"troublesome\" test cases into the regression suite as experience has taught that trouble will, on occasion, emerge again.
  *Critical errors*                            100%                      
  *Moderate or minor errors*                   10% to 20%                
  Test cases for basic functionality           5% to 10%                In regression tests there should be an under-emphasis on basic functionality. In our case, it does not make sense to create extensive regressions tests for out-of-the-box (OOTB) iValua functionality. Examples of basic tests are: navigation, link following, using the OOTB portal functionality, login, logout etc.
  Test cases for complex features              25% to 50%               Complex features have a large potential for the introduction of unintentional errors when changes are applied. The chance of finding regression errors is therefore higher and adding these test cases to the test suite adds values.
  Test cases for heavily used features         25% to 50%               Heavily used features have greater user visibility and we need to make sure that no unforeseen errors sneak in.
  Test cases for business-critical features    50% to 100%              Business critical features deal with finances and personal information. Failure of these features would cause data corruption, information breach or could leave the members data incomplete or incorrect.
  Bad fix test cases                           100%                     Bad fix is the term for a defect that was fixed but after re-test was still found in error. It is good practice to include these in the regression test suite.

In our test management tool (Zephyr) we will categorize and document all
our test cases so that candidacy for the regression test suite can
easily be identified and understood.

**Source of regression test cases**

Regression test cases are obtained from the following sources:

-   Manual Test cases developed by the testers

-   Exploratory Test session results

-   Failed Test cases

-   Bad fix test cases

-   Developer input

-   Business Analyst input

-   Test Automation input

**Increasing coverage**

With test automation, we can, over time, increase the coverage beyond
the mentioned minimal coverage for our regression test suite.

When considering expanding the regression test suite we will consider
the following:

-   Does the new test case add unique value? (untested area, new
    > functionality, new high risk realization)

-   Is the new test the \"best\" test for the goal we need to achieve.

-   How much time will the new test add to the execution of the
    > regression test suite?

-   What are the requirements for the test case to run in the regression
    > test suite context? (order of execution, test data needed,
    > date/time requirements etc.)

-   Do we have time to create test automation? If not how can we
    > mitigate the risk of not doing it?

**Regression Test Suite Maintenance**

A common problem with regression test suites is that they become stale
and new team members often do not understand why certain tests are even
in the suite. It is not wise to consider the regression test suite a
static entity that will deliver value indefinitely.

There are several factors that diminish the effectiveness of the
regression test suites:

-   The most important among them is when enhancements to the test suite
    > (addition of tests to the test suites) get out of sync with
    > respect to the enhancements to the product. When features get
    > added to the product as part of a Release, there might not be an
    > equal amount of tests added to adequately test the new
    > functionality implemented in the Release. This in effect reduces
    > the functionality coverage achieved by the test suite. 

-   Another factor that affects the **effectiveness** of the test suites
    > is when tests get added to the suite with a short-term
    > perspective. One typical scenario is the case where
    > testers/developers add tests to quickly test a particular
    > functionality or a small part of the feature that is being
    > developed for the current Release or to test a least significant
    > part of a feature or module, mostly as part of their unit testing
    > efforts. Later, these tests, if not removed from the test suite,
    > become a liability because of the improper and insufficient
    > scenarios they test. 

-   A related factor affecting the test suite is the presence
    > of** redundant tests**. There are many scenarios by which a test
    > suite can end up with redundant tests or with two sets of tests
    > that validate almost the same or similar functionality. Testers
    > might add new tests to validate a feature, even when the same
    > could be achieved by modifying some of the existing
    > tests/framework. There might be a case where a feature gets
    > implemented across Releases. When this happens, the corresponding
    > tests also get staggered across Releases. It could happen that the
    > regression test suite would then contain many small tests, each
    > testing trivial parts of the feature, making the test suite
    > bulky. 

-   In most cases, as the product goes on adding new features, the
    > regression **test suite gets heavy** due to the tests that get
    > added to it over a period of time. This will pose new problems.
    > The entire test set might take a longer time now to complete all
    > tests. This will mean that defect identification takes more time,
    > and so also the defect verification after a fix. For example, if
    > it takes a week for the testers to complete all the automated
    > tests for a Release, then it is worth spending time to analyze new
    > ways and means of lessening the time taken for execution and
    > analysis of these tests. 

**Summary**

The following factors are the common causes for diminishing
effectiveness of the regression test suites:

-   Decrease in functionality coverage

-   Tests that get added to the suite with a short-term perspective

-   Presence of redundant tests in the test suites

-   Decrease in test execution time due to presence of many tests

 We will counter the above factors by:

-   Implementing a good tracking mechanism between the feature and its
    > corresponding tests in Zephyr

-   Monitoring addition of tests to the tests suite

-   Optimizing tests when they get bulky

-   Evaluating different Regression Test Selection strategies to avoid
    > time and effort overrun for a Release, but maintaining the minimal
    > coverage guidelines

-   Periodically cleaning of tests and test suite

-   Planning and explore changes in the regression test suite framework
    > if there are major changes in the product focus (reacting as part
    > of our agile methodology)

-   Using metrics to evaluate the effectiveness of the test suite
    > (defect find/miss rates, run time etc.)

Test Execution

Manual regression testing will take place in the regular test
environment and will be scheduled in per build, based on our analysis.

The automated regression tests will be executed:

-   As part of the build and release process

-   Any time a build is placed in an environment

-   Any time any change is introduced in an environment (code,
    > configuration, system etc.)

-   In the Test environments

A fully developed regression test suite is **not** intended to run when
the application is released in the production environment.

Data Requirements

The regression test would need similar test data to what was already
identified for existing tests or it will need to be created. See Test
Environments Needs

The regression test data would work with its own set of accounts etc.
This to avoid any cross-contamination with data that is used by other
users, developers and testers. This own set of data is critical to the
stability of the automated regression test runs.

Infrastructure Requirements

Manual regression testing will take place in the regular TEST
environment.

Automated regressions test will also utilize the TEST environment.

 

 

Performance Test Strategy

June 25, 2019

9:44 AM

This section provides an overview of the test approach that will be
undertaken for Performance Testing.

The risk analysis is attached to this page.

\<\<PPR Performance Risks Worksheet.xlsx\>\>

Definition

Performance testing is a type of testing intended to determine the
responsiveness, throughput, reliability, and/or scalability of a system
under a given workload.

Objectives

-   Assess production readiness

-   Evaluate against performance criteria

-   Find the source of performance problems

-   Support system tuning

Expected Benefits

-   Confidence that the solution will support the anticipated user load

-   Right-sizing of the infrastructure to limit the capital outlay

-   Find errors that can only be found with the solution under load

-   Validation infrastructure choices

Responsibilities

[RASCI
Legend](onenote:RASCI%20Legend.one#section-id={75397548-6BE0-46FB-80CC-551FBC2B6C97}&end&base-path=https://citz.sp.gov.bc.ca/sites/Shared/Project/BidR/BCBid/CONTRACT%20%20SCHEDULE/Testing/Resources/Testing%20Notes)

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead                            X                        
  Test Automation Specialist   X                                
  Developer                                    X                
  Developer Lead                               X                
  Solution Architect                                   X        
  Release Manager                                              X
  Project Manager                                              X

* *

 

 

Security Test Strategy

June 25, 2019

9:44 AM

This section provides an overview of the test approach that will be
undertaken for Security Testing. We will follow the OWASP Testing Guide,
that can be
found [here](https://www.owasp.org/index.php/OWASP_Testing_Guide_v4_Table_of_Contents).

Security testing is a highly specialized task and the project will
depend on an external vendor to deliver. 

Definition

A security test is a method of evaluating the security of a computer
system or network by methodically validating and verifying the
effectiveness of application security controls. 

Objectives

-   Actively analyze the application for any weaknesses, technical
    > flaws, or vulnerabilities. Any security issues that are found will
    > be presented to the system owner, together with an assessment of
    > the impact, a proposal for mitigation or a technical solution.

-   Seek to eliminate the risk of exposing member data to non-authorized
    > parties.

Expected Benefits

-   Improved security

-   Increased level of confidence with the solution

-   Due diligence has been executed

-   Clear identification of remaining risks

-   Recommendations for improvements

Responsibilities

[RASCI
Legend](onenote:RASCI%20Legend.one#section-id={75397548-6BE0-46FB-80CC-551FBC2B6C97}&end&base-path=https://citz.sp.gov.bc.ca/sites/Shared/Project/BidR/BCBid/CONTRACT%20%20SCHEDULE/Testing/Resources/Testing%20Notes)

  **Role **                    **R**   **A**   **S**   **C**   **I**
  ---------------------------- ------- ------- ------- ------- -------
  Test Lead/External Party     X                                
  Test Automation Specialist                   X                
  Developer                                    X                
  Developer Lead               X                                
  Solution Architect                                   X        
  Release Manager                                              X
  Project Manager                      X                        

Scope

The system scope of the security test is:

-   iValua installation

-   PPR Implementation

-   Integration with external services

-   Installation/Configuration of the solution

-   Installation and configuration of the physical/virtual
    > infrastructure

Approach

At a high level the following activities will be executed during the
delivery of security testing:

  **Activity**               **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   **Participants**
  -------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- -----------------------
  Discovery                  The purpose of this stage is to identify systems within scope and the services in use. It is not intended to discover vulnerabilities, but version detection may highlight deprecated versions of software / firmware and thus indicate potential vulnerabilities.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                CGI, iValua
  Vulnerability Scan         Following the discovery stage this looks for known security issues by using automated tools to match conditions with known vulnerabilities. The reported risk level is set automatically by the tool with no manual verification or interpretation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               iValua, CGI, Province
  Vulnerability Assessment   This uses discovery and vulnerability scanning to identify security vulnerabilities and places the findings into the context of the environment under test.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       iValua, CGI, Province
  Security Assessment        Builds upon Vulnerability Assessment by adding manual verification to confirm exposure, but does not include the exploitation of vulnerabilities to gain further access. Verification could be in the form of authorized access to a system to confirm system settings and involve examining logs, system responses, error messages, codes, etc. A Security Assessment is looking to gain a broad coverage of the systems under test but not the depth of exposure that a specific vulnerability could lead to.                                                                                                                                                                                                                                                                                                                   iValua, CGI, Province
  Penetration Test           Penetration test simulates an attack by a malicious party. Building on the previous stages and involves exploitation of found vulnerabilities to gain further access. Using this approach will result in an understanding of the ability of an attacker to gain access to confidential information, affect data integrity or availability of a service and the respective impact. Each test is approached using a consistent and complete methodology in a way that allows the tester to use their problem solving abilities, the output from a range of tools and their own knowledge of networking and systems to find vulnerabilities that would/ could not be identified by automated tools. This approach looks at the depth of attack as compared to the Security Assessment approach that looks at the broader coverage.   iValua, CGI, Province

Additionally the following activities could form part of the engagement
but technically fall outside of the security testing scope:

-   **Security Audit** - Driven by an Audit / Risk function to look at a
    > specific control or compliance issue. Characterised by a narrow
    > scope, this type of engagement could make use of any of the
    > earlier approaches discussed (vulnerability assessment, security
    > assessment, penetration test).

-   **Security Review** - Verification that industry or internal
    > security standards have been applied to system components or
    > product. This is typically completed through gap analysis and
    > utilises build / code reviews or by reviewing design documents and
    > architecture diagrams. This activity does not utilize any of the
    > earlier approaches (Vulnerability Assessment, Security Assessment,
    > Penetration Test, Security Audit)

**Security related activities by the development and release team**

The following are
the [OWASP](https://www.owasp.org/index.php/Main_Page) guidelines for
the development and release team activities:

 

**OWASP Guidelines**

 

**Phase 1: Before Development Begins**

 

**Phase 1.1: Define a SDLC**

Before application development starts an adequate SDLC must be defined
where security is inherent at each stage.

 

**Phase 1.2: Review Policies and Standards**

Ensure that there are appropriate policies, standards, and documentation
in place. Documentation is extremely important as it gives development
teams guidelines and policies that they can follow.

*People can only do the right thing if they know what the right thing
is.*

If the application is to be developed in Java, it is essential that
there is a Java secure coding standard. If the application is to use
cryptography, it is essential that there is a cryptography standard. No
policies or standards can cover every situation that the development
team will face. By documenting the common and predictable issues, there
will be fewer decisions that need to be made during the development
process.

 

**Phase 1.3: Develop Measurement and Metrics Criteria and Ensure
Traceability**

Before development begins, plan the measurement program. By defining
criteria that need to be measured, it provides visibility into defects
in both the process and product. It is essential to define the metrics
before development begins, as there may be a need to modify the process
in order to capture the data.

 

**Phase 2: During Definition and Design**

 

**Phase 2.1: Review Security Requirements**

Security requirements define how an application works from a security
perspective. It is essential that the security requirements are tested.
Testing in this case means testing the assumptions that are made in the
requirements and testing to see if there are gaps in the requirements
definitions.

For example, if there is a security requirement that states that users
must be registered before they can get access to the whitepapers section
of a website, does this mean that the user must be registered with the
system or should the user be authenticated? Ensure that requirements are
as unambiguous as possible.

When looking for requirements gaps, consider looking at security
mechanisms such as:

-   User Management

-   Authentication

-   Authorization

-   Data Confidentiality

-   Integrity

-   Accountability

-   Session Management

-   Transport Security

-   Tiered System Segregation

-   Legislative and standards compliance (including Privacy, Government
    > and Industry standards)

 

**Phase 2.2: Review Design and Architecture**

Applications should have a documented design and architecture. This
documentation can include models, textual documents, and other similar
artifacts. It is essential to test these artifacts to ensure that the
design and architecture enforce the appropriate level of security as
defined in the requirements.

Identifying security flaws in the design phase is not only one of the
most cost-efficient places to identify flaws, but can be one of the most
effective places to make changes. For example, if it is identified that
the design calls for authorization decisions to be made in multiple
places, it may be appropriate to consider a central authorization
component. If the application is performing data validation at multiple
places, it may be appropriate to develop a central validation framework
(ie, fixing input validation in one place, rather than in hundreds of
places, is far cheaper). If weaknesses are discovered, they should be
given to the system architect for alternative approaches. 

 

**Phase 2.3: Create and Review Models**

Once the design and architecture is complete, build models that describe
how the application works. In some cases, these may already be
available. Use these models to confirm with the systems designers an
exact understanding of how the application works. If weaknesses are
discovered, they should be given to the system architect for alternative
approaches. 

 

**Phase 2.4: Create and Review Threat Models**

Armed with design and architecture reviews and the UML models explaining
exactly how the system works, undertake a threat modeling exercise.
Develop realistic threat scenarios. Analyze the design and architecture
to ensure that these threats have been mitigated, accepted by the
business, or assigned to a third party, such as an insurance firm. When
identified threats have no mitigation strategies, revisit the design and
architecture with the systems architect to modify the design. 

 

**Phase 3: During Development**

Theoretically, development is the implementation of a design. However,
in the real world, many design decisions are made during code
development. These are often smaller decisions that were either too
detailed to be described in the design, or issues where no policy or
standard guidance was offered. If the design and architecture were not
adequate, the developer will be faced with many decisions. If there were
insufficient policies and standards, the developer will be faced with
even more decisions. 

 

**Phase 3.1: Code Walk Through (a [Unit Test
Activity](http://localhost:8090/display/TQA/5.1+Unit+Test+Strategy))**

The security team should perform a code walk through with the
developers, and in some cases, the system architects. A code walk
through is a high-level walk through of the code where the developers
can explain the logic and flow of the implemented code. It allows the
code review team to obtain a general understanding of the code, and
allows the developers to explain why certain things were developed the
way they were.

The purpose is not to perform a code review, but to understand at a high
level the flow, the layout, and the structure of the code that makes up
the application. 

 

**Phase 3.2: Code Reviews (a [Unit Test
Activity](http://localhost:8090/display/TQA/5.1+Unit+Test+Strategy))**

Armed with a good understanding of how the code is structured and why
certain things were coded the way they were, the tester can now examine
the actual code for security defects.

Static code reviews validate the code against a set of checklists,
including:

-   Business requirements for availability, confidentiality, and
    > integrity.

-   OWASP Guide or Top 10 Checklists for technical exposures (depending
    > on the depth of the review).

-   Specific issues relating to the language or framework in use, such
    > as the Scarlet paper for PHP or Microsoft Secure Coding checklists
    > for ASP.NET.

-   Any industry specific requirements, such as Sarbanes-Oxley 404,
    > COPPA, ISO/IEC 27002, APRA, HIPAA, Visa Merchant guidelines, or
    > other regulatory regimes.

In terms of return on resources invested (mostly time), static code
reviews produce far higher quality returns than any other security
review method and rely least on the skill of the reviewer. However, they
are not a silver bullet and need to be considered carefully within a
full-spectrum testing regime.

For more details on OWASP checklists, please refer to [OWASP Guide for
Secure Web
Applications](https://www.owasp.org/index.php/OWASP_Guide_Project), or
the latest edition of the [OWASP Top
10](https://www.owasp.org/index.php/OWASP_Top_10).

 

**Phase 4: During Deployment (Security Testing)**

 

**Phase 4.1: Application Penetration Testing**

Having tested the requirements, analyzed the design, and performed code
review, it might be assumed that all issues have been caught. Hopefully
this is the case, but penetration testing the application after it has
been deployed provides a last check to ensure that nothing has been
missed. 

 

**Phase 4.2: Configuration Management Testing**

The application penetration test should include the checking of how the
infrastructure was deployed and secured. While the application may be
secure, a small aspect of the configuration could still be at a default
install stage and vulnerable to exploitation.

 

**Phase 5: Maintenance and Operations**

 

**Phase 5.1: Conduct Operational Management Reviews**

There needs to be a process in place which details how the operational
side of both the application and infrastructure is managed.

 

**Phase 5.2: Conduct Periodic Health Checks**

Monthly or quarterly health checks should be performed on both the
application and infrastructure to ensure no new security risks have been
introduced and that the level of security is still intact.

 

**Phase 5.3: Ensure Change Verification**

After every change has been approved and tested in the QA environment
and deployed into the production environment, it is vital that the
change is checked to ensure that the level of security has not been
affected by the change. This should be integrated into the change
management process.

Process and Schedule for Secure Code reviews and Tests

-   A ticket in JIRA will be created for each sprint, and will document
    > the security tasks to be completed for that sprint.

-   Additionally, in every second sprint, there will be a dedicated 1-2
    > day(s) session to review code for secure code and update if
    > required.

-   Appropriate compliance will be achieved before the January release
    > date.

Schedule and tools that will be used:

-   Vulnerability scanner

    -   OWASP ZAP scanner; schedule TBD

-   Penetration testing

    -   Two penetration tests, two weeks before go-live

-   Manual testing

    -   Manual; Weekly

Test Execution

Security Testing can be executed as part of the sprint test process.

The security testing execution will have to be done well before the
release date once the full integrated and configured system becomes
available.

Data Requirements

Security testing will be executed in the staging environment containing
full size data.

Infrastructure Requirements

The staging environment needs to be configured exactly as the intended
production environment.

This means that the following is identical:

-   Data Size and complexity

-   Application Configuration

-   System Configuration

-   Authentication mechanisms

-   Tools and utilities that will be run on the platforms during
    > production

-   Levels of encryption

 

 

Test Automation Strategy

June 25, 2019

10:34 AM

his section provides an overview of our test automation approach. 

In agile projects, test automation is essential to build, integrate,
test and deploy an application with production-like quality every day.
Agile projects have limited time to conduct existing regression tests
manually so they depend on accurate automated regression testing in
order to maintain effective progress. Test automation is seen as a key
enabler for Agile projects, especially when practices like continuous
integration are used. It also enables the test team to test aspects of
the application that could either be very cumbersome or not possible in
a manual test.

Definition

Automated software testing is a process in which software tools execute
pre-scripted tests on a software application before it is released into
production.

Objectives

The objective of automated testing is to simplify as much of the testing
effort as possible with a minimum set of scripts. Automated testing
tools are capable of executing tests, reporting outcomes and comparing
results with earlier test runs. Tests carried out with these tools can
be run repeatedly, at any time of day.

Specifically test automation aims to:

-   Automate all Unit and Integration tests, so that they can be run as
    > part of the automated build process (CI) (Not applicable to PPR)

-   Provide automated functional tests, that will be used to regression
    > test the solution on a ongoing basis

-   Provide in depth testing in cases where a large amount of variants
    > need to be tested

-   Enable performance testing

Expected Benefits

The following benefits are expected from test automation:

-   Consistent Functional Regression Testing

-   Consistent and frequent smoke testing

-   Prove that new changes did not break the application

-   Consistency and predictability of results

-   Ability to test more variants efficiently

-   Ability to do more testing in the same amount of time

-   Free up the testers to focus on complex test situations and expand
    > on the test design

-   Build up of a body of tests that will repeatedly runs over the
    > lifetime of the application

Responsibilities

[RASCI
Legend](onenote:RASCI%20Legend.one#section-id={75397548-6BE0-46FB-80CC-551FBC2B6C97}&end&base-path=https://citz.sp.gov.bc.ca/sites/Shared/Project/BidR/BCBid/CONTRACT%20%20SCHEDULE/Testing/Resources/Testing%20Notes)

+----------------------------+-------+-------+-------+-------+-------+
| **Role **                  | **R** | **A** | **S** | **C** | **I** |
+============================+=======+=======+=======+=======+=======+
| Test Lead                  |       |  X    |       |       |       |
+----------------------------+-------+-------+-------+-------+-------+
| Test Analyst (Agile)       |       |       | X     |       |       |
+----------------------------+-------+-------+-------+-------+-------+
| Business Tester            |       |       |       |       | X     |
+----------------------------+-------+-------+-------+-------+-------+
| Test Automation Specialist | X     |       |       |       |       |
+----------------------------+-------+-------+-------+-------+-------+
| Business Analyst           |       |       |       | X     |       |
+----------------------------+-------+-------+-------+-------+-------+
| Business Lead              |       |       |       | X     |       |
+----------------------------+-------+-------+-------+-------+-------+
| Developer                  | X     |       |       |       |       |
+----------------------------+-------+-------+-------+-------+-------+
| Developer Lead             |       |  X    |       |       |       |
+----------------------------+-------+-------+-------+-------+-------+
| Solution Architect         |       |       | X     |       |       |
+----------------------------+-------+-------+-------+-------+-------+
| Release Manager            |       |       |       |       | X     |
+----------------------------+-------+-------+-------+-------+-------+
| Subject Matter Expert      |       |       |       |   X   |       |
+----------------------------+-------+-------+-------+-------+-------+
| Auditor                    |       |       |       |       | X     |
|                            |       |       |       |       |       |
|                            |       |       |       |       |       |
+----------------------------+-------+-------+-------+-------+-------+
| Project Manager            |       |       |       |       |  X    |
|                            |       |       |       |       |       |
|                            |       |       |       |       |       |
+----------------------------+-------+-------+-------+-------+-------+

Even though developer and test automation specialist are responsible, we
will aim to include all agile testers in the development of test
automation.

Scope

The scope of test automation in an agile project is potentially wide:

+----------------+----------------+----------------+----------------+
| **Activity**   | **Test         | *              | **Re           |
|                | Automation     | *Description** | sponsibility** |
|                | Activity**     |                |                |
+================+================+================+================+
| **Unit         | Automated      | Developers     | Developers,    |
| Testing**      | jUnit Tests    | create jUnit   | DevOps         |
|                |                | test scripts   |                |
|                |                | that they      |                |
|                |                | initially will |                |
|                |                | execute on     |                |
|                |                | their own      |                |
|                |                | workstation.   |                |
|                |                |                |                |
|                |                | These scripts  |                |
|                |                | are also       |                |
|                |                | executed as    |                |
|                |                | part on the    |                |
|                |                | continuous     |                |
|                |                | integration    |                |
|                |                | and build      |                |
|                |                | processes.     |                |
+----------------+----------------+----------------+----------------+
| **Integration  | Automated      | Developers     | Developers,    |
| Testing**      | jUnit Tests    | create jUnit   | DevOps         |
|                |                | test scripts   |                |
|                |                | that they      |                |
|                |                | initially will |                |
|                |                | execute on     |                |
|                |                | their own      |                |
|                |                | workstation.   |                |
|                |                | These scripts  |                |
|                |                | will differ    |                |
|                |                | from the unit  |                |
|                |                | test scripts   |                |
|                |                | as these       |                |
|                |                | scripts will   |                |
|                |                | assume         |                |
|                |                | the            |                |
|                |                |  **integration |                |
|                |                | of the unit    |                |
|                |                | under test     |                |
|                |                | with other     |                |
|                |                | units**.       |                |
|                |                |                |                |
|                |                | These scripts  |                |
|                |                | are also       |                |
|                |                | executed as    |                |
|                |                | part on the    |                |
|                |                | continuous     |                |
|                |                | integration    |                |
|                |                | and build      |                |
|                |                | processes.     |                |
+----------------+----------------+----------------+----------------+
|                | Automated      | Developers     | Developers,    |
|                | jUnit Tests    | create jUnit   | DevOps         |
|                |                | test scripts   |                |
|                |                | that they      |                |
|                |                | initially will |                |
|                |                | execute on     |                |
|                |                | their own      |                |
|                |                | workstation.   |                |
|                |                | These scripts  |                |
|                |                | differ from    |                |
|                |                | the unit test  |                |
|                |                | scripts and    |                |
|                |                | the earlier    |                |
|                |                | mentioned      |                |
|                |                | integration    |                |
|                |                | test scripts   |                |
|                |                | as these       |                |
|                |                | scripts test   |                |
|                |                | the            |                |
|                |                | ** integration |                |
|                |                | with external  |                |
|                |                | systems** (the |                |
|                |                | BCPC back end  |                |
|                |                | and facilities |                |
|                |                | like Address   |                |
|                |                | Complete).     |                |
|                |                | These scripts  |                |
|                |                | are also       |                |
|                |                | executed as    |                |
|                |                | part on the    |                |
|                |                | continuous     |                |
|                |                | integration    |                |
|                |                | and build      |                |
|                |                | processes.     |                |
+----------------+----------------+----------------+----------------+
| **Functional   | Automated      | The test       | Test           |
| Testing**      | Functional     | automation     | Automation     |
|                | Tests          | specialist     | Specialist     |
|                |                | develo         |                |
|                |                | ps **automated |                |
|                |                | functional     |                |
|                |                | tests** based  |                |
|                |                | on the test    |                |
|                |                | design and     |                |
|                |                | test ideas     |                |
|                |                | developed by   |                |
|                |                | the test       |                |
|                |                | group. The     |                |
|                |                | automated      |                |
|                |                | functional     |                |
|                |                | tests are used |                |
|                |                | to             |                |
|                |                | crea           |                |
|                |                | te **automated |                |
|                |                | regression     |                |
|                |                | test** suites  |                |
|                |                | that are       |                |
|                |                | repeatedly run |                |
|                |                | during the     |                |
|                |                | sprints and    |                |
|                |                | the lifetime   |                |
|                |                | of the         |                |
|                |                | application.   |                |
+----------------+----------------+----------------+----------------+
|                | Automated      | The test       | Test           |
|                | Functional     | automation     | Automation     |
|                | Tests          | specialist     | Specialist     |
|                |                | develops       |                |
|                |                | au             |                |
|                |                | tomated** high |                |
|                |                | volume/many    |                |
|                |                | variants       |                |
|                |                | functional     |                |
|                |                | tests** based  |                |
|                |                | on the test    |                |
|                |                | design and     |                |
|                |                | test ideas     |                |
|                |                | developed by   |                |
|                |                | the test       |                |
|                |                | group. These   |                |
|                |                | tests are      |                |
|                |                | typically not  |                |
|                |                | candidates for |                |
|                |                | the regression |                |
|                |                | test suite as  |                |
|                |                | they are meant |                |
|                |                | for intensive  |                |
|                |                | time consuming |                |
|                |                | in depth tests |                |
+----------------+----------------+----------------+----------------+
|                | Automated      | The test       | Test           |
|                | Functional     | automation     | Automation     |
|                | Tests          | specialist     | Specialist     |
|                |                | develo         |                |
|                |                | ps **automated |                |
|                |                | functional     |                |
|                |                | smoke          |                |
|                |                | tests** based  |                |
|                |                | on the test    |                |
|                |                | design and     |                |
|                |                | test ideas     |                |
|                |                | developed by   |                |
|                |                | the test       |                |
|                |                | group. These   |                |
|                |                | tests are used |                |
|                |                | on an ongoing  |                |
|                |                | basis during   |                |
|                |                | the sprints    |                |
|                |                | and the        |                |
|                |                | lifetime of    |                |
|                |                | the            |                |
|                |                | application.   |                |
+----------------+----------------+----------------+----------------+
| **Performance  | Performance    | The test       | Test           |
| Testing**      | Test           | automation     | Automation     |
|                |                | specialist     | Specialist     |
|                |                | develops user  |                |
|                |                | simulation     |                |
|                |                | scripts that   |                |
|                |                | will be used   |                |
|                |                | for            |                |
|                |                | performance    |                |
|                |                | and load       |                |
|                |                | testing.       |                |
+----------------+----------------+----------------+----------------+

Approach

Test automation forms the core of the test exercise and is, as mentioned
before, a key enabler for the agile project. That is why a large amount
of test activity is geared towards feeding the test automation
development.

The following activities feed into test automation development:

  **Activity**                                            **Participant**                                **Delivers**
  ------------------------------------------------------- ---------------------------------------------- ------------------------------------------------
  Detailed Technical Design/Code                          Developers                                     Automated Unit Tests
  Test Design - Based on Acceptance Criteria and others   Testers, Business Analysts                     Key scope to be automated
  Exploratory Testing                                     Testers                                        Test Ideas for automation
  Test Design System and Non-functional requirements      Testers, Development Team, Business analysts   Key scope to be automated
  Variant Testing Needs                                   Testers                                        Additional scope to be automated
  Smoke Test Definition                                   Testers, Developers, DevOps                    Key activity to be automated
  Regression Test definition                              Testers                                        Minimum need for the automated regression test

The goal is to have value added automation, not to automate for the sake
of automation. We need to balance run time, complexity and value
delivered.

**Approach for Functional Test Automation**

 

  **Phase**       **Activity**                                                     **Description**
  --------------- ---------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Plan**        ** **                                                            ** **
                  Review Application road map                                      Understand what is included in the sprint\'s scope and what items we definitely have to address.
                  Review manual test cases (see above for other sources as well)   The testers start to create manual test cases and these will provide the test ideas for the test automation.
                  Verify Testability                                               Not all manual tests can be automated, tests that depend on human visual processing for instance are impossible to automate. An example of a category of tests that cannot be automated is usability testing.
                  Selection of Automation Candidates                               Once the inventory of potential candidates has been reviewed, we are able to select the test automation candidates.
                  Define Test Strategy/Plan                                        Then we create the automation plan, this set up the general guidelines, the structure and the planned time needed.
  **Design**      ** **                                                            ** **
                  Re-factor manual tests to be ready for automation                Manual tests are often not yet fit for test automation and need to be reworked to achieve the same objective but now in an automated form. It is a common pitfall in test automation to try to exactly replicate the manual tests.
                  Framework design/approach                                        A test automation framework is an integrated system that sets the rules of automation of a specific product. This system integrates the function libraries, test data sources, object details and various reusable modules. These components act as small building blocks which need to be assembled to represent a business process. The framework provides the basis of test automation and simplifies the automation effort.
                  Plan reusable libraries and actions                              Identification of re-usable components and actions greatly improves the efficiency of the test automation effort. We strive towards a situation where most of our tests can be defined by variable data and the test automation framework will be able to execute.
                  Define other abstraction layers                                  Specialized automated functions like direct database queries, connection to external systems etc. can be abstracted for easier use in the test automation scripts.
                  Data Management Plan                                             We define how we handle the data needed for our test automation runs. To be able to repeatedly run our test automation suites, we handle our test data in a very organized way. This includes upload of test data, delete of data, restore/refresh activities, date forwarding/retarding etc.
  **Develop**     ** **                                                            ** **
                  Create Test scripts                                              Our scripts are created in BDDStack, we use Groovy + Selenium as the programming language as it offers better features with regards to web testing.
                  Data Management                                                  Test data management is to be automated as well and we develop the scripts and batch jobs to do so.
                  Build execution flow                                             For test automation execution run smoothly, we create an execution order/flow that consists of start up, data initiation, application initiation, test case execution, application shutdown, data shutdown and execution shutdown activities. If set up right, such a flow allows for easy improvements and extensions.
                  Recovery Scenarios                                               Test automation runs fail, this is a fact of life. In order to prepare for such an event we need to be clear on what we need to do and how to recover. This could involve a data restore or deletion.
                  Add to function libraries                                        Identified general functions are built and added to the functional libraries.
                  Tools Extensions                                                 BDDStack offers some extensions that are configured in order to have BDDStack connect with JIRA. This way the tool can send information on failed test cases directly into JIRA. We configure the tool to connect with Zephyr and report test results into our central test management tool Zephyr.
                  Repository Management                                            We could use the repository management functions in BDDStack and integrate this with the a version control system like GitHub. BCGov is maintaining an area on GitHub, this area is actively used by many projects.
                  Documentation                                                    We document the set up, the configuration, the extension configuration and general system requirements. The intent is to document to such a degree that this set up can be replicated in the future.
  **Execution**   ** **                                                            ** **
                  Create new Test environment                                      For every test run we need to either create or refresh our test environment to be guaranteed of a fresh start.
                  Deploy Test Suite                                                Identify the test suite we need to run in BDDStack. This can either be done through the tool or by scripted invocation. The latter would happen in case of fully automated build and test.
                  Execute Test Scripts                                             Test scripts are executed by the test automation tool engine and the scripts point to one of our test environments.
                  Results reporting                                                The tool collects all the results and communicate these to Zephyr. (To be build)
                  Defect Management                                                Once the results are communicated, we review the failures and decide if this is an actual defect or not (a surprising amount of false positives come out of test automation tests runs). If this is a valid defect we use the integration with JIRA to record the details as obtained by the tool and add our own observation to it. This defect will then start the defect workflow just like any other defect.
  **Maintain**    ** **                                                            ** **
                  Update Assets                                                    Test automation keeps on working well if the assets (scripts, functions, actions) are kept up-to-date, clean and efficient.
                  Archive Test Suite                                               Test Suites are valuable assets and are kept carefully as part of good practice but also for restore/recovery purposes.
                  Maintain Test Suite(s)                                           Test suite maintenance involves adding new scripts, re-ordering scripts and pruning scripts that are no longer needed.
                  Regression TestSuite                                             Maintenance on the regression test suite is ongoing and the suite would typically grow over time. Please refer to the regression test strategy for a discussion on the activities that involved in the creation and maintenance of regression test suites.

Test automation will create several Automated test Suites, they are:

-   Regression Test Suite

-   Smoke Test Suite

-   Functional Test Suite, containing additional tests, in-depth tests
    > and multiple variations tests

Test Design

Test automation will leverage existing test design from the testers and
others as mentioned above.

However, there are additions to the test design that automation can and
will make. These additions are:

-   Repetition: Automated tests can repeat certain actions for a long
    > time. This could potentially trigger errors that are hard or even
    > impossible to find when doing manual tests.

-   Variations: Once an automated test has been defined it can be fed
    > with data variations offering the unique possibility to completely
    > explore all possibilities. This is something that a manual tester
    > would simply not have the time for.

-   Stress: Automated tests can put quite a bit of stress on a system,
    > particularly if several suites are run in parallel.

-   Low value tests: Once an automated test is defined it can be run
    > over and over for almost no effort and cost. That means that even
    > low value tests (tests that a manual tester would skip) could be
    > included in the test suite.

-   Extended Checking: An automated test can include system calls to
    > different platforms (database, external systems) to check if the
    > result observed is correct. A manual tester would spend
    > significantly more time doing the same.

Test Execution

Test automation execution can and will also be manually triggered by:

-   Test Automation Specialist to:

    -   Test the Test Suite (during development of the test suites)

    -   Run specialized automated tests that are not part of the Smoke
        > test or regression test suite

    -   Run any test suite when the need is there

-   Agile Tester to:

    -   Test a specific Test Script (during development of the test
        > script)

    -   Run specialized automated tests that are not part of the Smoke
        > test or regression test suite

    -   Run any test suite or subset when the need is there

![](media/image4.jpeg){width="10.113194444444444in"
height="3.8520833333333333in"}

Data Requirements

Test Automation needs data that:

-   Is uniquely designed/selected for the type of test automation. This
    > means that we need sets for: Unit Testing, Regression Testing,
    > Smoke Testing and any other test suites.

-   Is restorable so that the test automation can run with the same data
    > in the same state over and over.

-   Many PPR business functions are date dependent, to obtain
    > repeatability of test execution we need to create our data from
    > scratch to that we can control the order of activities.

-   Will **[*only* ]{.underline}**be used for its intended purpose. This
    > means that we need separate data sets for development of test
    > automation and test execution.

Infrastructure Requirements

The following infrastructure needs to be present:

-   1 QA Workstation Configured

 

 

 

Management Strategies

June 26, 2019

1:31 PM

This section describes the different test management strategies and
approaches.

* *

 

 

Status Reporting Strategy

June 26, 2019

1:32 PM

Testing Status will be available continuously from JIRA and Zephyr, this
status is meant for day-to-day management. Self-serve for immediate
questions and/or concerns is intended for team members and project
management. 

Weekly reports are intended for project management and client.

 

> **Caveat**
>
> Weekly reports represent a snapshot at the time of generation. Online
> status through JIRA and Zephyr might no longer reflect the weekly
> report as this information is always current. In case of concerns, it
> is always recommended to contact the project manager for
> clarification.

Objectives

-   Provide continuous insight in the test status

-   Identify issues and opportunities for improvement

-   Provide progress reports

Key Guidelines

-   Dashboards showing test and defect status will be available in JIRA

-   All reporting will be automatically generated from Zephyr and JIRA

-   Weekly reports will summarize and condense the automatic reports
    > from Zephyr and JIRA

Key Caveats

-   Weekly reports will have a very short useful lifespan giving the
    > high pace of change in an agile project

-   On demand reports from Zephyr are only available through the test
    > team

-   Continuous status dashboard might lack the context required for
    > proper interpretation by non-project members

Planned reports

+----------------+---------------+----------------+----------------+
| **Report       | **Frequency** | **Role         | **Comment**    |
| Name**         |               | Re             |                |
|                |               | sponsibility** |                |
+================+===============+================+================+
| Status Report  | Weekly        | Test Lead      | This report    |
|                |               |                | will be on     |
|                |               |                | SharePoint     |
+----------------+---------------+----------------+----------------+
| Test Run       | On Demand     | Test Lead      | Zephyr offers  |
| Results        |               |                | a continues    |
|                |               |                | view on        |
|                |               |                | progress. An   |
|                |               |                | extract will   |
|                |               |                | be             |
|                |               |                | incorporated   |
|                |               |                | in the weekly  |
|                |               |                | status report. |
|                |               |                |                |
|                |               |                | Test run       |
|                |               |                | results will   |
|                |               |                | include        |
|                |               |                | results from:  |
|                |               |                |                |
|                |               |                | -   Build      |
|                |               |                |                |
|                |               |                | > Verification |
|                |               |                |     > Test     |
|                |               |                |     > (BVT)    |
|                |               |                |     > runs     |
|                |               |                |                |
|                |               |                | -   Automated  |
|                |               |                |     > Unit     |
|                |               |                |     > tests    |
|                |               |                |                |
|                |               |                | -   Automated  |
|                |               |                |                |
|                |               |                |   > Functional |
|                |               |                |     > tests    |
|                |               |                |                |
|                |               |                | -              |
|                |               |                |    Exploratory |
|                |               |                |     > Testing  |
|                |               |                |     > Sessions |
|                |               |                |                |
|                |               |                | -   Other      |
|                |               |                |     > Manual   |
|                |               |                |     > Testing  |
|                |               |                |                |
|                |               |                | -   User       |
|                |               |                |                |
|                |               |                |   > Acceptance |
|                |               |                |     > Testing  |
+----------------+---------------+----------------+----------------+
| Test Activity  | Sprint End    | Test Lead      | Summarization  |
| Wrapup         |               |                | of results,    |
|                |               |                | lessons        |
|                |               |                | learned and    |
|                |               |                | tasks that     |
|                |               |                | will need to   |
|                |               |                | be scheduled   |
|                |               |                | for a later    |
|                |               |                | sprint.        |
+----------------+---------------+----------------+----------------+

 

 

Test Data Strategy

June 26, 2019

1:32 PM

Testing depends on the availability of high quality test data.

Test data needs to conform to the following characteristics:

-   It is meaningful

-   It allows the tests to be executed

-   It can be adapted/changed/copied and deleted to support multiple
    > test cycles

-   It allows for time and date shifting

-   It does not unnecessarily expose the testers to private and/or
    > sensitive data

 

> **Test Data Principle**
>
>  
>
> **Basic assumption(s):**

-   Testing uses test data.

-   Testing owns the test data.

-   High quality, dedicated test data is available.

-   Developers are responsible for the creation of Unit Test Data.

> **Test Principle:**

-   The test environments contain either fictional test data or
    > masked/de-identified production data.

-   The Business/User Acceptance Test environment contains production
    > data or masked/de-identified production data.

-   Production data will not be used for testing outside of PPR.

Test Data Usage

  **Usage**                      **Environment**   **Type of Test Data**                                                                                            **User**                     **Comments**
  ------------------------------ ----------------- ---------------------------------------------------------------------------------------------------------------- ---------------------------- --------------
  Developer Testing              DEV               Purposely created                                                                                                Developer                     
  Functional Testing             TEST              Subset of masked data and purposely created test data (Set 1)                                                    Testers (Agile)               
  Automated Functional Testing   TEST              Subset of masked data and purposely created test data, but using a different and stable subset of data (Set 2)   Test Automation Specialist    
  System Integration Testing     TEST              Subset of masked data and purposely created test data, but using a different and stable subset of data (Set 3)   All testing                   
  Performance Testing            TEST              Full size masked data                                                                                            Test Automation Specialist    
  User Acceptance Testing        Staging           Masked/de-identified production data                                                                             Business Testers             * *

 

 

Defect Management Strategy

June 26, 2019

1:32 PM

Defect reports are the main output from the testing process, they
represent a significant investment and are essential in understanding
the state of the system under test (SUT). Solid defect management has
proven to be the key success factor in complex projects and provides key
progress and quality information.

We will adhere to our defined defect management principles:

 

> **Basic assumption(s):**

-   Defects need to be managed.

-   There will be *one* defect management tool used during analysis,
    > design, development and testing.

-   The defect management tool, user procedures and reviews will enforce
    > consistent, high quality defect reporting.

> **Test Principle:**

-   Defect Management will follow the standard defect management
    > process.

-   All defects will be reported in and managed by a central defect
    > management tool.

-   All personnel involved in the creation, roll-out and sustainment of
    > a solution will have access to the central tool and will be able
    > to review the project\'s defects.

Objectives

-   Provide documentation on detected defects

-   Provide insight in the state of the application under test

-   Manage defects through defined process

Key Guidelines

-   Each defect report contains one defect

-   Everybody can write a defect report

-   Everybody can comment on a defect report

-   The test lead is the facilitator of the defect management process

-   All defects are reviewed, categorized and assigned, this is a
    > cooperative exercise

-   Defect management has several specific roles defined

-   Defect reports are written with the notion that:

-   They might not be fixed right now

-   The developer might not be on site

-   The test data might not be available

-   The business context might not be familiar to a developer 

Key Caveats

-   The number of defect reports is not immediately correlated with the
    > quality of the SUT

-   Not all defects will be fixed at the end of a sprint

-   Not all defects are valid, unique or worth the project\'s time, they
    > will be closed with reasoning included

-   A defect observed without a defect report is a missed opportunity
    > for improvement

-   Defect volumes are not to be used to assess tester and developer
    > productivity

 

 

Rating Defects

June 26, 2019

1:43 PM

Categorizing and rating defects is often a topic of contention and
discussion. It is important to avoid unnecessary churn on this topic and
we do that by very clearly defining the rating process.

There are three elements involved in the rating of defects, they are:

-   **Symptom**: What happened? What went wrong?

-   **Severity**: How does the found defect impact the functionality,
    > quality, risk etc.

-   **Priority**: How quickly does this defect need to be fixed

By defining how symptoms relate to severity and who is responsible for
the setting symptom, severity and priority, we will have a process that
adds value to the development effort.

A defined process does not mean that we can forego the \"apply reason\"
rule, in this case the process is meant for consistency and guidance.

Who is responsible for setting\....?

[RASCI
Legend](onenote:RASCI%20Legend.one#section-id={75397548-6BE0-46FB-80CC-551FBC2B6C97}&end&base-path=https://citz.sp.gov.bc.ca/sites/Shared/Project/BidR/BCBid/CONTRACT%20%20SCHEDULE/Testing/Resources/Testing%20Notes)

  ** **                 **Symptom**   **Severity**   **Priority**
  --------------------- ------------- -------------- --------------
  **Tester**            **R**         **R**          C
  **Test Lead**         A             A              S
  **Developer**         C             C              C
  **Dev.Lead**          S             S              S
  **Project Manager**   I             I              A
  **Business Lead**     S             S              **R**
  **Release Manager**   S             S              **R**
  **Product Owner**     I             I              C

By clearly separating symptom, severity and priority setting
responsibilities, we will be able to put the right responsibility with
the right team members. We now could potentially have a critical
severity issue that gets the lowest priority or vice versa a low
criticality item that gets the highest priority.

Severity

We will use the following severity definition:

  **Severity Level**   **Description**
  -------------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Severity 1:**      **Cannot use any part of System until the problem is fixed.**
  **Critical**         Unable to proceed with the test.  
                       Severity 1 usually means a major, critical business function or process is broken and no workarounds can be identified.
  **Severity 2:**      **Can use the system, but a 'workaround' is required.**
  **High**             Test is severely restricted due to a defect encountered for which there is no acceptable circumvention. 
                       The application executes, but wrong results are encountered, or problems are discovered which significantly affect product operation or the test to be conducted. 
                       A fix is required in order to proceed with this function.  A work-around may exist but its use is unsatisfactory.  
  **Severity 3:**      **Can use the system and testing may proceed.**
  **Medium**           Able to proceed with limited function which is not crucial to the test. 
                       There may be discrepancies between product operation and the product documentation. Additionally, any problem that is caused by extreme or unlikely circumstances (such as environments or operator sequences) provided a straightforward workaround exists and there is no unrecoverable data loss. 
                       The existence of the problem may cause user dissatisfaction.  
  **Severity 4:**      **Shortcoming with no immediate impact to test. **
  **Low**              Discrepancies are found that are of insignificant nature and do not affect satisfactory operation or usability of the product (examples may include improper presentation of menus, messages, prompts, minor functional deviations that can be easily avoided).
                       General documentation problems or cosmetic problems. 
  **Severity 5:**      **Identified needed enhancement**
  **Enhancement**      A previously unrecognized feature or requirement needs to be added
                       A technical correct implementation of a business requirement does not meet the business needs
                       A new requirement has been identified during testing

JIRA will be configured to contain the severity field.

Symptoms versus Severity

A very good practice is to define a connection between found symptoms
and the severity that will be used. For instance a typo would never get
a severity \"Critical\", but a database crash would.

  **Symptom / Severity Matrix **                                              ** **                                    **Severity **                                                     
  -------------------------------- ------------------------------------------ ---------------------------------------- --------------------- ------------- --------------- ------------ ----------------
  ** **                            **Symptom **                               **Immediately escalate to test lead **   **5-Catastrophic **   **4-High **   **3-Medium **   **2-Low **   **1-Minimal **
  **General **                     System Crash with data loss                X                                        X                                                                 
                                   System Crash without data loss             X                                        X                                                                 
                                   Enhancement Request                                                                                                                                  X 
                                   General failure                            X                                        X                                                                 
                                   Installation/deployment Failure            X                                                              X             O                             
  **Application **                 Incorrect operation                                                                                       X             O                             
                                   Report Incorrect (printing)                                                                               X             O                             
                                   Report Incorrect (information)                                                                            X             O                             
                                   Requirement, incorrect                                                                                                                               X 
                                   Requirement, missing                                                                                                                                 X 
                                   Requirement, new                                                                                                                                     X 
                                   Security/Access violation or error         X                                        X                     O                                           
                                   Slow performance                                                                                          X             O                             
  **Data **                        Data cannot be stored                                                               X                     O                                           
                                   Data is corrupted or clipped                                                        X                     O                                           
                                   Data is exposed to unauthorized parties    X                                        X                                                                 
                                   Data is lost                                                                        X                                                                 
  **Standards **                   Compliance, BCGov UI                                                                                                    X               O             
                                   Compliance, iValua                                                                                                      X               O             
                                   Compliance, Web                                                                                           X             O                             
                                   Compliance, Windows                                                                 X                     O                                           
                                   Compliance, Security Policy                                                                                             X               O             
  **Usability **                   Behaviour, unexpected                                                                                                   X               O             
                                   Behaviour, unfriendly                                                                                                   X               O             
                                   Navigation                                                                                                              X               O             
                                   Presentation                                                                                                            X               O             
                                   Spelling/label                                                                                                          X               O             
                                   Wording, business/technical                                                                                             X               O             
                                   Wording, grammatical                                                                                                    X               O             
  **Web **                         Broken Link                                                                                               X                                           
                                   Misplaced element                                                                                                       X               O             
                                   Display issue                                                                                             X             O                             
                                   Browser incompatibility                                                                                   X             O                             
                                   Mobile browser incompatibility                                                                                          O               X             
                                                                                                                                                                                         
  **Legend **                                                                                                                                                                            
                                   Preferred                                  X                                                                                                          
                                   Optional                                   O                                                                                                          

JIRA will be configured to contain the symptoms field.

Priority

For priority we will use the standard JIRA priorities (with the standard
explanation):

  **Priority Level**   **Description**
  -------------------- ------------------------------------------------------
   Highest             This problem will block progress.
   High                Serious problem that could block progress.
   Medium              Has the potential to affect progress.
   Low                 Minor problem or easily worked around.
   Lowest              Trivial problem with little or no impact on progress

 

 

Test Results Strategy

June 26, 2019

1:32 PM

The value of test results to a project is that they provide an insight
in the readiness/completeness of the system under test (SUT).

Test Results will be used to provide information on:

-   Coverage: How much of the application was tested?

-   Requirement/Acceptance Criteria Traceability

-   Test Plan Progress: How far has the plan progressed?

-   Failure Rate: How many tests failed?

-   Fix Rate: How many of earlier fails now pass

We are guided by the following testing principles:

 

**Traceability Principle**

 

**Basic assumption(s):**

-   All requirements must be tested.

-   Test progress must be measured against coverage of requirements.

**Test Principle:**

-   Testers will map all test cases back to requirements to ensure they
    > have all been covered by test cases.

-   Test Lead will report progress based on requirements coverage.

 

**Test Execution Principle**

**Basic assumption(s):**

-   Tests need to be executed.

-   The right resources need to execute the tests.

**Test Principle:**

-   Unit Tests are executed by developers.

-   Quality Tests are executed by the quality testers.

-   Acceptance Tests are executed by the Acceptance testers and Business
    > Users.

Objectives

-   Provide continuous insight in the state of the application under
    > test

-   Detect trends, failure and fix rates to allow management of the test
    > process

-   Provide progress reports

Key Guidelines

-   Each test will be connected to a Requirement/User Story

-   Reporting will be done on progress on plan and coverage

-   All tests and results will be documented in Zephyr

-   Dashboards showing the test progress and results will be available
    > in Jira

-   All reporting will be automatically generated from Zephyr/Jira

Key Caveats

-   High quality test reporting depends on consistent and disciplined
    > usage of the test management tool and Jira

-   With continuous reporting, confusion can emerge about the readiness
    > of a testing activity or cycle

 

 

 

Test Environment Needs

June 26, 2019

2:01 PM

The test environment needs definition is governed by the test
environment principle:

 

> **Test Environment Principle**
>
>  
>
> **Basic assumption(s):**

-   All developed and configured software must be tested.

-   Test environments are available and configured.

-   Multiple projects/activities may need to use the same test
    > environments.

-   Usage of the same environment by different project/activity can
    > cause interference.

-   Test environment resource conflicts need to be addressed.

> **Test Principle:**

-   Testing uses dedicated Test Environments.

-   The project is responsible for communicating:

-   Coordination of test environment usage.

-   Facilitating negotiations on usage and planning.

-   Facilitating the creation of new test environments.

> The project and the internal Testing Services group owns the Test
> environments.

 

+----------------+----------------+----------------+----------------+
| **Type of      | **En           | **Who**        | *              |
| Testing**      | vironment(s)** |                | *Description** |
+================+================+================+================+
| Developer      | DEV            | Developers,    | Automated Unit |
| Testing        |                | DevOps         | tests are      |
|                |                |                | developed by   |
|                |                |                | the developers |
|                |                |                | on their own   |
|                |                |                | workstation    |
|                |                |                | and these test |
|                |                |                | scripts get    |
|                |                |                | submitted with |
|                |                |                | the code they  |
|                |                |                | created.       |
|                |                |                | Subsequently   |
|                |                |                | the unit tests |
|                |                |                | will be        |
|                |                |                | executed       |
|                |                |                | during the     |
|                |                |                | continuous     |
|                |                |                | integration    |
|                |                |                | process.       |
+----------------+----------------+----------------+----------------+
| Smoke Test     | ALL            | Test           | A smoke test   |
|                |                | Automation     | will be run    |
|                |                | Specialist     | after moving   |
|                |                |                | into Test and  |
|                |                |                | Staging. A     |
|                |                |                | subset of this |
|                |                |                | smoke test     |
|                |                |                | will most      |
|                |                |                | likely be      |
|                |                |                | deployed from  |
|                |                |                | production     |
|                |                |                | validation as  |
|                |                |                | well. The      |
|                |                |                | exact scope    |
|                |                |                | for this needs |
|                |                |                | to be          |
|                |                |                | determined as  |
|                |                |                | a smoke test   |
|                |                |                | in production  |
|                |                |                | cannot create  |
|                |                |                | data.          |
+----------------+----------------+----------------+----------------+
| Functional     | TEST           | Agile Testers  | Functional     |
| Testing        |                |                | Testing has    |
|                |                |                | aspects to it, |
|                |                |                | first we\'ll   |
|                |                |                | have the       |
|                |                |                | \              |
|                |                |                | 'traditional\' |
|                |                |                | test cases and |
|                |                |                | scripts, but   |
|                |                |                | we will also   |
|                |                |                | engage in      |
|                |                |                | exploratory    |
|                |                |                | testing.       |
|                |                |                |                |
|                |                |                | This type of   |
|                |                |                | testing can    |
|                |                |                | co-exist with  |
|                |                |                | Automated      |
|                |                |                | Functional     |
|                |                |                | Testing as     |
|                |                |                | long as we     |
|                |                |                | keep a clear   |
|                |                |                | data           |
|                |                |                | separation     |
|                |                |                | between the 2  |
|                |                |                | activities.    |
+----------------+----------------+----------------+----------------+
| Automated      | TEST           | Test           | Automated      |
| Functional     |                | Automation     | Functional     |
| Testing        |                | Specialist     | Testing trails |
|                |                |                | functional     |
|                |                |                | testing and    |
|                |                |                | works on       |
|                |                |                | automating key |
|                |                |                | functional     |
|                |                |                | test cases and |
|                |                |                | creating new   |
|                |                |                | automation for |
|                |                |                | those cases    |
|                |                |                | where we need  |
|                |                |                | a large amount |
|                |                |                | of variants to |
|                |                |                | be tested.     |
+----------------+----------------+----------------+----------------+
| Integration    | TEST           | Developers,    |                |
| Testing        |                | Solution       |                |
|                |                | Architect      |                |
+----------------+----------------+----------------+----------------+
| System /       | Test           | Agile Testers  | In this        |
| Intersystem    |                |                | environment we |
| Testing        |                |                | will be able   |
|                |                |                | to test the    |
|                |                |                | full end to    |
|                |                |                | end            |
|                |                |                | integration    |
|                |                |                | including back |
|                |                |                | end services.  |
+----------------+----------------+----------------+----------------+
| Regression     | Test           | Agile Testers, | The output     |
| Testing        |                | Test           | from the       |
|                |                | Automation     | functional     |
|                |                | Specialist     | test           |
|                |                |                | automation     |
|                |                |                | will be used   |
|                |                |                | in the         |
|                |                |                | integrated     |
|                |                |                | environment to |
|                |                |                | run regression |
|                |                |                | tests.         |
+----------------+----------------+----------------+----------------+
| Performance    | Staging        | Test           | Depending on   |
| Testing        |                | Automation     | identified     |
|                |                | Specialist     | need and risk  |
|                |                |                | we will run    |
|                |                |                | performance    |
|                |                |                | testing in an  |
|                |                |                | environment    |
|                |                |                | that is as     |
|                |                |                | close to       |
|                |                |                | production as  |
|                |                |                | we can get it. |
+----------------+----------------+----------------+----------------+
| Security       | Staging        | TBD            | Security       |
| Testing        |                |                | testi          |
|                |                |                | ng/Penetration |
|                |                |                | will need an   |
|                |                |                | environment    |
|                |                |                | that is either |
|                |                |                | production     |
|                |                |                | (before it is  |
|                |                |                | actually live) |
|                |                |                | or an          |
|                |                |                | environment    |
|                |                |                | that is close  |
|                |                |                | to identical   |
|                |                |                | as production. |
+----------------+----------------+----------------+----------------+
| User           | Staging        | Testers        | The UAT will   |
| Acceptance     |                | (User/Business | require a      |
| Testing        |                | Focus)         | system that    |
|                |                |                | contains       |
|                |                |                | masked         |
|                |                |                | /de-identified |
|                |                |                | production     |
|                |                |                | data.          |
+----------------+----------------+----------------+----------------+

 

 

 

Test Tool Needs

June 27, 2019

4:32 PM

+-----------------+-----------------+-----------------+-----------+
| **Tool**        | **Description** | **Usage**       | **Resp.** |
+=================+=================+=================+===========+
| **JIRA**        | Project and     | The team uses   | BC Gov    |
|                 | issue tracking  | JIRA as their   |           |
|                 | software        | agile work      |           |
|                 | development     | management and  |           |
|                 | tool used by    | documentation   |           |
|                 | agile teams to  | tool and its    |           |
|                 | plan, track,    | issue tracking  |           |
|                 | release, and    | capabilities    |           |
|                 | report          | for tracking    |           |
|                 | software.       | tasks, project  |           |
|                 |                 | risks, project  |           |
|                 |                 | issues.         |           |
|                 |                 |                 |           |
|                 |                 | The test team   |           |
|                 |                 | specifically    |           |
|                 |                 | uses [defect    |           |
|                 |                 | management](one |           |
|                 |                 | note:#Defect%20 |           |
|                 |                 | Management%20Pr |           |
|                 |                 | ocess&section-i |           |
|                 |                 | d={3CE1FE52-2D1 |           |
|                 |                 | E-4E71-85AF-F13 |           |
|                 |                 | D3A0985E7}&page |           |
|                 |                 | -id={11524133-F |           |
|                 |                 | DC5-401B-A19A-7 |           |
|                 |                 | F2FE67AC0AD}&en |           |
|                 |                 | d&base-path=htt |           |
|                 |                 | ps://citz.sp.go |           |
|                 |                 | v.bc.ca/sites/S |           |
|                 |                 | hared/Project/B |           |
|                 |                 | idR/BCBid/CONTR |           |
|                 |                 | ACT%20%20SCHEDU |           |
|                 |                 | LE/Testing/Reso |           |
|                 |                 | urces/Testing%2 |           |
|                 |                 | 0Notes/Test%20S |           |
|                 |                 | trategy.one) as |           |
|                 |                 | their main      |           |
|                 |                 | communication   |           |
|                 |                 | conduit on      |           |
|                 |                 | defects and     |           |
|                 |                 | issues found.   |           |
+-----------------+-----------------+-----------------+-----------+
| **SharePoint**  | Team            | The team uses   | BC Gov    |
|                 | collaboration   | SP as the       |           |
|                 | software that   | centre of the   |           |
|                 | allows for      | universe for    |           |
|                 | teams to        | all             |           |
|                 | create,         | documentation,  |           |
|                 | organize, and   | knowledge and   |           |
|                 | discuss.        | collaboration.  |           |
+-----------------+-----------------+-----------------+-----------+
| **Skype for     | Service for     | Team            | BC Gov    |
| Business**      | internal &      | Collaboration   |           |
|                 | private chat,   | Tool            |           |
|                 | instant         |                 |           |
|                 | messaging,      |                 |           |
|                 | videos, and     |                 |           |
|                 | file sharing.   |                 |           |
+-----------------+-----------------+-----------------+-----------+
| **Zephyr**      | Web-based Test  | Testers will    | BC Gov    |
|                 | Management tool | use Zephyr to   |           |
|                 | integrated with | execute their   |           |
|                 | JIRA.           | assigned test   |           |
|                 |                 | cases, report   |           |
|                 |                 | results         |           |
+-----------------+-----------------+-----------------+-----------+
| **MS Office     | A collection of | Documentation,  | BC Gov    |
| suite**         | bundled         | early test case |           |
|                 | productivity    | development     |           |
|                 | software used   | (for upload to  |           |
|                 | to create, edit | Zephyr),        |           |
|                 | test documents. | general         |           |
|                 |                 | utility.        |           |
+-----------------+-----------------+-----------------+-----------+
| **BDDStack**    | Tool            | Functional Test | BC Gov    |
|                 | to cr           | Automation      |           |
|                 | eate [automated |                 |           |
|                 | functional      |                 |           |
|                 | tes             |                 |           |
|                 | ts](https://git |                 |           |
|                 | hub.com/BCDevOp |                 |           |
|                 | s/BDDStack) for |                 |           |
|                 | websites, web   |                 |           |
|                 | apps, and       |                 |           |
|                 | mobile web      |                 |           |
|                 | applications.   |                 |           |
+-----------------+-----------------+-----------------+-----------+
| **JMeter**      | Performance     | Performance     | TBD       |
|                 | Test Tool       | Testing         |           |
+-----------------+-----------------+-----------------+-----------+
| **OWASP ZAP**   | Security        | Testing         | TBD       |
|                 | Testing Tool    |                 |           |
+-----------------+-----------------+-----------------+-----------+

 

 

 

Roles, Responsibilities, Staffing, and Training Needs

June 24, 2019

4:41 PM

The RASCI Matrices are used to describe the participation by various
roles across the test activities.

**Key Responsibility Definition**

**R**-- Responsible (for process execution/management):  This is the
person who actually performs the task.

**A** -- Approves/Accountable:  This is the person who is accountable
for the quality and timeliness of the completion of the task, and is
frequently the person to whom the responsible person reports.

**S** -- Supports: This is the person who is required to support the
testing process

**C** -- Consulted: These are the subject matter experts, or other
people who provide information needed for correct execution of the task.

**I** -- Informed: These are the people who are impacted by the progress
of the task, and so are advised of milestones or significant
developments.

 

  **Roles**                         **Unit Test**   **Functional Test**   **User Acceptance Test**   **Regression Test**   **Security Test**   **Integration Test**   **System Test**   **Smoke Test**   **Performance Test**   **Test Automation**
  --------------------------------- --------------- --------------------- -------------------------- --------------------- ------------------- ---------------------- ----------------- ---------------- ---------------------- ---------------------
  **Test Lead**                     S               **A**                 S                          **A**                 R                   S                      **A**             **A**            **A**                  **A**
  **Senior Test Analyst (Agile)**   I               R                     S                          S                                         S                      R                 S                                       S
  **Test Analyst (Agile)**                          R                     S                          S                                         S                      R                                                         S
  **Business Tester**                               I                     R                          S                                                                S                                                         I
  **Test Automation Specialist**    S               S                     S                          R                     S                   S                      S                 R                R                      R
  **Business Analyst**                              C                     S                          C                                                                C                                                         C
  **UAT Lead**                                      I                     **A**                      I                     I                   I                      I                 I                I                       
  **Business Lead**                                 C                     S                          C                                                                C                                                         C
  **Developer**                     R               S                     S                          C                     S                   R                      S                 S                S                      R
  **DevOps**                        S                                                                S                                         S                      S                 **A**                                   S
  **Developer Lead**                **A**           I                     I                          C                     R                   **A**                  I                 S                S                      S
  **Solution Architect**            C                                     I                          C                     C                   I                      C                                  C                      S
  **Release Manager**               S               I                     S                          I                     I                   I                      S                 S                I                      I
  **Subject Matter Expert**                         C                     C                          C                     C                   C                      C                                  C                      C
  **Auditor**                                       I                     I                          I                     I                                          I                                  I                      I
  **Project Manager**               I               I                     I                          I                     **A**               I                      I                 I                I                      I

 

Staffing

The following test roles have been identified to support the effort.

The recommended team configuration calls for 4 distinct testing roles,
these roles are:

-   Test Analyst (Agile)

-   Senior Test Analyst (Agile)

-   Senior Test Automation/Tools Specialist

-   Business Tester

>  

  **Experience Level**                                                                                                                           
  ---------------------------------------- ------------------- -------------------- ----------------------------------------------------------- -------------------------
  **Role**                                 **Years in Role**   **Years with PPR**   **Comment**                                                 **Estimated \# needed**
  Business Tester                          2+                  2+                   End-User Focus (Black-Box UAT)                              2
  Test Analyst (Agile)                     2+                  2+                   Exploratory Testing Focus                                   3
  Senior Test Automation/Tool Specialist   4+                  0+                   Test Engineer                                               1
  Senior Test Analyst (Agile)              4+                  2+                   Need significant Agile and Exploratory Testing Experience   1

 

Training Needs

  **Topic**                     **Participants**                                 **Comment**
  ----------------------------- ------------------------------------------------ ------------------------------------------------------------------------------------------------------------------------
  Agile Workshop                All Team members, SMEs and other participants.   Several workshops have already been conducted, but so far, the testers were not involved.
  Testing Fundamentals          Testers                                          A level setting training, to allow everybody to start at the same point with the same information.
  Exploratory Testing           Testers                                          A major technique that will be embedded in our session-based testing (SBT) approach. Training Materials are available.
  JIRA Introduction             All team members                                 Introduction to our project management system.
  JIRA - Defect Management      All team members                                 The defect management process for PPR as supported by JIRA.
  Project Onboarding/Training   All team members                                  
  Zephyr                        Testers                                          The test management tool that allows for collaboration, planning, execution and reporting.

 

 

 

Definition of Done for Testing (DoD)

June 27, 2019

4:45 PM

At the highest level the DoD  for testing is when:** **

> **\"All planned testing tasks have been completed and no open defects
> are remaining.\"**

How do we determine Done?

To arrive at such a high level conclusion we would need to understand
our level of \"done\" for individual activities. The following is a list
(checklist, some would say) that we\'ll use for assessing our level of
\"done\" for the different testing activities.

**What is it?**

Definition of done is crucial to a highly functioning Scrum team. The
following are characteristics that we look for in our definition of done
for testing. Verifying that our DoD meets these criteria will ensure
that we are truly done with testing, not only in terms of functionality
but in terms of quality as well.

 

*DoD is a checklist of valuable activities required to produce
software.*

Definition of Done is a simple list of activities (writing code, coding
comments, unit testing, integration testing, release notes, design
documents, etc.) that add verifiable/demonstrable value to the product.
Focusing on value-added steps allows the team to focus on what must be
completed in order to build software while eliminating wasteful
activities that only complicate software development efforts.

 

*DoD is the primary reporting mechanism for team members.*

Reporting in its simplest form is the ability to say, "This feature is
done." After all, a feature or Product Backlog Item is either done or it
is not-done. DoD is a simple artifact that adds clarity to the
"Feature's done" statement.  Using DoD as a reference for this
conversation a team member can effectively update other team members and
the product owner. 

 

*DoD is informed by reality.*

Actual results, statistics and observations from the test process drives
the DoD.

 

*DoD is not static.*

The DoD changes over time. Organizational support and the team's ability
to remove impediments may enable the inclusion of additional activities
into the DoD for features or sprints.

 

*DoD is an auditable checklist.*

Features/stories are broken down into tasks both during sprint planning
and also within a sprint, these include the testing tasks. The DoD is
used to validate whether all major tasks are accounted for (hours
remaining). Also, after a feature or sprint is done, DoD is used as a
checklist to verify whether all necessary value-added activities were
completed.

This definition of done is independent of the user acceptance criteria
(functional acceptance) for a feature and the focus on the test
activities. Definition of done is informed by reality where it captures
activities that can be realistically committed by the test team to be
completed at each sprint.

\- See more
at: <https://www.scrumalliance.org/community/articles/2008/september/what-is-definition-of-done-(dod)#sthash.mCx6mHl7.dpuf>

 

+----------------+----------------+----------------+----------------+
| **Test         | **Done when:** | **PPR          | **Comment**    |
| Activity**     |                | Relevance/     |                |
|                |                | Re             |                |
|                |                | sponsibility** |                |
+================+================+================+================+
| **Unit Test**  | -   All Unit   | No/iValua      |                |
|                |     > Tests    |                |                |
|                |     > are      |                |                |
|                |                |                |                |
|                |    > automated |                |                |
|                |                |                |                |
|                | -   All Unit   |                |                |
|                |     > Tests    |                |                |
|                |     > Pass     |                |                |
+----------------+----------------+----------------+----------------+
| **Functional   | -   All        | Yes/CGI &      | Minimum level  |
| Test**         |     > priority | Province       | of done.       |
|                |     > 1 and 1  |                | Failed test    |
|                |     > test     |                | cases of lower |
|                |     > cases    |                | priority will  |
|                |     > Pass     |                | have to be     |
|                |                |                | added to the   |
|                | -   All        |                | project        |
|                |     > priority |                | backlog.       |
|                |     > 1 and 2  |                |                |
|                |     > test     |                |                |
|                |     > cases    |                |                |
|                |     > have     |                |                |
|                |     > been     |                |                |
|                |                |                |                |
|                |    > automated |                |                |
|                |                |                |                |
|                | -   All        |                |                |
|                |                |                |                |
|                |    > resulting |                |                |
|                |     > defects  |                |                |
|                |     > are:     |                |                |
|                |                |                |                |
|                |     -   Closed |                |                |
|                |                |                |                |
|                |      > (fixed) |                |                |
|                |                |                |                |
|                |     -   Closed |                |                |
|                |         > (not |                |                |
|                |                |                |                |
|                |    > relevant) |                |                |
|                |                |                |                |
|                |                |                |                |
|                |   -   Deferred |                |                |
|                |         > (on  |                |                |
|                |         > the  |                |                |
|                |                |                |                |
|                |     > backlog) |                |                |
+----------------+----------------+----------------+----------------+
| **User         | -   All        | Yes/Province   |                |
| Acceptance     |     > priority |                |                |
| Test**         |     > 1 and 2  |                |                |
|                |     > test     |                |                |
|                |     > cases    |                |                |
|                |     > Pass     |                |                |
|                |                |                |                |
|                | -   All        |                |                |
|                |                |                |                |
|                |    > resulting |                |                |
|                |     > defects  |                |                |
|                |     > are:     |                |                |
|                |                |                |                |
|                |     -   Closed |                |                |
|                |                |                |                |
|                |      > (fixed) |                |                |
|                |                |                |                |
|                |     -   Closed |                |                |
|                |         > (not |                |                |
|                |                |                |                |
|                |    > relevant) |                |                |
|                |                |                |                |
|                |                |                |                |
|                |   -   Deferred |                |                |
|                |         > (on  |                |                |
|                |         > the  |                |                |
|                |                |                |                |
|                |     > backlog) |                |                |
+----------------+----------------+----------------+----------------+
| **Regression   | -   All        | Yes/CGI and    | This activity  |
| Test**         |                | Province       | needs to be    |
|                |   > identified |                | successful. A  |
|                |                |                | regression     |
|                |   > regression |                | test suite     |
|                |     > test     |                | will contain a |
|                |     > cases    |                | subset of all  |
|                |     > have     |                | other tests.   |
|                |     > been     |                |                |
|                |                |                |                |
|                |    > automated |                |                |
|                |                |                |                |
|                | -   All test   |                |                |
|                |     > cases    |                |                |
|                |     > Pass     |                |                |
|                |                |                |                |
|                | -   All        |                |                |
|                |                |                |                |
|                |    > resulting |                |                |
|                |     > defects  |                |                |
|                |     > are:     |                |                |
|                |                |                |                |
|                | -   Closed     |                |                |
|                |     > (fixed)  |                |                |
+----------------+----------------+----------------+----------------+
| **Security     | -   Security   | Yes/CGI and    | It might be    |
| Test**         |     > testing  | Province       | that security  |
|                |     > has been |                | testing is not |
|                |                |                | a planned      |
|                |    > performed |                | activity in    |
|                |                |                | every sprint.  |
|                | -   All        |                |                |
|                |     > critical |                |                |
|                |     > defects  |                |                |
|                |     > have     |                |                |
|                |     > been     |                |                |
|                |     > fixed    |                |                |
|                |                |                |                |
|                | -   All        |                |                |
|                |                |                |                |
|                |    > resulting |                |                |
|                |     > defects  |                |                |
|                |     > are:     |                |                |
|                |                |                |                |
|                | -   Closed     |                |                |
|                |     > (fixed)  |                |                |
|                |                |                |                |
|                | -   Closed     |                |                |
|                |     > (not     |                |                |
|                |                |                |                |
|                |    > relevant) |                |                |
|                |                |                |                |
|                | -   Deferred   |                |                |
|                |     > (on the  |                |                |
|                |     > backlog) |                |                |
+----------------+----------------+----------------+----------------+
| **Integration  | -   All test   | Yes/iValua,    | As the         |
| Test**         |     > cases    | CGI and        | integration    |
|                |     > Pass     | Province       | components are |
|                |                |                | the key        |
|                | -   All test   |                | enabler for    |
|                |     > cases    |                | the built      |
|                |     > have     |                | functionality, |
|                |     > been     |                | we do need a   |
|                |                |                | full pass and  |
|                |    > automated |                | automation.    |
|                |                |                |                |
|                | -   All        |                |                |
|                |                |                |                |
|                |    > resulting |                |                |
|                |     > defects  |                |                |
|                |     > are:     |                |                |
|                |                |                |                |
|                | -   Closed     |                |                |
|                |     > (fixed)  |                |                |
|                |                |                |                |
|                | -   Closed     |                |                |
|                |     > (not     |                |                |
|                |                |                |                |
|                |    > relevant) |                |                |
|                |                |                |                |
|                | -   Deferred   |                |                |
|                |     > (on the  |                |                |
|                |     > backlog) |                |                |
+----------------+----------------+----------------+----------------+
| **System       | -   All        | Yes/iValua,    |                |
| Test**         |     > priority | CGI            |                |
|                |     > 1 and 2  |                |                |
|                |     > test     |                |                |
|                |     > cases    |                |                |
|                |     > Pass     |                |                |
|                |                |                |                |
|                | -   All        |                |                |
|                |     > priority |                |                |
|                |     > 1 and 2  |                |                |
|                |     > test     |                |                |
|                |                |                |                |
|                |    > scenarios |                |                |
|                |     > have     |                |                |
|                |     > been     |                |                |
|                |                |                |                |
|                |    > automated |                |                |
|                |                |                |                |
|                | -   All        |                |                |
|                |                |                |                |
|                |    > resulting |                |                |
|                |     > defects  |                |                |
|                |     > are:     |                |                |
|                |                |                |                |
|                |     -   Closed |                |                |
|                |                |                |                |
|                |      > (fixed) |                |                |
|                |                |                |                |
|                |     -   Closed |                |                |
|                |         > (not |                |                |
|                |                |                |                |
|                |    > relevant) |                |                |
|                |                |                |                |
|                |                |                |                |
|                |   -   Deferred |                |                |
|                |         > (on  |                |                |
|                |         > the  |                |                |
|                |                |                |                |
|                |     > backlog) |                |                |
+----------------+----------------+----------------+----------------+
| **Smoke Test** | -   Smoke test | Yes/All        | A failed smoke |
|                |     > passes   |                | test would     |
|                |     > 100%     |                | mean that the  |
|                |                |                | solution does  |
|                | -   No         |                | not run.       |
|                |     >          |                |                |
|                |  open/deferred |                |                |
|                |     > defects  |                |                |
|                |     > allowed  |                |                |
+----------------+----------------+----------------+----------------+
| **Performance  | -   All        | Yes/iValua &   | It might be    |
| Test**         |     > priority | CGI            | that           |
|                |     > 1 and 2  |                | performance    |
|                |                |                | testing is not |
|                |  > performance |                | a planned      |
|                |     > goals    |                | activity in    |
|                |     > are      |                | every sprint.  |
|                |     > reached  |                |                |
|                |                |                |                |
|                | -              |                |                |
|                |    Performance |                |                |
|                |     > Test     |                |                |
|                |     > Scripts  |                |                |
|                |     > have     |                |                |
|                |     > been     |                |                |
|                |     > created  |                |                |
|                |     > and      |                |                |
|                |     > executed |                |                |
|                |                |                |                |
|                | -   All        |                |                |
|                |                |                |                |
|                |    > resulting |                |                |
|                |     > defects  |                |                |
|                |     > are:     |                |                |
|                |                |                |                |
|                |     -   Closed |                |                |
|                |                |                |                |
|                |      > (fixed) |                |                |
|                |                |                |                |
|                |     -   Closed |                |                |
|                |         > (not |                |                |
|                |                |                |                |
|                |    > relevant) |                |                |
|                |                |                |                |
|                |                |                |                |
|                |   -   Deferred |                |                |
|                |         > (on  |                |                |
|                |         > the  |                |                |
|                |                |                |                |
|                |     > backlog) |                |                |
+----------------+----------------+----------------+----------------+
| **Test         | -   All test   | Maybe          | Test           |
| Automation**   |                |                | automation is  |
|                |   > automation |                | a key enabler, |
|                |     > tasks    |                | which will     |
|                |     > have     |                | allow the      |
|                |     > been     |                | project to     |
|                |     > executed |                | keep moving    |
|                |                |                | forward        |
|                |    > resulting |                | through the    |
|                |     > in:      |                | sprints. If    |
|                |                |                | not finished   |
|                |                |                | the project    |
|                |  -   Automated |                | will incur     |
|                |                |                | issues and     |
|                |     > Function |                | challenges     |
|                | al/Integration |                | during later   |
|                |                |                | sprints and/or |
|                |        > Tests |                | post release   |
|                |                |                | maintenance.   |
|                |                |                |                |
|                |  -   Automated |                |                |
|                |                |                |                |
|                |       > System |                |                |
|                |                |                |                |
|                |        > Tests |                |                |
|                |                |                |                |
|                |                |                |                |
|                |  -   Automated |                |                |
|                |                |                |                |
|                |   > Regression |                |                |
|                |         > Test |                |                |
|                |                |                |                |
|                |                |                |                |
|                |   -   Scripted |                |                |
|                |                |                |                |
|                |  > performance |                |                |
|                |                |                |                |
|                |        > tests |                |                |
|                |                |                |                |
|                |                |                |                |
|                |    -   Updated |                |                |
|                |         > test |                |                |
|                |                |                |                |
|                |   > automation |                |                |
|                |         > run  |                |                |
|                |         > book |                |                |
+----------------+----------------+----------------+----------------+
| **Defects**    | -   *          | Yes/ ALL       | At the end of  |
|                | *All** defects |                | the sprint     |
|                |     > have     |                | there will be  |
|                |     > been     |                | no open (new,  |
|                |     > reviewed |                | in progress,   |
|                |     > and      |                | re-opened,     |
|                |                |                | failed)        |
|                |    > addressed |                | defects.       |
|                |                |                |                |
|                | -   All        |                | Defects are    |
|                |                |                | either closed  |
|                |    > resulting |                | (no action     |
|                |     > defects  |                | necessary) or  |
|                |     > are:     |                | deferred and   |
|                |                |                | entered in the |
|                | -   Closed     |                | project        |
|                |     > (fixed)  |                | backlog. The   |
|                |                |                | deferral is    |
|                | -   Closed     |                | decided by the |
|                |     > (not     |                | team.          |
|                |                |                |                |
|                |    > relevant) |                |                |
|                |                |                |                |
|                | -   Deferred   |                |                |
|                |     > (on the  |                |                |
|                |     > backlog) |                |                |
+----------------+----------------+----------------+----------------+
| **Test         | -   All test   | Yes/Roland     |                |
| Management     |     > plans    |                |                |
| (Zephyr)**     |     > are      |                |                |
|                |                |                |                |
|                |    > finalized |                |                |
|                |     > and      |                |                |
|                |     > closed   |                |                |
|                |                |                |                |
|                | -   All        |                |                |
|                |     > reports  |                |                |
|                |     > have     |                |                |
|                |     > been     |                |                |
|                |                |                |                |
|                |    > generated |                |                |
|                |                |                |                |
|                | -   The        |                |                |
|                |                |                |                |
|                |   > activities |                |                |
|                |     > for the  |                |                |
|                |     > current  |                |                |
|                |                |                |                |
|                |    > milestone |                |                |
|                |     > have     |                |                |
|                |                |                |                |
|                |    > concluded |                |                |
|                |                |                |                |
|                | -   The work   |                |                |
|                |     > for this |                |                |
|                |     > cycle    |                |                |
|                |     > has been |                |                |
|                |     > locked   |                |                |
|                |     > and      |                |                |
|                |     > archived |                |                |
+----------------+----------------+----------------+----------------+
| **D            | -   Test       | Yes/Province   |                |
| ocumentation** |     >          | Team           |                |
|                |  Documentation |                |                |
|                |     > has been |                |                |
|                |     > updated  |                |                |
+----------------+----------------+----------------+----------------+
| **Project      | -   The        | Yes/Scrum      |                |
| Backlog**      |     > project  | Master         |                |
|                |     > backlog  |                |                |
|                |     > is       |                |                |
|                |     > updated  |                |                |
|                |     > with     |                |                |
|                |     > items    |                |                |
|                |     > that     |                |                |
|                |     > emanated |                |                |
|                |     > from     |                |                |
|                |     > testing  |                |                |
|                |                |                |                |
|                | -   The team   |                |                |
|                |     > has      |                |                |
|                |     > agreed   |                |                |
|                |     > on the   |                |                |
|                |     > new      |                |                |
|                |     > testing  |                |                |
|                |     > items in |                |                |
|                |     > the      |                |                |
|                |     > backlog  |                |                |
+----------------+----------------+----------------+----------------+

 

 

 

Testing Principles

June 24, 2019

2:43 PM

-   Introduction

    -   Context

    -   Key Terminology

-   Leading Principles

-   General Software Test Principle

-   Test Strategy Principle

-   Test Planning Principle

-   Traceability Principle

-   Test Estimation Principle

-   Test Design Principle

-   Unit Test Design Principle

-   Business/User Acceptance Test Design Principle

-   Test Execution Principle

-   Automated Test Execution Principle

-   Regression Test Principle

-   Test Environment Principle

-   Test Data Principle

-   Defect Management Principle

-   Testware Management Principle

-   Test Closure Principle

 

Introduction

A Principle represents a preferred course of action and the assumptions
on which they are based. 

By creating testing principles a company creates clarity and direction
which are conducive for the acceptance and implementation of testing
processes and procedures.

In this document, the PPR Team describes the high level policies that
govern software testing.

Context

Quality Assurance (QA) is the overarching name for the practices that
instill proper processes and procedures in order to improve quality
whereas Quality Control (QC) covers the activities that measure and
control quality.  Software testing is the main technique in the QC and
typically of such importance and impact that it sometimes has become
synonymous with QA and QC.

Key Terminology

Here are the key terms used within the context of the testing
principles.

Please be aware that these terms might have a different interpretation
outside this context.

  **Acceptance Test**                               The AT focuses on the *capability* to perform the Business Processes and variations. The AT assumes a functionally correct SUT.
  ------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Requirement/User Story/Acceptance Criterion**   Any statement on what the system should be doing. This includes business requirements, system requirements, design requirements etc.
  **SUT**                                           System Under Test
  **Test Lead**                                     Refers to the **role** of test lead.
  **Test Requirement**                              One requirement/user story has one or more test requirements. In a test requirement we state what needs to be tested in order to prove that the requirement passed.
  **Testware**                                      Artefacts produced during the test process required to plan, design, and execute tests, such as documentation, scripts, inputs, expected results, set-up and clear-up procedures, files, databases, environment, and any additional software or utilities used in testing.
  **Test Design**                                   The process of transforming general testing objectives into tangible test conditions and test cases.

Leading Principles

When describing policies, it is important to understand the leading
principles from which they emanate.

-   Testing is a planned activity.

-   Testing is a risk management activity.

-   Testing involves: Planning, Analysis, Design, Execution, Evaluation,
    > Reporting and Test Closure.

-   Testware is a valuable asset that needs to be carefully kept and
    > maintained.

-   Testing needs to be a plan-able and predictable activity.

-   Testing requires verification, validation and experiments by an
    > independent
    > party.[\[1\]](file:///C:/Users/Roland/Documents/Pensions/Test%20Policy.docx#_ftn1)

-   Testing provides information on the state and condition of the SUT.

-   Management makes decisions on acceptability of defects moving into
    > production.

-   Everybody involved with the deployment of systems is responsible for
    > quality.

-   More complete and better defined input results in better testing.

-   Testing aims to verify all stated and tacit requirements.

-   The testing phases are accumulative; each phase builds on the
    > achievements of an earlier phase without repeating the work of the
    > previous phase.

-   Testers are specialized resources with a mindset distinctly
    > different from developers.

-   Testing needs to be aware of context and adjust its approach
    > accordingly.

-   Well planned and executed testing provides unmatched understanding
    > on the readiness of the application to be deployed.

-   Testing assumes that the SUT is broken, the more this assumption is
    > proven wrong, the weaker the assumption becomes.

-   Testing is expensive and therefore needs to be planned in such a way
    > that it delivers the most value per dollar invested.

-   Testing will often be squarely on the critical path of a project.

-   Testing will not find all defects.

-   Different test techniques and approaches yield more defects.

-   Repetitive tests need to be automated.

-   A centralized defect management process is the backbone of the test
    > process.

General Software Test Principle

> **Basic assumption(s):**

-   All developed and configured software must be tested.

-   All changes to existing systems must be tested.

> **Test Principle:**

-   Developers, Testers and Business Users will test all systems based
    > on Test Strategy, Test Plan and activities as described in the
    > testing process before the system is used in production.

Test Strategy Principle

> **Basic assumption(s):**

-   Testing is a planned activity.

-   Testing helps manage the risks when implementing new or changed
    > software.

> **Test Principle:**

-   The test lead will produce a test strategy describing the test
    > approach.

-   The test strategy needs agreement from the stakeholders.

Test Planning Principle

> **Basic assumption(s):**

-   Testing is a planned activity.

> **Test Principle:**

-   The test lead will deliver a test plan describing how the test
    > strategy will be implemented.

Traceability Principle

> **Basic assumption(s):**

-   All requirements must be tested.

-   Test progress must be measured against coverage of requirements.

> **Test Principle:**

-   Testers will map all test cases back to requirements to ensure they
    > have all been covered by test cases.

-   Test Lead will report progress based on requirements coverage.

Test Estimation Principle

**Basic assumption(s):**

-   Project Management needs realistic testing estimates.

-   Test estimation covers: Scope, Time and Resources (human and system)

-   Test estimation applies resources there where they bring the most
    > benefit for the project.

> **Test Principle:**

-   Every test effort will be estimated and approved first before
    > testing commences.

-   The test estimation takes the identified project/system risks into
    > account.

-   Estimates for testing will be delivered by the test lead.

-   Estimates for testing will be refined in detailed plans as more
    > information becomes available.

Test Design Principle

> **Basic assumption(s):**

-   All test requirements need to be met.

-   All requirements need to be covered.

-   Tests need to be documented.

> **Test Principle:**

-   Testers will create test design for Integration and System Testing.

-   Testers will create Testing charters to be executed during the
    > sprints.

-   Test design is documented and stored for re-use and reference.

Unit Test Design Principle

> **Basic assumption(s):**

-   All modules/functions/components/interfaces need to be Unit tested
    > by the developer.

-   Unit tests need to be re-usable.

-   Unit tests need to cover design specification requirements.

-   Unit Tests need to be implemented as automated tests.

> **Test Principle:**

-   Developers will create a unit test design for each component they
    > produce.

-   Unit Test design is documented and stored for re-use and reference.

Business/User Acceptance Test Design Principle

> **Basic assumption(s):**

-   Business Users will get a solution that will allow them to meet
    > their business objectives.

> **Test Principle:**

-   The Business/User Acceptance Tester will create a test design
    > focused on proving that the solution meets the Business Users
    > needs.

-   The Business/User Acceptance Test design reflects the common and
    > exception operations of the business.

-   The Business/User Acceptance Test design will contain all the test
    > cases needed to obtain the information for acceptance of the
    > system.

Test Execution Principle

> **Basic assumption(s):**

-   Tests need to be executed.

-   The right resources need to execute the tests.

> **Test Principle:**

-   Unit Tests are executed by developers.

-   Quality Tests are executed by the quality testers.

-   Business/User Acceptance Tests are executed by the Acceptance
    > testers and Business Users.

Automated Test Execution Principle

> **Basic assumption(s):**

-   Tests need to be executed in an efficient and repeatable manner.

-   All unit testing needs to be automated.

-   Systems need to be tested for regression errors after changes.

-   Not all tests will be automated.

-   Tests will be automated in order to improve efficiency.

> **Test Principle:**

-   Automated Unit Tests are executed by the Developers.

-   Automated Tests are executed by the Test Automation Specialists.

-   Performance Tests are executed by the Performance Test Specialists.

-   Functional Regression tests will be automated.

Regression Test Principle

> **Basic assumption(s):**

-   Systems need to be tested for regression errors after changes.

-   The scope of the regression test is dependent on risk.

> **Test Principle:**

-   Systems will be regression tested to mitigate risk on unintended
    > errors after changes.

-   Regression tests will be automated where appropriate.

Test Environment Principle

> **Basic assumption(s):**

-   All developed and configured software must be tested.

-   Test environments are available and configured.

-   Multiple projects need to use the same test environments.

-   Usage of the same environment by different project can cause
    > interference.

-   Test environment resource conflicts need to be addressed.

> **Test Principle:**

-   Testing uses dedicated Test Environments.

-   The project is responsible for communicating:

-   Coordination of test environment usage.

-   Facilitating negotiations on usage and planning.

-   Facilitating the creation of new test environments.

-   The project and the internal Testing Services group owns the Test
    > environments.

Test Data Principle

> **Basic assumption(s):**

-   Testing is using test data.

-   Testing owns the test data.

-   High quality, dedicated test data is available.

-   Developers are responsible for the creation of Unit Test Data.

> **Test Principle:**

-   The test environments contain either fictional test data or
    > masked/de-identified production data.

-   The Business/User Acceptance Test environment can contain production
    > data or masked/de-identified production data.

Defect Management Principle

> **Basic assumption(s):**

-   Defects need to be managed.

-   There will be *one* defect management tool used during analysis,
    > design, development and testing.

-   The defect management tool, user procedures and reviews will enforce
    > consistent, high quality defect reporting.

> **Test Principle:**

-   Defect Management will follow the standard defect management
    > process.

-   All defects will be reported in and managed by a central defect
    > management tool.

-   All personnel involved in the creation, roll-out and sustainment of
    > a solution will have access to the central tool and will be able
    > to review the project issues.

Testware[**\[2\]**](file:///C:/Users/Roland/Documents/Pensions/Test%20Policy.docx#_ftn2) Management
Principle

> **Basic assumption(s):**

-   All testware needs to be kept.

-   Testware will be re-used.

-   Testware has significant value to the corporation.

> **Test Principle:**

-   Developers will store and consolidate all Unit Test Testware for
    > later re-use and reference.

-   Testers will store and consolidate all Quality Testing Testware for
    > later re-use and reference.

-   Acceptance Testers and Business Users will store and consolidate all
    > Business/User Acceptance Test Testware for later re-use and
    > reference.

-   The PPR Project is the initial testware guardian.

Test Closure Principle

> **Basic assumption(s):**

-   Closure of the test activities will provide an opportunity to
    > consolidate results, obtain/extract relevant metrics and identify
    > improvement opportunities for the future.

> **Test Principle:**

-   The planning for testing will include a test closure activity.

-   The Test Services groups and the Business Support groups are the
    > main stakeholders in the test closure activity.

 

 

[\[1\]](file:///C:/Users/Roland/Documents/Pensions/Test%20Policy.docx#_ftnref1) Except
in unit testing where the developer tests his own work.

[\[2\]](file:///C:/Users/Roland/Documents/Pensions/Test%20Policy.docx#_ftnref2) Artefacts
produced during the test process required to plan, design, and execute
tests, such as documentation, scripts, inputs, expected results, set-up
and clear-up procedures, files, databases, environment, and any
additional software or utilities used in testing.

 

 

 

Continuous Improvement Process (CIP)

July 2, 2019

9:48 AM

A  **continuous improvement process** (abbreviated as CIP or CI), is an
ongoing effort to improve products, services, or processes. These
efforts can seek \"incremental\" improvement over time or
\"breakthrough\" improvement all at once.

In an agile project CIP is a permanent mindset, where every sprint
intends to include improvements of what was done in the previous
sprint(s). This is most clear in the defined review
and retrospective events for each sprint.

 

+----------------+----------------+--------------+----------------+
| **Event**      | *              | **Duration** | **Frequency**  |
|                | *Description** |              |                |
+================+================+==============+================+
| **Sprint       | Product Owner  | 1-2 hours    | Once per       |
| Review**       | explains what  |              | Sprint         |
|                | Product        |              |                |
|                | Backlog items  |              |                |
|                | have been      |              |                |
|                | "done" and     |              |                |
|                | what has not   |              |                |
|                | been "done"    |              |                |
|                |                |              |                |
|                | The team       |              |                |
|                | demonstrates   |              |                |
|                | that the work  |              |                |
|                | that it has    |              |                |
|                | "done"  and    |              |                |
|                | answers        |              |                |
|                | questions      |              |                |
|                |                |              |                |
|                | Entire group   |              |                |
|                | collaborates   |              |                |
|                | on what to do  |              |                |
|                | next, this     |              |                |
|                | serves as an   |              |                |
|                | input to the   |              |                |
|                | Sprint         |              |                |
|                | Planning       |              |                |
|                | meeting        |              |                |
|                |                |              |                |
|                | the team       |              |                |
|                | discusses what |              |                |
|                | worked well,   |              |                |
|                | what problems  |              |                |
|                | they had and   |              |                |
|                | how they       |              |                |
|                | solved them    |              |                |
+----------------+----------------+--------------+----------------+
| **Sprint       | Reflect as a   | 1 hour       | Once per       |
| R              | team on what   |              | Sprint         |
| etrospective** | did and didn't |              |                |
|                | work during    |              |                |
|                | the course of  |              |                |
|                | the prior      |              |                |
|                | sprint         |              |                |
|                |                |              |                |
|                | Create         |              |                |
|                | actionable     |              |                |
|                | work items to  |              |                |
|                | directly       |              |                |
|                | address areas  |              |                |
|                | the team can   |              |                |
|                | improve upon   |              |                |
|                |                |              |                |
|                | Revisit prior  |              |                |
|                | retrospective  |              |                |
|                | work items     |              |                |
|                | found from     |              |                |
|                | previous       |              |                |
|                | sprints        |              |                |
+----------------+----------------+--------------+----------------+

In the Test Closure Process we indicate that we will collect information
to feed into CIP.

An output of the two above mentioned events is an updated Agile practice
status. This has value but is at a high level and does not completely
address specific testing related processes.

For evaluating the testing activities and suggest potential
improvements, we will use the following checklist to collect feedback
for every sprint retrospective:

 

+----------------+----------------+----------------+----------------+
| ** **          | **Issues?**    | *              | **Suggested    |
|                |                | *Description** | Change         |
|                |                |                | /Improvement** |
+================+================+================+================+
| **General**    |                |                |                |
+----------------+----------------+----------------+----------------+
| Scope of work  | **N/A**        |                |                |
|                |                |                |                |
|                | **NO ISSUES**  |                |                |
|                |                |                |                |
|                | **SOME         |                |                |
|                | CONCERNS**     |                |                |
|                |                |                |                |
|                | **NEEDS        |                |                |
|                | IMPROVEMENT**  |                |                |
|                |                |                |                |
|                | **BRIGHT       |                |                |
|                | IDEA**         |                |                |
+----------------+----------------+----------------+----------------+
| Planning       | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Resourcing     | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| **Process**    |                |                |                |
+----------------+----------------+----------------+----------------+
| Test           | **N/A**        |                |                |
| Initiation     |                |                |                |
+----------------+----------------+----------------+----------------+
| Test Planning  | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Test Design    | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Test Execution | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Test Closure   | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Status         | **N/A**        |                |                |
| Reporting      |                |                |                |
+----------------+----------------+----------------+----------------+
| Test Results   | **N/A**        |                |                |
| Reporting      |                |                |                |
+----------------+----------------+----------------+----------------+
| Defect         | **N/A**        |                |                |
| Management     |                |                |                |
+----------------+----------------+----------------+----------------+
| **Test         |                |                |                |
| Activities**   |                |                |                |
+----------------+----------------+----------------+----------------+
| Unit Testing   | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Integration    | **N/A**        |                |                |
| Testing        |                |                |                |
+----------------+----------------+----------------+----------------+
| Functional     | **N/A**        |                |                |
| Testing        |                |                |                |
+----------------+----------------+----------------+----------------+
| System Testing | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| User           | **N/A**        |                |                |
| Acceptance     |                |                |                |
| Testing        |                |                |                |
+----------------+----------------+----------------+----------------+
| Smoke Testing  | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Regression     | **N/A**        |                |                |
| Testing        |                |                |                |
+----------------+----------------+----------------+----------------+
| Performance    | **N/A**        |                |                |
| Testing        |                |                |                |
+----------------+----------------+----------------+----------------+
| Security       | **N/A**        |                |                |
| Testing        |                |                |                |
+----------------+----------------+----------------+----------------+
| Test           | **N/A**        |                |                |
| Automation     |                |                |                |
+----------------+----------------+----------------+----------------+
| **Tool         |                |                |                |
| s/Data/Other** |                |                |                |
+----------------+----------------+----------------+----------------+
| Test Data      | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Test           | **N/A**        |                |                |
| Environments   |                |                |                |
+----------------+----------------+----------------+----------------+
| Test Tools     | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+
| Other          | **N/A**        |                |                |
+----------------+----------------+----------------+----------------+

**Legend:**

**NO ISSUES**

**SOME CONCERNS**

**NEEDS IMPROVEMENT**

**BRIGHT IDEA**

 

 

 

 

July 11, 2019

9:34 AM

 

 

 

SBTM Session Debrief Checklist

June 25, 2019

11:30 AM

Charter

-   Did you review relevant approved session reports?

-   Does it match the bulk of the testing that was actually done?

Areas

-   Is there at least one O/S keyword (unless it\'s not applicable)?

-   Is the build keyword accurate?

-   Is there at least one strategy keyword?

-   Is there at least one product area, as specific as meaningful to
    > specify?

Duration

-   Is the duration code in line with the actual duration?

-   Was the session continuous and uninterrupted?

Opportunity

-   If the opportunity number is over 0%, what was the opportunity?

-   If the opportunity number is over 25%, consider modifying the
    > charter.

-   If the opportunity number is over 50%, modify the charter for this
    > session and consider doing a new session based on the original
    > charter.

Data Files

-   If there were no data files, why not?

-   If there were data files, were they original or re-used? If re-used,
    > were they modified in any way? If so, how do they now relate to
    > other sessions that refer to the same data?

-   Is there an associated test coverage outline that should be
    > referenced?

Test Notes

-   Are they comprehensible?

-   In conjunction with the charter, do they answer the question \"what
    > happened in this test session?\"

-   Do they include information about coverage, oracles, and strategy?

-   Is there anything in the notes that can be re-used in a future
    > session? If not, that may be okay, but remember: part of the
    > reason for the notes is to build a better plan for testing.

-   Is this section free of issues and bugs?

Defects

-   Is enough information included to reproduce the problem?

-   Is the section free of test notes and issues?

Issues

-   If there are no issues, does that mean there was no confusion, no
    > remaining questions, and no obstacles in the path of testing?

-   Do any issues require actions to be taken?

-   Is the section free of test notes and bug reports?

Overall

-   Will metrics based on this session sheet faithfully represent the
    > testing that was done?

-   Do the results of this session suggest the need for another session?

-   Should this session be extended and amended?

 

 

 

RASCI Legend

June 25, 2019

2:58 PM

**Key Responsibility Definition**

**R**-- Responsible (for process execution/management):  This is the
person who actually performs the task.

**A** -- Approves/Accountable:  This is the person who is accountable
for the quality and timeliness of the completion of the task, and is
frequently the person to whom the responsible person reports.

**S** -- Supports: This is the person who is supporting the testing
process

**C** -- Consulted: These are the subject matter experts, or other
people who provide information needed for correct execution of the task.

**I** -- Informed: These are the people who are impacted by the progress
of the task, and so are advised of milestones or significant
developments.

 

 

 

Defect Management Workflow

Tuesday, June 11, 2019

2:39 PM

![Untitled picture Start here
](media/image5.png){width="9.790972222222223in"
height="7.747916666666667in"}

 

 

 

Issue Types

Tuesday, June 11, 2019

2:32 PM

+----------+----------+----------+----------+----------+----------+
| **Type** | **Pr     | *        | **       | *        | **N      |
|          | esent?** | *Updates | Workflow | *Current | eeded?** |
|          |          | re       | re       | Lo       |          |
|          |          | quired** | quired** | cation** |          |
+==========+==========+==========+==========+==========+==========+
| As       | Yes      | TBD      | No -     | PPR -    | Y        |
| sumption |          |          | Maybe    | Issue    |          |
|          |          |          | some     | (BBI)    |          |
|          |          |          | stre     |          |          |
|          |          |          | amlining |          |          |
+----------+----------+----------+----------+----------+----------+
| Risk     | Yes      | TBD      | No -     | PPR -    | Y        |
|          |          |          | Maybe    | Issue    |          |
|          |          |          | some     | (BBI)    |          |
|          |          |          | stre     |          |          |
|          |          |          | amlining |          |          |
+----------+----------+----------+----------+----------+----------+
| Issue    | Yes      | TBD      | No -     | PPR -    | Y        |
|          |          |          | Maybe    | Issue    |          |
|          |          |          | some     | (BBI)    |          |
|          |          |          | stre     |          |          |
|          |          |          | amlining |          |          |
+----------+----------+----------+----------+----------+----------+
| Decision | Yes      | TBD      | No -     | PPR -    | Y        |
|          |          |          | Maybe    | Issue    |          |
|          |          |          | some     | (BBI)    |          |
|          |          |          | stre     |          |          |
|          |          |          | amlining |          |          |
+----------+----------+----------+----------+----------+----------+
| Story    | Yes      | TBD      |          | PPR -    | Y        |
|          |          |          |          | Product  |          |
|          |          |          |          | (BBP)    |          |
|          |          |          |          |          |          |
|          |          |          |          | PPR -    |          |
|          |          |          |          | Build    |          |
|          |          |          |          | (BBB)    |          |
|          |          |          |          |          |          |
|          |          |          |          | PPR -    |          |
|          |          |          |          | General  |          |
|          |          |          |          | (BBG)    |          |
+----------+----------+----------+----------+----------+----------+
| Business | Yes      | TBD      |          | PPR -    | N        |
| Rule     |          |          |          | Product  |          |
|          |          |          |          | (BBP)    |          |
|          |          |          |          |          |          |
|          |          |          |          | PPR -    |          |
|          |          |          |          | Build    |          |
|          |          |          |          | (BBB)    |          |
+----------+----------+----------+----------+----------+----------+
| Epic     | Yes      | TBD      |          | PPR -    | Y        |
|          |          |          |          | Product  |          |
|          |          |          |          | (BBP)    |          |
|          |          |          |          |          |          |
|          |          |          |          | PPR -    |          |
|          |          |          |          | Build    |          |
|          |          |          |          | (BBB)    |          |
|          |          |          |          |          |          |
|          |          |          |          | PPR -    |          |
|          |          |          |          | General  |          |
|          |          |          |          | (BBG)    |          |
+----------+----------+----------+----------+----------+----------+
| Task     | Yes      | TBD      |          | PPR -    | Y        |
|          |          |          |          | Product  |          |
|          |          |          |          | (BBP)    |          |
|          |          |          |          |          |          |
|          |          |          |          | PPR -    |          |
|          |          |          |          | Build    |          |
|          |          |          |          | (BBB)    |          |
|          |          |          |          |          |          |
|          |          |          |          | PPR -    |          |
|          |          |          |          | General  |          |
|          |          |          |          | (BBG)    |          |
+----------+----------+----------+----------+----------+----------+
| Test     | Yes      | TBD      |          | PPR -    | Y        |
|          |          |          |          | Build    |          |
|          |          |          |          | (BBB)    |          |
|          |          |          |          |          |          |
|          |          |          |          | PPR -    |          |
|          |          |          |          | General  |          |
|          |          |          |          | (BBG)    |          |
+----------+----------+----------+----------+----------+----------+
| Defect   | Yes      | Yes      | Yes      | PPR -    | Y        |
|          |          |          |          | General  |          |
|          |          |          |          | (BBG)    |          |
+----------+----------+----------+----------+----------+----------+
| Enh      | Yes      | Yes      |          | PPR -    | N        |
| ancement |          |          |          | General  |          |
|          |          |          |          | (BBG)    |          |
+----------+----------+----------+----------+----------+----------+
| Ac       | No       | Yes      | Yes,     | PPR -    | Y        |
| ceptance |          |          | sub-task | General  |          |
| Cr       |          |          |          | (BBG)    |          |
| iterion/ |          |          |          |          |          |
| Scenario |          |          |          |          |          |
| (we\'ll  |          |          |          |          |          |
| see what |          |          |          |          |          |
| the      |          |          |          |          |          |
| pr       |          |          |          |          |          |
| eference |          |          |          |          |          |
| is)      |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Sub-Task | Yes      | No       |          | PPR -    | Y        |
|          |          |          |          | General  |          |
|          |          |          |          | (BBG)    |          |
+----------+----------+----------+----------+----------+----------+
|          |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
|          |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
|          |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
|          |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+

 

 

 

 

Issue Type Relationships

Tuesday, June 11, 2019

2:37 PM

![Machine generated alternative text: Jira Issue Type Relations Issue
Management Risk Assumption Decision Sub-Task Definition Epic Story Test
Action Defect Task ](media/image6.png){width="13.086805555555555in"
height="9.252083333333333in"}

 

 

 

Screens

June 11, 2019

4:14 PM

  **Action**          **Starting Screen**         **Resulting Screen**   **Resulting Status**   **Limitations**
  ------------------- --------------------------- ---------------------- ---------------------- --------------------------------------------------------------------------
  Create new defect   N/A                         Defect Enter           Open                   Open to anybody, needs validations
  Ready for Review    Defect Enter                Defect View            Review                 Only reporter and test lead admin can move forward
  Ready for Triage    Defect View                 Defect Triage          Triage                 Test lead/admin can move forward
  Triage              Defect Triage               Triage Details         Triage                 Only after this screen - the Fix option will be available
  Fix                 Defect Triage (completed)   Defect View            Fix Queue              Items are placed in the fixed queue as \"unassigned\"
  Assign Work         Defect View                 Defect Full View       In Progress            Focused on developers, they are the only ones that can progress to fixed
  Fixed               Defect Full View                                                           

 

 

 

Fields

June 12, 2019

1:45 PM

  **Name**                   **Close**   **Default**   **Defer**   **Fix**   **Info Screen**   **Re-Open**   **Review**   **Ready Validation**   **Triage**   **Validate**   **View**
  -------------------------- ----------- ------------- ----------- --------- ----------------- ------------- ------------ ---------------------- ------------ -------------- ----------
  Affects Version/s                      RW                                                                                                                                   
  Assignee                   SYSTEM      RW                                                                                                      RW                           
  Attachment                             RW                        RW                          RW            R                                   R            R               
  Comment                    RW          RW            RW          RW        RW                RW            RW           RW                     RW           RW             RW
  Component/s - HIGH LEVEL               RW                        RW                          R                                                                              
  Customer value                                       RW          R                           R             RW                                  RW                           
  Date of First Response     SYSTEM                                                                                                                                           
  Description                R           RW            R           R         R                 R             RW           R                      RW           R              R
  Due Date                                                         R                                                                             RW                           
  Environment                            RW                        R                                                                                          R               
  Expected behavior                      RW                        R                                                                                          R               
  External Ref ID                        RW                                                                                                                                   
  External Ref Type                      RW                                                                                                                                   
  Fix Version/s              R                                     RW                                                     R                      RW           R               
  Function Affected                      RW            R           RW                                                                            R                            
  Issue Linking                          ACTION                                                R             RW                                  RW                          R
  Issue Type                 R           SYSTEM        R           R         R                 R             R            R                      R            R              R
  Modules Affected                                                 RW                                                                            RW           R               
  OS                                     RW                        RW                                                                                                         
  Other Areas Affected                   RW                        RW                                                                            RW                           
  Other Contact                          RW                        RW                                        RW                                  RW                           
  Platform                               RW                        RW                                                                                                         
  Priority                                                         R                                                                             RW           R               
  Product                                                                                                                                                                     
  Product status                         RW                                                                                                                                   
  Project phase                          RW            RW          RW                                                                                         RW              
  Repeatability                          RW                        R                                         R                                   R                            
  Reporter                               RW            R           R         R                 R             R            R                      R            R              R
  Requirement Description                RW            R           R                                         R                                   R            R               
  Requirement ID                         RW            R           R                                         R                                   R            R               
  Requirement URL                        RW            R           R                                         R                                   R            R               
  Requirement Version                    RW            R           R                                         R                                   R            R               
  Resolution                 RW                                                                              R                                                                
  Root Cause                                                       RW                                                                                                         
  Security Level                         SYSTEM                                                                                                                               
  Severity                               RW - HIDDEN   R           R                           R             R                                   R            R               
  Steps to reproduce                     RW                        R                                                                                                          
  Summary                    System      RW                        R                           R             R                                   R                            
  Symptom                                RW - HIDDEN   R           R                           R             R                                   R            R               
  Symptom/Severity                       RW            R           R                           R             R                                   R            R               
  Systems Impacted                       RW                        RW                                                                            R            R               
  Tag                                    RW                                                                                                                                   
  Test Case Description                  RW                        R                                                                                          R               
  Test Case ID                           RW                        R                                                                                          R               
  Test Case URL                          RW                        R                                                                                          R               
  Test Case Version                      RW                        R                                                                                          R               
  Test Cycle Day                         RW                        R                                                                                          R               
  Test Environment                       RW                        R                                                                                          R               
  Test Run                               RW                        R                                                                                          R               
  Time in Status                                                                                                                                                              
  Type of Defect             R           RW                        R                           R             R                                   R            R               
  Design Description                     RW                        R                                                                                          R               
  Design ID                              RW                        R                                                                                          R               
  Design URL                             RW                        R                                                                                          R               
  Design Version                         RW                        R                                                                                          R               
  Development Description                RW                        R                                                                                          R               
  Dev. ID                                RW                        R                                                                                          R               
  Dev. URL                               RW                        R                                                                                          R               
  Dev. Version                           RW                        R                                                                                          R               
  Handshake reference                    RW                                                                                                                                   

 

 

 

Ideas and Things to fix

June 19, 2019

11:15 AM

-   Decision logging in RIDAL: Requires dependencies check

-   Have system admin in Jira for Team - requested

-   Define User Story Priority

-   Define Defect Priority

-   Add new CGI Users: Done?

-   Set up components and leads

-   Tag BBB with Pilot2/Phase2 - Why do we have multiple projects?

-   Post missing at Sprint Review and Sprint Planning - What is this?

-   Close mitigated risk for Phase 1

-   Close Releases - Releases need to be every code release and every
    > major release

-   Defect Workflow updates and training

-   Defect reporting - What was here?

-   Add labels to RIDAL (Components?) - What Labels?

-   Tag Backlog defects

-   Schedule Deployments CGI Test Env

-   Retro: Testing and Process

-   Backlog: defect workflow step vs actual backlog

-   Defects in sprint: No same as RIDAL

-   1st pass backlog

-   Schedule backlog clean-up

>  

 

 

 

User IDs

Tuesday, June 11, 2019

2:31 PM

Do we have:

-   Generic User IDs?

-   If so, do we have roles and access defined?

-   If not why not?

-   Need to set up users, roles, organizations, expense authorities

-   Probable need multiple of each.

Current list:

-   jason.buyer Password!23 old Buyer Admin

-   bid.userid4 Password!23 BCeID Supplier

-   james.admin Password!23 old Admin

-   Rstens old supplier

-   Rstens IDIR Admin

-   Roland.bid

-   Moses.bid

-   Roland.gov

  **BCeID Account Information**   
  ------------------------------- --------------------------------------------------------------
  Registration Date:              **June 5, 2019**
  Account Type:                   **Basic BCeID**
  User ID:                        **alex.bid**
  Given/First Name:               **Alex**
  Surname:                        **ValueTest**
  Email:                          [**roland.stens\@gmail.com**](mailto:roland.stens@gmail.com)

*From \<<https://www.test.bceid.ca/register/basic/confirmation.aspx>\>*

  **BCeID Account Information**   
  ------------------------------- --------------------------------------------------------------
  Registration Date:              **June 6, 2019**
  Account Type:                   **Basic BCeID**
  User ID:                        **antonio.bid**
  Given/First Name:               **Antonio**
  Surname:                        **Valuas**
  Email:                          [**roland.stens\@gmail.com**](mailto:roland.stens@gmail.com)

*From \<<https://www.test.bceid.ca/register/basic/confirmation.aspx>\>*

  **BCeID Account Information**   
  ------------------------------- --------------------------------------------------------------
  Registration Date:              **June 10, 2019**
  Account Type:                   **Basic BCeID**
  User ID:                        **geraldo.bid**
  Given/First Name:               **Geraldo**
  Surname:                        **Grandia**
  Email:                          [**roland.stens\@gmail.com**](mailto:roland.stens@gmail.com)

***Not yet registered as supplier!***

  **BCeID Account Information**                                                      
  --------------------------------------------------------------------------------- -----------------------------
  Registration Date:                                                                **June 24, 2019**
  Account Type:                                                                     **Basic BCeID**
  User ID:                                                                          **adrian.bid**
  Given/First Name:                                                                 **Adrian**
  Surname:                                                                          **Grandia**
  Email:                                                                            **roland.stens\@gmail.com**
  Phone:                                                                            **6048313629**
  [Basic BCeID Terms of Use](https://www.test.bceid.ca/aboutbceid/tou_basic.aspx)    

[Continue to Service
Directory](javascript:__doPostBack('proceedToSubscriptionsButton',''))

 

*From \<<https://www.test.bceid.ca/register/basic/confirmation.aspx>\>*

 

 

 

 

Unlimited GMail Addresses

Tuesday, June 11, 2019

2:33 PM

A nice little feature that most people do not know of.

Say you have your Gmail email account like <john.smith@gmail.com>

You can create additional email address that will all result in the
emails arriving at your regular address.

Examples:

<john.smith+address1@gmail.com>

<john.smith+address2@gmail.com>

<john.smith+address3@gmail.com>

<john.smith+address4@gmail.com>

<john.smith+address5@gmail.com>

All the above would be seen as different addresses by most systems, but
emails sent to them will all arrive in the same email box
(<john.smith@gmail.com>).

Additionally <john.smith@gmail.com> and <johnsmith@gmail.com> are
identical in google, so that is another way to create multiple email
addresses that are all the same address.

Examples:

<john.smith@gmail.com>

<johnsmith@gmail.com>

<j.ohnsmith@gmail.com>

<Johnsm.ith@gmail.com>

Etc.

 

 

 

 

Business Tester Requirements

Tuesday, June 11, 2019

2:34 PM

Business Tester
===============

Description:
------------

The Business Tester will be responsible for representing the user in
testing the new BC Bid system as part of the Agile development team.

The business testers are guided and supported by the project\'s Test
Lead and project team members.

Requirements:
-------------

-   Significant knowledge of BC Bid processes, disciplines and standards

-   Represents one or more roles in the BC procurement process

-   Understands the purpose of bringing an end-user perspective to the
    > test process

-   Open to learning how User Acceptance Testing is conducted

-   Familiar with web-based applications

-   Is detail oriented

-   Possesses analytical, problem solving, and communication skills

-   Nice to have: has been involved with the project during discovery,
    > design or usability testing

Time Line:
----------

-   With go-live planned in January, it is assumed that all UAT testing
    > will need to be concluded by mid December.

-   The actual UAT execution will take 4-5 weeks, requiring the business
    > testers to be ready to start the work by early to mid November

    -   Ready to do UAT means that the Business Testers are/do:

        -   On-boarded with the project

        -   Trained in tool usage and familiar with the application

        -   Understand the processes

    -   Also:

        -   Test cases and scenarios have been defined and reviewed

        -   Test Data, Integrated systems and the Acceptance Test
            > Environment have been set up and verified

        -   Test location has been identified and moved into

Effort:
-------

+----------------+----------------+----------------+----------------+
| **Role**       | **On-board     | **Start of     | **Comment**    |
|                | ing/Training** | Work**         |                |
|                |                |                |                |
|                | **% of time    |                |                |
|                | needed**       |                |                |
+================+================+================+================+
| Business       | July 15 --     | July 15 -      | End-User Focus |
| Tester         | September 30   | Until December | (Black-Box     |
|                | 20%            | 31th - First   | UAT)           |
|                |                | week of        |                |
|                |                | January : as   |                |
|                |                | close to 100%  |                |
|                |                | working in     |                |
|                |                | parallel with  |                |
|                |                | BC Bid Team    |                |
+----------------+----------------+----------------+----------------+

Team Composition:
-----------------

An effective UAT Team has the following roles:

-   Business Lead - This person will provide guidance with regards to
    > UAT scope, business priorities and will be instrumental in guiding
    > the business testers through UAT.

-   Test Lead - This is a BC Bid Team member who will make sure that the
    > pre-requisites (like system readiness, test data, access etc.) are
    > met and will drive and facilitate the day to day UAT activities.
    > The test lead will also facilitate the defect triage

-   Business Testers - 4-6 SMEs (current estimate). There is potential
    > to start with 2-3 senior SMEs and then add more junior ones later.

-   Business Analyst(s) - These are BC Bid team members that will assist
    > with testing, but more specifically will analyse issues found and
    > provide guidance to the BC Bid team and will communicate with
    > Business Leadership if needed.

-   System Integrator - CGI - These are the developers of the system and
    > will provide bug fixes for the issues that were found and needed
    > to be fixed.

 

Activities:
-----------

The business testers will be involved in the following activities
(supported by the BC Bid Team):

-   Review of requirements and identification of tests to test the
    > individual scenarios

-   Identification of the end-to-end business scenarios that need to be
    > verified

-   Identification of the exceptional and out of the ordinary scenarios
    > that need to be verified

-   Creation of test scenarios and test scripts that will give answers
    > to the questions that the business users will need to get
    > answered.

-   Review all test scenarios and verify scenarios with system before
    > the actual test execution

-   Execute defined tests

-   Engage in Exploratory testing

-   Report Defects and discuss with team

-   Re-test fixed defects and report result

-   Escalated any critical issues to the Test Lead and the BC Bid team

-   Participate in BC Bid team discussion and session where appropriate

-   Review of the sprint\'s deliverables and initial exploratory testing

Success Factors for UAT:
------------------------

-   Business user (SME) perspective to be represented *throughout* the
    > sprints

-   Senior SMEs - SMEs that have possibly worked in multiple roles and
    > have had significant exposure to most aspects of the BC Government
    > procurement processes.

-   SMEs working in parallel with the BC Bid team during all sprints
    > will improve communication and understanding - this will make the
    > final UAT almost a non-event and more a final check

-   The participating SMEs will be centres of knowledge once they return
    > to their operational tasks

-   A full time commitment - a of-the-side-of-your-desk approach will
    > typically yield a sub-par result and increase stress levels

-   A strong \"buck stops here\" business lead/owner who will make key
    > decisions

-   A commitment from business leadership for time and participation

-   One location - Particularly when starting up and doing the final UAT
    > execution, it is beneficial and efficient to have people together.

Benefits for the Business:
--------------------------

-   Confidence in the solution meeting the needs of the business

-   Early training and instruction for key SMEs

-   SMEs able acquire additional skills to further their career and/or
    > build the confidence that they can grow

-   Issues, observations, opinions will be conveyed in business language

 

 

 

 

Data Usage

June 26, 2019

9:50 AM

For training and test:

-   New data all the time?

-   Re-use existing data?

-   If we have new data all the time do we have to wipe/reset?

-   Do we give people data examples to implement (so the can focus on
    > the things they need to do?)

-   How \"real\" can the data be?

-   Are we enabling/disabling the training url or will this always be
    > available

-   What about instructions on not touching existing data?

-   Are there data \"starting points?

>  
>
>  

 

 

 

User ID Usage for Testing and Training

June 26, 2019

9:53 AM

What do we want to accomplish?

-   Training different roles with BCeID and IDIR

-   Personal IDIRs can be used but they need to be set up in a specific
    > role(s).

-   Currently we can only set up basic bceids, whereas in production
    > there will be business bceids, we have not tested this yet

-   Also for the pilot we would encourage for supplier to have only one
    > contact

>  
>
>  

 

 

 

Non-Functional Requirements

Tuesday, June 11, 2019

2:35 PM

+----------+----------+----------+----------+----------+----------+
| **Non-Fu | **Risk   | **Li     | **Risk   | **Descr  | **Test   |
| nctional | Rating** | kelihood | R        | iption** | Requi    |
| Requi    |          | (1-5)**  | anking** |          | rement** |
| rement** | **(1-    |          |          |          |          |
|          | Low to   |          |          |          |          |
|          | 5-       |          |          |          |          |
|          | Ex       |          |          |          |          |
|          | treme)** |          |          |          |          |
+==========+==========+==========+==========+==========+==========+
| Accuracy | 4        | 3        | 7        |          |          |
+----------+----------+----------+----------+----------+----------+
| Audi     | 2        | 2        | 4        | I        |          |
| tability |          |          |          | ncluding |          |
|          |          |          |          | Google   |          |
|          |          |          |          | A        |          |
|          |          |          |          | nalytics |          |
+----------+----------+----------+----------+----------+----------+
| Business | 3        | 4        | 7        |          |          |
| Co       |          |          |          |          |          |
| mpliance |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Compa    | 2        | 3        | 5        |          |          |
| tibility |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Confide  | 5        | 2        | 7        |          |          |
| ntiality |          |          |          |          |          |
| and      |          |          |          |          |          |
| Security |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Cost     | 0        | 0        | 0        |          |          |
| Effec    |          |          |          |          |          |
| tiveness |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Customer | 3        | 4        | 7        |          |          |
| service  |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Data     | 3        | 3        | 6        |          |          |
| I        |          |          |          |          |          |
| ntegrity |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Ef       | 3        | 2        | 5        |          |          |
| ficiency |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Fu       | 2        | 3        | 5        |          |          |
| nctional |          |          |          |          |          |
| comp     |          |          |          |          |          |
| leteness |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Fu       | 4        | 4        | 8        |          |          |
| nctional |          |          |          |          |          |
| cor      |          |          |          |          |          |
| rectness |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Instal   | 0        | 0        | 0        |          |          |
| lability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Interope | 4        | 4        | 8        |          |          |
| rability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Maintai  | 2        | 2        | 4        |          |          |
| nability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Per      | 2        | 4        | 6        |          |          |
| formance |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Recove   | 3        | 1        | 4        |          |          |
| rability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Rel      | 3        | 3        | 6        |          |          |
| iability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Re-u     | 0        | 0        | 0        |          |          |
| sability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Ro       | 3        | 2        | 5        |          |          |
| bustness |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Sca      | 2        | 2        | 4        |          |          |
| lability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| S        | 4        | 4        | 8        |          |          |
| tability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| T        | 1        | 1        | 2        |          |          |
| echnical |          |          |          |          |          |
| Co       |          |          |          |          |          |
| mpliance |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Test     | 4        | 2        | 6        |          |          |
| Ability  |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Ti       | 4        | 4        | 8        |          |          |
| meliness |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| Upgrad   | 3        | 1        | 4        |          |          |
| eability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
| U        | 5        | 3        | 8        |          |          |
| sability |          |          |          |          |          |
+----------+----------+----------+----------+----------+----------+
|          |          |          | 0        |          |          |
+----------+----------+----------+----------+----------+----------+

 

 

 

 

Training to be delivered

Tuesday, June 11, 2019

2:36 PM

-   Basic UAT Training

-   JIRA Training

-   Zephyr Training

-   Define Test Scope training

-   Create test Cases Training

 

 

 

 

Requirements

Tuesday, June 11, 2019

3:25 PM

Where are the Requirements?

What about the non-functional requirements?

How do the requirements relate to the acceptance criteria?

 

 

 

 

Jira Updates made in test

July 5, 2019

3:41 PM

-   Added/Updated Resolutions

-   Added Issue linking entry

>  

 

 

 

Resolutions

July 5, 2019

3:42 PM

  **Value**                      **Description**
  ------------------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Accidental Report              The reporter accidently submitted this report.
  Cannot Reproduce               All attempts at reproducing this issue failed, or not enough information was available to reproduce the issue. Reading the code produces no clues as to why this behavior would occur. If more information appears later, please reopen the issue.
  Done                           Work has been completed on this issue.
  Duplicate                      The problem is a duplicate of an existing issue.
  Fix Validated                  The fixed issue is validated by the reporter.
  Fixed                          Issue has been fixed.
  Obsolete                       Issue is no longer relevant.
  Reporter Misunderstanding      The reporter misunderstood the observed event as a defect.
  Test problem                   The system operates correctly, however there is a problem with the test (test case, test scripts, environment or test data).
  Training docs not referenced   User did not reference documentation.
  Training Gap                   Instructions not identified in training documentation.
  Will not fix                   Decision to not fix by Product Owner.
  Works as designed              The product actually works as intended.
  Won\'t Do                      This issue won\'t be actioned.

 

 

 

 

 

Priorities

July 8, 2019

11:54 AM

No changes

 

![Machine generated alternative text: Low Medium(Detault) urgent
](media/image7.png){width="1.382638888888889in"
height="1.1479166666666667in"}

 

 

 

Issue Linking

July 8, 2019

4:23 PM

  **Name**        **Outward Description**   **Inward Description**
  --------------- ------------------------- ------------------------
  **Blocks**      blocks                    is blocked by
  **Cloners**     clones                    is cloned by
  **Delivers**    delivers                  is delivered By
  **Duplicate**   duplicates                is duplicated by
  **Relates**     relates to                relates to
  **Tests**       tests                     is tested by

 

 

 

Repeatability

July 9, 2019

4:18 PM

New Custom field:

  Repeatability   One time occurrence
  --------------- ---------------------
  Repeatability   Intermittent
  Repeatability   Recurring
  Repeatability   Reproducible
  Repeatability   Unknown

>  

 

 

 

Symptoms

July 9, 2019

5:15 PM

+----------+--------------------------------------------------+
| Options: | -   **Application**                              |
|          |                                                  |
|          |     -   Incorrect error condition/state          |
|          |                                                  |
|          |     -   Incorrect operation                      |
|          |                                                  |
|          |     -   Job/Batch error/run instructions         |
|          |                                                  |
|          |     -   Printing incorrectly                     |
|          |                                                  |
|          |     -   Requirement, incorrect                   |
|          |                                                  |
|          |     -   Requirement, missing                     |
|          |                                                  |
|          |     -   Requirement, new                         |
|          |                                                  |
|          |     -   Requirement, omitted from Design/Product |
|          |                                                  |
|          |     -   Security violation                       |
|          |                                                  |
|          |     -   Slow performance                         |
|          |                                                  |
|          | -   **Database**                                 |
|          |                                                  |
|          |     -   Error                                    |
|          |                                                  |
|          |     -   File locking/contention                  |
|          |                                                  |
|          |     -   Data corruption                          |
|          |                                                  |
|          |     -   Data loss                                |
|          |                                                  |
|          | -   **General**                                  |
|          |                                                  |
|          |     -   Crash with data loss                     |
|          |                                                  |
|          |     -   Crash without data loss                  |
|          |                                                  |
|          |     -   Documentation, Spelling                  |
|          |                                                  |
|          |     -   Enhancement Request                      |
|          |                                                  |
|          |     -   General failure                          |
|          |                                                  |
|          |     -   Installation/deployment                  |
|          |                                                  |
|          | -   **Standards**                                |
|          |                                                  |
|          |     -   Compliance, BCGov UI                     |
|          |                                                  |
|          |     -   Compliance, iValua                       |
|          |                                                  |
|          |     -   Compliance, Web                          |
|          |                                                  |
|          |     -   Compliance, Windows                      |
|          |                                                  |
|          |     -   Compliance, Security Policy              |
|          |                                                  |
|          | -   **Usability**                                |
|          |                                                  |
|          |     -   Behaviour, unexpected                    |
|          |                                                  |
|          |     -   Behaviour, unfriendly                    |
|          |                                                  |
|          |     -   Navigation                               |
|          |                                                  |
|          |     -   Presentation                             |
|          |                                                  |
|          |     -   Spelling/Label                           |
|          |                                                  |
|          |     -   Wording, business/technical              |
|          |                                                  |
|          |     -   Wording, grammatical                     |
|          |                                                  |
|          | -   **Web**                                      |
|          |                                                  |
|          |     -   Broken Link                              |
|          |                                                  |
|          |     -   Misplaced element                        |
|          |                                                  |
|          |     -   Display issue                            |
|          |                                                  |
|          |     -   Browser incompatibility                  |
|          |                                                  |
|          |     -   Mobile browser incompatibility           |
+----------+--------------------------------------------------+

 

 

 

Showing 4 workflow actions

July 22, 2019

3:21 PM

Each transition to \"Triage\" should have the following property set:

**ops.bar.group.size.opsbar-transitions = 4 (In the transition
properties)**

 

 

 

 

 

Opsbar-sequence

July 22, 2019

3:23 PM

The opsbar-sequence is set for every set of transitions shown in the
page. This is done to show them in the correct (and most logical order)

 

The most important ranking in that one in Triage, as the original order
did not make sense.

 

 

 

Mapping status/resolution

August 13, 2019

3:19 PM

![Machine generated alternative text: \[881-145) TSL: What requirement C
Not secure X Statuses- Jira X Publish Workflows - - Minist X test. imb.j
ira.i m.gov .bc.ca/secure/project/SelectProjectWorkflowSchemeStep2!
default.jspa ?draftMig ration - -10503 Current Status 88G Bug Workflow
IN PROGRESS FIX NOW CLOSED - DO NOT FIX NOT REPRODUCIBLE WAITING FOR
MORE l\... USER FEEDBACK NEEDED FIXED(UNVERIFIED) FIXED(VERIFIED)
RELEASED IMPEDED DUPLICATE u ø o Administration Q Search admin
Applications Projects Issues ISSUE TYPES Issue types Issue type schemes
Sub-tasks WORKFLOWS Wo rkflows Workflow schemes SCREENS Screens Screen
schemes Issue type screen schemes FIELDS Custom fields Field
configurations Field configuration schemes PRIORITIES Priorities
Priority schemes ISSUE FEATURES Time tracking Issue linking ISSUE
ATTRIBUTES Statuses Resolutions Citz Defect Workfl\....xm Manage apps
User management Publish Workflows Latest upgrade report System
JiraSupport \[SUAJI! Step 1 of 2: The current status of each issue needs
to be changed so that it is compatible with the new workflows. Issue
Type Citz Default Workf\....xml New Status 8C81D Defect Workflow Fixing
Waiting for Fix Closed Closed Review Review Closed Closed Closed Waiting
for Fix Closed Associate Cancel Show all
](media/image8.png){width="20.0in" height="10.834722222222222in"}

 

 

 

 

Fixing Resolutions

August 13, 2019

4:40 PM

-   Add a new workflow step referring back to itself, and set the proper
    > resolution in the post actions

-   Query them all and do a bulk transition to the new step.

-   All resolutions will be set automatically.

-    

 

 

 

Introduction

Tuesday, June 11, 2019

3:26 PM

From:
<https://www.getzephyr.com/resources/whitepapers/how-behavior-driven-development-can-fuel-your-software-testing-program>

How Behavior Driven Development Can Fuel Your Software Testing Program
======================================================================

What is Behavior-Driven Development?
------------------------------------

The software development industry is flooded today with 'new ideas' that
are supposed to help make things better. Agile. Scrum. Test-Driven
Development. RAD. Many of these ideas are valuable and can improve your
development and testing process. With a market flooded with ideas, how
do you decide where to start? Many of these are complicated to
implement, call for retooling and culture change, and often the methods
to implement are unclear. What's so special about Behavior-Driven
development (BDD), and why is it worth your time

Behavior-Driven Development is, conceptually, a derivation of
Test-Driven Development. BDD was developed by Dan North, and it has been
around since the mid-2000s. Its goal is to [bring the most important
code and test cases to
focus](https://www.getzephyr.com/insights/difference-between-behavior-driven-design-and-test-driven-design).
It affects how you write requirements, how you write code, how you write
test cases, and how you test code. It also is designed to help bridge
the gap between non-technical people, attempting to write down what they
need, and technical people, attempting to build what the non-technical
people asked for.

All these promises sound like they require massive changes to achieve.
Let's walk through an example and see how big the impact will be to your
processes.

How Behavior-Driven Development works
-------------------------------------

#### *Implementing BDD is comprised of the following steps:*

1.  Change the structure of the sentences you use to write requirements
    > to follow a particular pattern

2.  Focus writing code to fulfill the criteria of the sentences

3.  Focus writing test cases on testing that the criteria of the
    > sentence is met

4.  Rejoice that things are more clear

#### *Sounds too good to be true, doesn't it?*

#### *In Behavior-Driven Development, you change your requirements to look more like this:*

**Title:** Give the story a clear title

**Narrative:** write a simple paragraph that states:

1.  Who is the primary user

```{=html}
<!-- -->
```
2.  What is the effect the user wants

```{=html}
<!-- -->
```
3.  What is the business value for the user

**Acceptance Criteria:**

Write as many acceptance criteria as you need to describe exactly what
needs to happen to satisfy the user. When you write them, write them in
the following format:

1.  Given \<this situation\>

```{=html}
<!-- -->
```
2.  When \<the user does this\>

```{=html}
<!-- -->
```
3.  Then \<this outcome occurs\>

![](media/image9.png){width="8.052083333333334in"
height="2.2784722222222222in"}

Old School
----------

 

![](media/image10.png){width="8.852083333333333in"
height="2.5131944444444443in"}

New School
----------

That's primary change called for in what you do today. By changing how
you think about acceptance criteria and writing them in this format, you
construct how you state your problems more like how the developer solves
the problem in code, and more like how the QA tester builds test cases.
The most likely way to solve the problem is obvious, and the way the
product must work is also more obvious.

Software development and Testing gain the immediate ability to identify
and focus on what code and tests must be built first and are most
important. [Developers and
QA](https://www.getzephyr.com/insights/live-webinar-getting-dev-qa-work-better-together)
can also flag their code and tests with direct references to the section
of each acceptance criteria it addresses by adding comments that copy
and paste from the acceptance criteria. Now your code and test cases are
searchable based on each requirement and section of requirement. You
have direct traceability from requirement to code to test case, which
reduces cost for future changes and for defect resolution.

A typical Agile Shop
--------------------

Let's walk through an example at a typical Agile Development shop. The
shop is using off-the-shelf software to run their Agile process. They
have the typical roles- Business Analyst, Developer, and Quality
Assurance. A 'Green' initiative in the company has led to more effort to
recycle consumables, reconditioning them and returning them to
inventory, rather than simply throw them all away. The items can be
recycled once before they go bad and must be thrown away permanently.
The system needs new features to support this new initiative. The
software development team is called together, holds a meeting with the
product owner, listens to the software problem, talks it over, and then
sets about their tasks.

![](media/image11.png){width="7.321527777777778in"
height="4.626388888888889in"}

#### *First, the business analyst writes up the user story. He creates the story itself:*

*As an Inventory Manager, I want to be able to add recycled items back
into inventory, so that I can reuse them.*

#### *Next, he outlines the functional needs:*

1.  A method is needed to add recycled items back into inventory to be
    > used again.

```{=html}
<!-- -->
```
2.  A method is needed to identify recycled inventory so that it is not
    > reused again.

#### *After that, he outlines some business rules:*

1.  Consumable inventory items may be recycled and added back into
    > inventory.

```{=html}
<!-- -->
```
2.  A recycled item may only be added back once. It must be disposed of
    > after the second use.

```{=html}
<!-- -->
```
3.  Non-consumable inventory is not recycled and is not considered for
    > this story.

#### *Next, he outlines some acceptance criteria:*

1.  There must be a way to add consumable inventory back into inventory
    > as a recycled item.

```{=html}
<!-- -->
```
2.  There must be a way to identify recycled consumable items in
    > inventory.

```{=html}
<!-- -->
```
3.  Recycled inventory, once removed to be used, may not be added back
    > into inventory.

```{=html}
<!-- -->
```
4.  Non-consumable inventory may not be added back as recycled
    > inventory.

The developer now looks through this documentation. It accurately
describes the problem, but the developer is left with where to start.
She decides to start with data first. The system already has flags for
consumable inventory and permanent inventory, so she adds a flag for
recycled and modifies the user interface to handle the new flag.

Next, she starts designing changes to the add inventory function. She
adds the ability for the user to indicate if a consumable being added to
inventory is a recycled item or not. She adds the ability to indicate
how many times the item has been recycled. She adds error messages if
the item is recycled more than once. She adds error handling to prevent
a non-consumable from being flagged as recycled, even though it
shouldn't be possible, to make sure her code handles all the acceptance
criteria cleanly and has good coverage of possible permutations. All
this ends up affecting a lot of screens, as the recycled flag must be
handled wherever a user can add, view, edit or delete inventory.

#### *The QA Analyst looks through the story and builds test cases, including:*

1.  Trying to add a recycled item

```{=html}
<!-- -->
```
2.  Trying to add a recycled non-consumable

```{=html}
<!-- -->
```
3.  Trying to add a recycled item back into inventory

```{=html}
<!-- -->
```
4.  Trying to remove a recycled item from inventory

```{=html}
<!-- -->
```
5.  Trying to change a consumable into a recycled item in inventory edit
    > screens

The team completes the code in a few weeks. It goes to production and
things are fine for a while. Four months later, a lot of new features
have been added that depend on the recycled product feature. A bug shows
up that somehow allows recycled items to be added back into inventory as
a regular consumable. QA looks through their test cases and cannot find
a test case for that. The Business Analyst can't find the business rule
specific to that. Development starts picking through code. Everyone on
the team understands the problem and knows it shouldn't happen, but they
aren't sure why they made the design decisions they made. Eventually,
it's traced to a problem with the recycled flag. No one is sure why they
chose to go with a flag, but it meets the requirements and test cases.
The BA documentation, the QA test cases, nor the code comments line up
cleanly, so it's hard to say exactly what went wrong with their logic
process originally. On top of that, the lack of line-up of everything
makes it difficult to identify all of the implications of changing how
the flag behaves. The group hunkers down for a round of analysis,
repeating old research, to solve the problem.

The Business Analyst may very well go on and develop all of the other
documentation that happened at the Agile shop -- calling out a list of
business rules, for example, or functional requirements. Under BDD,
however, the [Acceptance Criteria is the key
driver](https://www.getzephyr.com/insights/business-driven-development-it-systems-satisfy-business-needs)
to what everyone does. When the Business Analyst has finished work he
passes the card for the story on to the Developer. When the Developer
opens the card, the acceptance criteria make the desired end result
obvious. It can be read as a single, clear sentence, but note what
breaking it up into lines does:

1.  Each part of what you want to happen is discrete and easy to
    > understand

```{=html}
<!-- -->
```
2.  Each line effectively translates to a single chunk of code

```{=html}
<!-- -->
```
3.  Each line effectively translates into a testable criteria, so
    > writing test cases is easy

She looks at the user's two steps: the user enters a product number. The
product is not a recycled product. The developer modifies adding new
product numbers to inventory so that when a new consumable type is
created, a second product number is also created that ends in --R.
Inventory that ends in --R is recycled inventory. She adds code comments
"the system adds the consumable to inventory as a recycled product" and
"the product is NOT a non-consumable product".

A BDD Shop
----------

In a software shop across town, an Agile shop has implemented
Behavior-Driven Development. They are still using the same tools as the
other shop, but they now [use BDD to drive how they write
requirements](https://www.getzephyr.com/insights/steps-creating-quality-product-business-driven-development-testing-part-ii).

When the same requirement comes up for recycled items in their shop,
they meet, discuss requirements, and the Business Analyst begins by
writing the following:

#### *First, he gives the story a title.*

**Title:** Add Recycled Products to Inventory

#### *Next, he writes a simple narrative of what's trying to be solved.*

**Narrative:** Users need a method to add recycled consumables back into
inventory. Products may only be recycled once. Users need to be able to
tell a recycled item from a regular item.

#### *Next, the business analyst writes the acceptance criteria in BDD format:*

**Acceptance Criteria:**

**Criteria 1:**

Given that a user needs to add a consumable to inventory when the user
enters the product number and the product is NOT a recycled product and
the product is NOT a non-consumable product then the system adds the
consumable to inventory to as a recycled product.

She next modifies the add consumables feature so that the user is to
enter the current product number and the number to be added to
inventory. If the current product number doesn't end in --R, then the
inventory is added to the --R product number. Now it's recycled
inventory. She again adds code comments "the system adds the consumable
to inventory as a recycled product".

If the current product number ends in --R, then the system will know
it's recycled inventory, and gives the user an error, telling them that
recycled inventory cannot be used again, and giving instructions for
disposal of the inventory. She adds comments "The product is NOT a
recycled product".

#### *The QA Analyst builds the following test case immediately:*

1.  Try to add inventory to system. Enter product number that is not for
    > a recycled product.

```{=html}
<!-- -->
```
2.  Try to add inventory to system. Enter product number that is for a
    > non-consumable product.

```{=html}
<!-- -->
```
3.  Try to add inventory to system. Enter product number that is for a
    > recycled product.

He adds to the first test case the comment "the user enters a product
number and the product is NOT a recycled product". To the second, he
adds the comment "and the product is NOT a non-consumable product". To
the third, he adds "then the system adds the consumable to inventory as
a recycled product".

Suddenly, your Business Analysts, Developers and Quality Assurance all
speak the same language. There are many things you can test about the
code above, but the most important test is clearly the one that aligns
with Criteria 1. If your solution doesn't meet this test, you shouldn't
release. Getting from development complete to tested and
production-ready becomes a much shorter path. If a bug appears four
months later for this team, they identify what the bug applies to, for
example, adding recycled products, and they can immediately do a text
search and find the acceptance criteria for it, the code for it, and the
test cases. It takes minutes to achieve traceability and start
diagnosing the problem.

Note also how the construction of the acceptance criteria leads both the
developer and the QA analyst to different solutions than before. The
developer constructs their solution differently, that takes on the
problem directly, and is likely cheaper to build. The QA analyst
immediately jumps to the most important test cases. They can see what
the must-do criteria are immediately. They will write additional test
cases, of course, but the key tests stand out.

Implementation
--------------

Implementation of Behavior-Driven Development is straightforward. First,
there's a period of training for your people involved in your
requirements documentation- whether you're doing Agile, Waterfall, or
something else, this approach will work. It's a simple redefinition of
[how you write acceptance
criteria](https://www.getzephyr.com/insights/relationship-between-behavior-driven-development-and-api-design),
not a radical alteration to process.

Second, you must communicate the changes to your developers and [QA
teams](https://www.getzephyr.com/resources/case-studies/building-hyper-productive-globally-distributed-qa-teams).
Work with them to educate them on what the change will be, and how to
read and interpret the new method of documentation. Plan how you will
incorporate this into your code and test case documentation. You don't
want to ruin the traceability that BDD offers by failing to set
standards around how you will document it.

After that, you set a date, and start. It's best to start with a single
project and single release, to pilot the process first. Establish some
metrics before you start- were requirements faster or slower to
document? What about code? Testing? Were defects reduced? Explore your
existing metrics and set up some measurable to make sure that the
changes work for you.

Another attractive aspect of this is that if it somehow fails to meet
your needs, it's easy to undo. You go back to writing requirements the
old way. No retooling. No big process rewrites. No retraining. Just
write sentences the way you used to do it. Both the cost and risk is
very low with BDD compared to many other methodologies out there.

Adopting Behavior-Driven Development is very straightforward. It calls
for changes to how requirements are written and holding some educational
meetings with your teams, but it does not mean retooling, major process
change, or culture shift. Risk of implementing is very low, since it can
be removed very easily. Behavior-Driven Development is a worthwhile
practice for any software shop to at least evaluate and try, and it has
the potential to have big benefits to your development and software

 

 

 

 

Common Gherkin Syntax

Tuesday, June 11, 2019

3:33 PM

Common gherkin syntax
---------------------

 

**We\'ll need to map this to our internal terminology!**

Like YAML or Python, Gherkin is a line-oriented language that uses
indentation to define structure. Line endings terminate statements
(called steps) and either spaces or tabs may be used for indentation.
(We suggest you use spaces for portability.) Finally, most lines in
Gherkin start with a special keyword:

**Feature:** Some terse yet descriptive text of what is desired\
In order to realize a named business value\
As an explicit system actor\
I want to gain some beneficial outcome which furthers the goal

 

**Scenario:** Some determinable business situation

 

**Given** some precondition

**And** some other precondition

**When** some action by the actor

> **And** some other action
>
> **And** yet another action

**Then** some testable outcome is achieved

**And** something else we can check happens too

 

**Scenario:** A different situation\
\...

The parser divides the input into features, scenarios and steps. Let's
walk through the above example:

1.  Feature: Some terse yet descriptive text of what is desired starts
    > the feature and gives it a title. Learn more about features in the
    > "[Features](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#features)"
    > section.

2.  Behat does not parse the next 3 lines of text. (In order to\... As
    > an\... I want to\...). These lines simply provide context to the
    > people reading your feature, and describe the business value
    > derived from the inclusion of the feature in your software.

3.  Scenario: Some determinable business situation starts the scenario,
    > and contains a description of the scenario. Learn more about
    > scenarios in the
    > "[Scenarios](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#scenarios)"
    > section.

4.  The next 7 lines are the scenario steps, each of which is matched to
    > a regular expression defined elsewhere. Learn more about steps in
    > the
    > "[Steps](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#steps)"
    > section.

5.  Scenario: A different situation starts the next scenario, and so on.

When you're executing the feature, the trailing portion of each step
(after keywords like Given, And, When, etc) is matched to a regular
expression, which executes a PHP callback function. You can read more
about steps matching and execution in *[Defining Reusable Actions - Step
Definitions](http://docs.behat.org/en/v2.5/guides/2.definitions.html).*

features
--------

Every \*.feature file conventionally consists of a single feature. Lines
starting with the keyword Feature: (or its localized equivalent)
followed by three indented lines starts a feature. A feature usually
contains a list of scenarios. You can write whatever you want up until
the first scenario, which starts with Scenario: (or localized
equivalent) on a new line. You can use
[tags](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#tags) to
group features and scenarios together, independent of your file and
directory structure.

Every scenario consists of a list of
[steps](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#steps),
which must start with one of the keywords Given, When, Then, But or And
(or localized one). Behat treats them all the same, but you shouldn't.
Here is an example:

**Feature:** Serve coffee\
In order to earn money\
Customers should be able to\
buy coffee at all times

 

**Scenario:** Buy last coffee

 

**Given** there are 1 coffees left in the machine

**And** I have deposited 1 dollar

**When** I press the coffee button

**Then** I should be served a coffee

In addition to basic
[scenarios](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#scenarios),
feature may contain [scenario
outlines](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#scenario-outlines)
and
[backgrounds](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#backgrounds).

scenarios
---------

Scenario is one of the core Gherkin structures. Every scenario starts
with the Scenario: keyword (or localized one), followed by an optional
scenario title. Each feature can have one or more scenarios, and every
scenario consists of one or more
[steps](http://docs.behat.org/en/v2.5/guides/1.gherkin.html#steps).

The following scenarios each have 3 steps:

**Scenario:** Wilson posts to his own blog

 

**Given** I am logged in as Wilson

**When** I try to post to \"Expensive Therapy\"

**Then** I should see \"Your article was published.\"

 

**Scenario:** Wilson fails to post to somebody else\'s blog

**Given** I am logged in as Wilson

**When** I try to post to \"Greg\'s anti-tax rants\"

**Then** I should see \"Hey! That\'s not your blog!\"

 

**Scenario:** Greg posts to a client\'s blog

**Given** I am logged in as Greg

**When** I try to post to \"Expensive Therapy\"

**Then** I should see \"Your article was published.\"

 

 

 

 

 

PPR Gherkin Syntax

Tuesday, June 11, 2019

3:46 PM

Starting with the common syntax as shown in the previous page:

 

**Feature:** Some terse yet descriptive text of what is desired\
In order to realize a named business value\
As an explicit system actor\
I want to gain some beneficial outcome which furthers the goal\
\
**Scenario:** Some determinable business situation

**Given** some precondition\
**And** some other precondition\
**When** some action by the actor\
**And** some other action\
**And** yet another action\
**Then** some testable outcome is achieved\
**And** something else we can check happens too

We\'ll have to describe as follows in Jira (No worries it is all the
same, simply different names)

 

**Story Summary:** Some terse yet descriptive text of what is desired\
In order to realize a named business value

**Story Description:**

As an explicit system actor\
I want to gain some beneficial outcome which furthers the goal

**Acceptance Criterion Summary:** Some determinable business situation

**Acceptance Criterion Description:**

**Given** some precondition\
**And** some other precondition\
**When** some action by the actor\
**And** some other action\
**And** yet another action\
**Then** some testable outcome is achieved\
**And** something else we can check happens too

 

 

 

 

 

 

 

 

 

Testing Handover with James

July 10, 2019

3:01 PM

Hi James,

 

Let's talk about the handover of the testing work.

Potential topics:

-   What was done

-   Your reporting

-   Your daily testing related activities

-   The challenges

-   Stuff you found out that really helped you do this

-   Etc.

 

Late hiring of me.

 

-   No w Zephyr set up

-   No documenting testing

-   Confidence sheet

-   Maybe implement in Jira

 

Test

-   Design documents

-   All the work done before

-   Broke it down by deliverables

-   The deliverables were part of what we wanted to test

-   Just test everything because of potential issue with quality

-   BBB the user stories

-   BBB -\> what into pilot - Pilot field indicated

-   Mainly done by Vivek and Audra

-   End-to-end testing part of work package

-   Validate against requirement in BBB

-   Most of them where covered some deferred

-   Zephyr - Create a test case for every BBB item - seemed impossible

-   Broke up the workflow in 3-4 major test cases

-   Tc were assigned and defects found

-   The concept of test cases were going away (more exploratory Testing)

-   CGI deems the project team as the users

-   Need to make a picture

 

Reporting

-   Some stats and dashboard

-   Test Status

-   Defect burn down

-   Defect triage

-   Takes Vivek\'s meeting

-   Definition of done for testing

 

Daily Routine

-   Dashboard - 4 widgets

    -   Pie chart, status

    -   Use cases validations -

    -   Looking what was developed

    -   Looking at the activity stream -

    -   Assigned to me

>  
>
>  
>
>  
>
>  

 

>  
>
>  

 

 

 

Build and Deployment Processes

July 11, 2019

12:57 PM

Deb:

-   Make sure that all knows that deployment is up

-   Env. Stable

-   Prior: Validation test - Running sourcing event end-to-end

-   2 deployment resources

-   J,M and Deb do validation

-   Deployment creates \"Tag\" ivalua deployment package

-   Then into dev env. (2 dev environments? 1 for development, 1 for
    > maintenance prod aligned. (hot fixes))

-   If tag deployed correctly

-   The deploy into test

-   Tags get version numbers

-   Rollbacks are possible - by iValua

-   Is tag number visible in front-end? V in bar

-   Scope of changes will not contain \"content\"

-   They need to be manually moved - time needed dependent on what needs
    > to move

-   Are there any completely manual steps? Yes but not very many

-   Then a validation test again in the target environment.

-   Then we\'ll deploy to training. We\'ll keep that until test is
    > released.

-   Deb is checking if a set up can be stored for restore later.
    > (Training)

-   iValua rolls out in prod

-   Discussion needed between Pascal and Tlel for hot fix updates, who
    > does what.

-   New version from iValua - documented in .... (PMP?)

>  
>
>  

![](media/image12.png){width="10.64375in" height="7.582638888888889in"}

 

 

 

Transition Notes

October 22, 2019

2:04 PM

Defect Management
=================

I believe we have a rhythm and we have become efficient in addressing
issues.

Key players moving this forward are:

-   James

-   Jason

-   Deb

James and Jason could lead the reviews as they are already the most
active.

An additional thought could be to have either Kim or Marisa run the
review sessions. This might be a good idea as it will relieve James and
Jason from having to set up and be available.

 

Deb will, independently from the meetings, pick up \"low hanging fruit\"
items from the triage list and forward them into her workflow. We need
to take care of keeping the triage meeting as regularly as our initial
review meetings and things pile up rather quickly.

 

I think Defect management is the least of our worries. The current
sessions need to be set up by somebody else when I leave as links with
become invalid.

 

Exploratory Testing by the BAs
==============================

All the sessions are planned out and available in Jira. Testing by the
BAs is happening but not in a way that let\'s us monitor progress. In
other words the facilities in Jira are not used to (even after urging to
do so) track progress and test results. Testing is on people\'s list but
I have no ideas what has been done and what is still out there to be
done.

 

Blocks of time were reserved and user stories were created for the Bas.
But workload and priorities often do not allow for the blocked time to
be consumed in the intended fashion.

 

Given the overall workload and testing becoming under pressure, it would
make sense to set up a dedicated test team that takes care of the test
activities in a consistent fashion showing actual progress. The business
testers do not deliver that kind of rigor and are not a replacement for
full time testers. I believe that 3-4 testers focused could fully test
and validate the solution against the requirements and stated
contractual obligations. If such a set up is not possible, then I\'d
imagine that the solution will eventually go live in a very uncertain
state.

 

User Story/Requirement Validation and Testing
=============================================

All user stories have been added as tests and would require individual
validation and they represent contractual obligations. None of these
have been executed or any detail test design has happened on them. Next
week I\'ll go through them with the UAT folks to see if we can get a
preliminary idea on what we can endorse and which ones are unproven.
That will give us more guidance going toward January.

 

With almost 250 user stories, additional requirements this is
non-trivial effort that would take a test team months to go through.

 

User Acceptance Testing
=======================

Due to resource availability both early enough in the calendar and
actual availability per day/week, we have arrived at a very ad hoc,
freeform of UAT that so far has yielded quite a few observations. Once
the testers are on the job, they are quite serious about it, but given
the state of the application, the lack of doing any planning with them
(UAT is owned by the business) we are adding value albeit not the level
of value that would typically be required for such an important
application.

 

Saving grace is that I\'d consider this UAT as the \"trial\" UAT where
people are getting familiar with the application and get trained on its
use.

 

As UAT is owned by the business, I would shy away from giving them step
by step guidance on what they need to do. The typical process is that
they would get a high level overview and then from there they will bring
their objectives to the table and we pull those together in a plan for
UAT. The current group looks at me to tell them on a day to day basis
what to do, this has as a side effect that that can cause \"Well, we
were never told to do this.\"

I realize now that there is very limited to no experience with doing UAT
in this organization and that the usability sessions are almost seen as
quiet enough.

 

The availability for individuals in the planned sessions is about 80%,
we have one person who has not shown up for any work session. 2 others
have only been there for 50% of the planned sessions (which are about
50% of their total work time).

 

Going forward
-------------

I\'d suggest to create high level scenarios and variation\'s on the
scenarios for future UAT sessions. This will give us better tracking on
progress. I have the current group doing that by asking them to find
examples of small, medium and large previous RFP (ITQ and RFI) and then
replay the creation, validation, publishing, bidding, closing,
evaluation and awarding process inside PPR. We are on track to do that.

 

During UAT we would need somebody in the room/online to keep the
momentum going. The presence of Jason during the last sessions was
beneficial as well. I would be great if PSB could second/appoint an UAT
lead who takes responsibility for the work performed by the business
users.

 

Materials
=========

On SharePoint I have training materials and the main OneNote document
with the strategy and plan (only up to October 31th).

There are also some videos (unlisted on youtube, I have the link on SP).

The materials and videos can be used for onboarding new people.
