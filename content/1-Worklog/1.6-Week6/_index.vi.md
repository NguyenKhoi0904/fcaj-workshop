---
title: "Worklog Tuần 6"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---


### Mục tiêu tuần 6:
* Làm project kỹ thuật
* Tiếp tục viết FCAJ workshop

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Sync nhanh với nhóm trước khi bắt đầu.<br>- Tìm hiểu Amazon Cognito: tạo User Pool, App Client (không dùng client secret vì gọi từ frontend), gắn Cognito Authorizer vào API Gateway.                                            |  27/07/2026  |  27/07/2026  |  |
| 3   | - Thống nhất với nhóm mục tiêu ngày hôm nay.<br>- Nghiên cứu Amazon ElastiCache Serverless & Semantic Cache (tính embedding câu hỏi mới, so sánh cosine similarity với ngưỡng threshold)                                            |  28/07/2026  |  28/07/2026  |  |
| 4   | - Viết Worklog tuần 2, 3, 4 và Blog posted 1                                            |  29/07/2026  |  29/07/2026  |  |
| 5   | - **Thực hành:**<br>&emsp;+ Tạo S3 bucket <br>&emsp;+ Tải dữ liệu <br>&emsp;+ Bật tính năng static website <br>&emsp;+  Cấu hình Block Public Access <br>&emsp;+ Cấu hình public object <br>&emsp;+ Kiểm Tra Website <br>&emsp;+ Chặn tất cả truy cập công cộng vào S3 <br>&emsp;+ Cấu hình Amazon CloudFront <br>&emsp;+ Kiểm tra Amazon CloudFront <br>&emsp;+ Bucket Versioning <br>&emsp;+  Di chuyển Object <br>&emsp;+ Sao chép S3 Object sang region khác                                           |  30/07/2026  |  30/07/2026  | <https://000057.awsstudygroup.com/vi/> |
| 6   | - Thiết kế luồng: Câu hỏi → Embedding → Tra Redis (ElastiCache) → Nếu miss mới đi tiếp retrieval + Bedrock.                                            |  31/07/2026  |  31/07/2026  |  |


### Kết quả đạt được tuần 6:
* Tiếp tục thực hiện technical projects đồng thời vận dụng các kiến thức về AWS, Cloud vào quá trình phát triển project.
* Thực hành quản lý và triển khai website tĩnh với Amazon S3, bao gồm:
    * Tạo và cấu hình S3 Bucket.
    * Upload dữ liệu lên S3.
    * Bật tính năng Static Website Hosting.
    * Cấu hình Block Public Access.
    * Cấu hình quyền truy cập public cho Object.
    * Kiểm tra hoạt động của website.
    * Chặn lại toàn bộ truy cập công cộng vào S3.
* Nắm được cách sử dụng Amazon CloudFront để phân phối nội dung từ S3 và thực hành:
    * Cấu hình CloudFront Distribution.
    * Kiểm tra hoạt động của website thông qua CloudFront.
* Thực hành quản lý phiên bản và dữ liệu trên Amazon S3, bao gồm:
    * Bật và sử dụng Bucket Versioning.
    * Di chuyển S3 Object.
    * Sao chép S3 Object sang AWS Region khác.
* Hiểu được cách kết hợp Amazon S3 và Amazon CloudFront để triển khai và phân phối một website tĩnh, đồng thời nâng cao khả năng quản lý quyền truy cập và bảo vệ dữ liệu trên S3.
* Hoàn thành Worklog tuần 2, tuần 3, tuần 4, Blog Posted 1
* Tiếp tục rèn luyện kỹ năng triển khai và quản lý tài nguyên AWS thông qua các bài thực hành và technical project trong chương trình FCAJ.

