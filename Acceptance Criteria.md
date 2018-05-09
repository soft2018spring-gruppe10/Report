# Acceptance Criteria

Date: 29/04/2018


### Introduction
In regards  to our final test assignment this semester, and in response to the requirement of acceptance criterias for the first review   session with Tine, we have developed some user stories based on the requirements of the assignment description, and we have based our acceptance criterias on these user stories.

#### User stories

#####  User story 1:
"As a user, I want to enter a city, and the application returns all book titles with with corresponding authors, that mentions this specific city, so that I can find the book that I want to read."

##### Acceptance criteria:
```
Given a user picks copenhagen as a city
When the user ask for all book titles with corresponding authors that is mentioned in copenhagen
Then the user will get all books with corresponding authors that is mentioned in copenhagen
```

##### User story 2:
As a user, i want to enter a book title, and the application plots all cities mentioned in this book onto a map, so that I can get a visualization of books onto the map.

##### Acceptance Criteria:
```
Given a user gives a book title "Salute to Adventurers"
When the user ask for all cities mentioned in that book
And the user ask for all those cities plotted on a map
Then the user will get a map with all cities mentioned in the book plotted on that map.
```

##### User story 3:
As a user, i want to enter an authors name and get all books by that author and a map of with plots of all cities mentioned in any of the books so that i can find a book that i want to read.

##### Acceptance Criteria:
```
Given a User gives a author name "William Shakespeare"
When the user ask for all books by that author
And the user ask for all cities mentioned in those books
And the user ask for all those cities plotted on a map
Then the user will get a map with all cities mentioned in those books plotted on that map.
```


##### User story 4:

As a user, i want to give a location and get all books which mentions a city in the vicinity of that location, so i can find a book that i want to read.

##### Acceptance Criteria:
```
Given a User gives a location "10,30"
When the user ask for all books that mentions cities near that location
Then the user gets all books mentioning a city near that location
```

##### Questions
- is it correct that given is as it is, compared to the above user stories arrangement style.   

- does it need to be more specific as in 100% specific data, given the data size would enlarge these statements alot.   
