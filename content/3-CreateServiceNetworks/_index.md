---
title : "Create Service Network"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

### Create Service Network

1. In the **VPC** interface:
    - Select **Service networks**
    - Select **Create service network**

    ![Create VPC](/images/3/0001-createservicenetwork.PNG?featherlight=false&width=90pc)

2. Configure **Service Network**:
    - **Service network name**: Enter **vpc-lattice-service-network**

    ![Create VPC](/images/3/0002-createservicenetwork.PNG?featherlight=false&width=90pc)

    - Select **Add VPC association**.
    - Select **VPC**: **client-vpc**
    - Select **Security group**: **client-sg**
    - Select **Add VPC association**.
    - Select **VPC**: **service1-vpc**
    - Select **Security group**: **service1-sg**

    ![Create VPC](/images/3/0003-createservicenetwork.PNG?featherlight=false&width=70pc)

3. Check **Summary** detail and click **Create serivce network**

    ![Create VPC](/images/3/0004-createservicenetwork.PNG?featherlight=false&width=70pc)

4. Click **VPC association**, check status of all VPC associations

    ![Create VPC](/images/3/0005-createservicenetwork.PNG?featherlight=false&width=70pc)