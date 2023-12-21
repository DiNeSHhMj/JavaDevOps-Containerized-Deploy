# JavaDevOps-Containerized-Deploy

This project is a Java application with integrated DevOps practices for continuous integration and deployment.

## Tools and Prerequisites

Before you begin, make sure you have the following tools and prerequisites installed:

- [JDK (Java Development Kit)](https://www.oracle.com/java/technologies/javase-downloads.html) - Oracle JDK 8 is recommended.
- [Maven](https://maven.apache.org/download.cgi) - Build and project management tool.
- [SonarQube](https://www.sonarqube.org/) - Continuous Inspection tool for static code analysis.
- [AWS CLI](https://aws.amazon.com/cli/) - AWS Command Line Interface for interacting with AWS services.
- [Jenkins](https://www.jenkins.io/download/) - Automation server used for building, testing, and deploying.

# Project Structure

The project is organized with the following structure:

- **src:** Contains the source code for the Java application.

- **userdata:** This directory contains scripts for setting up Jenkins, Nexus, and SonarQube. These scripts are designed to streamline the deployment and configuration process. The individual scripts include:

  - `setup-jenkins.sh`: Script for setting up Jenkins.
  - `setup-nexus.sh`: Script for setting up Nexus.
  - `setup-sonar.sh`: Script for setting up SonarQube.

- **Vagrant:** This directory includes a `Vagrantfile` for provisioning a virtual machine (VM) on the host system. Additionally, scripts are provided to install various tools within the VM. The files in this directory are:

  - `Vagrantfile`: Configuration file for creating and configuring the VM.
  - `install-tools.sh`: Script for installing different tools within the VM.


## Configuration

### Jenkins

1. **Create Jenkins Pipeline Job:**
   - Set up a Jenkins pipeline job.

2. **Trigger Pipeline on Code Changes:**
   - Configure Jenkins to trigger the pipeline on code changes.

### SonarQube

1. **Set Up SonarQube Server:**
   - Set up a SonarQube server.

2. **Integrate with Jenkins:**
   - Configure the Jenkins pipeline to integrate with SonarQube for code analysis.

### AWS

1. **Set Up AWS ECR:**
   - Create an AWS ECR repository for storing Docker images.

2. **Set Up AWS ECS:**
   - Set up an AWS ECS cluster and service for deploying the application.

### Jenkinsfile

1. **Update Jenkinsfile:**
   - Modify the Jenkinsfile to include the correct configurations for your environment.

### Running the Pipeline

1. **Trigger Manually or Set Up Webhooks:**
   - Trigger the Jenkins pipeline manually or set up webhooks for automatic triggers.

## Pipeline Stages

1. **Checkout:**
   - Clone the Git repository.

2. **Build:**
   - Build the Java application using Maven.

3. **SonarQube Analysis:**
   - Run code analysis with SonarQube.

4. **Build Docker Image:**
   - Build a Docker image of the application.

5. **Backup to Docker Hub:**
   - Push the Docker image to Docker Hub for backup.

6. **Push to AWS ECR:**
   - Push the Docker image to AWS ECR.

7. **Deploy to AWS ECS:**
   - Deploy the application on AWS ECS.

