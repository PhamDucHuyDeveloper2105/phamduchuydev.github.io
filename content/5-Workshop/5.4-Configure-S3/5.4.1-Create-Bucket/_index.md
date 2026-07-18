---
title : "Create S3 Bucket"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.4.1. </b> "
---

In this step, we will create an **Amazon S3 Bucket** to store images for the **English Study Online System**.

### Creating an S3 Bucket

1. Log in to the **AWS Management Console**.
2. Search for **Amazon S3**.
3. Select **Buckets**.
4. Select **Create bucket**.
5. Configure the Bucket with the following information:
   - **Bucket name:** `english-study-online-images-huy`
   - **AWS Region:** `Asia Pacific (Singapore) - ap-southeast-1`
6. Keep the default settings and select **Create bucket**.

After successful creation, the Bucket will appear in the Amazon S3 Buckets list.

![Amazon S3 Bucket](/cloud/images/5-Workshop/5.1-Workshop-overview/S3.png)

### Checking the Bucket

Select the **english-study-online-images-huy** Bucket to check the stored objects.

In the Bucket, the system has organized folders to manage images by function:

- **avatars/**: Stores avatar images.

- **courses/**: Stores course images.

- **lessons/**: Stores lesson images.

![Amazon S3 Objects](/cloud/images/5-Workshop/5.1-Workshop-overview/s3-objects.png)

### Checking CloudFront

After successful creation, the Distribution status will change to **Enabled**.

Copy the CloudFront **Domain name** for use in the Backend or Frontend when accessing images.

![CloudFront Running](/cloud/images/5-Workshop/5.1-Workshop-overview/cloufront.png)

After completing this step, the system will use CloudFront to distribute images from Amazon S3, speeding up loading and improving access performance.
After completing this step, Amazon S3 is ready for the Backend to store and retrieve system images.