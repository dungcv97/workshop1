---
title : "Create EC2 Instance"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

### Create EC2 Instance in Client VPC

1. In the **EC2** interface:
    - Select **Instances**
    - Select **Launch instances**

    ![Create VPC](/images/2/2.3-ec2/0001-createec2.PNG?featherlight=false&width=90pc)

2. Provide a Name and tags for the instance, enter **client-ec2**

    ![Create VPC](/images/2/2.3-ec2/0002-createec2.PNG?featherlight=false&width=60pc)

3. Choose the **AMI**:
    - Select **Quick Start**
    - Choose **Amazon Linux**
    - Select an **AMI**

    ![Create VPC](/images/2/2.3-ec2/0003-createec2.PNG?featherlight=false&width=80pc)

4. Select an **Instance type** and a **key pair** (create new if don't have)

    ![Create VPC](/images/2/2.3-ec2/0004-createec2.PNG?featherlight=false&width=80pc)

5. Configure the **Network**:
    - Select the **VPC**: **client-vpc**
    - Choose the Subnet: **client-subnet-public1-region**
    - Enable **Auto-assign public IP**
    - For **Firewall (Security Group)**, select **Select existing security group**. Choose **client-sg**
    - Click **Launch instance**

    ![Create VPC](/images/2/2.3-ec2/0005-createec2.PNG?featherlight=false&width=90pc)

6. Complete the instance creation

    ![Create VPC](/images/2/2.3-ec2/0006-createec2.PNG?featherlight=false&width=90pc)

7. Wait for about 5 minutes until the **Status check** shows **2/2 checks passed**

    ![Create VPC](/images/2/2.3-ec2/0007-createec2.PNG?featherlight=false&width=90pc)

### Create EC2 Instance in Service 1 VPC

8. In the **EC2** interface:
    - Select **Instances**
    - Select **Launch instances**

    ![Create VPC](/images/2/2.3-ec2/0008-createec2.PNG?featherlight=false&width=90pc)

9. Provide a Name and tags for the instance, enter **service1-ec2**

    ![Create VPC](/images/2/2.3-ec2/0009-createec2.PNG?featherlight=false&width=60pc)

10. Choose the **AMI**:
    - Select **Quick Start**
    - Choose **Amazon Linux**
    - Select an **AMI**

    ![Create VPC](/images/2/2.3-ec2/0003-createec2.PNG?featherlight=false&width=80pc)

11. Select an **Instance type** and a **key pair** (create new if don't have)

    ![Create VPC](/images/2/2.3-ec2/0004-createec2.PNG?featherlight=false&width=80pc)

12. Configure the **Network**:
    - Select the **VPC**: **service1-vpc**
    - Choose the Subnet: **service1-subnet-private1-region**
    - Disable **Auto-assign public IP**
    - For **Firewall (Security Group)**, select **Select existing security group**. Choose **service1-sg**

    ![Create VPC](/images/2/2.3-ec2/0010-createec2.PNG?featherlight=false&width=90pc)

13. Click **Advanced details**

    ![Create VPC](/images/2/2.3-ec2/0011-createec2.PNG?featherlight=false&width=90pc)

14. Add the below code into **User data**. After that, select **Launch instances**
    ```
    #!/bin/bash
    # Use this for your user data (script from top to bottom)
    # install httpd (Linux 2 version)
    yum update -y
    yum install -y httpd
    systemctl start httpd
    systemctl enable httpd
    echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
    ```
    ![Create VPC](/images/2/2.3-ec2/0012-createec2.PNG?featherlight=false&width=90pc)

15. Complete the instance creation

    ![Create VPC](/images/2/2.3-ec2/0013-createec2.PNG?featherlight=false&width=90pc)

16. Wait for about 5 minutes until the **Status check** shows **2/2 checks passed**

    ![Create VPC](/images/2/2.3-ec2/0014-createec2.PNG?featherlight=false&width=90pc)