---
title : "Tạo Target Group"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5.5 </b> "
---

### Tạo Target Group (Trong tài khoản AWS được chia sẻ tài nguyên)

1. Trong giao diện **VPC**:
    - Chọn **Target groups**
    - Bấm vào **Create target group**

    ![Create VPC](/images/5/5.5-targetgroup/0001-createtargetgroup.PNG?featherlight=false&width=90pc)

2. Cấu hình **Target Group**:
    - Chọn loại mục tiêu: **Instances**

    ![Create VPC](/images/5/5.5-targetgroup/0002-createtargetgroup.PNG?featherlight=false&width=90pc)

    - Tên target group: nhập **service2-tg**
    - Chọn giao thức **HTTP** và cổng **80**
    - Chọn **VPC** có tên **service2-vpc**

    ![Create VPC](/images/5/5.5-targetgroup/0003-createtargetgroup.PNG?featherlight=false&width=90pc)

    - Bấm vào **Next**

    ![Create VPC](/images/5/5.5-targetgroup/0004-createtargetgroup.PNG?featherlight=false&width=90pc)

3. Chọn **service1-ec2** instance và bấm vào **Include as pending below**

    ![Create VPC](/images/5/5.5-targetgroup/0005-createtargetgroup.PNG?featherlight=false&width=90pc)

4. Kiểm tra instance trong **Review targets** và bấm vào **Create target group**

    ![Create VPC](/images/5/5.5-targetgroup/0006-createtargetgroup.PNG?featherlight=false&width=90pc)

5. Hoàn thành việc tạo target group

    ![Create VPC](/images/5/5.5-targetgroup/0007-createtargetgroup.PNG?featherlight=false&width=90pc)
