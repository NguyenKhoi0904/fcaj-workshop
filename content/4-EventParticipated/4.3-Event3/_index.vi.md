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
    - Đóng vai trò là cầu nối quan trọng giúp Agent lưu giữ thông tin, vượt qua giới hạn của context window (cửa sổ ngữ cảnh) để cá nhân hóa trải nghiệm.
    - Short-term Memory (Bộ nhớ ngắn hạn)
        - Lưu trữ dữ liệu thô (raw data) từ các sự kiện hội thoại như tin nhắn giữa người dùng và Agent.
        - Cơ chế hoạt động: Đồng bộ (synchronous) để đảm bảo cuộc hội thoại diễn ra liền mạch.
        - Mục đích là giúp Agent truy xuất nhanh các thông tin vừa trao đổi gần nhất.
    - Long-term Memory (Bộ nhớ dài hạn)
        - Trích xuất các ý chính (*insights*) và tri thức từ hội thoại, sau đó chuyển đổi thành dạng *vector* để lưu trữ.
        - Giúp Agent "nhớ" được sở thích, tính cách hoặc các yêu cầu đặc thù của người dùng ngay cả sau một thời gian dài.
    - Các chiến lược lưu trữ (Memory Strategies)
        - Summary: Nén các cuộc hội thoại lớn thành các đoạn tóm tắt để tiết kiệm token và tối ưu chi phí.
        - User Preference: Lưu trữ các mẫu hình hành vi và sở thích của người dùng để cá nhân hóa.
        - Semantic: Lưu trữ các kiến thức chuyên môn hoặc các định nghĩa về lĩnh vực cụ thể.
        - Episodic: Ghi lại các hành động và quyết định của Agent để nó tự học hỏi và hoàn thiện.
    - Quản lý dữ liệu bằng Namespace
        - Để tổ chức dữ liệu hiệu quả, hệ thống sử dụng Namespace theo cấu trúc phân cấp (giống như thư mục trên máy tính): /Strategy/Actor/Session. Việc phân loại này giúp Agent thu hẹp phạm vi tìm kiếm dữ liệu, từ đó giảm thiểu số lượng token tiêu thụ và tăng tốc độ truy xuất thông tin.
- **Evaluations**
    - Là lớp bảo mật và kiểm chứng chất lượng quan trọng để đảm bảo Agent hoạt động chính xác, hữu ích và đạt được mục tiêu đề ra. Nếu không có quy trình đánh giá, Agent dễ gặp phải các lỗi như ảo giác (hallucination), lập luận sai hoặc lựa chọn công cụ không phù hợp.
    - Vai trò của Evaluations:
        - Đánh giá năng lực của Agent trong việc giải quyết tác vụ.
        - Xác định các điểm thất bại (*point of failure*) trong quá trình tư duy, lập kế hoạch và thực thi của Agent.
        - Cung cấp cơ sở dữ liệu để tinh chỉnh (*fine-tune*) và cải thiện Agent trước khi đưa lên môi trường sản xuất (production).
    - Các chế độ vận hành:
        - On-demand Evaluation: Thường được sử dụng trong giai đoạn phát triển (*development*). Developer chủ động kích hoạt đánh giá để kiểm tra hiệu năng trước khi triển khai thực tế.
        - Online Evaluation: Giám sát liên tục (*real-time monitor*) trên môi trường production. Hệ thống sử dụng *telemetry* để thu thập log, dựa vào các chỉ số (metrics) để đánh giá chất lượng phản hồi tức thời.
    - Các cấp độ đánh giá:
        - Session level: Đánh giá mục tiêu tổng thể của toàn bộ phiên trò chuyện.
        - Trace level: Đánh giá độ chính xác, tính hữu ích và mức độ an toàn của từng câu trả lời đơn lẻ.
        - Span level: Đánh giá việc sử dụng công cụ (*tool usage*) và các tham số truyền vào có tối ưu hay không.
    - Cơ chế đánh giá:
        - Hệ thống sử dụng Judge (Giám khảo)—thường là một mô hình AI khác—để phân tích step-by-step logic của Agent. Kết quả đánh giá sẽ được ghi nhận vào lớp Observability để người quản trị (SME - Subject Matter Expert) có thể theo dõi và can thiệp kịp thời.
