---
title : "Create DynamoDB Table"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.3.1. </b> "
---

In the **Dental Clinic Management System**, **Amazon DynamoDB** tables are not manually created on the AWS Console but are automatically initialized through the Spring Boot backend source code.

The backend uses the `DynamoDbTableInitializer` class to check and create the necessary tables when the application starts.

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
        createTableIfNotExists("invoices", Invoice.class);
        createTableIfNotExists("feedbacks", Feedback.class);
        createTableIfNotExists("doctor_schedules", DoctorSchedule.class);
        createTableIfNotExists("doctors", Doctor.class);
        createTableIfNotExists("services", DentalService.class);
        createTableIfNotExists("consultations", Consultation.class);
        createTableIfNotExists("blogs", Blog.class);
        createTableIfNotExists("appointments", Appointment.class);
        createTableIfNotExists("categories", Category.class);
        createTableIfNotExists("specialties", Specialty.class);
        createTableIfNotExists("clinics", Clinic.class);
    }
}
```

When the Spring Boot backend runs, the `@PostConstruct` annotation will automatically call the `createTables()` method. This method checks and creates DynamoDB tables if they do not already exist.

The tables created automatically include:

| Table | Function |
|-------|-----------|
| users | Save user account information |
| invoices | Save invoice information |
| feedbacks | Save patient reviews |
| doctor_schedules | Save doctor's schedule |
| doctors | Save doctor information |
| services | Save dental service information |
| consultations | Save consultation requests |
| blogs | Save blog posts |
| appointments | Save appointment schedules |
| categories | Save blog categories |
| specialties | Save specialties |
| clinics | Save clinic information |

After the application starts successfully, access **AWS Console → DynamoDB → Tables** to check the tables that have been created.

![DynamoDB Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/dynamodb-tables.png)

If the tables show **Active** status, the DynamoDB table initialization process is complete.