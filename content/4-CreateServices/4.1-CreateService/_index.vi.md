---
title : "Tạo Service"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

### Tạo Service

1. Trong giao diện **VPC**:
    - Chọn **Services**
    - Bấm vào **Create service**

    ![Create VPC](/images/4/4.1-createservice/0001-createservice.PNG?featherlight=false&width=90pc)

2. Cấu hình **Service**:
    - **Service name**: Nhập **service1-vpc-lattice-service**

    ![Create VPC](/images/4/4.1-createservice/0002-createservice.PNG?featherlight=false&width=90pc)

    - Bấm vào **Next**.

    ![Create VPC](/images/4/4.1-createservice/0003-createservice.PNG?featherlight=false&width=70pc)

3. Xác định định tuyến:
    - Bấm vào **Add listener**
    - Chọn giao thức **HTTP** và cổng **80**
    - Chọn Target Group: **service1-tg**
    - Bấm vào **Next**

    ![Create VPC](/images/4/4.1-createservice/0004-createservice.PNG?featherlight=false&width=70pc)

4. Tạo các liên kết mạng:
    - Chọn VPC Lattice service networks: **vpc-lattice-service-network**
    - Bấm vào **Next**

    ![Create VPC](/images/4/4.1-createservice/0005-createservice.PNG?featherlight=false&width=70pc)

5. Bấm vào **Create VPC Lattice service**

    ![Create VPC](/images/4/4.1-createservice/0006-createservice.PNG?featherlight=false&width=70pc)

6. Hoàn thành tạo VPC Lattice service

    ![Create VPC](/images/4/4.1-createservice/0007-createservice.PNG?featherlight=false&width=70pc)