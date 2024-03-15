---
title : "Services"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 1.2 </b> "
---

## Services

Trong VPC Lattice, một dịch vụ (service) là một đơn vị phần mềm triển khai độc lập, cung cấp một tác vụ hoặc chức năng cụ thể.

Dịch vụ có thể chạy trên các instance, container hoặc là hàm serverless trong cùng một tài khoản hoặc một VPC. Mỗi dịch vụ có một listener sử dụng các quy tắc, gọi là listener rules, để định tuyến lưu lượng đến các đích (target) của nó. Các đích này có thể là instance EC2, địa chỉ IP, hàm Lambda serverless, Bộ cân bằng tải ứng dụng (Application Load Balancers) hoặc Pod Kubernetes. Chúng ta có thể liên kết một dịch vụ với nhiều mạng dịch vụ khác nhau.

![Services](/images/1/0003-introduce.png?featherlight=false&width=50pc)
