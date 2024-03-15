---
title : "Test Connection"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

### Test connection

In this section, we will test connection between server in **Client VPC** and **Service 1 VPC**

1. In the **VPC** interface:
    - Select **Services**
    - Choose **service1-vpc-lattice-service**
    - In the **Details** tab, copy **domain name**

    ![Create VPC](/images/4/4.2-testconnection/0001-testconnection.PNG?featherlight=false&width=90pc)

2. In the **EC2** interface:
    - Select **Instances**
    - Choose **client-ec2** instance
    - Click **Connect**

    ![Create VPC](/images/4/4.2-testconnection/0002-testconnection.PNG?featherlight=false&width=90pc)

3. Connect to instance:
    - Select **EC2 Instance Connect**
    - Choose **Connect using EC2 Instance Connect**
    - Click **Connect**

    ![Create VPC](/images/4/4.2-testconnection/0003-testconnection.PNG?featherlight=false&width=70pc)

4. Execute the following command to test the connection from server in **Client VPC** to **Service 1 VPC**
    ```
    curl <your_vpc_lattice_service_domain_name>
    ```

    ![Create VPC](/images/4/4.2-testconnection/0004-testconnection.PNG?featherlight=false&width=90pc)

5. Let's try remove service network association of VPC Lattice Service and test connection again
    - Select **Services** in **VPC** interface
    - Choose **service1-vpc-lattice-service**
    - Select **Service network associations** tab
    - Choose service network
    - Click **Action**
    - Click **Delete network associations**


    ![Create VPC](/images/4/4.2-testconnection/0005-testconnection.PNG?featherlight=false&width=90pc)

    - Deletion successful

    ![Create VPC](/images/4/4.2-testconnection/0006-testconnection.PNG?featherlight=false&width=90pc)

    - Now we can not connect from server in **Client VPC** to **Service 1 VPC** 
    ![Create VPC](/images/4/4.2-testconnection/0007-testconnection.PNG?featherlight=false&width=90pc)