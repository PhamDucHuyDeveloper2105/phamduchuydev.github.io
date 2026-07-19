---
title : "Verify Email"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.5.1. </b> "
---

In this section, we will configure **Amazon SNS** to send notification emails from the online English learning platform.

### 1. Create an SNS Topic

Log in to the **AWS Management Console**, search for **Amazon SNS**, and open the **Topics** page.

Choose **Create topic** and configure the following settings:

- **Type:** Standard
- **Name:** `english-study-notification`

Keep the default options and click **Create topic**.

---

### 2. Create a Subscription

After the topic is created, add an email address that will receive notifications.

1. Open the newly created topic.
2. Click **Create subscription**.
3. In **Protocol**, choose **Email**.
4. In **Endpoint**, enter the email address that should receive the messages.
5. Click **Create subscription**.

---

### 3. Confirm the Subscription

AWS SNS will send a confirmation email to the address you entered.

Open the email and click **Confirm subscription** to complete the setup.

After confirmation, the subscription status will change to **Confirmed**.

---

### 4. Test the Notification

On the topic page, select **Publish message**.

Enter the test information:

- **Subject:** English Study Notification
- **Message:** This is a test notification from the online English learning system.

Then click **Publish message**.

If everything is configured correctly, the email address you registered will receive the notification.

At this point, Amazon SNS is ready to be connected with the backend for sending alerts and notifications.