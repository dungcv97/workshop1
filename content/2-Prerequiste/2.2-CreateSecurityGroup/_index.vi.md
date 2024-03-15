---
title : "Tạo Security Group"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

### Tạo Security Group cho máy chủ trong Client VPC

1. Trong giao diện **VPC**:
    - Lựa chọn **Security Group**
    - Bấm vào **Create security group**

    ![Create VPC](/images/2/2.2-securitygroup/0001-createsecuritygroup.PNG?featherlight=false&width=90pc)

2. Cấu hình **Security Group**:
    - **Security Group name**: Nhập **client-sg**
    - **Description**: Nhập **Allow SSH servers in the public subnet**
    - Chọn **VPC** có tên **client-vpc**

    ![Create VPC](/images/2/2.2-securitygroup/0002-createsecuritygroup.PNG?featherlight=false&width=90pc)

3. Cấu hình **Inbound rules**:
    - Trong **Inbound rules**, bấm vào **Add rule**.
    - Chọn **Type**: **SSH** và **Source**: **Anywhere**. Cho phép SSH từ bất kỳ địa chỉ IP nào.
    - Trong **Inbound rules**, bấm vào **Add rule**.
    - Chọn **Type**: **HTTP** và **Source**: **Anywhere**. Cho phép lưu lượng truy cập từ bất kỳ địa chỉ IP nào.

    ![Create VPC](/images/2/2.2-securitygroup/0003-createsecuritygroup.PNG?featherlight=false&width=90pc)

4. Kiểm tra **Outbound rules** và bấm vào **Create security group**

    ![Create VPC](/images/2/2.2-securitygroup/0004-createsecuritygroup.PNG?featherlight=false&width=90pc)

5. Hoàn thành việc tạo security group cho máy chủ nằm trong **Client VPC**

    ![Create VPC](/images/2/2.2-securitygroup/0005-createsecuritygroup.PNG?featherlight=false&width=90pc)

### Tạo a Security Group cho máy chủ trong Service 1 VPC

6. Trong giao diện **VPC**:
    - Lựa chọn **Security Groups**
    - Bấm vào **Create security group**

    ![Create VPC](/images/2/2.2-securitygroup/0001-createsecuritygroup.PNG?featherlight=false&width=90pc)

7. Cấu hình **Security Group**:
    - **Security group name**, nhập **service1-sg**
    - **Description**, nhập **Allow traffic from VPC Lattice to targets**
    - Chọn **VPC** có tên **service1-vpc**

    ![Create VPC](/images/2/2.2-securitygroup/0006-createsecuritygroup.PNG?featherlight=false&width=90pc)

8. Cấu hình **Inbound rules**:
    - Trong **Inbound rules**, bấm vào **Add rule**.
    - Chọn **Type**: **HTTP** và **Source**: **Custom**. Tìm kiếm và chọn **com.amazonaws.region.vpc-lattice** Để cho phép lưu lượng từ mạng VPC đến mục tiêu
    
    ![Create VPC](/images/2/2.2-securitygroup/0007-createsecuritygroup.PNG?featherlight=false&width=90pc)

9. Bấm vào **Create security group**

    ![Create VPC](/images/2/2.2-securitygroup/0004-createsecuritygroup.PNG?featherlight=false&width=90pc)

11. Hoàn thành việc tạo security group cho máy chủ nằm trong **private subnet** của **Service 1 VPC**

    ![Create VPC](/images/2/2.2-securitygroup/0009-createsecuritygroup.PNG?featherlight=false&width=90pc)
