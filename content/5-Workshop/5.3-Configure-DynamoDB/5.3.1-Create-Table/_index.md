---
title : "Create DynamoDB Tables"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.3.1. </b> "
---

In this online English learning project, **Amazon DynamoDB** tables are not created manually in the AWS Console. Instead, they are initialized automatically when the Spring Boot backend starts.

The backend uses a class named `DynamoDbTableInitializer` to check whether the required tables already exist and create them if needed.

```java
@Configuration
public class DynamoDbTableInitializer {

    private final DynamoDbEnhancedClient enhancedClient;

    public DynamoDbTableInitializer(DynamoDbEnhancedClient enhancedClient) {
        this.enhancedClient = enhancedClient;
    }

    @PostConstruct
    public void createTables() {
        createTableIfNotExists("users", User.class);
        createTableIfNotExists("lessons", Lesson.class);
        createTableIfNotExists("quizzes", Quiz.class);
        createTableIfNotExists("progress", Progress.class);
        createTableIfNotExists("feedbacks", Feedback.class);
    }
}
```

When the Spring Boot application starts, the `@PostConstruct` annotation automatically triggers the `createTables()` method. This method ensures that the required DynamoDB tables are available before the system begins serving users.

The tables created automatically include:

| Table | Purpose |
|-------|---------|
| users | Store user account information |
| lessons | Store lesson content and topics |
| quizzes | Store quiz questions and answers |
| progress | Track learner progress and scores |
| feedbacks | Store feedback from users |

After the application starts successfully, open **AWS Console → DynamoDB → Tables** to verify that the tables have been created.

![DynamoDB Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/dynamodb-tables.png)

If the tables appear with **Active** status, the DynamoDB initialization process is complete.