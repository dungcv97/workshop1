---
title : "Share service network"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 5.1 </b> "
---

### Create Resource Access Manager

1. Access the **AWS Management Console** interface:
   - Locate and click on **RAM**
   - Choose **Resource Access Manager**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0001-shareservicenetwork.PNG?featherlight=false&width=90pc)

2. Within the **Resource Access Manager** interface:
   - Select **Resource shares**
   - Click on **Create resource share**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0002-shareservicenetwork.PNG?featherlight=false&width=90pc)

3. Configure resource share details:
   - Name: Enter **vpc-lattice-service-network-rs**
   - Search **VPC Lattice Service Networks**
   - Select **ARN**
   - Select **Resources**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0003-shareservicenetwork.PNG?featherlight=false&width=90pc)

4. Click **Next**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0004-shareservicenetwork.PNG?featherlight=false&width=90pc)

5. Click **Next**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0005-shareservicenetwork.PNG?featherlight=false&width=90pc)

6. Grant access to principals:
    - Select **Allow sharing with anyone**
    - Choose **AWS account** in principal type
    - Enter another AWS ID: <your_another_aws_id>

    ![Create VPC](/images/5/5.1-shareservicenetwork/0006-shareservicenetwork.PNG?featherlight=false&width=90pc)

7. Click **Next**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0007-shareservicenetwork.PNG?featherlight=false&width=90pc)

8. Click **Create resource share**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0008-shareservicenetwork.PNG?featherlight=false&width=90pc)

9. Resource share successfully created. The status of Resource ID is **Associating**, now we need to switch AWS account and approve the shared resource

    ![Create VPC](/images/5/5.1-shareservicenetwork/0009-shareservicenetwork.PNG?featherlight=false&width=90pc)

10. Switch to shared resource AWS account. Within the **Resource Access Manager** interface:
    - Select **Resource shares**
    - Click on **vpc-lattice-service-network-rs**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0010-shareservicenetwork.PNG?featherlight=false&width=90pc)

11. Click **Accept resource share**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0011-shareservicenetwork.PNG?featherlight=false&width=90pc)

12. Invitation accepted

    ![Create VPC](/images/5/5.1-shareservicenetwork/0012-shareservicenetwork.PNG?featherlight=false&width=90pc)

13. Within the **VPC** interface:
    - Select **Service networks**. We can see the service network **vpc-lattice-service-network** 

    ![Create VPC](/images/5/5.1-shareservicenetwork/0013-shareservicenetwork.PNG?featherlight=false&width=90pc)

14. Now in the Owner resource AWS account, the status of Resource ID is **Associated**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0014-shareservicenetwork.PNG?featherlight=false&width=90pc)
