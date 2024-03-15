---
title : "Tạo Target Group"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

### Tạo Target Group

1. Trong giao diện **VPC**:
    - Lựa chọn **Target groups**
    - Bấm vào **Create target group**

    ![Create VPC](/images/2/2.4-targetgroup/0001-createtargetgroup.PNG?featherlight=false&width=90pc)

2. Cấu hình **Target Group**:
    - Chọn loại target: **Instances**

    ![Create VPC](/images/2/2.4-targetgroup/0002-createtargetgroup.PNG?featherlight=false&width=90pc)

    - Tên target group: Nhập **service1-tg**
    - Chọn giao thức **HTTP** và cổng **80**
    - Chọn **VPC** tên **service1-vpc**

    ![Create VPC](/images/2/2.4-targetgroup/0003-createtargetgroup.PNG?featherlight=false&width=70pc)

    - Bấm vào **Next**

    ![Create VPC](/images/2/2.4-targetgroup/0004-createtargetgroup.PNG?featherlight=false&width=90pc)

3. Chọn **service1-ec2** instance và bấm vào **Include as pending below**

    ![Create VPC](/images/2/2.4-targetgroup/0005-createtargetgroup.PNG?featherlight=false&width=90pc)

4. Kiểm tra instance trong **Review targets** và bấm vào **Create target group**

    ![Create VPC](/images/2/2.4-targetgroup/0006-createtargetgroup.PNG?featherlight=false&width=90pc)

5. Hoàn thành việc tạo target group

    ![Create VPC](/images/2/2.4-targetgroup/0007-createtargetgroup.PNG?featherlight=false&width=90pc)