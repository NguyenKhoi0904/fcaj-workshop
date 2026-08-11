---
title: "Worklog Tuần 7"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---


### Mục tiêu tuần 7:
* Hoàn thành project kỹ thuật
* Tiếp tục hoàn thiện workshop

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Kết nối AWS Chatbot với Slack Workspace của nhóm — xử lý bước OAuth authorize Slack (nhờ trưởng nhóm cấp quyền admin workspace).                                            |  03/08/2026  |  03/08/2026  |  |
| 3   | - Tạo các CloudWatch Alarm riêng biệt: Lambda Errors (ngưỡng > 5 lỗi/5 phút → Warning), API Gateway 5xx (ngưỡng tương tự → Warning)                                            |  04/08/2026  |  04/08/2026  |  |
| 4   | - Tìm hiểu sâu framework RAGAS — cụ thể là cách 3 chỉ số được tính: Faithfulness đo mức độ câu trả lời có bám sát nội dung context được truy xuất (dùng chính LLM để chấm chéo), Answer Relevancy đo câu trả lời có đúng trọng tâm câu hỏi, Context Precision đo chất lượng của bước retrieval.                                            |  05/08/2026  |  05/08/2026  |  |
| 5   | - Dùng script gửi 50 request đồng thời tới API Gateway để xem hệ thống phản ứng ra sao. <br> - Phát hiện ElastiCache Serverless xử lý tốt nhưng Lambda Chat Engine bị giới hạn concurrency mặc định (1000)                                            |  06/08/2026  |  06/08/2026  |  |
| 6   | - Viết worklog tuần 5, 6, 7 event 2, blog posted 2                                            |  07/08/2026  |  07/08/2026  |  |


### Kết quả đạt được tuần 7:
* Tiếp tục triển khai technical project, đồng thời vận dụng các kiến thức đã học về AWS, Cloud vào quá trình xây dựng project.
* Củng cố kỹ năng phân tích yêu cầu, triển khai và xử lý các vấn đề phát sinh trong quá trình thực hiện technical project.
* Tiếp tục nâng cao khả năng sử dụng các dịch vụ và công cụ AWS thông qua quá trình thực hành và phát triển project.
* Hoàn thành Worklog tuần 5, tuần 6, tuần 7, Event 2 và Blog Posted 2, qua đó tổng hợp và hệ thống hóa lại các kiến thức, kỹ năng đã học và kết quả đạt được trong quá trình tham gia chương trình FCAJ.
* Duy trì tiến độ thực hiện technical project và chuẩn bị nền tảng cho các công việc tiếp theo.