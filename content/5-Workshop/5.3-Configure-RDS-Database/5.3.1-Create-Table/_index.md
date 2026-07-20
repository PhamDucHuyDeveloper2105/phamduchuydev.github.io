---
title : "Initialize Amazon RDS Database"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.3.1. </b> "
---

In this online English learning project, the application uses **Amazon RDS** as the primary relational database for storing user information, courses, lessons, quizzes, and learning progress.

Unlike Amazon DynamoDB, the database tables are **not created manually** through the AWS Console. Instead, the Spring Boot application automatically initializes the database schema using **Spring Data JPA** together with **Hibernate**.

The application is configured to connect to the Amazon RDS instance using the following properties:

```properties
spring.datasource.url=jdbc:mysql://<rds-endpoint>:3306/english_learning
spring.datasource.username=admin
spring.datasource.password=********

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

The `spring.jpa.hibernate.ddl-auto=update` configuration allows Hibernate to automatically create or update database tables based on the entity classes when the application starts.

Example entity:

```java
@Entity
@Table(name = "users")
public class User {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String fullName;

    private String email;

    private String password;
}
```

When the Spring Boot application starts, Hibernate scans all entity classes and creates the corresponding tables in the Amazon RDS database if they do not already exist.

The database tables created automatically include:

| Table | Purpose |
|-------|---------|
| users | Store user account information |
| courses | Store course information |
| lessons | Store lesson content |
| quizzes | Store quiz questions and answers |
| progress | Track learner progress and scores |
| feedbacks | Store user feedback |

After the application starts successfully, connect to the **Amazon RDS** instance using **MySQL Workbench**, **DBeaver**, or **SQL Server Management Studio (SSMS)** (depending on the database engine you selected).

Execute the following SQL command to verify that the tables have been created successfully:

```sql
SHOW TABLES;
```

If the expected tables appear in the database, the Amazon RDS initialization process has completed successfully.

![Amazon RDS Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/rds-tables.png)