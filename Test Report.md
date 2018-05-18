# Test Report
> by Kristian, Daniel, Edmund

## Table of Content
1. Summary
  - Introduction
  - The Task
2. Initial Design Sprint
  - The Initial Conditions
  - The Data
  - Test Strategy
  - End of Initial Sprint
3. Main Development Sprint
  - Left Shift Testing
  - Inclusion of Gherkin and Cucumber
  - End of Main Sprint
4. Last Sprint
  - Report
  - Refactoring
  - End of Last Sprint
5. Conclusion

## 1. Summary
###  - Introduction
This report is the dokumentation of our work on the final assignment in the summer semester of 2018 software development course,
this report will focus on the testing part of the assignment which is specified 
[here.](https://github.com/datsoftlyngby/soft2018spring-test-teaching-material/blob/master/exercises/Final%20Assignment%202018.pdf)   
The short summary is that we're to follow the final database assignment, while incorperating as many testing strategies as possible,
as the main focus on the testing part is to work as a agile team, following the agile principles and using ATTD, TTD and the likes.
###  - The Task
the task is to work on the assignment in a agile team, that is able to change and adapt as the product owner changes requirements doing
the timetable of the assignment. The main goal is to setup the product for continous itegration and delivery pipeline, so it's possible
for the product to evolve in the proposed time of Q3 2018 following the following projection. 
![](https://www.praqma.com/images/stories/code-storyline/storyline.jpg)
## 2. Initial Design Sprint
###  - The Initial Conditions
Doing our introduction to the project, we noted that we were to focus on documenting our initial draft of test strategies, 
yet we found ourself pressed for time, given we were assigned three other projects
as the main project started, this resulted in us choosing to focus on those assignment primarily to ensure that the remaining time
could be focused entirely on this project.
###  - The Data
Given we had our hands full, we identified early on the biggest problem with the project was the data, we were tasked with aquiring and processing a very large amount of data from the gutenberg project shown [here](http://www.gutenberg.org/), we were initially told
the data would take around 36 hours to fully aquire, and this is not taking into account the amount of time it would take to process said data. As mentioned earlier we choose to put the project on hold but we made sure to focus on aquiring and processing the data above all else, which in retrospect was a kneejerk reaction to the initial time table.
###  - Test Strategy

#### Early Plan
Given the assignments primary requirements is developing with left testing mindset, we take this as our main pillar for our test strategy,
to furfill this we will focus on using Gherkin syntax for our initial user stories and acceptance criterias, while also
implementing test first principles for the assignment through the use of cucumber that can implement said Gherkin syntax quaries.   

Our primary focus of the testing quadrant will be on the Q2 "automated and manual" given our focus on early story tests,
our intend is to implement the user stories and then use cucumber to make unit tests that run on mockable features, cucumber also allows
us to dig into manually setting up scenarios that are harder to implement as boundary or state diagrams.

#### Understanding Requirements:
• Requirement specifications will be specified by our product owner(tine and helge) + our own proxy product owner   

• Understanding of requirements will be done by everyone on the team

#### Preparing Test Cases:
The team will be preparing test cases based on the Scenarios given by the product owners (type of end-user quaries). 
This will cover all requirements

#### Creating Test Data:   
Test data will be created by respective team member who's responsible for said database based on scenarios and Test cases.   
- **Executing Test Cases:**   

• Test cases will be executed by Continues Integration platform of the teams choice based on 
designed scenarios, test cases and Test data.   

• Test result (Actual Result, Pass/Fail) will updated in chosen Continues Integration platform and Reporting:   
Continues Integration platform will be logging the defect/bugs in build status, found during execution of test
cases. After this, Continues Integration platform will inform respective developer about the defect/bugs.   

- **Retesting and Regression Testing:**   
Retesting for fixed bugs will be done by the Continues Integration platform once it is resolved by respective
developer and bug/defect status will be updated accordingly.

#### Deployment/Delivery:
• Once all bugs/defect reported after complete testing is fixed and no other bugs are found,
report will be deployed to staging environment by the Continues Integration platform.   

• Once build is in staging environment proxy product owner.   

• Once Product owner accepts staging environment, the build will be deployed to production.

#### Testing types
- Black box testing:   

- White box testing:   

- GUI Testing:   

- Integration Testing:   

#### Test Plan
- **Functional Testing:**   
Functional testing will be covered through the use of automated black box unit tests to ensure the primary requirements are meet.   
- **System Testing:**   
System testing will be done with integration through the use of black box tests.   
- **Performance Testing:**   
Check the response time is below 1 second   
- **User acceptance testing:**   
acceptance criteria will be tested though the use of automated cucumber tests.   
- **Alpha testing:**   
The alpha test is conducted at the developer's site by proxy product owner.

###  - End of Initial Sprint
At the end of our initial sprint we had cleared out our current time obstacles of the project, we initially tried to log our efforts doing this time, but found little time to go into a habit of logging our meetings, we also found this highly redundant as the projects requirements and the situation would change on a daylie basis, so past writings became obsolete rather quickly in the agile development.
At this time one of our 4 members had left our group, and our perceived timetable narrowed down further as we hurried to adapt to
the new circumstances, it was at this time we realised we havn't figure out much in terms of business testing, other than left shift testing.
## 3. Main Development Sprint
###  - Left Shift Testing
###  - Inclusion of Gherkin and Cucumber
###  - End of Main Sprint
## 4. Last Sprint
###  - Report
###  - Refactoring
###  - End of Last Sprint
## 5. Conclusion
