---
title : "Kiểm tra kết nối"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 5.7 </b> "
---

### Kiểm tra kết nối

Trong phần này, chúng ta sẽ kiểm tra kết nối giữa máy chủ trong **Client VPC** (trong tài khoản AWS chủ sở hữu tài nguyên) và **Service 2 VPC** (trong tài khoản AWS được chia sẻ tài nguyên)

1. Trong giao diện **VPC**:
    - Lựa chọn **Services**
    - Chọn **service2-vpc-lattice-service**
    - Trong mục **Details**, sao chép **domain name**

    ![Create VPC](/images/5/5.7-testconnection/0001-testconnection.PNG?featherlight=false&width=90pc)

2. Chuyển sang tài khoản AWS chủ sở hữu tài nguyên. Trong giao diện **EC2**:
    - Lựa chọn **Instances**
    - Chọn **client-ec2** instance
    - Bấm vào **Connect**

    ![Create VPC](/images/5/5.7-testconnection/0002-testconnection.PNG?featherlight=false&width=90pc)

3. Kết nối với instance:
    - Lựa chọn **EC2 Instance Connect**
    - Chọn **Connect using EC2 Instance Connect**
    - Bấm vào **Connect**

    ![Create VPC](/images/5/5.7-testconnection/0003-testconnection.PNG?featherlight=false&width=70pc)

4. Thực hiện lệnh sau để kiểm tra kết nối từ máy chủ trong **Client VPC** tới **Service 2 VPC**
    ```
    curl <your_vpc_lattice_service_domain_name>
    ```

    ![Create VPC](/images/5/5.7-testconnection/0004-testconnection.PNG?featherlight=false&width=90pc)