- **Observability**
    - Được ví như "đôi mắt" của hệ thống. Nó cho phép lập trình viên nhìn thấu vào bên trong cách thức hoạt động của Agent, giúp gỡ lỗi (debug), theo dõi hiệu năng và cải thiện hệ thống.
    - Ba trụ cột chính của Observability
        - Logs: Lưu lại các sự kiện cụ thể, các *request* và phản hồi, giúp xác định "điều gì đã xảy ra".
        - Traces: Theo dõi toàn bộ hành trình của một yêu cầu từ khi người dùng bắt đầu gửi *prompt* cho đến khi Agent đưa ra phản hồi cuối cùng, giúp hiểu "làm thế nào nó xảy ra".
        - Metrics: Các chỉ số đo lường như chi phí (*token cost*), độ trễ (*latency*), và tỷ lệ lỗi (*error rate*), giúp đánh giá "ảnh hưởng như thế nào" đến hệ thống.
    - Các tính năng nổi bật:
        - Open Telemetry: Sử dụng giao thức mã nguồn mở để thu thập và chuẩn hóa dữ liệu từ các thành phần khác nhau trong hệ sinh thái *Agent Core.*
        - Giám sát thời gian thực: Cho phép quản trị viên xem biểu đồ trạng thái của Agent, từ đó thiết lập các cảnh báo (*alert*) tự động. Nếu tài nguyên như CPU hay GPU vượt ngưỡng cho phép, hệ thống có thể tự động điều chỉnh hoặc thông báo để can thiệp kịp thời.
        - Quản lý phân cấp: Dữ liệu được tổ chức theo cấp độ *Session* (phiên làm việc), *Trace* (truy vết), và *Span/Sub-span* (chi tiết thực thi), giúp việc tìm kiếm thông tin trở nên dễ dàng và hiệu quả hơn.
