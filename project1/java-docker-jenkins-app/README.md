# Java Docker Jenkins Application

This project is a Java Spring Boot application designed to be built and deployed using Docker and Jenkins CI/CD pipeline. The application serves a simple web page and demonstrates the integration of various technologies.

## Project Structure

```
java-docker-jenkins-app
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── example
│   │   │           ├── Application.java
│   │   │           ├── controller
│   │   │           │   └── HomeController.java
│   │   │           └── model
│   │   │               └── User.java
│   │   └── resources
│   │       ├── application.properties
│   │       └── templates
│   │           └── index.html
│   └── test
│       └── java
│           └── com
│               └── example
│                   └── ApplicationTest.java
├── Dockerfile
├── Jenkinsfile
├── pom.xml
├── sonar-project.properties
└── README.md
```

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd java-docker-jenkins-app
   ```

2. **Build the Application**
   Ensure you have Maven installed, then run:
   ```bash
   mvn clean install
   ```

3. **Run the Application Locally**
   You can run the application locally using:
   ```bash
   mvn spring-boot:run
   ```
   Access the application at `http://localhost:9090`.

4. **Docker Build**
   To build the Docker image, run:
   ```bash
   docker build -t java-docker-jenkins-app .
   ```

5. **Docker Run**
   To run the Docker container:
   ```bash
   docker run -p 9090:9090 java-docker-jenkins-app
   ```

6. **Jenkins CI/CD Pipeline**
   The Jenkinsfile defines the CI/CD pipeline with the following stages:
   - Code Checkout
   - Maven Build
   - SonarQube Testing
   - Docker Build
   - ECR Push
   - Deploy Container

## Usage

Once the application is running, you can access it by navigating to `http://localhost:9090` in your web browser. The application will display a simple welcome message or sample content defined in the `index.html` template.

## Additional Information

- Ensure you have Docker and Jenkins installed and configured properly.
- Modify the `application.properties` file for any specific configurations needed for your environment.
- The project uses Maven for dependency management and build processes.