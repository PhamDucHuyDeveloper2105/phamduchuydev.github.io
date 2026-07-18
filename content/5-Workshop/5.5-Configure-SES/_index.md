---
title : "Configure Amazon SES & SNS"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

In the Dental Clinic Management System, Amazon SES is used to send appointment confirmation emails and notifications to users, while Amazon SNS is used to manage notifications via the Publish/Subscribe model.

### 1. Configuring Amazon SES

Log in to the AWS Management Console, search for Amazon SES, and select Configuration → Identities.

Select Create identity, then select Email address and enter the email address that will be used to send notifications from the system.

![Amazon SES Identity](/cloud/images/5-Workshop/5.1-Workshop-overview/SES.png)

After successful creation, AWS will send a verification email to the registered address. Open the email and select Verify email address to complete the verification process.

---

### 2. Configuring Amazon SNS

Log in to the **AWS Management Console**, search for **Amazon SNS**, and select **Topics**.

Select **Create topic**, choose the **Standard** type, and name the topic:

```text
dental-clinic-notification
```

Then click **Create topic** to create the topic.

![Amazon SNS Topic](/cloud/images/5-Workshop/5.1-Workshop-overview/SNS.png)

After successful creation, the system will generate a **Topic ARN**, which is used by the backend to send notifications to Amazon SNS.

---

### 3. Backend Configuration

Update the `application.yml` file to declare the necessary information:

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
- `AWS_SNS_TOPIC_ARN`: The ARN of the Topic created on Amazon SNS.

After completing the configuration and restarting the Backend, the system is ready to send emails via Amazon SES and broadcast notifications via Amazon SNS.