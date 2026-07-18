---
title : "System Testing"
date : 2024-01-01
weight : 7
chapter : false
pre : " <b> 5.7. </b> "
---

After completing the deployment of the **Dental Clinic Management System** to AWS, the final step is to test the entire system to ensure that the services are stable and can communicate with each other.

In this section, we will verify that the Amazon EC2 Backend has successfully connected to Amazon DynamoDB, Amazon S3, Amazon SES, and Amazon SNS, and test the main functions of the system.

### 5.7.1. Checking EC2 Status

First, access the **Amazon EC2 Console** and check the status of the Instance.

If the Instance shows a **Running** status and passes all **Status Checks**, this indicates that the server is ready to run the Backend application.

![EC2 Running](/cloud/images/5-Workshop/5.1-Workshop-overview/EC2p3.png)

---

### 5.7.2. Checking Data Storage

Log in to the system and create or update data.

Then access **Amazon DynamoDB** to confirm that the data has been successfully saved to the system tables.

![DynamoDB](/cloud/images/5-Workshop/5.1-Workshop-overview/database.png)

---

### 5.7.3. Checking Image Upload

Upload a profile picture or service image from the system interface.

After a successful upload, access **Amazon S3** and check the Bucket to confirm that the image file has been saved.

![Amazon S3](/cloud/images/5-Workshop/5.1-Workshop-overview/s3avata.png)

---

### 5.7.4. Checking Email Sending

Schedule an appointment or use the email sending function from the system.

If the user receives a notification email in Gmail, it proves that Amazon SES has been configured and is functioning correctly.

![Amazon SES](/cloud/images/5-Workshop/5.1-Workshop-overview/nhangmail.png)

---

After completing the above checks, the **Dental Clinic Management System** has been successfully deployed on the AWS platform. The backend is stable on Amazon EC2 and can connect to Amazon DynamoDB, Amazon S3, Amazon SES, and Amazon SNS to fully support the system's functions.