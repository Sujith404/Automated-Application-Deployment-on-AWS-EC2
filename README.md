# Jenkins CI/CD Pipeline with Docker and SonarQube

## Project Overview

This project demonstrates an automated CI/CD pipeline using Jenkins, Maven, SonarQube and Docker.

The pipeline retrieves application source code from GitHub, performs code quality analysis, builds the application using Maven, creates Docker images for the application and database, and deploys containers on the Docker host.

## Technologies Used

- Jenkins – CI/CD automation
- Groovy – Jenkins Pipeline scripting
- Git & GitHub – Source code management
- Maven – Build automation
- SonarQube – Code quality analysis
- Docker – Containerization
- Linux – Deployment environment

## Pipeline Stages

### 1. Code
- Checkout application source code from GitHub.
- Repository: https://github.com/devops0014/dockerwebapp.git

### 2. Code Quality Analysis (CQA)
- Integrate Jenkins with SonarQube.
- Execute Maven-based SonarQube analysis.
- Analyze source code quality using the configured SonarQube project.

### 3. Build
- Execute Maven clean and package.
- Generate application build artifacts.
- Copy the target directory into the Docker application build context.

### 4. Docker Image Creation
- Build the application Docker image (`appimage`).
- Build the database Docker image (`dbimage`).

### 5. Deployment
- Create and run the database container.
- Deploy the application container.
- Map application port 8080 to host port 1234.
- Connect the application container to the database container.

## Jenkins Pipeline

The Jenkins pipeline is maintained in the `Jenkinsfile` at the project root.

## Expected Deployment

- Application container: `appcont`
- Database container: `devopsdb`
- Application host port: `1234`
- Database host port: `3306`

## Learning Outcomes

- Implemented a multi-stage Jenkins declarative pipeline.
- Integrated Maven with Jenkins.
- Integrated SonarQube for code quality analysis.
- Automated Docker image creation.
- Deployed application and database containers using Docker.
