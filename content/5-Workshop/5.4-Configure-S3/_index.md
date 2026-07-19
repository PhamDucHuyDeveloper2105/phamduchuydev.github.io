﻿---
title : "Configure Amazon S3"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

In the online English learning project, **Amazon S3** is used to store image files such as lesson thumbnails, user avatars, and other uploaded media.

### 1. Create an S3 Bucket

Sign in to the **AWS Management Console**, search for **Amazon S3**, and open the **Buckets** page.

Choose **Create bucket** and enter the required information:

- **Bucket name:** `english-study-online-images-huy`
- **AWS Region:** `Asia Pacific (Singapore) - ap-southeast-1`

After completing the setup, click **Create bucket**.

![Amazon S3 Bucket](/cloud/images/5-Workshop/5.1-Workshop-overview/S3.png)

Once the bucket is created successfully, it will appear in the bucket list and be ready for use.

---

### 2. Configure S3 in the Backend

After creating the bucket, add its configuration to the backend `application.yml` file:

```yaml
aws:
  region: ${AWS_REGION}

  s3:
    bucket-name: ${AWS_S3_BUCKET_NAME}
```

Where:

- `AWS_REGION`: The AWS region used for deployment.
- `AWS_S3_BUCKET_NAME`: The name of the S3 bucket, such as `english-study-online-images-huy`.

The backend will use these values to connect to Amazon S3 and handle upload, download, and file management operations.

Once the configuration is complete and the application is running, the system can store and retrieve files directly from S3.