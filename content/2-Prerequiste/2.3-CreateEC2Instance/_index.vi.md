---
title : "Tạo EC2 Instance"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

### Tạo EC2 Instance trong Client VPC

1. Trong giao diện **EC2**:
    - Chọn **Instances**
    - Bấm vào **Launch instances**

    ![Create VPC](/images/2/2.3-ec2/0001-createec2.PNG?featherlight=false&width=90pc)

2. Cung cấp tên cho instance, nhập **client-ec2**

    ![Create VPC](/images/2/2.3-ec2/0002-createec2.PNG?featherlight=false&width=60pc)

3. Chọn **AMI**:
    - Lựa chọn **Quick Start**
    - Chọn **Amazon Linux**
    - Chọn một **AMI**

    ![Create VPC](/images/2/2.3-ec2/0003-createec2.PNG?featherlight=false&width=60pc)

4. Chọn một loại **Instance type** và **key pair** (tạo mới nếu không có)

    ![Create VPC](/images/2/2.3-ec2/0004-createec2.PNG?featherlight=false&width=60pc)

5. Cấu hình **Network**:
    - Chọn **VPC**: **client-vpc**
    - Chọn subnet: **client-subnet-public1-region**
    - Cho phép **Auto-assign public IP**
    - Trong **Firewall (Security Group)**, lựa chọn **Select existing security group**. Chọn **client-sg**
    - Bấm vào **Launch instance**

    ![Create VPC](/images/2/2.3-ec2/0005-createec2.PNG?featherlight=false&width=90pc)

6. Hoàn thành việc tạo instance

    ![Create VPC](/images/2/2.3-ec2/0006-createec2.PNG?featherlight=false&width=90pc)

7. Đợi khoảng 5 phút cho đến khi **Status check** hiển thị **2/2 checks passed**

    ![Create VPC](/images/2/2.3-ec2/0007-createec2.PNG?featherlight=false&width=90pc)

### Tạo EC2 Instance trong Service 1 VPC

8. Trong giao diện **EC2**:
    - Chọn **Instances**
    - Bấm vào **Launch instances**

    ![Create VPC](/images/2/2.3-ec2/0008-createec2.PNG?featherlight=false&width=90pc)

9. CUng cấp tên cho instance, nhập **service1-ec2**

    ![Create VPC](/images/2/2.3-ec2/0009-createec2.PNG?featherlight=false&width=60pc)

10. Chọn **AMI**:
    - Lựa chọn **Quick Start**
    - Chọn **Amazon Linux**
    - Chọn một **AMI**

    ![Create VPC](/images/2/2.3-ec2/0003-createec2.PNG?featherlight=false&width=60pc)

11. Chọn một loại **Instance type** và **key pair** (tạo mới nếu không có)

    ![Create VPC](/images/2/2.3-ec2/0004-createec2.PNG?featherlight=false&width=60pc)

12. Cấu hình **Network**:
    - Chọn **VPC**: **service1-vpc**
    - Chọn Subnet: **service1-subnet-private1-region**
    - Vô hiệu hóa **Auto-assign public IP**
    - Trong **Firewall (Security Group)**, chọn **Select existing security group**. Chọn **service1-sg**

    ![Create VPC](/images/2/2.3-ec2/0010-createec2.PNG?featherlight=false&width=90pc)

13. Bấm vào **Advanced details**

    ![Create VPC](/images/2/2.3-ec2/0011-createec2.PNG?featherlight=false&width=90pc)

14. Thêm mã dưới đây vào **User data**. Sau đó, bấm vào **Launch instances**
    ```
    #!/bin/bash
    # Use this for your user data (script from top to bottom)
    # install httpd (Linux 2 version)
    yum update -y
    yum install -y httpd
    systemctl start httpd
    systemctl enable httpd
    echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
    ```
    ![Create VPC](/images/2/2.3-ec2/0012-createec2.PNG?featherlight=false&width=90pc)

15. Hoàn thành việc tạo instance

    ![Create VPC](/images/2/2.3-ec2/0013-createec2.PNG?featherlight=false&width=90pc)

16. Đợi khoảng 5 phút cho đến khi **Status check** hiển thị **2/2 checks passed**

    ![Create VPC](/images/2/2.3-ec2/0014-createec2.PNG?featherlight=false&width=90pc)