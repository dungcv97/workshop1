---
title : "Test Connection"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 5.7 </b> "
---

### Test connection

In this section, we will test connection between server in **Client VPC** (in Owner Resource AWS Account) và **Service 2 VPC** (in Shared Resource AWS Account)

1. In the **VPC** interface:
    - Select **Services**
    - Choose **service2-vpc-lattice-service**
    - In the **Details** tab, copy **domain name**

    ![Create VPC](/images/5/5.7-testconnection/0001-testconnection.PNG?featherlight=false&width=90pc)

2. Switch to **Owner Source AWS Account**. In the **EC2** interface:
    - Select **Instances**
    - Choose **client-ec2** instance
    - Click **Connect**

    ![Create VPC](/images/5/5.7-testconnection/0002-testconnection.PNG?featherlight=false&width=90pc)

3. Connect to instance:
    - Select **EC2 Instance Connect**
    - Choose **Connect using EC2 Instance Connect**
    - Click **Connect**

    ![Create VPC](/images/5/5.7-testconnection/0003-testconnection.PNG?featherlight=false&width=70pc)

4. Execute the following command to test the connection from server in **Client VPC** to **Service 2 VPC**
    ```
    curl <your_vpc_lattice_service_domain_name>
    ```

    ![Create VPC](/images/5/5.7-testconnection/0004-testconnection.PNG?featherlight=false&width=90pc)