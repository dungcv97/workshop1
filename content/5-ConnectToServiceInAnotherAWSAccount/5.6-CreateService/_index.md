---
title : "Create Service"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 5.6 </b> "
---

### Create Service (In Shared Resource AWS account)

1. In the **VPC** interface:
    - Select **Services**
    - Select **Create service**

    ![Create VPC](/images/5/5.6-service/0001-createservice.PNG?featherlight=false&width=90pc)

2. Configure **Service**:
    - **Service name**: Enter **service2-vpc-lattice-service**

    ![Create VPC](/images/5/5.6-service/0002-createservice.PNG?featherlight=false&width=90pc)

    - Click **Next**.

    ![Create VPC](/images/5/5.6-service/0003-createservice.PNG?featherlight=false&width=90pc)

3. Define routing:
    - Click **Add listener**
    - Choose **HTTP** protocol and port **80**
    - Choose Target Group: **service1-tg**
    - Click **Next**

    ![Create VPC](/images/5/5.6-service/0004-createservice.PNG?featherlight=false&width=90pc)

4. Create network associations:
    - Choose VPC Lattice service networks: **vpc-lattice-service-network**
    - Click **Next**

    ![Create VPC](/images/5/5.6-service/0005-createservice.PNG?featherlight=false&width=90pc)

5. Click **Create VPC Lattice service**

    ![Create VPC](/images/5/5.6-service/0006-createservice.PNG?featherlight=false&width=90pc)

6. Complete the VPC Lattice service creation

    ![Create VPC](/images/5/5.6-service/0007-createservice.PNG?featherlight=false&width=90pc)
