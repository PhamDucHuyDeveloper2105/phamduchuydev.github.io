﻿---
title : "Configure Amazon S3"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

In the **English Study Online System**, **Amazon S3 (Simple Storage Service)** is used to store system image files such as teacher photos, course photos, and user-uploaded files.

### 1. Creating an S3 Bucket

Log in to the **AWS Management Console**, search for **Amazon S3**, and select **Buckets**.

In the Amazon S3 interface, select **Create bucket** to create a new bucket.

Set up the basic information:

- **Bucket name:** `dental-service-images-huy`
- **AWS Region:** `Asia Pacific (Singapore) - ap-southeast-1`

After completing the configuration, select **Create bucket**.

![Amazon S3 Bucket](/cloud/images/5-Workshop/5.1-Workshop-overview/S3.png)

After successful creation, the `dental-service-images-huy` Bucket will appear in the Buckets list and be ready for use.

---

### 2. Configuring Amazon S3 in the Backend

After creating the Bucket, configure the Bucket information in the `application.yml` file of the Backend.

```yaml
aws:
  region: ${AWS_REGION}

  s3:
    bucket-name: ${AWS_S3_BUCKET_NAME}
```

Where:

- `AWS_REGION`: The region where the AWS service is deployed.

- `AWS_S3_BUCKET_NAME`: The name of the Amazon S3 Bucket (`english-study-online-images-huy`).

The backend will use this information to connect to Amazon S3 and perform image upload, download, and management operations within the system.

After completing the configuration and launching the application, the backend can store and retrieve images directly from Amazon S3.