---
title : "Tạo Security Group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 5.3 </b> "
---

### Tạo Security Group cho máy chủ trong Service 2 VPC (Trong tài khoản AWS được chia sẻ tài nguyên)

1. Trong giao diện **VPC**:
    - Chọn **Security Groups**
    - Bấm vào **Create security group**

    ![Create VPC](/images/5/5.3-securitygroup/0001-createsecuritygroup.PNG?featherlight=false&width=90pc)

2. Cấu hình **Security Group**:
    - Trong **Security group name**, nhập **service2-sg**
    - Trong **Description**, nhập **Allow traffic from VPC Lattice to targets**
    - Chọn **VPC** có tên **service2-vpc**

    ![Create VPC](/images/5/5.3-securitygroup/0002-createsecuritygroup.PNG?featherlight=false&width=90pc)

3. Cấu hình **Inbound rules**:
    - Trong **Inbound rules**, bấm vào **Add rule**.
    - Chọn **Type**: **HTTP** và **Source**: **Custom**. Tìm kiếm và chọn **com.amazonaws.region.vpc-lattice** Để cho phép lưu lượng từ VPC Lattice đến mục tiêu
    
    ![Create VPC](/images/5/5.3-securitygroup/0003-createsecuritygroup.PNG?featherlight=false&width=90pc)

4. Bấm vào **Create security group**

    ![Create VPC](/images/5/5.3-securitygroup/0004-createsecuritygroup.PNG?featherlight=false&width=90pc)

5. Hoàn thành việc tạo ra security group cho máy chủ nằm trong **private subnet** của **Service 2 VPC**

    ![Create VPC](/images/5/5.3-securitygroup/0005-createsecuritygroup.PNG?featherlight=false&width=90pc)
