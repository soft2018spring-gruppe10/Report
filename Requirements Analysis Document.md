# Requirements Analysis Document

## Introduction
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
  
## Current system

## Proposed system

### Overview

### Functional requirements
The product must support atleast 2 different databases with two different paradigms.   
The product must also allow the end user to execute at minimum the following commands:   
1. Given a city name your application returns all book titles with corresponding authors that mention this city.   
2. Given a book title, your application plots all cities mentioned in this book onto a map.   
3. Given an author name your application lists all books written by that author and plots all cities mentioned in any of the books onto a map.   
4. Given a geolocation, your application lists all books mentioning a city in vicinity of the given geolocation.   
The Database must all at minimum contain the Author's name, the books title, names of cities, the geolocations of said cities and thier occurences in test, aswell as any other relevant information that is needed.   

The product must be able to handle queries with at least five queries per type, see section above. That is, in total the end-user query test set contains at least 20 queries.

### Nonfunctional requirements
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

### System models
1. Scenarios   

2. Use case model   

3. Analysis object model   

4. Dynamic model   

5. User   

4. Glossary
