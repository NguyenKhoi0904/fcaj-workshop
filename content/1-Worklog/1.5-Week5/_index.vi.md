---
title: "Worklog Tuần 5"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---


### Mục tiêu tuần 5:

* Thực hành về Amazon SageMaker, AWS CLI
* Làm Project kỹ thuật
* Làm FCAJ workshop

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - **Thực hành:**<br>&emsp;+ Tạo SageMaker Studio <br>&emsp;+ Chuẩn bị Dataset <br>&emsp;+ Cài đặt Data Wrangler <br>&emsp;+ Phân tích Dataset <br>&emsp;+ Phân tích tương quan <br>&emsp;+ Chuyển đổi dữ liệu <br>&emsp;+ Feature Store <br>&emsp;+ Export Data tới S3 <br>&emsp;+ Train & Tune model <br>&emsp;+ Deploy model <br>&emsp;+ Đánh giá hiệu suất model <br>&emsp;+ Tune model tự động                                                                                             |  20/07/2026  |  20/07/2026  | <https://cloudjourney.awsstudygroup.com/vi/7-aimlservice/> |
| 3   | - Tìm hiểu Amazon Textract (OCR file scan/ảnh) <br>- **Thực hành:** Lambda poll message từ SQS và xử lý file                                            |  21/07/2026  |  21/07/2026  |  |
| 4   | - Viết Worklog tuần 1, event 1, blog 1 |  22/07/2026  |  22/07/2026  |  |
| 5   | - **Thực hành:**<br>&emsp;+ Khởi tạo EC2 Instance <br>&emsp;+ Cài đặt AWS CLI <br>&emsp;+ Kiểm tra tài nguyên qua CLI <br>&emsp;+ Sử dụng AWS CLI để khởi tạo tài nguyên S3 <br>&emsp;+ Sử dụng AWS CLI với Amazon SNS <br>&emsp;+ Sử dụng AWS CLI với IAM <br>&emsp;+ Sử dụng AWS CLI với VPC <br>&emsp;+ Sử dụng AWS CLI với Internet Gateway <br>&emsp;+ Tạo EC2 sử dụng AWS CLI                 |  23/07/2026  |  23/07/2026  | <https://000011.awsstudygroup.com/vi/> |
| 6   | - Build hoàn chỉnh Luồng 1 – S3 (upload) → S3 Event → SQS (buffer + retry) → Lambda (Document Processor) → OCR nếu là file scan                                                                                         |  24/07/2026  |  24/07/2026  |  |


### Kết quả đạt được tuần 5:

* Thực hành quy trình xây dựng và triển khai mô hình Machine Learning trên Amazon SageMaker, bao gồm:
    * Khởi tạo SageMaker Studio.
    * Chuẩn bị và phân tích Dataset.
    * Sử dụng SageMaker Data Wrangler để xử lý và chuyển đổi dữ liệu.
    * Phân tích tương quan giữa các đặc trưng.
    * Quản lý Feature với SageMaker Feature Store.
    * Export dữ liệu lên Amazon S3.
    * Train và Tune model.
    * Deploy model.
    * Đánh giá hiệu suất model.
    * Thực hiện tự động hóa quá trình Model Tuning.
* Hiểu được quy trình cơ bản của Machine Learning Workflow trên AWS, từ bước chuẩn bị và xử lý dữ liệu đến huấn luyện, tối ưu, triển khai và đánh giá mô hình.
* Sử dụng AWS CLI để kiểm tra và quản lý tài nguyên AWS, bao gồm:
    * Amazon S3.
    * Amazon SNS.
    * AWS IAM.
    * Amazon VPC.
    * Internet Gateway.
    * Amazon EC2.
* Thực hành khởi tạo và quản lý AWS resources bằng AWS CLI, qua đó hiểu rõ hơn cách sử dụng CLI bên cạnh AWS Management Console.
* Hoàn thành Worklog tuần 1, Event 1 và Blog 1, qua đó rèn luyện khả năng ghi chép, tổng hợp và trình bày lại kiến thức đã học trong chương trình FCAJ.
* Hiểu và triển khai được kiến trúc event-driven cơ bản: S3 Event → SQS → Lambda.
* Tự động OCR được file ảnh/scan bằng Amazon Textract.


