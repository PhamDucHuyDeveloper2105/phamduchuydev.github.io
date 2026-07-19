---
title : "Configure Amazon SES & SNS"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

In the online English learning project, **Amazon SES** is used to send email notifications such as account confirmation or course updates, while **Amazon SNS** is used to deliver messages through the Publish/Subscribe model.

### 1. Configure Amazon SES

Sign in to the **AWS Management Console**, search for **Amazon SES**, and open **Configuration → Identities**.

Choose **Create identity**, select **Email address**, and enter the address that will be used to send system notifications.

![Amazon SES Identity](/cloud/images/5-Workshop/5.1-Workshop-overview/SES.png)

After creation, AWS sends a verification email to that address. Open the email and click **Verify email address** to complete the setup.

---

### 2. Configure Amazon SNS

Open the **AWS Management Console**, search for **Amazon SNS**, and go to **Topics**.

Select **Create topic**, choose the **Standard** type, and name the topic:

```text
english-study-notification
```

Then click **Create topic**.

![Amazon SNS Topic](/cloud/images/5-Workshop/5.1-Workshop-overview/SNS.png)

Once the topic is created, AWS generates a **Topic ARN**, which the backend can use to publish notifications.

---

### 3. Configure the Backend

Update the backend `application.yml` file with the necessary values:

```yaml
aws:
  region: ${AWS_REGION}

  ses:
    sender-email: ${AWS_SES_SENDER_EMAIL}

  sns:
    topic-arn: ${AWS_SNS_TOPIC_ARN}
```

Where:

- `AWS_SES_SENDER_EMAIL`: The email address verified on Amazon SES.
- `AWS_SNS_TOPIC_ARN`: The ARN of the SNS topic created earlier.

After completing the configuration and restarting the backend, the system will be ready to send emails through Amazon SES and publish notifications through Amazon SNS.