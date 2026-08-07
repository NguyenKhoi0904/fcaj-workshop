---
title: "Worklog Tuần 2"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---


### Mục tiêu tuần 2:

* Hiểu lý thuyết về AWS Virtual Private Cloud, Compute VM on AWS, EC2 Autoscalling - EFS/FSx - Lightsail - MGN 
* Nghiên cứu cách quản lý chi phí sử dụng trên AWS.
* Tìm hiểu các yêu cầu hỗ trợ trên AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Học về khái niệm, cấu trúc, giới hạn và cách phân tách môi trường của VPC <br> - Tìm hiểu về Subnet, Quản trị mạng và kết nối, VPC Endpoint, Internet Gateway và Nat Gate Way. <br> - Tìm hiểu VPN là gì, Direct Connect, LoadBalancer, ExtraResources <br> - Tìm tòi về VPC Security và Multi-VPC Features |  29/06/2026  |  29/06/2026  | <https://www.youtube.com/watch?v=O9Ac_vGHquM&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=25> <br> <https://www.youtube.com/watch?v=BPuD1l2hEQ4&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=26> <br> <https://www.youtube.com/watch?v=CXU8D3kyxIc&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=27>
| 3   | - Học lý thuyết về EC2 Instance Type, AMI, Backup, Key Pair, Elastic Block Store, Instance Store<br>- **Thực hành:** <br>&emsp; + Quản lý chi phí sử dụng với AWS Budgets <br>&emsp; + Cách tạo yêu cầu hỗ trợ và thay đổi gói hỗ trợ với AWS Support                                            | 30/06/2026   | 30/06/2026      | <https://www.youtube.com/watch?v=e7XeKdOVq40&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=73><br>https://www.youtube.com/watch?v=yAR6QRT3N1k&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=74<br><https://www.youtube.com/watch?v=hKr_TfGP7NY&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=75><br><https://www.youtube.com/watch?v=6IHNDJ85aoQ&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=76><br><https://www.youtube.com/watch?v=_v_43Wi7zjo&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=77><br><https://000007.awsstudygroup.com/vi/> <br> <https://000009.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu lý thuyết về EC2 User data, Meta data, Auto-Scalling, LightSail, EFS/FSX, MGN <br> - **Thực hành:** <br>&emsp; + Quản lý quyền truy cập với AWS IAM <br>&emsp; +Tạo IAM Group và IAM User <br>&emsp; +Tạo IAM Role và IAM User <br>&emsp; + Chuyển đổi IAM Role <br>&emsp; + Tự tạo 1 IAM User và Policies tương ứng để phục vụ việc làm lab  |  01/07/2026  |  01/07/2026  | <https://www.youtube.com/watch?v=Ew3QRaKJQSA&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=78><br><https://www.youtube.com/watch?v=bbLcPitXJSY&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=79><br><https://www.youtube.com/watch?v=hFVYG8WqfU0&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=80><br><https://000002.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu các dịch vụ lưu trữ trên AWS: <br>&emsp; + S3, Access Point, Storage Class <br>&emsp; + S3 Static Website và CORS, Control Access, Object Key và Performance, Glacier <br>&emsp; + Snow Family, Storage Gateway, Backup |  02/07/2026  |  02/07/2026  | <https://www.youtube.com/watch?v=_yunukwcAwc&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=104><br><https://www.youtube.com/watch?v=mPBjB6Ltl_Q&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=105><br><https://www.youtube.com/watch?v=YXn8Q_Hpsu4&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=106> |
| 6   | - **Thực hành: Triển khai hạ tầng mạng với VPC** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Tạo NAT Gateway <br>&emsp; + Sử dụng Reachability Analyzer <br>&emsp; + Triển khai CloudWatch Monitoring và Alerting + Tạo cấu hình VPN <br>&emsp; + Cấu hình kết nối VPN                                                                                         | 03/07/2026   | 03/07/2026      | <https://000003.awsstudygroup.com/vi/> |


### Kết quả đạt được trong tuần 2:

* Hiểu được kiến trúc mạng trên AWS và nắm được vai trò của các thành phần trong Amazon VPC, bao gồm:: 
  * VPC
  * Public Subnet và Private Subnet
  * Internet Gateway
  * NAT Gateway
  * VPC Endpoint
  * Route Table
  * Security Group và Network ACL

* Hiểu các phương thức kết nối giữa hạ tầng on-premises và AWS thông qua:
  * VPN
  * AWS Direct Connect

* Nắm được nguyên lý hoạt động và các trường hợp sử dụng của:
  * Elastic Load Balancer (ELB)
  * Multi-VPC Architecture
  * VPC Security
  * Reachability Analyzer

* Hiểu các khái niệm và thành phần quan trọng của Amazon EC2, bao gồm:
  * EC2 Instance Types
  * Amazon Machine Image (AMI)
  * Key Pair
  * Amazon Elastic Block Store (EBS)
  * Instance Store
  * Backup cho EC2

* Tìm hiểu các dịch vụ hỗ trợ triển khai và mở rộng hệ thống trên AWS như:
  * EC2 User Data
  * EC2 Metadata
  * Auto Scaling
  * Amazon Lightsail
  * Amazon EFS
  * Amazon FSx
  * AWS Application Migration Service (MGN)

* Hiểu mô hình quản lý danh tính và phân quyền trên AWS thông qua AWS Identity and Access Management (IAM).
* Thực hành quản lý quyền truy cập với AWS IAM, bao gồm:
  * Tạo và quản lý IAM User, IAM Group, IAM Role
  * Thực hiện chuyển đổi (Switch Role) giữa các IAM Role.
  * Tự xây dựng một IAM User cùng các quyền cần thiết để phục vụ cho quá trình thực hiện các bài lab.
* Tìm hiểu các dịch vụ lưu trữ trên AWS và nắm được đặc điểm của:
  * Amazon S3
  * Amazon S3 Glacier
  * AWS Snow Family
  * AWS Storage Gateway
  * AWS Backup
* Thực hành quản lý tài khoản AWS thông qua:
  * Thiết lập và theo dõi chi phí bằng AWS Budgets.
  * Tạo yêu cầu hỗ trợ và tìm hiểu quy trình làm việc với AWS Support.
* Thực hành triển khai hạ tầng mạng trên AWS, bao gồm:
  * Tạo và cấu hình Amazon VPC.
  * Triển khai EC2 Instance trong VPC.
  * Kết nối SSH tới EC2 và cấu hình NAT Gateway cho Private Subnet.
  * Kiểm tra kết nối mạng bằng Reachability Analyzer.
  * Thiết lập giám sát và cảnh báo với Amazon CloudWatch.
  * Tạo và cấu hình kết nối Site-to-Site VPN.


