﻿---
title : "Create EC2 Instance"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.6.1. </b> "
---

In this step, we will create an **Amazon EC2 Instance** to deploy the Spring Boot backend of the **English Study Online System**.

### Accessing Amazon EC2

Log in to the **AWS Management Console**, search for **EC2**, and select the **EC2** service.

In the left-hand menu, select **Instances**, then click **Launch instances** to begin creating a new server.

### Configuring the Instance Name

In the **Name and tags** section, enter the Instance name:

```text
EnglishStudy-Backend
```

This name makes it easy to identify the server used to deploy the system's backend.

### Select Operating System

In the **Application and OS Images (Amazon Machine Image)** section, select:

```text
Amazon Linux 2023 AMI
```

This AMI provides a stable Linux environment for installing Docker and running backend applications.

### Select Instance Type

In the **Instance type** section, select:

```text
t3.micro
```

This instance type is suitable for practice and test deployment environments.

### Select Key Pair

In the **Key pair (login)** section, select the previously created Key Pair:

```text
keydental
```

This Key Pair is used to SSH connect to the EC2 Instance after the server is initialized.

![EC2 Configuration](/cloud/images/5-Workshop/5.1-Workshop-overview/EC2p1.png)

### Security Group Configuration

In the **Network settings** section, create a new Security Group or use an existing one.

In this workshop, the Security Group is configured to open the necessary ports:

| Type | Port | Purpose |
|------|------|----------|
| SSH | 22 | SSH connection to EC2 |
| HTTP | 80 | Access application via HTTP |
| Custom TCP | 8080 | Access Spring Boot Backend |

The source is configured as:

```text
0.0.0.0/0
```

to allow internet access in the practice environment.

![EC2 Security Group](/cloud/images/5-Workshop/5.1-Workshop-overview/EC2p2.png)

### Initializing an EC2 Instance

After completing the configuration, review the **Summary** section on the right side of the screen.

If the information is correct, click **Launch instance** to create the EC2 Instance.

Upon successful initialization, AWS will display the message **Successfully initiated launch of instance**.

### Checking the Instance

Return to the **Instances** page to check the status of the EC2 Instance.

When the Instance changes to **Running** and **Status check** is displayed successfully, the EC2 is ready to use.

![EC2 Running](/cloud/images/5-Workshop/5.1-Workshop-overview/EC2p3.png)

After completing this step, we have successfully created an EC2 instance to deploy the system's Spring Boot backend.