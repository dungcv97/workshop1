---
title : "Create Target Group"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5.5 </b> "
---

### Create Target Group (In Shared Resource AWS account)

1. In the **VPC** interface:
    - Select **Target groups**
    - Select **Create target group**

    ![Create VPC](/images/5/5.5-targetgroup/0001-createtargetgroup.PNG?featherlight=false&width=90pc)

2. Configure the **Target Group**:
    - Select **Instances** target type

    ![Create VPC](/images/5/5.5-targetgroup/0002-createtargetgroup.PNG?featherlight=false&width=90pc)

    - Target group name: Enter **service2-tg**
    - Select **HTTP** protocol and port **80**
    - Select the **VPC** named **service2-vpc**

    ![Create VPC](/images/5/5.5-targetgroup/0003-createtargetgroup.PNG?featherlight=false&width=90pc)

    - Click **Next**

    ![Create VPC](/images/5/5.5-targetgroup/0004-createtargetgroup.PNG?featherlight=false&width=90pc)

3. Choose **service1-ec2** instance and click **Include as pending below**

    ![Create VPC](/images/5/5.5-targetgroup/0005-createtargetgroup.PNG?featherlight=false&width=90pc)

4. Check instance in **Review targets** and click **Create target group**

    ![Create VPC](/images/5/5.5-targetgroup/0006-createtargetgroup.PNG?featherlight=false&width=90pc)

5. Complete the target group creation

    ![Create VPC](/images/5/5.5-targetgroup/0007-createtargetgroup.PNG?featherlight=false&width=90pc)
