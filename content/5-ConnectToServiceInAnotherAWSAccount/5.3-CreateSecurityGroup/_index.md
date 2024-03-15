---
title : "Create Security Group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 5.3 </b> "
---

### Create a Security Group for Servers in Service 2 VPC (In Shared Resource AWS account)

1. In the **VPC** interface:
    - Select **Security Groups**
    - Select **Create security group**

    ![Create VPC](/images/5/5.3-securitygroup/0001-createsecuritygroup.PNG?featherlight=false&width=90pc)

2. Configure the **Security Group**:
    - In the **Security group name** field, enter **service2-sg**
    - In the **Description** section, enter **Allow traffic from VPC Lattice to targets**
    - Select the **VPC** named **service2-vpc**

    ![Create VPC](/images/5/5.3-securitygroup/0002-createsecuritygroup.PNG?featherlight=false&width=90pc)

3. Configure **Inbound rules**:
    - In **Inbound rules**, select **Add rule**.
    - Select **Type**: **HTTP** and leave **Source**: **Custom**. Search and select **com.amazonaws.region.vpc-lattice** to allow traffic from VPC Lattice to targets
    
    ![Create VPC](/images/5/5.3-securitygroup/0003-createsecuritygroup.PNG?featherlight=false&width=90pc)

4. Select **Create security group**

    ![Create VPC](/images/5/5.3-securitygroup/0004-createsecuritygroup.PNG?featherlight=false&width=90pc)

5. Complete the creation of the security group for the server located in the **private subnet** of **Service 2 VPC**

    ![Create VPC](/images/5/5.3-securitygroup/0005-createsecuritygroup.PNG?featherlight=false&width=90pc)
