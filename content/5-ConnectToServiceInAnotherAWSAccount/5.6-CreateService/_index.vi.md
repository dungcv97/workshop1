---
title : "Tạo Service"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 5.6 </b> "
---

### Tạo Service (Trong tài khoản AWS được chia sẻ tài nguyên)

1. Trong giao diện **VPC**:
    - Chọn **Services**
    - Bấm vào **Create service**

    ![Create VPC](/images/5/5.6-service/0001-createservice.PNG?featherlight=false&width=90pc)

2. Cấu hình **Service**:
    - Tên: Nhập **service2-vpc-lattice-service**

    ![Create VPC](/images/5/5.6-service/0002-createservice.PNG?featherlight=false&width=90pc)

    - Bấm vào **Next**.

    ![Create VPC](/images/5/5.6-service/0003-createservice.PNG?featherlight=false&width=90pc)

3. Xác định định tuyến:
    - Bấm vào **Add listener**
    - Chọn giao thức **HTTP** và cổng **80**
    - Chọn Target Group: **service1-tg**
    - Bấm vào **Next**

    ![Create VPC](/images/5/5.6-service/0004-createservice.PNG?featherlight=false&width=90pc)

4. Tạo liên kết mạng:
    - Chọn VPC Lattice service networks: **vpc-lattice-service-network**
    - Bấm vào **Next**

    ![Create VPC](/images/5/5.6-service/0005-createservice.PNG?featherlight=false&width=90pc)

5. Bấm vào **Create VPC Lattice service**

    ![Create VPC](/images/5/5.6-service/0006-createservice.PNG?featherlight=false&width=90pc)

6. Hoàn thành việc tạo VPC Lattice service

    ![Create VPC](/images/5/5.6-service/0007-createservice.PNG?featherlight=false&width=90pc)
