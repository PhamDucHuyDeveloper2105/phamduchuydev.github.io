﻿---
title : "Connect Backend"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.3.2. </b> "
---

In this section, we will look at how to configure the Spring Boot backend to securely connect to the **Amazon DynamoDB** service via the AWS SDK for Java.

### 1. Configuring Credentials

For the backend to access DynamoDB, the system needs to be provided with credentials (Access Key & Secret Key). Instead of hardcoding directly in the code, the project uses the `application.yml` file to read these values ​​from **Environment Variables**:

```yaml
aws:
  credentials:
    access-key-id: ${AWS_ACCESS_KEY_ID}
    secret-access-key: ${AWS_SECRET_ACCESS_KEY}
  region: ${AWS_REGION}

### 2. Check DynamoDB Connection

After configuring the connection information, run the Spring Boot Backend using the command:

```bash
mvn spring-boot:run
```

When the application starts, the `DynamoDbTableInitializer` class will automatically check for DynamoDB tables. If the table already exists, the system will display the message `Table already exists`.

```text
Checking and creating DynamoDB tables if they do not exist...
Table already exists: users
Table already exists: teachers
Table already exists: courses
Table already exists: lessons
Table already exists: enrollments
Table already exists: feedbacks
```
The results in Terminal show that Backend has successfully connected to Amazon DynamoDB:

![DynamoDB Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/connetdb.png)
The above logs prove that Backend has accessed DynamoDB and successfully checked the system's data tables.