---
title : "Verify Email"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.5.1. </b> "
---

In this section, we will configure the **Amazon Simple Notification Service (SNS)** to send notifications from the **Dental Clinic Management System** via an SNS Topic.

### 1. Creating an SNS Topic

Log in to the **AWS Management Console**, search for **Amazon SNS**, and select **Topics**.

Select **Create topic** and configure the following information:

- **Type:** Standard
- **Name:** `dental-clinic-notification`

Keep the default settings and select **Create topic**.

---

### 2. Creating a Subscription

After the Topic is created, register an email address to receive notifications.

1. Open the newly created Topic.
2. Select **Create subscription**.
3. Under **Protocol**, select **Email**.
4. Under **Endpoint**, enter the email address that will receive notifications.
5. Select **Create subscription**.

---

### 3. Confirm Subscription

Amazon SNS will send a confirmation email to your registered email address.

Open the email and select **Confirm subscription** to complete the registration process.

After successful confirmation, the subscription status will change to **Confirmed**.

---

### 4. Test Notification Sending

On the Topic interface, select **Publish message**.

Enter the following information for testing:

- **Subject:** Dental Clinic Notification
- **Message:** Test notification from Dental Clinic Management System.

Then select **Publish message**.

If the configuration is successful, your registered email address will receive notifications from Amazon SNS.

At this point, Amazon SNS is ready to integrate with the Backend to send notifications from the **Dental Clinic Management System**.