---
title : "Kiểm tra kết nối"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

### Kiểm tra kết nối

Trong phần này, chúng tôi sẽ kiểm tra kết nối giữa máy chủ trong **Client VPC** và **Service 1 VPC**

1. Trong giao diện **VPC**:
    - Chọn **Services**
    - Chọn **service1-vpc-lattice-service**
    - Trong mục **Details**, sao chép **domain name**

    ![Create VPC](/images/4/4.2-testconnection/0001-testconnection.PNG?featherlight=false&width=90pc)

2. Trong giao diện **EC2**:
    - Chọn **Instances**
    - Chọn **client-ec2** instance
    - Bấm vào **Connect**

    ![Create VPC](/images/4/4.2-testconnection/0002-testconnection.PNG?featherlight=false&width=90pc)

3. Kết nối tới instance:
    - Chọn **EC2 Instance Connect**
    - Chọn **Connect using EC2 Instance Connect**
    - Bấm vào **Connect**

    ![Create VPC](/images/4/4.2-testconnection/0003-testconnection.PNG?featherlight=false&width=70pc)

4. Thực hiện lệnh sau để kiểm tra kết nối từ máy chủ trong **Client VPC** tới **Service 1 VPC**
    ```
    curl <your_vpc_lattice_service_domain_name>
    ```

    ![Create VPC](/images/4/4.2-testconnection/0004-testconnection.PNG?featherlight=false&width=90pc)

5. Hãy thử xóa service network association của VPC Lattice Service và kiểm tra lại kết nối 
    - Chọn **Services** trong **VPC** giao diện
    - Chọn **service1-vpc-lattice-service**
    - Chọn **Service network associations** tab
    - Chọn service network
    - Bấm vào **Action**
    - Bấm vào **Delete network associations**


    ![Create VPC](/images/4/4.2-testconnection/0005-testconnection.PNG?featherlight=false&width=90pc)

    - Xóa thành công

    ![Create VPC](/images/4/4.2-testconnection/0006-testconnection.PNG?featherlight=false&width=90pc)

    - Bây giờ chúng ta không thể kết nối từ máy chủ trong **Client VPC** tới **Service 1 VPC** 
    ![Create VPC](/images/4/4.2-testconnection/0007-testconnection.PNG?featherlight=false&width=90pc)