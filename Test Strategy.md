# Test Strategy

## Early Plan
Given the assignments primary requirements is developing with left testing mindset, we take this as our main pillar for our test strategy,
to furfill this we will focus on using Gherkin syntax for our initial user stories and acceptance criterias, while also
implementing test first principles for the assignment through the use of cucumber that can implement said Gherkin syntax quaries.   

Our primary focus of the testing quadrant will be on the Q2 "automated and manual" given our focus on early story tests,
our intend is to implement the user stories and then use cucumber to make unit tests that run on mockable features, cucumber also allows
us to dig into manually setting up scenarios that are harder to implement as boundary or state diagrams.

## Understanding Requirements:
• Requirement specifications will be specified by our product owner(tine and helge) + our own proxy product owner   

• Understanding of requirements will be done by everyone on the team

## Preparing Test Cases:
The team will be preparing test cases based on the Scenarios given by the product owners (type of end-user quaries). 
This will cover all requirements

## Creating Test Data:   
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

## Deployment/Delivery:
• Once all bugs/defect reported after complete testing is fixed and no other bugs are found,
report will be deployed to staging environment by the Continues Integration platform.   

• Once build is in staging environment proxy product owner.   

• Once Product owner accepts staging environment, the build will be deployed to production.

## Testing types
- Black box testing:   

- White box testing:   

- GUI Testing:   

- Integration Testing:   

## Test Plan
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
