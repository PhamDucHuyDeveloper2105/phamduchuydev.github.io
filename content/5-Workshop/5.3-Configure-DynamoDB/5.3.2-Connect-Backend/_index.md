﻿---
title : "Connect Backend"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.3.2. </b> "
---

In this section, we will configure the Spring Boot backend to connect securely to **Amazon DynamoDB** using the AWS SDK for Java. This step is essential for an online English learning platform to store users, lessons, quiz results, and feedback.

### 1. Configure Credentials

The backend needs an Access Key, Secret Key, and AWS region to access DynamoDB. Instead of hardcoding these values in source code, the project reads them from the `application.yml` file through environment variables:

```yaml
aws:
  credentials:
    access-key-id: ${AWS_ACCESS_KEY_ID}
    secret-access-key: ${AWS_SECRET_ACCESS_KEY}
  region: ${AWS_REGION}
```

Make sure the required environment variables are set before starting the application.

### 2. Verify the DynamoDB Connection

After the configuration is ready, start the backend with the following command:

```bash
mvn spring-boot:run
```

When the application starts, the `DynamoDbTableInitializer` class will automatically check whether the required tables already exist. If they do, the system will print messages such as `Table already exists`.

```text
Checking and creating DynamoDB tables if they do not exist...
Table already exists: users
Table already exists: lessons
Table already exists: quizzes
Table already exists: progress
Table already exists: feedbacks
```

If the terminal shows these messages, it means the backend has successfully connected to Amazon DynamoDB and is ready to work with the database.

![DynamoDB Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/connetdb.png)