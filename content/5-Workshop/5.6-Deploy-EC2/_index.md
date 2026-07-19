---
title : "Deploy Backend on EC2"
date : 2024-01-01
weight : 6
chapter : false
pre : " <b> 5.6. </b> "
---

In this section, we will deploy the **Spring Boot Backend** of the **English Study Online System** to **Amazon EC2**. After successful deployment, the Backend will connect to AWS services such as **Amazon DynamoDB**, **Amazon S3**, **Amazon SES**, and **Amazon SNS** to provide full system functionality.

---

### 5.6.1. Creating an EC2 Instance

Log in to the **AWS Management Console**, search for **Amazon EC2**, and select **Launch Instance**.

Configure the EC2 as follows:

- **Name:** EnglishStudy-Backend
- **Amazon Machine Image (AMI):** Amazon Linux 2023
- **Instance type:** t3.micro
- **Key pair:** Use or create a new Key Pair to connect via SSH.
- **Security Group:**
  - SSH (22)
  - HTTP (80)
  - Custom TCP (8080)

After completing the configuration, press **Launch Instance** to create the EC2 server.

![Create EC2](/cloud/images/5-Workshop/5.1-Workshop-overview/EC2p3.png)

---

### 5.6.2. Connecting to EC2

After EC2 enters **Running** mode, use **EC2 Instance Connect** or SSH to connect to the server.

Example:

```bash
ssh -i keyenglishstudy.pem ec2-user@<Public-IP>
```

After a successful connection, update the system and install Docker to prepare for application deployment.

---

### 5.6.3. Deploying the Backend

Upload the backend source code or Docker image to EC2.

Next, start the application using Docker:

```bash
docker build -t englishstudy-backend .
docker run -d -p 8080:8080 --env-file .env englishstudy-backend
```

After the application starts successfully, the backend will automatically connect to:

- Amazon DynamoDB
- Amazon S3
- Amazon SES
- Amazon SNS

to handle data storage, image management, and email notifications.

---

### 5.6.4. Testing the System

After deployment is complete, access the backend via the EC2 public IP address:

```text
http://<Public-IP>:8080
```

Or use **Postman** to test the system APIs.

If the backend responds successfully and can access data from Amazon DynamoDB, upload images to Amazon S3, and send emails via Amazon SES and Amazon SNS, then the deployment is complete.