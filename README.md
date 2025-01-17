# 📖 Minimalist Book Manager API

## Introduction
This is the starter repository for the Further APIs session. It provides a start to creating a Minimalist Book Manager API
using a Test-Driven Development approach.

### Pre-Requisites
- Java SE Development Kit 11
- Maven

### Technologies & Dependencies
- Spring Boot
- Spring Web
- H2 Database
- Lombok
- Spring Data JPA

### How to Get Started
- Fork this repo to your Github and then clone the forked version of this repo

### Main Entry Point
- The Main Entry Point for the application is: [BookmanagerApplication.java](src/main/java/com/techreturners/bookmanager/BookmanagerApplication.java)

### Running the Unit Tests
- You can run the unit tests in IntelliJ, or you can go to your terminal and inside the root of this directory, run:

`mvn test`

### Tasks

Here are some tasks for you to work on:

📘 Discussion Task

Explore the code and make notes on the following features and how it is being implemented in the code. We'd like you to note down what classes and methods are used and how the objects interact.

The features are:
- Get All Books
- Get a Book by ID
- Add a Book
- Update a Book

📘 Task 1: Implement the following User Story with tests.

`User Story: As a user, I want to use the Book Manager API to delete a book using its ID`


📘 Extension Task: Oh no! 😭 We've only covered the happy paths in the solution, can you figure out a way
to add in exception handling to the project? 

- Clue 1: What if someone wants to add a book with an ID for a book that already exists? How do we handle this gracefully?


- Clue 2: What if someone wants to find a book by an ID that doesn't yet exist? 
  How can we improve the API by handling errors gracefully and show a helpful message to the client?
  
### Solution for Delete Book by ID

For implementing the delete book feature, we need to consider 2 scenarios:

1) When the book does not exist.
2) When the book exists and it is deleted.

#### TDD approach:

- Add test for scenario 1, when book does not exist. See test [here](https://htmlview.glitch.me/?https://github.com/abcpaem/book-manager-api/blob/main/docs/TestResults01.html).
- Add test for scenario 2, when book exists. See test [here](https://htmlview.glitch.me/?https://github.com/abcpaem/book-manager-api/blob/main/docs/TestResults02.html).

### Extension Task Solution

There are 2 scenarios for the extension task:

1) Return error when trying to add a new book with an ID that already exists.
2) Return error when user is trying to retrieve a book with an ID that doesn't exist.

#### Considerations

HTTP Status codes will be returned accordingly, 509 for Conflict and 404 for Not found, so I'm not considering that the user of the API is a human with no HTTP knowledge, but a person or system that understands the meaning of HTTP Status codes.

#### TDD approach:

- Add test for scenario 1, when trying to add a book with an ID that already exists. See test [here](https://htmlview.glitch.me/?https://github.com/abcpaem/book-manager-api/blob/main/docs/TestResults03.html).
- Add test for scenario 2, when user is trying to retrieve a book with an ID that doesn't exist. See test [here](https://htmlview.glitch.me/?https://github.com/abcpaem/book-manager-api/blob/main/docs/TestResults04.html).

