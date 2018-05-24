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
  - Continouse Integration & Delivery
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
The system must handle each query on a case by case basis as fast as possible, but must never exceed 2 seconds duration for the user to see results from the given command.

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
Check the response time is below 2 second   
- **User acceptance testing:**   
acceptance criteria will be tested though the use of automated cucumber tests.   
- **Alpha testing:**   
The alpha test is conducted at the developer's site by proxy product owner.

###  - End of Initial Sprint
At the end of our initial sprint we had cleared out our current time obstacles of the project, we initially tried to log our efforts doing this time, but found little time to go into a habit of logging our meetings, we also found this highly redundant as the projects requirements and the situation would change on a daylie basis, so past writings became obsolete rather quickly in the agile development.
At this time one of our 4 members had left our group, and our perceived timetable narrowed down further as we hurried to adapt to
the new circumstances, it was at this time we realised with the use of our burndown chart from [Waffle.io](https://waffle.io/) that we were behind schedule as seen in our two minor test review sprints   
"note that test review 1 is faulty and the two last where done but it's still 1 day behind"   
![](https://i.gyazo.com/b19ec1bd7e0e7b2918b1a4c99cec9fd7.png)   
![](https://i.gyazo.com/49fd3de81560e78a5c8a4438d24cefac.png)   
we also had a overall project deadline, where we assigned the rest of our task on, our deadline for delivery on test was on the 25th
and database was on the 28th, we choose to say the total final deadline was on the 24th to ensure adaptability at the last stretch
incase of unforseen events.   
![](https://i.gyazo.com/e685f66a9568c04f268cd3f0c6ae1fd3.png)   
With this overview we found out, that we havn't gotten much documentation or plans in terms of business testing, other than left shift testing.
## 3. Main Development Sprint
###  - The Product
At the start of the main sprint we had the system design ready, for a short introduction the system consist of 3 parts, a frontend web client, that allows the product owner to interact with the product, a backend API that handles the web clients requests and calls the databases for the request data, and the databases that consist of multiple different database which was required by the database course.

#### API
##### Functionality:
This api's functionality is to link the frontend with the database. This api will do the heavily lifting of business logic and database interactions. It will query database for information tranform the data into a valid form and reduce the amount of information needed for the frotnend. It will send information as json. 
[![https://gyazo.com/b66a557ce5bf48562d6b2f858d78f0e3](https://i.gyazo.com/b66a557ce5bf48562d6b2f858d78f0e3.png)](https://gyazo.com/b66a557ce5bf48562d6b2f858d78f0e3)

The Api is capable of getting the information which correspond with the end-user queries in the project descriptions.

##### Overview
![](https://github.com/soft2018spring-gruppe10/Backend/blob/master/Documentation/Pictures/Classdiagram2.png)

##### Code quality
We have designed the system with high quality in focus. We wanted to be able to maintain and test the code we build. We have taken advantage of interfaces throughout the system. Notably the DataAcessor and the DataObjects, these can be switched out with any implementation of these interfaces. This has resulted in a very decoupled system. To change how the objects are being serialized, we can change the code 1 place and it works automaticly for all dataobjects. If we want to change the format of one of the protocols, we only need change in one place. furthermore, we can change the Database freely because of the DataAcessor interface. It has also caused very low technical dept. This is the outcome of good design, which has surfaces with the use of a testing mindset.

To put it our maintability into perspective, we had a case where we wanted to have all data in all dataobjects which contained city cordinates to have different names. we wanted to change from latitude to lat and longitude to lng, because it was easy and more convinenient for the front-end library to plot in these objects with these names that way. All we had to do to change the whole systems behavior when it came to handling cities with cordinates data was the following commits:
- [change](https://github.com/soft2018spring-gruppe10/Backend/commit/6032c043d54f325a4a5b92bb9f04a594c6338243) /Apart from changing jdk
- [tests were using these values](https://github.com/soft2018spring-gruppe10/Backend/commit/ef825157a7f78af28d8afdd78e2de791a3ff3218)

###  - Left Shift Testing
As our main sprint went into effect, we found ourself focusing on both loosely upholding left shift testing guidelines while managing
the enomous amount of data we had to process, but we choose to trust in eachothers ability to document and uphold agile test standards,
so that we could focus on getting the data handled.

###  - Continouse Integration & Delivery
We have setup a jenkins server with the following architecture:

![](https://github.com/soft2018spring-gruppe10/Backend/blob/master/Documentation/Pictures/Deploymentdiagram1.png)

Because of time and money restrictions we do not practise ideal procedures. We are deploying staging to the build server, and are using test database as staging database. Idealy we would like to have a seperate enviroment for the whole staging enviroment, idealy allmost identical to the/a production enviroment. All the containers talk easily together in a custom docker bridge network shared on the droplet. This way, the dns is created and can be accesed by the docker containers name with the ingress network.

[![https://gyazo.com/b7c8cdd4c19532aa2dda24ef68a985ea](https://i.gyazo.com/b7c8cdd4c19532aa2dda24ef68a985ea.png)](https://gyazo.com/b7c8cdd4c19532aa2dda24ef68a985ea)

We have 4 simple jobs

- 1. Test and build api
- 2. Stage api
- 3. build and stage website
- 4. system test (ui-testing)

[![https://gyazo.com/160f0b378c7674364ac563e3dd5bcf54](https://i.gyazo.com/160f0b378c7674364ac563e3dd5bcf54.png)](https://gyazo.com/160f0b378c7674364ac563e3dd5bcf54)

###  - Inclusion of Gherkin and Cucumber
in regards to our previous we mentioned three additional assignments that had to be cleared, one of these was a test assignment that
focused on writing tests using Gherkins syntax and Cucumber testing, as we lacked business logic and we had difficulty in maintaining
a overview of the API's test functions, it was proposed to set in stone the excat requirements of the API using Cucumber, we used this to help write the tests that would allow us to finally make the implementation of our API, but in retrospect we didn't take the time to write the Cucumber tests at that time and only used the Gherkin syntax for the development of the code tests, we refactored later to verify Syntax agreement with Cucumber.
####  - Acceptance Criteria
```
Written
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
At the end of the sprint we combined our Burndown Chart, to allowed us general overview of the progression of the project, another reason for this was that we weren't able to do advance documentation of our progress, given the free use of waffle.io doesn't give that many tools, the burndown chart looked like this.
![](https://i.gyazo.com/673ed384c147080a0dcc969959721fc7.png)   
At this point in time we had finished up alot of the main issues we had stumpled into, although the data proved to be a continoues problem we had to wrestle with, given we had several failures in downsizing the data into a digestable size, where 2 instances wasted 3 days of computational power on a blocker, that was third party software related. but we had a useable data set which we used as our actively tested dataset, given there were no modification requirements of the data, so it made more sense than to use mocked database.
## 4. Last Sprint
###  - Report
As the last Sprint begins our focus were devided, we had to finish up the product so the final parts were in place for documentation on the database course, though it was possible to write this report doing the last sprint, as the test side were in practice "done" at this stage, yet we choose to focus on additional testing through the use of refactoring our test cases and the product.
###  - Refactoring
Given we had focused on doing 4 databases instead of 2, resulted in us taking shortest path to achieve functional test code and product. When we began to run benchmark test the problems showed themselves, as it was needed to have both the unuptimized data queries and uptimized. Several parts of the code needed to be modified or even reworked depending on a case by case basis, yet the recursive unit test we defined early on in development allowed us to quickly pinpoint errors in the fresh code, helping to reduce the cost of refactoring greatly.
###  - End of Last Sprint
At the very end our Burndown chart had increase greatly in size as we used issue tracking to track all documentation needs we had to finish for both this Test Report and the Database Report, as of writing this the Burndown chart looked like this ![](https://i.gyazo.com/53593b0c31a14268d31d58a95c0534e7.png)    
it does look like we slacked behind, but that's partly because we don't handle the size of each issue and treat them all equally important, this is a issue as major things like parts of the Test report or Full checkup is considered the same as a returning refactor review.

## 5. Conclusion
The lack of required manpower has affected the process of this project, however we where able to adjust on a moment to moment basis because of the agile development mindset. We practiced almost daylie meetings where we dicussed the current situation of the time, and adjusted focus depending on blockers and the likes, we also performed alot of pair programming because Left shift testing mindset, which in the beginning slowed down our progress and initially made us make kneejerk reactionary actions to solve issues that would arise, however these pair programming session helped foster a shared insight of the system both through active perticipation of the creation, and through recursive testing of said earlier test focused fundament.   
One thing to note about this project, is how the test focus is more attached to the database part of the course, rather than it's own specifically designed project, this has resulted in very little business logic, so much of the test cases and techniques are left out due to redundency and in our case time constraints.
