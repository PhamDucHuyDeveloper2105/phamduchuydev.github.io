---
title : "Configure Amazon RDS"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

In this section, we will verify the **Amazon RDS** database used by the online English learning project.

Sign in to the **AWS Management Console**, search for **Amazon RDS**, and open the **Databases** page.

Select the database instance that was created for the project. Verify that the database status is **Available** before proceeding.

After connecting to the database using **MySQL Workbench**, **DBeaver**, or **SQL Server Management Studio (SSMS)** (depending on the selected database engine), verify that the required tables have been created successfully.

The core tables used by the system are listed below:

| Table | Description |
|-------|-------------|
| users | Stores user account information |
| courses | Stores course information |
| lessons | Stores lesson content and learning materials |
| quizzes | Stores quiz questions and answers |
| progress | Tracks learner progress and scores |
| feedbacks | Stores user feedback |

Run the following SQL command to display all tables in the database:

```sql
SHOW TABLES;
```

The output should include all tables required by the application.

![Amazon RDS Database](/cloud/images/5-Workshop/5.1-Workshop-overview/rds-database.png)

Verify that the Amazon RDS instance is in the **Available** state and that all required tables have been created successfully before continuing to the next steps.