- AgentCore Components
    - Registry
        - Đóng vai trò là một trung tâm quản trị tập trung. Đây là giải pháp giải quyết bài toán về khả năng tái sử dụng (reusability) và quản lý tài nguyên trong các doanh nghiệp có quy mô lớn với nhiều nhóm phát triển khác nhau.
        - Vai trò của Registry:
            - Quản trị tập trung: Thay vì mỗi nhóm tự phát triển và lưu trữ cục bộ, các *Agent skill*, *tool*, và *API* sẽ được đăng ký lên *Registry* để mọi thành viên trong tổ chức có thể khám phá và sử dụng lại.
            - Giải quyết sự phân mảnh: Giúp tổ chức kiểm soát được ai đang phát triển cái gì, tránh tình trạng phát triển trùng lặp hoặc không biết tìm kiếm các *component* đã có sẵn ở đâu.
            - Hỗ trợ đa giao thức: *Registry* có khả năng vận hành linh hoạt với nhiều loại giao thức khác nhau như *RESTful*, *MCB* (Model Context Protocol), hoặc *A2A* (Agent-to-Agent).
        - Các vai trò người dùng trong Registry:
            - Admin: Người quản trị hệ thống, thiết lập quyền truy cập và giám sát toàn bộ tài nguyên.
            - Publisher: Các lập trình viên hoặc nhóm phát triển đưa (đẩy) các bộ *skill* hoặc *tool* đã hoàn thiện lên hệ thống.
            - Consumer: Các nhóm khác hoặc các *Agent* khác sử dụng các tài nguyên đã được đăng ký để tích hợp vào quy trình của họ.
    - Harness
        - Đóng vai trò là cơ chế tối giản giúp khởi tạo và vận hành một Agent một cách nhanh chóng và hiệu quả.
        - Vai trò của Harness:
            - Khởi tạo tối giản: Thay vì phải cấu hình phức tạp, *Harness* cho phép tạo ra một Agent độc lập chỉ với 3 thành phần cốt lõi: Model (mô hình ngôn ngữ), System Prompt (chỉ dẫn hệ thống), và Tool (công cụ thực thi).
            - Khả năng mở rộng (Scalability): *Harness* hoạt động như một khung sườn (framework) giúp phân tách Agent thành các thành phần microservice. Điều này cho phép hệ thống mở rộng theo chiều ngang (*horizontally scalable*) tương tự như cách xây dựng các ứng dụng phần mềm hiện đại.
            - Tích hợp hệ sinh thái: Sau khi được khởi tạo, Agent thông qua *Harness* có thể tự do khám phá và kết nối với các dịch vụ khác trong hệ sinh thái *Agent Core* như *Gateway*, *Browser* (để tìm kiếm), hoặc *Code Interpreter* (để thực thi code) mà không cần cấu hình thủ công quá nhiều ngay từ đầu.
    - Tools
        - Đóng vai trò là "cánh tay nối dài" giúp Agent tương tác và thực hiện các tác vụ bên ngoài môi trường ngôn ngữ thuần túy.
        - Vai trò của Tools:
            - Thực thi hành động: Cho phép Agent thực hiện các yêu cầu cụ thể như tra cứu thông tin, gửi email, tạo đơn hàng, hoặc gọi các API bên thứ ba.
            - Mở rộng khả năng: Thay vì chỉ suy luận dựa trên dữ liệu huấn luyện, Agent sử dụng *Tool* để truy cập dữ liệu thời gian thực hoặc tương tác với hạ tầng hệ thống (ví dụ: Lambda functions).
            - Cấu trúc linh hoạt: Trong hệ sinh thái *Agent Core*, các *Tool* được quản lý tập trung thông qua lớp *Gateway*, giúp việc kết nối và sử dụng trở nên bảo mật và dễ quản lý.
        - Cách thức hoạt động:
            - Quyết định (Reasoning): Khi nhận yêu cầu từ người dùng, Agent phân tích và xác định cần dùng *Tool* nào để hoàn thành nhiệm vụ.
            - Triệu gọi (Invocation): Agent gọi hàm tương ứng (ví dụ: thông qua *Lambda*) để thực hiện logic nghiệp vụ.
            - Phản hồi (Response): Kết quả từ *Tool* được trả về cho Agent, sau đó Agent tổng hợp kết quả này để tạo câu trả lời cuối cùng cho người dùng.
    - Payments
        - Được thiết kế để cho phép các Agent thực hiện các tác vụ thanh toán trực tiếp.
        - Các đặc điểm chính:
            - Hiện tại, hệ thống hỗ trợ tích hợp với hai cổng thanh toán phổ biến toàn cầu là Stripe và Coinbase.
            - Dịch vụ này tạo ra môi trường để Agent có thể trực tiếp xử lý các giao dịch tài chính, giúp tự động hóa quy trình thanh toán trong các ứng dụng thương mại điện tử hoặc dịch vụ khách hàng.
            - Mặc dù tích hợp sẵn các cổng lớn, hệ thống vẫn cho phép mở rộng để hỗ trợ các phương thức thanh toán tại địa phương (như ví điện tử hoặc mã QR) tùy theo nhu cầu của từng thị trường cụ thể.
    - Optimization
        - Đóng vai trò then chốt giúp Agent không chỉ hoạt động ổn định mà còn liên tục cải thiện hiệu suất sau khi đã được triển khai.
        - Vai trò chính của Optimization:
            - Phân tích thông minh: Dựa trên dữ liệu từ *Observability* (quan sát) và kết quả từ *Evaluation* (đánh giá), hệ thống sẽ phân tích các luồng giao tiếp và hành vi của Agent để tìm ra điểm nghẽn hoặc khu vực cần cải thiện.
            - Đề xuất cải tiến: Tự động đưa ra các khuyến nghị để tinh chỉnh cách Agent phản hồi, lựa chọn công cụ, hoặc tối ưu hóa chi phí (ví dụ: điều chỉnh tham số mô hình để giảm lượng *token* không cần thiết).
            - Kiểm thử A/B: Hỗ trợ quy trình kiểm thử các biến thể của Agent nhằm tìm ra phiên bản tối ưu nhất trước khi áp dụng thay đổi rộng rãi.
        - Các tính năng bổ trợ:
            - Một tính năng quan trọng trong nhóm tối ưu hóa là *Red Teaming* (kiểm thử bảo mật đối nghịch). Nó cho phép nhà phát triển mô phỏng các cuộc tấn công hoặc tình huống gây lỗi để kiểm tra lỗ hổng bảo mật và độ bền vững của Agent.
            - Vòng lặp tự học: Optimization tạo ra một vòng lặp phản hồi giúp hệ thống "tự hoàn thiện" (self-optimizing) thông qua việc phân tích log thực tế, giúp Agent ngày càng thông minh hơn theo thời gian.
    - Policy
        - Đóng vai trò là lớp kiểm soát an toàn và tuân thủ, giúp thiết lập các quy tắc nghiêm ngặt để quản lý hành vi của Agent trong môi trường thực tế.
        - Vai trò chính của Policy:
            - Quản trị hành vi: Trả lời cho các câu hỏi quan trọng như: Ai được phép làm gì và làm khi nào? Nó hoạt động như một bộ lọc ngăn chặn các hành động không mong muốn trước khi chúng được thực thi.
            - Human-in-the-loop: Cho phép tích hợp con người vào quy trình ra quyết định. Ví dụ: đối với các tác vụ nhạy cảm như hoàn tiền (*refund*) vượt hạn mức, Agent có thể tạm dừng và chờ sự phê duyệt từ quản trị viên.
            - Ngôn ngữ chính sách (Cedar): *Policy* được phát triển dựa trên ngôn ngữ *Cedar*, cho phép nhà phát triển định nghĩa các quy tắc bằng ngôn ngữ tự nhiên (tiếng Anh) rồi tự động biên dịch sang mã chính sách máy tính, giúp việc thiết lập trở nên đơn giản và dễ hiểu.
        - Các đặc điểm kỹ thuật:
            - Tính linh hoạt: Có hai chế độ vận hành là *Strict* (chặt chẽ, dùng cho môi trường sản xuất) và *Permissive* (thoải mái hơn, dùng cho kiểm thử).
            - Nguyên tắc đặc quyền tối thiểu (*Least Privilege*): Áp dụng cơ chế chỉ cấp những quyền tối thiểu cần thiết để Agent hoàn thành công việc, giảm thiểu tối đa rủi ro bảo mật.
            - Cấu hình tại lớp Gateway: *Policy* thường được thiết lập tại tầng *Gateway*, cho phép quản lý tập trung cho toàn bộ hệ thống Agent trong doanh nghiệp.

