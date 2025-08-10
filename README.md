# Continuous Integration - Continuous Deployment

This project is a simple Spring Boot application designed as a learning tool for implementing and practicing **Continuous Integration/Continuous Deployment (CI/CD)** workflows.  
It provides a lightweight backend service, perfect for experimenting with automated pipelines using tools like **Jenkins**, **GitHub Actions**, or **GitLab CI/CD**.

---

## Features
- **Simple RESTful API:** A basic endpoint (`/hello`) to verify the application is running and responsive.
- **JUnit 5 Tests:** Example unit tests to demonstrate automated testing in the pipeline.
- **Docker Support:** A `Dockerfile` is included to containerize the application for consistent deployments across environments.
- **Code Quality Integration:** Ready for integration with tools like **SonarQube** for static code analysis.

---

## Getting Started

### Prerequisites
- Java 21 or higher
- Maven
- Docker

### Building the Project
To build the project and run the tests locally:
```bash
mvn clean install
```

## **Running the Application**
Run application directly from the command line:

``` bash
mvn spring-boot:run
```

The application will be accessible at [`http://localhost:8080/hello`](http://localhost:8080/hello)

## You can also build and run the Docker image:

```bash
# Build the Docker image
docker build -t cicd-project .

# Run the Docker container
docker run -p 8080:8080 cicd-project
```

---

## CI/CD Pipeline Goals
The primary purpose of this project is to create and explore the following CI/CD pipeline stages:
1. **Checkout:** Checkout code from git repository.
2. **Build:** Compile the Java code and package it into a JAR file.
3. **Test:** Run automated unit and integration tests.
4. **Code Quality Check:** Analyze the code for bugs, vulnerabilities, and code smells.
5. **Containerization:** Build a Docker image of the application.
6. **Deployment:** Deploy the Docker image to a target environment (local, cloud, or Kubernetes).


> 💡 This project can be a foundation for building your own pipelines and experimenting with different CI/CD tools.

---

## API Endpoints
- **Get** `/hello`
    - **Description:** A simple endpoint that returns a greeting.
    - **Response:** `Hello From Spring Boot !`