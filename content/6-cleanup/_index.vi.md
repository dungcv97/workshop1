---
title : "Dọn dẹp tài nguyên"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 6. </b> "
---
## Dọn dẹp tài nguyên

Chúng ta sẽ tiến hành xóa các tài nguyên theo thứ tự sau:

#### Chấm dứt các EC2 Instances

- Truy cập bảng điều khiển Amazon EC2 tại [EC2](https://console.aws.amazon.com/ec2/).
- Trên thanh điều hướng bên trái, chọn "Instances."
- Chọn tất cả các EC2 instances liên quan đến bài thực hành.
- Chọn **Instance state**.
- Chọn **Terminate instance**.

#### Xóa service network associations trong VPC Lattice Service

- Truy cập trang Bảng điều khiển Amazon VPC tại [VPC](https://console.aws.amazon.com/vpc/).
- Trên thanh điều hướng bên trái, chọn "Services."
- Chọn service.
- Chọn mục **Service network associations**
- Chọn **Action**.
- Chọn **Delete network associations**.
- Nhập "confirm."

#### Xóa Service

- Truy cập trang Bảng điều khiển Amazon VPC tại [VPC](https://console.aws.amazon.com/vpc/).
- Trên thanh điều hướng bên trái, chọn "Services."
- Chọn service.
- Chọn **Action**.
- Chọn **Delete service**.
- Nhập "confirm."

#### Xóa Target Group

- Truy cập trang Bảng điều khiển Amazon VPC tại [VPC](https://console.aws.amazon.com/vpc/).
- Trên thanh điều hướng bên trái, chọn "Target groups."
- Chọn target group.
- Chọn **Action**.
- Chọn **Delete**.
- Nhập "confirm."

#### Xóa liên kết VPC trong VPC Lattice Service Networks

- Truy cập trang Bảng điều khiển Amazon VPC tại [VPC](https://console.aws.amazon.com/vpc/).
- Trên thanh điều hướng bên trái, chọn "Service networks."
- Chọn service network.
- Chọn mục **VPC associations**
- Chọn tất cả VPC liên quan đến bài thực hành.
- Chọn **Action**.
- Chọn **Delete VPC associations**.
- Nhập "confirm."

#### Xóa Service Networks

- Truy cập trang Bảng điều khiển Amazon VPC tại [VPC](https://console.aws.amazon.com/vpc/).
- Trên thanh điều hướng bên trái, chọn "Service networks."
- Chọn service network.
- Chọn **Action**.
- Chọn **Delete service network**.
- Nhập "confirm."

#### Xóa NAT gateways

- Xóa NAT Gateway và Elastic IP Address. AWS tính phí cho EIPS bị lãng phí, vì vậy bạn cần kiểm tra kỹ để tránh các khoản phí ngoài ý muốn.
- Truy cập trang Bảng điều khiển Amazon VPC tại [VPC](https://console.aws.amazon.com/vpc/).
- Trên thanh điều hướng bên trái, chọn "NAT Gateway."
- Chọn NAT Gateway.
- Chọn **Action**.
- Chọn **Delete NAT Gateway**.
- Nhập "delete."

#### Xóa VPC

- Truy cập trang Bảng điều khiển Amazon VPC tại [VPC](https://console.aws.amazon.com/vpc/).
- Trên thanh điều hướng bên trái, chọn "Your VPCs."
- Chọn tất cả VPC liên quan đến bài thực hành.
- Chọn **Action**.
- Chọn **Delete VPC**.
- Nhập "delete."

#### Xóa Elastic IP Address

- Truy cập trang Bảng điều khiển Amazon VPC tại [VPC](https://console.aws.amazon.com/vpc/).
- Trên thanh điều hướng bên trái, chọn "Elastic IP."
- Chọn tất cả địa chỉ Elastic IP chúng ta đã tạo.
- Chọn **Action**.
- Chọn **Release Elastic IP Address**.
- Chọn **Release**.
