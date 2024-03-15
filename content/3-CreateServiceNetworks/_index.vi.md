---
title : "Tạo Service Network"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

### Tạo Service Network

1. Trong giao diện **VPC**:
    - Chọn **Service networks**
    - Bấm vào **Create service network**

    ![Create VPC](/images/3/0001-createservicenetwork.PNG?featherlight=false&width=90pc)

2. Cấu hình **Service Network**:
    - **Service network name**: Nhập **vpc-lattice-service-network**

    ![Create VPC](/images/3/0002-createservicenetwork.PNG?featherlight=false&width=90pc)

    - Bấm vào **Add VPC association**.
    - Chọn **VPC**: **client-vpc**
    - Chọn **Security group**: **client-sg**
    - Bấm vào **Add VPC association**.
    - Chọn **VPC**: **service1-vpc**
    - Chọn **Security group**: **service1-sg**

    ![Create VPC](/images/3/0003-createservicenetwork.PNG?featherlight=false&width=70pc)

3. Kiểm tra chi tiết trong **Summary** và bấm vào **Create serivce network**

    ![Create VPC](/images/3/0004-createservicenetwork.PNG?featherlight=false&width=70pc)

4. Chọn **VPC association**, Kiểm tra trạng thái của tất cả các VPC associations

    ![Create VPC](/images/3/0005-createservicenetwork.PNG?featherlight=false&width=70pc)