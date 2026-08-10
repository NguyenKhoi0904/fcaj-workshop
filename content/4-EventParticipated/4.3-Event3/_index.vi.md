---
title: "Event 3"
date: 2026-01-01
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch sự kiện “Agent Forge - Deepdive Day 2”

**Thời gian:** 9:00AM - 12:00PM, Thứ 7, 08/08/2026
**Địa điểm:** Tầng 26, Bitexco Financial Tower, 2 Đ. Hải Triều, Sài Gòn, Hồ Chí Minh 700000, Việt Nam.
**Vai trò:** Người tham dự
**Các diễn giả:** <br>
- Nghia Tran - Agentic SA
- Anh Pham - Cloud Consultant G-AsiaPacific Vietnam

##### Nội dung chính:
Phần lý thuyết bao gồm các phần chính sau:
- **Memory**
    - Memory giúp Agent lưu giữ thông tin, vượt qua giới hạn context window và cá nhân hóa trải nghiệm.
    - Short-term Memory: lưu dữ liệu thô từ hội thoại, đồng bộ để truy xuất nhanh thông tin gần nhất.
    - Long-term Memory: trích xuất insight và tri thức từ hội thoại, chuyển thành vector để lưu trữ lâu dài.
    - Memory Strategies: gồm Summary, User Preference, Semantic và Episodic.
    - Namespace: tổ chức dữ liệu theo cấu trúc phân cấp như /Strategy/Actor/Session, giúp thu hẹp phạm vi tìm kiếm, giảm token và tăng tốc truy xuất.
- **Evaluations**
    - Evaluations đảm bảo Agent hoạt động chính xác, hữu ích và an toàn, đồng thời phát hiện hallucination, lỗi reasoning và lựa chọn tool không phù hợp.
    - Có hai chế độ:
        - On-demand Evaluation: đánh giá chủ động trong quá trình development.
        - Online Evaluation: giám sát liên tục trong production thông qua telemetry và metrics.
    - Đánh giá được thực hiện ở ba cấp:
        - Session level: đánh giá toàn bộ phiên.
        - Trace level: đánh giá từng response.
        - Span level: đánh giá việc sử dụng tool và parameters.
    - Hệ thống sử dụng Judge để phân tích hoạt động của Agent, sau đó đưa kết quả vào Observability để SME theo dõi và can thiệp.
- **Observability**
    - Observability giúp developer hiểu, debug và tối ưu hoạt động bên trong của Agent.
    - Ba thành phần chính:
        - Logs: cho biết điều gì đã xảy ra.
        - Traces: cho biết quá trình xảy ra như thế nào.
        - Metrics: đo lường tác động như latency, token cost và error rate.
    - Ngoài ra có OpenTelemetry, monitoring thời gian thực, alert và cơ chế phân cấp dữ liệu theo Session → Trace → Span/Sub-span.
- **AgentCore Components**
    - Các component chính gồm:
        - **Registry:** trung tâm quản lý và tái sử dụng Agent skills, tools và APIs; hỗ trợ Admin, Publisher và Consumer.
        - **Harness:** framework tối giản để khởi tạo Agent từ Model + System Prompt + Tool, đồng thời hỗ trợ khả năng mở rộng.
        - **Tools:** giúp Agent tương tác với hệ thống bên ngoài, thực hiện actions và truy cập dữ liệu/API thời gian thực.
        - **Payments:** cho phép Agent thực hiện thanh toán, hiện hỗ trợ Stripe và Coinbase.
        - **Optimization:** sử dụng dữ liệu từ Evaluation và Observability để tìm điểm cần cải thiện, hỗ trợ A/B testing, Red Teaming và self-optimizing loop.
        - **Policy:** lớp kiểm soát hành vi, bảo mật và compliance của Agent; hỗ trợ Human-in-the-loop, Cedar, Strict/Permissive mode và nguyên tắc Least Privilege.

Phần thực hành:  Hướng dẫn kỹ thuật triển khai với Agent SDK, thiết lập AWS Bedrock, và cách sử dụng công cụ dòng lệnh (CLI) để tạo project, deploy và test Agent trên AWS.
#### Bài học rút ra
Qua sự kiện Agent Forge - Deepdive Day 2, em hiểu rõ hơn về các thành phần cần thiết để xây dựng và vận hành một AI Agent trong môi trường production, đặc biệt là vai trò của Memory, Evaluations và Observability trong việc duy trì ngữ cảnh, đánh giá chất lượng và giám sát hoạt động của Agent. Không chỉ thế, em cũng hiểu được cách các thành phần của AgentCore như Registry, Harness, Tools, Policy và Optimization phối hợp với nhau để quản lý, mở rộng, bảo mật và liên tục cải thiện Agent. Đặc biệt, em nhận thức được tầm quan trọng của Least Privilege và Human-in-the-loop trong việc kiểm soát các hành động của Agent. Cuối cùng, phần thực hành giúp em làm quen với Agent SDK, AWS Bedrock và AWS CLI, đồng thời hiểu được quy trình cơ bản từ khởi tạo project, triển khai đến kiểm thử Agent trên AWS.

#### Một số hình ảnh khi tham gia sự kiện
<img src="/fcaj-workshop/images/AWS_Event_3_01.jpg" alt="My profile" width="50%">

