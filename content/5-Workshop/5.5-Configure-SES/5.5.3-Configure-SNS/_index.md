---
title : "Configure SNS Notifications"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.5.3. </b> "
---

In this section, we will configure **Amazon SNS** to automatically send notification emails such as system alerts or reports to a Gmail address.

### 1. Create an SNS Topic

1. Open the **AWS Management Console**, search for **Amazon SNS**, and select **Topics**.
2. Click **Create topic**.
3. In the **Type** section, select **Standard**.
4. Enter a **Name** such as `english-study-alerts`.
5. Keep the default settings and click **Create topic**.

### 2. Subscribe a Gmail Address

After the topic is created, add the email address that should receive notifications:

1. Open the new topic and go to the **Subscriptions** tab.
2. Click **Create subscription**.
3. In **Protocol**, choose **Email**.
4. In **Endpoint**, enter your Gmail address.
5. Click **Create subscription**.

### 3. Confirm the Subscription

1. AWS SNS will send a confirmation email to the Gmail address you entered.
2. Open your inbox and find the email with the subject **AWS Notification - Subscription Confirmation**.
3. Click the **Confirm subscription** link.
4. Return to the AWS Console and check that the status changes from *Pending confirmation* to **Confirmed**.

### 4. Publish a Test Message

1. On the topic page, click **Publish message**.
2. Enter a **Subject** such as *Test Alert from English Study System*.
3. Enter the message body, for example: *The system is working normally!*.
4. Click **Publish message**.
5. Check your Gmail inbox to confirm that the message arrives.

The SNS setup is now ready to be integrated with CloudWatch or the backend for automatic notifications.
