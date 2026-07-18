---
title : "Configure Access Permissions"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.4.2. </b> "
---

In the **Dental Clinic Management System**, securing image data (such as personal photos of doctors and patients) is crucial. Therefore, the system does not allow public access but uses a dynamic access granting mechanism via the backend.

### 1. Bucket Security Policy

In the Bucket creation step, we kept the default setting of **Block all public access**.

This means that no one on the internet can directly view or download images from Amazon S3 using the original URL. Attempts to access will result in Amazon S3 blocking and returning an **Access Denied** error.

Only the backend application (via the IAM User `dental-backend-user` with `AmazonS3FullAccess` permissions) can legitimately communicate with, read, and write files to this Bucket.

### 2. Granting Display Permissions Using Pre-signed URLs

To enable the Frontend (ReactJS) to display images to the user, the Spring Boot Backend acts as an intermediary, granting permissions through the **Pre-signed URL** mechanism (a digitally signed URL for authentication).

In the Backend source code, the `AwsConfig` class has initialized the `S3Presigner` Bean:

```java
    @Bean
    public S3Presigner s3Presigner(AwsCredentialsProvider credentialsProvider) {
        return S3Presigner.builder()
                .region(Region.of(region))
                .credentialsProvider(credentialsProvider)
                .build();
    }