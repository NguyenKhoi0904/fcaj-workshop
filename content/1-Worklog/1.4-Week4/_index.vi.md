---
title: "Worklog Tuần 4"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Tìm hiểu về Database Concepts, Amazon RDS, Amazon Aurora, Redshift, Elasticache
* Thực hành về AWS CloudWatch, cấp quyền cho ứng dụng truy cập AWS với IAM Role.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | -  Tìm hiểu về: <br>&emsp;+ Database là gì? <br>&emsp;+ Các khái niệm cốt lõi <br>&emsp;+ Cơ sở dữ liệu quan hệ với cơ sở dữ liệu phi quan hệ <br>&emsp;+ OLTP (Online Transaction Processing) là gì? <br>&emsp;+ OLAP (Online Analytical Processing) là gì? <br> - **Thực hành:**<br>&emsp;+ Tạo EC2 Instance <br>&emsp;+ Tạo S3 Bucket <br>&emsp;+ Tạo IAM User và access key <br>&emsp;+ Kết nối với EC2 <br>&emsp;+ Sử dụng access key để tải file lên S3. <br>&emsp;+ Tạo IAM Role <br>&emsp;+ Sử dụng IAM Role để tải file lên S3.                                                                                               |  13/07/2026  |  13/07/2026  | <https://www.youtube.com/watch?v=OOD2RwWuLRw&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=217><br><https://000048.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu về: <br>&emsp; + Amazon RDS (Relational Database Service) <br>&emsp;+ Amazon Aurora <br>&emsp;+ Redshift là gì? <br>&emsp;+ Amazon ElastiCache là gì? <br>                                           |  14/07/2026  |  14/07/2026  | <https://www.youtube.com/watch?v=qbrobQZrokY&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=218><br><https://www.youtube.com/watch?v=UvdiRW34aNI&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=219> |
| 4   | - **Thực hành:**<br>&emsp;+ Triển khai CloudFormation Stack <br>&emsp;+ Xem các Metrics <br>&emsp;+ Thực hiện các phép tìm kiếm <br>&emsp;+ Thực hiện các phép toán học <br>&emsp;+ Tạo dynamic labels <br>&emsp;+ Tạo CloudWatch Logs <br>&emsp;+ Tạo CloudWatch Logs Insights <br>&emsp;+ Tạo CloudWatch Metric Filter <br>&emsp;+ CloudWatch Alarms <br>&emsp;+ CloudWatch Dashboards  |  15/07/2026  |  15/07/2026  | <https://000008.awsstudygroup.com/vi/> |
| 5   | - **Thực hành:**<br>&emsp;+ Tạo VPC <br>&emsp;+ Tạo EC2 Security Group <br>&emsp;+ Tạo RDS Security Group <br>&emsp;+ Tạo DB Subnet Group <br>&emsp;+ Tạo EC2 instance <br>&emsp;+ Tạo RDS database instance <br>&emsp;+ Triển khai ứng dụng <br>&emsp;+ Backup và restore                 |  16/07/2026  |  16/07/2026  | <https://000005.awsstudygroup.com/vi/> |
| 6   | - Thực hành Sagemaker Studio theo bài lab nhưng bị lỗi liên quan tới Service Quotas <br> - Tìm hiểu và sửa các lỗi liên quan tới Service Quotas như Total domains = 0, Maximum Studio user profiles = 0, Maximum running Studio apps = 0                                                                                          |  17/07/2026  |  17/07/2026  | <https://cloudjourney.awsstudygroup.com/vi/7-aimlservice/> |


### Kết quả đạt được tuần 4:

* Hiểu được các khái niệm cơ bản về cơ sở dữ liệu (Database), bao gồm:
  * Các khái niệm cốt lõi của hệ quản trị cơ sở dữ liệu.
  * Sự khác nhau giữa cơ sở dữ liệu quan hệ (Relational Database) và phi quan hệ (NoSQL Database).
  * Mô hình xử lý giao dịch trực tuyến (OLTP).
  * Mô hình xử lý phân tích trực tuyến (OLAP).
* Nắm được chức năng và các trường hợp sử dụng của các dịch vụ cơ sở dữ liệu trên AWS, bao gồm:
  * Amazon RDS.
  * Amazon Aurora.
  * Amazon Redshift.
  * Amazon ElastiCache.
* Thực hành quản lý quyền truy cập tài nguyên AWS thông qua:
  * IAM User và Access Key.
  * IAM Role.
  * Truy cập Amazon S3 từ EC2 bằng Access Key và IAM Role.
* Hiểu được ưu điểm của việc sử dụng IAM Role so với Access Key khi cấp quyền cho các tài nguyên AWS.
* Thực hành sử dụng AWS CloudFormation để triển khai hạ tầng theo mô hình Infrastructure as Code (IaC).
* Thực hành giám sát và theo dõi hệ thống với Amazon CloudWatch, bao gồm:
  * Theo dõi Metrics.
  * Phân tích CloudWatch Logs và Logs Insights.
  * Tạo Metric Filter.
  * Cấu hình CloudWatch Alarms.
  * Xây dựng CloudWatch Dashboards.
* Thực hành triển khai ứng dụng sử dụng Amazon RDS, bao gồm:
  * Tạo VPC và Security Group.
  * Tạo DB Subnet Group.
  * Khởi tạo EC2 Instance và RDS Database Instance.
  * Kết nối ứng dụng với cơ sở dữ liệu.
  * Thực hiện sao lưu (Backup) và khôi phục (Restore) dữ liệu.
* Làm quen với Amazon SageMaker Studio và tìm hiểu cơ chế quản lý Service Quotas của AWS.
* Xác định và phân tích nguyên nhân các lỗi liên quan đến Service Quotas trong SageMaker Studio, như:
  * Total Domains.
  * Maximum Studio User Profiles.
  * Maximum Running Studio Apps.
