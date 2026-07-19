---
title : "Configure Amazon DynamoDB"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

In this section, we will verify the **Amazon DynamoDB** tables used by the online English learning project.

Sign in to the **AWS Management Console**, search for **DynamoDB**, and open the **Tables** page.

At this stage, the main database tables have already been created and are ready to support the application.

The core tables used by the system are listed below:

| Table | Description |
|-------|-------------|
| users | Stores user account information |
| lessons | Stores lesson content and topics |
| quizzes | Stores quiz questions and answers |
| progress | Tracks learner progress and scores |
| feedbacks | Stores user feedback |

![DynamoDB Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/dynamodb-tables.png)

Verify that each table appears with the **Active** status before moving on to the next steps.