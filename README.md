# Containerizing Java Applications with Docker and Publishing Images to Amazon ECR Using Jenkins Pipeline

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws)
![Jenkins](https://img.shields.io/badge/Jenkins-CI%2FCD-D24939?logo=jenkins)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Amazon ECR](https://img.shields.io/badge/Amazon_ECR-FF9900?logo=amazonaws&logoColor=white)
![Maven](https://img.shields.io/badge/Apache_Maven-C71A36?logo=apachemaven&logoColor=white)
![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=openjdk&logoColor=white)
![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?logo=sonarqube&logoColor=white)
![Nexus Repository](https://img.shields.io/badge/Nexus_Repository-2C3E50)
![Slack](https://img.shields.io/badge/Slack-4A154B?logo=slack&logoColor=white)
![Amazon ECR](https://img.shields.io/badge/Container_Registry-Amazon_ECR-FF9900)

## Enterprise DevOps Portfolio Project

This project demonstrates how a Java application can be *containerized using Docker* and automatically *published to Amazon Elastic Container Registry (Amazon ECR)* through a *Jenkins Declarative Pipeline*.

The implementation extends an enterprise Continuous Integration (CI) pipeline by integrating Docker image creation, image versioning, Amazon ECR authentication, automated image publishing, and Slack notifications. The completed pipeline validates application quality, packages the application into a Docker image, stores the build artifact in Nexus Repository Manager, publishes the container image to Amazon ECR, and notifies the development team upon pipeline completion.

> *Project Status:* ✅ Completed Successfully

## Project Overview

This project demonstrates the implementation of an enterprise-grade Continuous Integration (CI) pipeline that extends beyond traditional build automation by incorporating Docker containerization and Amazon Elastic Container Registry (Amazon ECR) integration.

The solution automates the complete application packaging workflow using a Jenkins Declarative Pipeline. Every pipeline execution compiles the Java application with Maven, performs automated testing, executes static code quality analysis with Checkstyle and SonarQube, evaluates the configured Quality Gate, publishes the generated WAR artifact to Nexus Repository Manager, builds a Docker image using a multi-stage Dockerfile, and securely pushes the image to a private Amazon ECR repository.

To support image versioning and deployment consistency, each successful pipeline execution tags the Docker image with both the Jenkins build number and the latest tag before publishing it to Amazon ECR. Upon completion, Slack notifications provide immediate feedback on the pipeline execution status.

Throughout the implementation, several real-world integration challenges—including SonarQube connectivity, webhook configuration, changing EC2 public IP addresses, AWS credential validation, and Amazon ECR authentication—were successfully diagnosed and resolved, resulting in a fully functional end-to-end CI pipeline suitable for modern containerized application delivery.
