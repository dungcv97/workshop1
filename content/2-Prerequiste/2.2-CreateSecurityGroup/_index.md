---
title : "Create Security Group"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Create Security Group for Servers in Client VPC

1. In the **VPC** interface:
    - Select **Security Group**
    - Select **Create security group**

    ![Create VPC](/images/2/2.2-securitygroup/0001-createsecuritygroup.PNG?featherlight=false&width=90pc)

2. Configure the **Security Group**:
    - **Security Group name**: Enter **client-sg**
    - **Description**: Enter **Allow SSH servers in the public subnet**
    - Select the **VPC** named **client-vpc**

    ![Create VPC](/images/2/2.2-securitygroup/0002-createsecuritygroup.PNG?featherlight=false&width=90pc)

3. Configure **Inbound rules**:
    - In **Inbound rules**, click **Add rule**.
    - Select **Type**: **SSH** and **Source**: **Anywhere**. Allow SSH from any IP address.
    - In **Inbound rules**, click **Add rule**.
    - Select **Type**: **HTTP** and **Source**: **Anywhere**. Allow traffic from any IP address.

    ![Create VPC](/images/2/2.2-securitygroup/0003-createsecuritygroup.PNG?featherlight=false&width=90pc)

4. Check **Outbound rules** and select **Create security group**

    ![Create VPC](/images/2/2.2-securitygroup/0004-createsecuritygroup.PNG?featherlight=false&width=90pc)

5. Complete the creation of the security group for the server located in the **Client VPC**

    ![Create VPC](/images/2/2.2-securitygroup/0005-createsecuritygroup.PNG?featherlight=false&width=90pc)

### Create a Security Group for a Server in Service 1 VPC

6. In the **VPC** interface:
    - Select **Security Groups**
    - Select **Create security group**

    ![Create VPC](/images/2/2.2-securitygroup/0001-createsecuritygroup.PNG?featherlight=false&width=90pc)

7. Configure the **Security Group**:
    - In the **Security group name** field, enter **service1-sg**
    - In the **Description** section, enter **Allow traffic from VPC Lattice to targets**
    - Select the **VPC** named **service1-vpc**

    ![Create VPC](/images/2/2.2-securitygroup/0006-createsecuritygroup.PNG?featherlight=false&width=90pc)

8. Configure **Inbound rules**:
    - In **Inbound rules**, select **Add rule**.
    - Select **Type**: **HTTP** and leave **Source**: **Custom**. Search and select **com.amazonaws.region.vpc-lattice** to allow traffic from VPC Lattice to targets
    
    ![Create VPC](/images/2/2.2-securitygroup/0007-createsecuritygroup.PNG?featherlight=false&width=90pc)

9. Select **Create security group**

    ![Create VPC](/images/2/2.2-securitygroup/0004-createsecuritygroup.PNG?featherlight=false&width=90pc)

11. Complete the creation of the security group for the server located in the **private subnet** of **Service 1 VPC**

    ![Create VPC](/images/2/2.2-securitygroup/0009-createsecuritygroup.PNG?featherlight=false&width=90pc)
