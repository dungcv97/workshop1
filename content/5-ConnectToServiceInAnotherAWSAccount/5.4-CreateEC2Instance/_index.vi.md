---
title : "Tạo EC2 Instance"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 5.4 </b> "
---

### Tạo EC2 Instance trong Service 2 VPC (Trong tài khoản AWS được chia sẻ tài nguyên)

1. Trong giao diện **EC2**:
    - Chọn **Instances**
    - Bấm vào **Launch instances**

    ![Create VPC](/images/5/5.4-ec2/0001-createec2.PNG?featherlight=false&width=90pc)

2. Cung cấp tên cho instance, nhập **service2-ec2**

    ![Create VPC](/images/5/5.4-ec2/0002-createec2.PNG?featherlight=false&width=80pc)

3. Chọn **AMI**:
    - Lựa chọn **Quick Start**
    - Chọn **Amazon Linux**
    - Chọn một **AMI**

    ![Create VPC](/images/5/5.4-ec2/0003-createec2.PNG?featherlight=false&width=80pc)

4. Chọn một **Instance type** và **key pair** (Tạo mới nếu không có)

    ![Create VPC](/images/5/5.4-ec2/0004-createec2.PNG?featherlight=false&width=60pc)

5. Cấu hình **Network**:
    - Chọn **VPC**: **service2-vpc**
    - Chọn Subnet: **service2-subnet-private1-region**
    - Vô hiệu hóa **Auto-assign public IP**
    - Trong **Firewall (Security Group)**, chọn **Select existing security group**
    - Chọn **service2-sg**

    ![Create VPC](/images/5/5.4-ec2/0005-createec2.PNG?featherlight=false&width=60pc)

6. Bấm vào **Advanced details**

    ![Create VPC](/images/5/5.4-ec2/0006-createec2.PNG?featherlight=false&width=90pc)

7. Thêm mã dưới đây vào **User data**. Sau đó, bấm vào **Launch instances**
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
    ![Create VPC](/images/5/5.4-ec2/0007-createec2.PNG?featherlight=false&width=90pc)

8. Hoàn thành việc tạo instance

    ![Create VPC](/images/5/5.4-ec2/0008-createec2.PNG?featherlight=false&width=90pc)

9. Đợi khoảng 5 phút cho đến khi **Status check** hiển thị **2/2 checks passed**

    ![Create VPC](/images/5/5.4-ec2/0009-createec2.PNG?featherlight=false&width=90pc)
