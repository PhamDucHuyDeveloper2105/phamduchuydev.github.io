﻿---
title : "Resource Cleanup"
date : 2024-01-01
weight : 8
chapter : false
pre : " <b> 5.8. </b> "
---

After completing the Workshop and successfully verifying the system's functionality, the final step is to clean up the resources created on AWS to avoid unnecessary costs.

In this section, we will sequentially delete the resources used during the deployment of the **English Study Online System**.

### 5.8.1. Deleting an EC2 Instance

1. Access **Amazon EC2**.
2. Select **Instances**.
3. Select the created EC2 Instance.
4. Select **Instance state → Terminate instance**.
5. Confirm the deletion.

![Terminate EC2](/cloud/images/5-Workshop/5.1-Workshop-overview/xoaEC2.png)

---

### 5.8.2. Deleting an Amazon S3 Bucket

1. Access **Amazon S3**.
2. Select the project's Bucket.
3. Delete all objects in the Bucket.
4. Then select **Delete bucket**.
5. Enter the Bucket name to confirm and complete the deletion.

> **Note:** In this Workshop, the team **did not delete the Amazon S3 Bucket** because the Bucket is still used to store system images and for development and testing in subsequent phases.

---

### 5.8.3. Deleting Amazon DynamoDB Tables

1. Access **Amazon DynamoDB**.
2. Select **Tables**.
3. Select the project tables such as:
    - users
    - teachers
    - courses
    - lessons
    - enrollments
    - feedbacks
4. Select **Delete table**.
5. Enter confirmation and complete the deletion.

> **Note:** In this workshop, the team **did not delete the Amazon DynamoDB tables** because the data is still being used for system development, testing, and demos.

### 5.8.4. Deleting Amazon SES Identity

1. Access **Amazon SES**.
2. Select **Configuration → Identities**.
3. Select the verified Email Identity.
4. Select **Delete** to delete the Identity.

> **Note:** In this workshop, the team **did not delete the Email Identity on Amazon SES** because it is still being used to send enrollment confirmation emails and system notifications.

After completing the above steps, all resources used in the workshop have been cleaned up. This helps avoid additional costs and keeps the AWS account clean and ready for future deployments.