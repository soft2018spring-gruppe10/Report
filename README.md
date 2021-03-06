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
  - Beginning of Production
  - The Product
  - Left Shift Testing
  - Continuous Integration & Delivery
  - The inclusion of Gherkin and Cucumber
    - Acceptance Criteria
  - Progress Logging
  - Dataset Testing
  - Frontend and UI testing
  - End of Main Sprint
4. Last Sprint
  - Report
  - Refactoring
    - Static Analysis
      - Cyclic Complexity
      - Coding Standards
      - Quality/Coupling and Polymorphism
  - Integration Testing
  - Performance Testing
  - Last minute Feature "Logger"
  - End of Last Sprint
5. Conclusion

## 1. Summary
###  - Introduction
This report is the documentation of our work on the final assignment in the summer semester of 2018 software development course,
this report will focus on the testing part of the assignment which is specified 
[here.](https://github.com/datsoftlyngby/soft2018spring-test-teaching-material/blob/master/exercises/Final%20Assignment%202018.pdf)   
The short summary is that we're to follow the final database assignment while incorporating as many testing strategies as possible,
as the main focus on the testing, part is to work as an agile team, following the agile principles and using ATTD, TTD and the likes.
The main goal is to set up the product for continuous integration and delivery pipeline, so it's possible
for the product to evolve in the proposed time of Q3 2018 following the following projection. 
![](https://www.praqma.com/images/stories/code-storyline/storyline.jpg)
###  - Requirements Analysis Document
to reduce the size of documentation, Requirements Analysis Document can be found [here](https://github.com/soft2018spring-gruppe10/Report/blob/master/documentation/Requirements%20Analysis%20Documentation.md)
## 2. Initial Design Sprint
###  - The Initial Conditions
Doing our introduction to the project, we noted that we were to focus on documenting our initial draft of test strategies, 
yet we found ourselves pressed for time, given we were assigned three other projects
as the main project started, this resulted in us choosing to focus on those assignments primarily to ensure that the remaining time
could be focused entirely on this project.
###  - The Data
Given we had our hands full, we identified early on the biggest problem with the project was the data, we were tasked with acquiring and processing a very large amount of data from the Gutenberg project shown [here](http://www.gutenberg.org/), we were initially told
the data would take around 36 hours to fully acquire, and this is not taking into account the amount of time it would take to process said data. As mentioned earlier we choose to put the project on hold but we made sure to focus on acquiring and processing the data above all else, which in retrospect was a kneejerk reaction to the initial timetable.
###  - Test Strategy

#### Early Plan
Given the assignments primary requirements is developing with left testing mindset, we take this as our main pillar for our test strategy,
to fulfill this we will focus on using Gherkin syntax for our initial user stories and acceptance criteria, while also
implementing test first principles for the assignment through the use of cucumber that can implement said Gherkin syntax queries.   

Our primary focus of the testing quadrant will be on the Q2 "automated and manual" given our focus on early story tests,
our intention is to implement the user stories and then use cucumber to make unit tests that run on mockable features, cucumber also allows
us to dig into manually setting up scenarios that are harder to implement as a boundary or state diagrams.

#### Understanding Requirements:
• Requirement specifications will be specified by our product owner(tine and Helge) + our own proxy product owner   

• Understanding of requirements will be done by everyone on the team

#### Preparing Test Cases:
The team will be preparing test cases based on the Scenarios given by the product owners (a type of end-user queries). 
This will cover all requirements

#### Creating Test Data:   
Test data will be created by the respective team member who's responsible for said database based on scenarios and Test cases.   
- **Executing Test Cases:**   

• Test cases will be executed by Continues Integration platform of the teams choice based on designed scenarios, test cases, and Test data.   

• Test result (Actual Result, Pass/Fail) will be updated in chosen Continues Integration platform and Reporting:   
Continues Integration platform will be logging the defect/bugs in build status, found during execution of test
cases. After this, Continues Integration platform will inform respective developer about the defect/bugs.   

- **Retesting and Regression Testing:**   
Retesting for fixed bugs will be done by the Continues Integration platform once it is resolved by respective
developer and bug/defect status will be updated accordingly.

#### Deployment/Delivery:
• Once all bugs/defect reported after complete testing is fixed and no other bugs are found, a report will be deployed to staging environment by the Continues Integration platform.   

• Once build is in staging environment proxy product owner will be notified.   

• Once Product owner accepts staging environment, the build will be deployed to production.

#### Testing types
- Black box testing:   

- White box testing:   

- GUI Testing:   

- Integration Testing:   

#### Test Plan
- **Functional Testing:**   
Functional testing will be covered through the use of automated black box unit tests to ensure the primary requirements are met.   
- **System Testing:**   
System testing will be done with integration through the use of black box tests with selenium.   
- **Performance Testing:**   
Check the response time is below 2 second   
- **User acceptance testing:**   
acceptance criteria will be tested through the use of automated cucumber tests.   
- **Alpha testing:**   
The alpha test is conducted at the developer's site by the proxy product owner.

###  - End of Initial Sprint
At the end of our initial sprint we had cleared out our current time obstacles of the project, we initially tried to log our efforts doing this time, but found little time to go into a habit of logging our meetings, we also found this highly redundant as the project's requirements and the situation would change on a daily basis, so past writings became obsolete rather quickly in the agile development.
At this time one of our 4 members had left our group, and our perceived timetable narrowed down further as we hurried to adapt to
the new circumstances, it was at this time we realised with the use of our burndown chart from [Waffle.io](https://waffle.io/) that we were behind schedule as seen in our two minor test review sprints   
"note that test review 1 is faulty and the two last where done but it's still 1 day behind"   
![](https://i.gyazo.com/b19ec1bd7e0e7b2918b1a4c99cec9fd7.png)   
![](https://i.gyazo.com/49fd3de81560e78a5c8a4438d24cefac.png)   
we also had an overall project deadline, where we assigned the rest of our task on, our deadline for delivery on test hand-in was on the 25th
and database hand-in was on the 28th, we choose to say the total final deadline was on the 24th to ensure adaptability at the last stretch
in case of unforeseen events.   
![](https://i.gyazo.com/e685f66a9568c04f268cd3f0c6ae1fd3.png)   
With this overview we found out, that we haven't gotten much documentation or plans in terms of business testing, other than left shift testing, which in turn didn't please the product owner as we didn't have any business value ready from this initial sprint, however we didn't lose the product owners faith, as our argumentation for clearing blockers gave value to future sprints.
## 3. Main Development Sprint
###  - Beginning of Production
At the start of the main sprint, we had the system design ready, most blockers where cleared out except for the data which was a continuous task to handle. Since we've been mostly shown tools and trades in the form of Java and related tools of the Java language, we found value in standardizing our production language as Java, this allowed us to use systems and tools we had previous knowledge on.

For the main sprint we choose to focus on making the initial foundation made with tests, so that we would gain a unified understanding of all feature communication, and allow for decoupled development of the systems, this gives great advantages for testing individual components, in comparison to others in the same system, since a decoupled system allows the individual developer to use mocks and stubs to their hearts content, while following the guidelines of the documentation.

because of the parallel work with the Database course, we found value in finishing up the data, so that we would have actual test data to use in our TDD process. We also needed a continuous integration and delivery system, to fulfill our promises to the proxy product owner, we would have to ensure this would also be done in this sprint to enable deployment of the databases for the database course as well.

###  - The Product
For a short introduction, the system consist of 3 parts, a frontend web client, that allows the product owner to interact with the product, a backend API that handles the web clients requests and calls the databases for the request data, and the databases that consist of multiple different database which was required by the database course.

#### API
##### Functionality:
This API's functionality is to link the frontend with the database. This API will do the heavy lifting of potential business logic and database interactions. It will query the database for information and transform the data into a valid form and reduce the amount of information needed for the frontend. It will send information as json. 
[![https://gyazo.com/b66a557ce5bf48562d6b2f858d78f0e3](https://i.gyazo.com/b66a557ce5bf48562d6b2f858d78f0e3.png)](https://gyazo.com/b66a557ce5bf48562d6b2f858d78f0e3)

The API is capable of getting the information which corresponds with the end-user queries in the project descriptions.

##### Overview
![](https://github.com/soft2018spring-gruppe10/Backend/blob/master/Documentation/Pictures/Classdiagram2.png)

##### Code quality
We have designed the system with high quality in focus. We wanted to be able to maintain and test the code we build. We have taken advantage of interfaces throughout the system. Notably the DataAcessor and the DataObjects, these can be switched out with any implementation of these interfaces. This has resulted in a very decoupled system. To change how the objects are being serialized, we can change the code 1 place and it works automatically for all data objects. If we want to change the format of one of the protocols, we only need change in one place. furthermore, we can change the Database freely because of the DataAcessor interface. It has also caused very low technical dept. This is the outcome of good design, which has surfaced with the use of a testing mindset.

To put our maintainability into perspective, we had a case where we wanted to have all data in all data objects, which contained city coordinates to have different names. we wanted to change from latitude to lat and longitude to lng because it was easy and more convenient for the front-end library to plot in these objects with these names that way. All we had to do to change the whole system's behavior when it came to handling cities with coordinates data was the following commits:
- [change](https://github.com/soft2018spring-gruppe10/Backend/commit/6032c043d54f325a4a5b92bb9f04a594c6338243) /Apart from changing JDK
- [tests were using these values](https://github.com/soft2018spring-gruppe10/Backend/commit/ef825157a7f78af28d8afdd78e2de791a3ff3218)

###  - Left Shift Testing
As our main sprint went into effect, we found ourselves focusing on both loosely upholding left shift testing guidelines while managing
the enormous amount of data we had to process, but we choose to trust in each others ability to document and uphold agile test standards,
so that we could focus on getting the data handled.

###  - Continuous Integration & Delivery
We have set up a Jenkins server with the following architecture:

![](https://github.com/soft2018spring-gruppe10/Backend/blob/master/Documentation/Pictures/Deploymentdiagram1.png)

Because of time and money restrictions we do not practice ideal procedures. We are deploying staging to the build server, and are using test database as staging database. Ideally, we would like to have a separate environment for the whole staging environment, ideally almost identical to the/a production environment. All the containers talk easily together in a custom docker bridge network shared on the droplet. This way, the DNS is created and can be accessed by the docker containers name with the ingress network.

[![https://gyazo.com/b7c8cdd4c19532aa2dda24ef68a985ea](https://i.gyazo.com/b7c8cdd4c19532aa2dda24ef68a985ea.png)](https://gyazo.com/b7c8cdd4c19532aa2dda24ef68a985ea)

We have 4 simple jobs

- 1. Test and build API
- 2. Stage API
- 3. build and stage website
- 4. system test (UI-testing)

[![https://gyazo.com/160f0b378c7674364ac563e3dd5bcf54](https://i.gyazo.com/160f0b378c7674364ac563e3dd5bcf54.png)](https://gyazo.com/160f0b378c7674364ac563e3dd5bcf54)

###  - Inclusion of Gherkin and Cucumber
in regards to our previous sprint we mentioned three additional assignments that had to be cleared, one of these was a test assignment that focused on writing tests using Gherkins syntax and Cucumber testing, as we lacked business logic and we had difficulty in maintaining an overview of the API's test functions, it was proposed to set in stone the excat requirements of the API using Cucumber, we used this to help write the tests that would allow us to finally make the implementation of our API, but in retrospect we didn't take the time to write the Cucumber tests at that time and only used the Gherkin syntax for the development of the code tests, we refactored later to verify Syntax agreement with Cucumber.
####  - Acceptance Criteria
to reduce the size of documentation, Acceptance criteria can be found [here](https://github.com/soft2018spring-gruppe10/Report/blob/master/documentation/Acceptance%20Criteria.md)

###  - Progress Logging
At the end of the sprint we combined our Burndown Chart, to allowed us general overview of the progression of the project, another reason for this was that we weren't able to do advance documentation of our progress, given the free use of waffle.io doesn't give that many tools, the burndown chart looked like this.
![](https://i.gyazo.com/673ed384c147080a0dcc969959721fc7.png)

###  - Dataset Testing
Although we had trouble with the data set initially, we did manage to acquire a functional data set that was close to the final stage, this helped us as the dataset didn't need to change, so it was possible to use it instead of mocking a database. Since we already set up our Test cases at this point, we were able to run test cases and compare the expected results with the actual results from the code, this way we not only had our own known state that the tests would respond, we also gained insight in which database was acting out of line, allowing for quicker debugging of the code related to that database.

Initially, we didn't have a smaller sample size for more predictable testing, in reality, we mostly compared the tests and found the outliers, which we then investigated to find faults. Around the second test review we were told it's in our best interest to create a smaller test set so that we could with 100% certainty predict what input would produce what output in a black box unit tests, the test data ended up looking like [this](https://github.com/soft2018spring-gruppe10/Databases/tree/master/TestData). This test data has been parsed by a program we wrote [TestParserProgram](https://github.com/soft2018spring-gruppe10/Databases/tree/master/TestDataScraper). While building this smaller data set we found it useful to create a stubbed data accessor, so that we could refactor our previous tests into a more refined state, the stubbed data accessor can be found [here](https://github.com/soft2018spring-gruppe10/Backend/blob/master/DBParadigmsGroup10/src/main/java/DataAcessors/StubbedDataAccessor.java).

###  - Frontend and UI testing
The frontend was build very quickly, late in development on the Vue.js framework, See [Repository](https://github.com/soft2018spring-gruppe10/Frontend).   
Given the late deployment of the UI, it was hard to write much pre-testing, and since Test pyramid states that we should do less UI and more Unit testing, we found little time or reason to dedicate additional resources to "exhaustively" test the frontend, we did, however, deploy a system test with the use of Selenium shown [here](https://github.com/soft2018spring-gruppe10/SeleniumTests/blob/master/sel/src/test/java/UITest.java).

###  - End of Main Sprint
At this point in time we had finished up a lot of the main issues we had stumbled into, although the data proved to be a continuous problem we had to wrestle with, given we had several failures in downsizing the data into a digestible size, where 2 instances wasted 3 days of computational power on a blocker, that was third party software related. but we had a useable data set which we used as our actively tested dataset, given there were no modification requirements of the data, so it made more sense than to use a mocked/stubbed database.

Likewise, we managed to set in stone our test foundation which at first slowed us down due to pair programming speed, yet the quality and the insight of those sessions further increased the speed of development both at the later parts of this sprint and beyond. Since the API was finalized early on, it was also possible to split up some task in mini sprints to speed up development process until the end.

It must be stressed this was an unusual Sprint, as it's very much larger than both the initial and the end sprint, we haven't been able to follow Scrum too well given our team size doesn't allow for standard scrum practices, however we managed this by almost holding constant mini sprints and meetings, this enabled us to handle all issues that would arise doing the main sprint.
## 4. Last Sprint
###  - Report
As the last Sprint begins our focus was divided, we had to finish up the product so the final parts were in place for documentation on the database course, though it was possible to write this report doing the last sprint, as the test side were in practice "done" at this stage, yet we choose to focus on additional testing through the use of refactoring our test cases and the product. Likewise we also realized at this stage that we havn't perfectly followed Performance or Intergration test practices, as we had mostly been neck deep in development, The Giraffe dilema comes to mind on this level over oversight, yet it was tasked of us to benchmark our databases performance and document our findings, which we both had to compare with the product and the databases, so that we would be able to argue which database would be more suitable for the given task, although late in development, this gave us a good point to start testing this aswell.

###  - Refactoring
Given we had focused on doing 4 databases instead of 2, resulted in us taking the shortest path to achieving functional test code and product. When we began to run benchmark test the problems showed themselves, as it was needed to have both the unoptimized data queries and optimized. Several parts of the code needed to be modified or even reworked depending on a case by case basis, yet the integration test we could use for regression testing, we defined early on in development allowed us to quickly pinpoint errors in the fresh code, helping to reduce the cost of refactoring greatly.

####  - Static Analysis
We wished we had remembered to document our earlier Static analysis from the project, but as stated all the way back at the initial sprint, logging our progress seemed at the time costly and with little value to our timetable, therefore we finally documenting it at the end of the project. 

##### - Code Coverage
We have also done code coverage with IntelliJ's own code coverage tool and JaCoCo, We found they both produced samy results. To view our code coverage report. clone backend repository and open index.html file in [StaticAnalysis Folder](https://github.com/soft2018spring-gruppe10/Backend/tree/master/Documentation/StaticAnalysis) with a browser to open the full report. To see a snapshot of the overview report.
[![https://gyazo.com/5e63f210ddc8413fd8a3366a663e657d](https://i.gyazo.com/5e63f210ddc8413fd8a3366a663e657d.png)](https://gyazo.com/5e63f210ddc8413fd8a3366a663e657d)

As can be seen, we do have close to 100% test coverage, we don't get all the way up there, because we chose not to test to simple methods such as "close()" method for dataaccessors. They are one-liners to close the database session, and we expect the third-party systems to have been tested.


#####  - Cyclic Complexity
Using the IntelliJ plugin [MatricsReloaded](https://plugins.jetbrains.com/plugin/93-metricsreloaded), We have calculated the Cyclic Complexity for the hole projects using CC2, to be at generally at around 3 or lower, while a few outliers complexity hit's the 6-7 level, which it could easily be refactored into a less complex solution, however due to time constraints we've chosen to reflect on this in our documentation instead of spending time refactoring these edge cases.   
See [Cyclic Complexity Report](https://github.com/soft2018spring-gruppe10/Backend/blob/master/Documentation/StaticAnalysis/Cyclic%20Complexity.csv) for more details.

#####  - Coding Standards
For code standard we choose to use the IDE [IntelliJ](https://www.jetbrains.com/idea/)'s standards, while also refactoring variables using its advice on issues it found, Besides typo's and most naming conventions, yet ignoring others we disagreed with on the tool but agreed on as a collective, however we did implement roughly 80% of its solutions.

#####  - Quality/Coupling and Polymorphism
Using the plugin [MatricsReloaded](https://plugins.jetbrains.com/plugin/93-metricsreloaded), we have calculated the code quality to be to be the following percentages from the table below.


Project |    Attribute hiding factor |    Attribute inheritance  factor |    Coupling factor |    Method hiding factor |    Method inhereitance factor |    Polymorphisms factor
:--------:|:--------:|:--------:|:--------:|:--------:|:--------:|:--------:
Project |     AHF |    AIF |    CF |    MHF |    MIF |     PF
Project |   52,31%  |  0,95%  |  19,53%  |  22,35%  |  8,04%  |  79,49%

It's initially surprising to us that our code has this level of quality, as we mostly have been in a constant literal sprint to finish this project. As shown in the table it can be seen that only roughly 20% of our code is tightly coupled, which we think is the fruit of our focus on polymorphism, which is roughly 80% of our code!

Note from the tool's description of how it calculates polymorphism. To get a detailed explanation of these metrics. please see [MetricsReloaded MOOD documentation](http://www.aivosto.com/project/help/pm-oo-mood.html)
```
Calculates the degree of polymorphism in a project as a whole. Essentially it reports on the probability that a given method will be overridden in a subclass. 
```

###  - Integration Testing
Given the lack of business logic in the project as a whole, we found it hard to implement unit tests for many of the system integration cases, likewise we also used a lot of third-party systems that we were told to trust from our reviews, since we should assume they have tested their system for us, and it would otherwise result in mostly exhaustive testing for us.

at this point in time, we use the full dataset, which ideally we would only use the test data. We did make said data but only managed to use said data for the stubbed tests, and since we at this stage had the final data set with working databases, we found more value in leaving the stubs behind but taking the knowledge with us to the rest of the development.

we did manage to refactor our initial implementation tests into two separate parameterized tests, for both Integration testing and Performance testing, See [Intergration tests](https://github.com/soft2018spring-gruppe10/Backend/blob/master/DBParadigmsGroup10/src/test/java/Interfaces/ParameterizedIntegrationTest.java) for more details.

###  - Performance Testing
As stated earlier in integration section, we managed to split up our implementation tests into their respective parts, see [Performance tests](https://github.com/soft2018spring-gruppe10/Backend/blob/master/DBParadigmsGroup10/src/test/java/Interfaces/ParameterizedPerformanceTest.java) for the refactored version.

With these refactored tests we managed to implement a full benchmark test for the database section, at this stage we intentionally used the full data set, since it was required of us to make an accurate benchmark of the different database's performance, see [Benchmark tests](https://github.com/soft2018spring-gruppe10/Backend/blob/master/DBParadigmsGroup10/src/test/java/Interfaces/DatabaseBenchmarkTest.java) for details on these.

After finalizing this we found it prudent to implement profiling, since the idea of the test project is to deliver a pipeline, where future implementations and refactoring should be commonplace, we used VisualVM [link to github](https://visualvm.github.io/), plugin for [IntelliJ](https://plugins.jetbrains.com/plugin/7115-visualvm-launcher) to Profile our code as can be seen in the following images.   
Note we don't automate these profilings stats though we would have done so given we had time.   
![](https://i.gyazo.com/8bbddf559b6ed01f382925d7f0fe732d.png)
![](https://i.gyazo.com/89986b7f2db22d0cf5e240364b673430.png)
![](https://i.gyazo.com/05c0bc9b5b7991462ee888c9ff4df6cb.png)
![](https://i.gyazo.com/ba69a3b67b86c59edae58a8f08aeabab.png)

###  - Last minute Feature "Logger"
Proxy product owner felt there were a lack of unit test and mocking in the project in general, since this is the case we would like to showcase examples that we could have implemented earlier in the project, see [benchmarker folder](https://github.com/soft2018spring-gruppe10/Backend/tree/master/DBParadigmsGroup10/src/main/java/Benchmarker), these logger tests are developed with mocking and where designed with TDD as a main focus from the start which resulted in these [tests](https://github.com/soft2018spring-gruppe10/Backend/tree/master/DBParadigmsGroup10/src/test/java/Benchmarker).

###  - End of Last Sprint
At the very end, our Burndown chart had increased greatly in size as we used issue tracking to track all documentation needs we had to finish for both this Test Report and the Database Report, as of writing this the Burndown chart looked like this ![](https://i.gyazo.com/53593b0c31a14268d31d58a95c0534e7.png)    
it does look like we slacked behind, but that's partly because we don't handle the size of each issue and treat them all equally important, this is an issue as major things like parts of the Test report or Full checkup is considered the same as a returning refactor review.

We managed to finalize and Refactor the last bit of code at this point, allowing us to better reflect on our progress and choices throughout the development time, it must be said we find we could have done this better had we more time and resources to do so, likewise working both parallel and divided between test and database course, did make it difficult to keep a overview on the process as a whole, or maybe our proxy product owner is a giraffe, either must be the case :D

## 5. Conclusion
The lack of required manpower has affected the process of this project, however, we were able to adjust on a moment to moment basis because of the agile development mindset. We practiced almost daylie meetings where we dicussed the current situation of the time, and adjusted focus depending on blockers and the likes, we also performed alot of pair programming because of the Left shift testing mindset, combined with the agile processes, which in the beginning slowed down our progress and initially made us make kneejerk reactionary actions to solve issues that would arise, however, these pair programming session helped foster a shared insight of the system both through active perticipation of the creation, and through recursive testing of said earlier test focused fundament.   
One thing to note about this project, is how the test focus is more attached to the database part of the course, rather than it's own specifically designed project, this has resulted in very little business logic, which made it difficult to make much of the test cases, and many of the techniques are left out, or lacking due to redundancy and in our case time constraints and using third-party systems.
