---
title : "Chia sẻ service network"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 5.1 </b> "
---

### Tạo Resource Access Manager

1. Truy cập giao diện **AWS Management Console**:
   - Định vị và nhấp vào **RAM**
   - Chọn **Resource Access Manager**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0001-shareservicenetwork.PNG?featherlight=false&width=90pc)

2. Trong giao diện **Resource Access Manager**:
   - Lựa chọn **Resource shares**
   - Bấm vào **Create resource share**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0002-shareservicenetwork.PNG?featherlight=false&width=90pc)

3. Cấu hình chi tiết chia sẻ tài nguyên:
   - Name: Nhập **vpc-lattice-service-network-rs**
   - Tìm kiếm **VPC Lattice Service Networks**
   - Lựa chọn **ARN**
   - Chọn **Resources**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0003-shareservicenetwork.PNG?featherlight=false&width=90pc)

4. Bấm vào **Next**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0004-shareservicenetwork.PNG?featherlight=false&width=90pc)

5. Bấm vào **Next**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0005-shareservicenetwork.PNG?featherlight=false&width=90pc)

6. Cấp quyền truy cập:
    - Lựa chọn **Allow sharing with anyone**
    - Chọn **AWS account** trong loại principal
    - Nhập AWS ID khác: <your_another_aws_id>

    ![Create VPC](/images/5/5.1-shareservicenetwork/0006-shareservicenetwork.PNG?featherlight=false&width=90pc)

7. Bấm vào **Next**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0007-shareservicenetwork.PNG?featherlight=false&width=90pc)

8. Bấm vào **Create resource share**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0008-shareservicenetwork.PNG?featherlight=false&width=90pc)

9. Chia sẻ tài nguyên được tạo thành công. Trạng thái của Resource ID đang là **Associating**, bây giờ chúng ta cần chuyển sang tài khoản AWS được chia sẻ và phê duyệt tài nguyên.

    ![Create VPC](/images/5/5.1-shareservicenetwork/0009-shareservicenetwork.PNG?featherlight=false&width=90pc)

10. Chuyển sang tài khoản AWS được chia sẻ. Trong giao diện **Resource Access Manager**:
    - Lựa chọn **Resource shares**
    - Bấm vào **vpc-lattice-service-network-rs**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0010-shareservicenetwork.PNG?featherlight=false&width=90pc)

11. Bấm vào **Accept resource share**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0011-shareservicenetwork.PNG?featherlight=false&width=90pc)

12. Lời mời được chấp nhận

    ![Create VPC](/images/5/5.1-shareservicenetwork/0012-shareservicenetwork.PNG?featherlight=false&width=90pc)

13. Trong giao diện **VPC**:
    - Chọn **Service networks**. Chúng ta có thể thấy service network **vpc-lattice-service-network** 

    ![Create VPC](/images/5/5.1-shareservicenetwork/0013-shareservicenetwork.PNG?featherlight=false&width=90pc)

14. Bây giờ trong tài khoản AWS của chủ tài nguyên, trạng thái của Resource ID là **Associated**

    ![Create VPC](/images/5/5.1-shareservicenetwork/0014-shareservicenetwork.PNG?featherlight=false&width=90pc)
