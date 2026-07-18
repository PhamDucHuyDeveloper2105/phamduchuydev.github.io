---
title : "Configure SNS Notifications"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.5.3. </b> "
---

In this section, we will configure **Amazon SNS (Simple Notification Service)** to automatically send notification emails (e.g., system alerts, reports) to your Gmail address.

### 1. Creating an SNS Topic

1. Access the **AWS Management Console**, search for **Amazon SNS**, and select **Topics**.
2. Click the **Create topic** button.
3. In the **Type** section, select **Standard**.
4. Enter a **Name** (e.g., dental-system-alerts).
5. Keep the default settings and click **Create topic**.

### 2. Subscribing to Gmail for notifications

After the topic is created, we need to add the email address that will receive notifications:

1. In the details interface of the newly created topic, switch to the **Subscriptions** tab and click **Create subscription**.
2. In the **Protocol** field, select **Email**.
3. In the **Endpoint** field, enter your **Gmail** address (e.g., your-email@gmail.com).
4. Click **Create subscription**.

### 3. Confirm Subscription

1. AWS SNS will send a confirmation email to the Gmail address you just entered.
2. Open your Gmail inbox and find the email with the subject **AWS Notification - Subscription Confirmation**.
3. Click the **Confirm subscription** link in the email.
4. Return to the AWS Console and check that the subscription status changes from *Pending confirmation* to **Confirmed**.

### 4. Publish Message

1. On the Topic interface in AWS, click the **Publish message** button.
2. Enter the **Subject** (e.g., Test Alert from Dental System).
3. Enter the message in the **Message body to send to the endpoint** field (e.g., The system is working normally!).
4. Scroll to the bottom and click **Publish message**.
5. Check your Gmail inbox; you will receive the message you just sent.

The SNS system is now ready to integrate with CloudWatch or the backend to automatically send notifications.
