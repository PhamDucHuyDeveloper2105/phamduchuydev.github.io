﻿---
title : "Connect Backend to Amazon RDS"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.3.2. </b> "
---

In this section, we will configure the Spring Boot backend to connect securely to **Amazon RDS**. Amazon RDS serves as the primary relational database for storing users, courses, lessons, quizzes, learning progress, and feedback in the online English learning platform.

### 1. Configure Database Connection

The backend connects to the Amazon RDS instance using the database endpoint, username, and password configured in the `application.yml` file.

```yaml
spring:
  datasource:
    url: jdbc:mysql://<rds-endpoint>:3306/english_learning
    username: ${DB_USERNAME}
    password: ${DB_PASSWORD}

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
```

Before starting the application, make sure the required environment variables are configured correctly:

- `DB_USERNAME`
- `DB_PASSWORD`

The database endpoint can be obtained from the **Amazon RDS Console**.

### 2. Verify the Amazon RDS Connection

After the configuration is completed, start the backend using the following command:

```bash
mvn spring-boot:run
```

When the application starts successfully, Spring Boot establishes a connection to the Amazon RDS instance and Hibernate automatically creates or updates the database schema based on the Entity classes.

The terminal should display messages similar to the following:

```text
HikariPool-1 - Start completed.

Hibernate:
create table users (...)

Hibernate:
create table courses (...)

Hibernate:
create table lessons (...)

Hibernate:
create table quizzes (...)

Hibernate:
create table progress (...)

Hibernate:
create table feedbacks (...)
```

If these messages appear without any errors, it means the backend has successfully connected to Amazon RDS and initialized the database.

### 3. Verify the Database

Open **AWS Console → Amazon RDS**, select your database instance, and connect using a database management tool such as **MySQL Workbench**, **DBeaver**, or **SQL Server Management Studio (SSMS)**.

Run the following SQL command:

```sql
SHOW TABLES;
```

The result should display the tables created by the application, such as:

- users
- courses
- lessons
- quizzes
- progress
- feedbacks

If the tables are displayed correctly, the backend has successfully connected to Amazon RDS and the database is ready for use.

![Amazon RDS Connection](/cloud/images/5-Workshop/5.1-Workshop-overview/connect-rds.png)