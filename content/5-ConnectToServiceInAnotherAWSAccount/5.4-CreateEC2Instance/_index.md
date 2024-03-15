---
title : "Create EC2 Instance"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 5.4 </b> "
---

### Create EC2 Instance in Service 2 VPC (In Shared Resource AWS account)

1. In the **EC2** interface:
    - Select **Instances**
    - Select **Launch instances**

    ![Create VPC](/images/5/5.4-ec2/0001-createec2.PNG?featherlight=false&width=90pc)

2. Provide a Name and tags for the instance, enter **service2-ec2**

    ![Create VPC](/images/5/5.4-ec2/0002-createec2.PNG?featherlight=false&width=80pc)

3. Choose the **AMI**:
    - Select **Quick Start**
    - Choose **Amazon Linux**
    - Select an **AMI**

    ![Create VPC](/images/5/5.4-ec2/0003-createec2.PNG?featherlight=false&width=80pc)

4. Select an **Instance type** and a **key pair** (create new if don't have)

    ![Create VPC](/images/5/5.4-ec2/0004-createec2.PNG?featherlight=false&width=60pc)

5. Configure the **Network**:
    - Select the **VPC**: **service2-vpc**
    - Choose the Subnet: **service2-subnet-private1-region**
    - Disable **Auto-assign public IP**
    - For **Firewall (Security Group)**, select **Select existing security group**
    - Choose **service2-sg**

    ![Create VPC](/images/5/5.4-ec2/0005-createec2.PNG?featherlight=false&width=60pc)

6. Click **Advanced details**

    ![Create VPC](/images/5/5.4-ec2/0006-createec2.PNG?featherlight=false&width=90pc)

7. Add the below code into **User data**. After that, select **Launch instances**
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
    ![Create VPC](/images/5/5.4-ec2/0007-createec2.PNG?featherlight=false&width=90pc)

8. Complete the instance creation

    ![Create VPC](/images/5/5.4-ec2/0008-createec2.PNG?featherlight=false&width=90pc)

9. Wait for about 5 minutes until the **Status check** shows **2/2 checks passed**

    ![Create VPC](/images/5/5.4-ec2/0009-createec2.PNG?featherlight=false&width=90pc)
