# Test Report
> by Kristian, Daniel, Edmund

## Table of Content
1. Summary
  - Introduction
  - Requirements Analysis Document
2. Initial Design Sprint
  - The Initial Conditions
  - The Data
  - Test Strategy
  - End of Initial Sprint
3. Main Development Sprint
  - The Product
  - Left Shift Testing
  - Inclusion of Gherkin and Cucumber
    - Acceptance Criteria
  - End of Main Sprint
4. Last Sprint
  - Report
  - Refactoring
  - End of Last Sprint
5. Conclusion

## 1. Summary
###  - Introduction
This report is the documentation of our work on the final assignment in the summer semester of 2018 software development course,
this report will focus on the testing part of the assignment which is specified 
[here.](https://github.com/datsoftlyngby/soft2018spring-test-teaching-material/blob/master/exercises/Final%20Assignment%202018.pdf)   
The short summary is that we're to follow the final database assignment, while incorperating as many testing strategies as possible,
as the main focus on the testing part is to work as a agile team, following the agile principles and using ATTD, TTD and the likes.
The main goal is to setup the product for continous itegration and delivery pipeline, so it's possible
for the product to evolve in the proposed time of Q3 2018 following the following projection. 
![](https://www.praqma.com/images/stories/code-storyline/storyline.jpg)
###  - Requirements Analysis Document
 1. Purpose of the system   
  The system allows users access to multiple databases containing data related to the Project Gutenberg described [here](http://www.gutenberg.org/), allowing for multitude of data request through a web interface.
  
  2. Scope of the system   
  The system needs to allow the user to ask a multitude of simple commands, where the system will handle said commands using all english written books from the Project Gutenberg, the system will also contain related data about cities to handle some of the simple commands the user may ask.
  
  3. Objectives and success criteria of the project   
  The system must be able to handle all the commands using any of the databases it has, aswell as handling said commands in a optimal time that allows for human reactionary use.
  
  4. Definitions, acronyms, and abbreviations   
  the term commands are the reader friendly version of database queries, given the system will both handle sequential query language based database and graph based database, we choose to simply use commands as a broad term.   
  when mentioning the system we mean the full product, both databases, API and user interface for reduction of redundancy, specification will be used on a moment to moment basis.
  
  5. References   
  [Database Assignment paper](https://github.com/datsoftlyngby/soft2018spring-databases-teaching-material/blob/master/assignments/Project%20Description.ipynb)   
  [Test assignment paper](https://github.com/datsoftlyngby/soft2018spring-test-teaching-material/blob/master/exercises/Final%20Assignment%202018.pdf)
  
  6. Overview   
  The System will be a server based system that allows users to access the systems databases through the use of a web browser, the web browser will present predetermined commands that can be filled out with information from the user, which then will be handled by the API using the database to return a answer to the users command.

#### Functional requirements
The product must support atleast 2 different databases with two different paradigms.   
The product must also allow the end user to execute at minimum the following commands:   
1. Given a city name your application returns all book titles with corresponding authors that mention this city.   
2. Given a book title, your application plots all cities mentioned in this book onto a map.   
3. Given an author name your application lists all books written by that author and plots all cities mentioned in any of the books onto a map.   
4. Given a geolocation, your application lists all books mentioning a city in vicinity of the given geolocation.   
The Database must all at minimum contain the Author's name, the books title, names of cities, the geolocations of said cities and thier occurences in test, aswell as any other relevant information that is needed.   

The product must be able to handle queries with at least five queries per type, see section above. That is, in total the end-user query test set contains at least 20 queries.

#### Nonfunctional requirements
1. Usability   
The system should have a base UI that allows for user with limited exposure to programming to execute the commands of thier desire.

2. Reliability   
The system may not crash doing any queries.

3. Performance   
The system must handle each query on a case by case basis as fast as possible, but must never exceed 10 seconds duration for the user to see results from the given command.

4. Supportability   
The system must allow use through popular web browsers like chrome, firefox or safari.

5. Implementation   


6. Interface   
The system requires a REST API that handles the implementation between database and Web UI.

7. Packaging   
No Packing(physical) requirements.

8. Legal   
No legal requirements.
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
###  - The Product
At the start of the main product
###  - Left Shift Testing
As our main sprint went into effect, we found ourself focusing on both loosely upholding left shift testing guidelines while managing
the enomous amount of data we had to process, but we choose to trust in eachothers ability to document and uphold agile test standards,
so that we could focus on getting the data handled, in retrospect it would have been wiser to start production of the main part of the projec
###  - Inclusion of Gherkin and Cucumber

####  - Acceptance Criteria
```
Date: 29/04/2018
```

#### Introduction
In regards  to our final test assignment this semester, and in response to the requirement of acceptance criterias for the first review   session with Tine, we have developed some user stories based on the requirements of the assignment description, and we have based our acceptance criterias on these user stories.

##### User stories

######  User story 1:
"As a user, I want to enter a city, and the application returns all book titles with with corresponding authors, that mentions this specific city, so that I can find the book that I want to read."

###### Acceptance criteria:
```
Given a user picks copenhagen as a city
When the user ask for all book titles with corresponding authors that is mentioned in copenhagen
Then the user will get all books with corresponding authors that is mentioned in copenhagen
```

###### User story 2:
As a user, i want to enter a book title, and the application plots all cities mentioned in this book onto a map, so that I can get a visualization of books onto the map.

###### Acceptance Criteria:
```
Given a user gives a book title "Salute to Adventurers"
When the user ask for all cities mentioned in that book
And the user ask for all those cities plotted on a map
Then the user will get a map with all cities mentioned in the book plotted on that map.
```

###### User story 3:
As a user, i want to enter an authors name and get all books by that author and a map of with plots of all cities mentioned in any of the books so that i can find a book that i want to read.

###### Acceptance Criteria:
```
Given a User gives a author name "William Shakespeare"
When the user ask for all books by that author
And the user ask for all cities mentioned in those books
And the user ask for all those cities plotted on a map
Then the user will get a map with all cities mentioned in those books plotted on that map.
```


###### User story 4:

As a user, i want to give a location and get all books which mentions a city in the vicinity of that location, so i can find a book that i want to read.

###### Acceptance Criteria:
```
Given a User gives a location "10,30"
When the user ask for all books that mentions cities near that location
Then the user gets all books mentioning a city near that location
```

###  - End of Main Sprint
## 4. Last Sprint
###  - Report
###  - Refactoring
###  - End of Last Sprint
## 5. Conclusion
