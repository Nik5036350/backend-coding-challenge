# Backend Senior Coding Challenge 🍿

Welcome to our Movie Rating System Coding Challenge! We appreciate you taking
the time to participate and submit a coding challenge! 🥳

In this challenge, you'll be tasked with designing and implementing a robust
backend system that handles user interactions and provides movie ratings. We
don't want to check coding conventions only; **we want to see your approach
to systems design!**

**⚠️ As a tech-agnostic engineering team, we ask you to pick the technologies
you are most comfortable with and those that will showcase your strongest
performance. 💪**

## Application tech stack
- Spring Boot
- Kotlin
- JOOQ
- PostgreSQL
- Gradle
- Flyway for database migrations
- Docker (required for during build phase for jooq code generation, testing with testcontainers, and running db locally)

## How to run the project locally

1. Build the project using Gradle:
   ```bash
   ./gradlew build
   ```
2. Run postgres db locally:
   application uses postgres as a database, so you need to have it running. To do so please navigate docker directory and run:
   ```bash
    docker compose up
    ```
3. Run the application:
  navigate back to the root directory of the project and run with application-local profile:
   ```bash
   ./gradlew bootRun --args='--spring.profiles.active=local'
   ```
4. It is also possible to run the application using IDE, just make sure using the
   `application-local.yml` profile.
5. Once the application is running, you can access the API documentation at:
   [http://localhost:8080/swagger-ui/index.html#/](http://localhost:8080/swagger-ui/index.html#/)

## Running via Docker
It is also possible to run containerized version, but due to the way Jooq works you
need to build app first locally:

1. Build the project using Gradle:
   ```bash
   ./gradlew build
   ```
2. Once the build is successful, you can run the application using docker-compose.yml in the root directory of the project(in will sping up both service and the db):
   ```bash
   docker compose up
   ```
3. Once the application is running, you can access the API documentation at:
   [http://localhost:8080/swagger-ui/index.html#/](http://localhost:8080/swagger-ui/index.html#/)

## ✅ Requirements

- ✅ The backend should expose RESTful endpoints to handle user input and
  return movie ratings.
- ✅ The system should store data in a database. You can use any existing
  dataset or API to populate the initial database.
- ✅ Implement user endpoints to create and view user information.
- ✅ Implement movie endpoints to create and view movie information.
- ✅ Implement a rating system to rate the entertainment value of a movie.
- ✅ Implement a basic profile where users can view their rated movies.
- ✅ Include unit tests to ensure the reliability of your code.
- ✅ Ensure proper error handling and validation of user inputs.

## ✨ Bonus Points

- [TODO] Implement authentication and authorization mechanisms for users.
  (I have  decided leave it for a discussion since in case of Spring boot it is more configuration related, but still takes a lot of time to do it right
  and would extend the scope beyond reasonable time limit)
- ✅ Provide documentation for your API endpoints using tools like Swagger. http://localhost:8080/swagger-ui/index.html#/
- ✅ Implement logging to record errors and debug information.
- ✅ Implement caching mechanisms to improve the rating system's performance.
- ✅ Implement CI/CD quality gates.

## 📋 Evaluation Criteria

- **Systems Design:** We want to see your ability to design a flexible and
  extendable system. Apply design patterns and software engineering concepts.
- **Code quality:** Readability, maintainability, and adherence to best
  practices.
- **Functionality:** Does the system meet the requirements? Does it provide
  movie
  ratings?
- **Testing:** Adequate test coverage and thoroughness of testing.
- **Documentation:** Clear documentation for setup, usage, and API endpoints.

## 📐 Submission Guidelines

- Fork this GitHub repository.
- Commit your code regularly with meaningful commit messages.
- Include/Update the README.md file explaining how to set up and run your
  backend, including any dependencies.
- Submit the link to your repository.

## 🗒️ Notes

- You are encouraged to use third-party libraries or frameworks to expedite
  development but be prepared to justify your choices.
- Feel free to reach out if you have any questions or need clarification on the
  requirements.
- Remember to approach the challenge as you would a real-world project, focusing
  on scalability, performance, and reliability.

## 🤔 What if I don't finish?

Part of the exercise is to see what you prioritize first when you have a limited
amount of time. For any unfinished tasks, please do add `TODO` comments to
your code with a short explanation. You will be given an opportunity later to go
into more detail and explain how you would go about finishing those tasks.
