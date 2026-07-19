---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Deploying an Online English Learning Platform on AWS

#### Overview

In this workshop, I will guide you through the deployment process of an **online English learning platform** on the **Amazon Web Services (AWS)** cloud platform.

The project is designed to solve common problems in online education, such as:

- Managing lessons, quizzes, and user progress in a centralized system.
- Providing a scalable platform that can support many learners at the same time.
- Storing learning content and media files securely in the cloud.
- Sending notifications and emails for important updates and user actions.
- Improving reliability and performance through cloud-based infrastructure.

To build this system, I use a modern **3-tier architecture** with **React** for the frontend, **Spring Boot** for the backend, and **Amazon DynamoDB** for data storage. Deploying the application on AWS helps improve scalability, availability, security, and maintainability.

Throughout this workshop, readers will learn how to prepare the cloud environment, configure core AWS services, deploy the backend, test the system, and clean up resources after the project is complete.

The AWS services used in this workshop include:

- Amazon EC2
- Amazon DynamoDB
- Amazon S3
- Amazon SES
- Amazon SNS
- Amazon CloudWatch
- AWS IAM
- AWS Secrets Manager

#### Contents

1. [Introduction](5.1-Workshop-overview/)
2. [Prerequisites](5.2-Prerequiste/)
3. [Configure DynamoDB](5.3-Configure-DynamoDB/)
4. [Configure Amazon S3](5.4-Configure-S3/)
5. [Configure Amazon SES & SNS](5.5-Configure-SES/)
6. [Deploy Backend on EC2](5.6-Deploy-EC2/)
7. [System Testing](5.7-System-Testing/)
8. [Resource Cleanup](5.8-Cleanup/)