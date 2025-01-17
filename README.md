# Node.js Application with Docker and CI/CD Pipeline

## Midterm - Navneet

This is to demonstrate the CI CD enablement

## Prerequisites
Node.js
npm
Docker
Git

## Instructions

### 1. Build and Run the Application

### To run the application locally:

1) 
   git clone 
   cd simple-node-app
	
2) npm install

### Run the application:
npm start

### The application should now be running on http://localhost:3000.
#### Run Tests

Unit tests are written using jest. To run the tests:

npm test

### CI Pipeline Setup
The CI pipeline is triggered on every push or pull request to the main branch. The pipeline consists of the following steps:
•	Build Phase: Installs dependencies and builds the application.
•	Test Phase: Runs the unit tests.
The pipeline is defined in .github/workflows/ci.yml.
## Docker Image 
A Dockerfile is provided to build a Docker image for this application.
To build and run the Docker image locally:
1.	Build the Docker image:
 docker build -t navyaemmy/midterm-nav:latest .
2.	Run the Docker container:
docker run -p 3000:3000 navyaemmy/midterm-nav:latest
The application will be available at http://localhost:3000.
Docker Image Push in CI Pipeline
The CI pipeline is configured to build and push the Docker image to a registry and same is executed in pipeline with below given credentials stored in secret_key
•	DOCKER_USERNAME
•	DOCKER_PASSWORD
