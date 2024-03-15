---
title : "Create Service"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

### Create Service

1. In the **VPC** interface:
    - Select **Services**
    - Select **Create service**

    ![Create VPC](/images/4/4.1-createservice/0001-createservice.PNG?featherlight=false&width=90pc)

2. Configure **Service**:
    - **Service name**: Enter **service1-vpc-lattice-service**

    ![Create VPC](/images/4/4.1-createservice/0002-createservice.PNG?featherlight=false&width=90pc)

    - Click **Next**.

    ![Create VPC](/images/4/4.1-createservice/0003-createservice.PNG?featherlight=false&width=70pc)

3. Define routing:
    - Click **Add listener**
    - Choose **HTTP** protocol and port **80**
    - Choose Target Group: **service1-tg**
    - Click **Next**

    ![Create VPC](/images/4/4.1-createservice/0004-createservice.PNG?featherlight=false&width=70pc)

4. Create network associations:
    - Choose VPC Lattice service networks: **vpc-lattice-service-network**
    - Click **Next**

    ![Create VPC](/images/4/4.1-createservice/0005-createservice.PNG?featherlight=false&width=70pc)

5. Click **Create VPC Lattice service**

    ![Create VPC](/images/4/4.1-createservice/0006-createservice.PNG?featherlight=false&width=70pc)

6. Complete the VPC Lattice service creation

    ![Create VPC](/images/4/4.1-createservice/0007-createservice.PNG?featherlight=false&width=70pc)