Phần thực hành:  Hướng dẫn kỹ thuật triển khai với Agent SDK, thiết lập AWS Bedrock, và cách sử dụng công cụ dòng lệnh (CLI) để tạo project, deploy và test Agent trên AWS.
#### Bài học rút ra
Qua sự kiện Agent Forge - Deepdive Day 2, em hiểu rõ hơn về các thành phần cần thiết để xây dựng và vận hành một AI Agent trong môi trường production, đặc biệt là vai trò của Memory, Evaluations và Observability trong việc duy trì ngữ cảnh, đánh giá chất lượng và giám sát hoạt động của Agent. Không chỉ thế, em cũng hiểu được cách các thành phần của AgentCore như Registry, Harness, Tools, Policy và Optimization phối hợp với nhau để quản lý, mở rộng, bảo mật và liên tục cải thiện Agent. Đặc biệt, em nhận thức được tầm quan trọng của Least Privilege và Human-in-the-loop trong việc kiểm soát các hành động của Agent. Cuối cùng, phần thực hành giúp em làm quen với Agent SDK, AWS Bedrock và AWS CLI, đồng thời hiểu được quy trình cơ bản từ khởi tạo project, triển khai đến kiểm thử Agent trên AWS.

#### Một số hình ảnh khi tham gia sự kiện
* Thêm các hình ảnh của các bạn tại đây
> Tổng thể, sự kiện không chỉ cung cấp kiến thức kỹ thuật mà còn giúp tôi thay đổi cách tư duy về thiết kế ứng dụng, hiện đại hóa hệ thống và phối hợp hiệu quả hơn giữa các team.
