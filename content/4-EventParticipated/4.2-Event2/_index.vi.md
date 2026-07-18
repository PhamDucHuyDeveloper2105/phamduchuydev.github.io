---

title: "Event 2"
date: 2026-06-06
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
----------------------

# BÀI THU HOẠCH SỰ KIỆN “SATURDAY MEET UP Ngày 06 Tháng 06 Năm 2026"

## Mục đích của sự kiện

* Tìm hiểu các ứng dụng thực tế của AWS trong nhiều lĩnh vực như game, hệ thống, dữ liệu, DevOps và bảo mật.
* Mở rộng kiến thức về Cloud Computing thông qua các chủ đề như WebSocket, Serverless, Graph Database, Docker và AWS WAF.
* Lắng nghe kinh nghiệm nghề nghiệp từ IT Helpdesk đến Senior Sysadmin và định hướng chuyển sang Cloud/DevOps.
* Hiểu thêm vai trò của teamwork trong quá trình học tập, làm project và phát triển sản phẩm.
* Tìm hiểu cách AI và Machine Learning có thể được ứng dụng trong GraphRAG và phát hiện tấn công mạng.

## Danh sách chủ đề và diễn giả

| STT | Chủ đề                                                                    | Diễn giả         | Nội dung chính                                                                     |
| --- | ------------------------------------------------------------------------- | ---------------- | ---------------------------------------------------------------------------------- |
| 1   | Multiplayer in the Cloud: Connecting Godot Clients with AWS WebSockets    | Nguyễn Quốc Bảo  | Xây dựng multiplayer game bằng Godot kết hợp AWS WebSocket, Lambda và DynamoDB.    |
| 2   | From IT Helpdesk to Senior Sysadmin                                       | Vinh Trần        | Chia sẻ lộ trình từ IT Helpdesk đến Sysadmin và chuyển hướng sang Cloud/DevOps.    |
| 3   | The Art of Effective Teamwork                                             | Trương Phước     | Trình bày các nguyên tắc giúp làm việc nhóm hiệu quả.                              |
| 4   | AWS Neptune for Building a Graph Knowledge Base for GraphRAG              | Việt Phát        | Giới thiệu GraphRAG, Amazon Neptune và cách xây dựng knowledge base dạng graph.    |
| 5   | Docker - A Containerization Technology                                    | Bảo Huỳnh        | Tìm hiểu Docker, containerization và vai trò của Docker trong phát triển phần mềm. |
| 6   | Combining AWS WAF with Machine Learning for Cyber Attack Detection on AWS | Lê Hoàng Gia Đại | Kết hợp AWS WAF và Machine Learning để phát hiện tấn công mạng trên AWS.           |

## Nội dung nổi bật

### Multiplayer in the Cloud: Connecting Godot Clients with AWS WebSockets

* Bài trình bày giới thiệu cách xây dựng một hệ thống multiplayer đơn giản trên cloud.
* Godot client có thể kết nối đến backend thông qua WebSocket.
* AWS API Gateway WebSocket được sử dụng để duy trì kết nối giữa client và backend.
* AWS Lambda xử lý logic như kết nối người chơi, matchmaking và kết quả trò chơi.
* DynamoDB được dùng để lưu trạng thái người chơi như connection ID, trạng thái chờ và thông tin đối thủ.
* Nội dung giúp người tham gia hiểu cách AWS có thể hỗ trợ các ứng dụng realtime ở mức cơ bản.

### From IT Helpdesk to Senior Sysadmin

* Bài chia sẻ tập trung vào lộ trình phát triển nghề nghiệp trong lĩnh vực IT Infrastructure.
* IT Helpdesk là nền tảng tốt để rèn luyện tư duy troubleshooting và kỹ năng giao tiếp với người dùng.
* Để phát triển lên Sysadmin, cần học thêm Linux, Networking, Server, Monitoring và Security.
* Khi chuyển sang Cloud/DevOps, cần làm quen với automation, Infrastructure as Code, CI/CD, Docker và cloud platform.
* Bài học quan trọng là không nên học quá nhiều thứ cùng lúc mà cần xây dựng nền tảng chắc chắn trước.

### The Art of Effective Teamwork

* Làm việc nhóm hiệu quả cần có mục tiêu rõ ràng và được chia sẻ giữa các thành viên.
* Mỗi thành viên nên được phân công đúng vai trò dựa trên kỹ năng và điểm mạnh.
* Giao tiếp cởi mở, lắng nghe chủ động và phản hồi rõ ràng giúp giảm hiểu lầm trong quá trình làm việc.
* Trách nhiệm cá nhân là yếu tố quan trọng để đảm bảo tiến độ chung của nhóm.
* Một số công cụ hỗ trợ teamwork có thể kể đến như Trello, ClickUp, Google Workspace, Slack và Discord.

### AWS Neptune for Building a Graph Knowledge Base for GraphRAG

* Bài trình bày giới thiệu GraphRAG, một hướng mở rộng của Retrieval-Augmented Generation.
* RAG truyền thống hỗ trợ LLM truy xuất thông tin từ nguồn dữ liệu bên ngoài, nhưng có thể hạn chế khi cần suy luận nhiều bước.
* GraphRAG sử dụng graph database để biểu diễn mối quan hệ giữa các thực thể.
* Amazon Neptune có thể được dùng để xây dựng graph knowledge base.
* GraphRAG phù hợp với các bài toán cần hiểu mối quan hệ phức tạp giữa dữ liệu, ví dụ hệ thống hỏi đáp thông minh hoặc knowledge base doanh nghiệp.
* Nội dung cũng nhắc đến việc kết hợp Amazon Bedrock, Neptune Analytics và pipeline xử lý dữ liệu để hỗ trợ truy vấn thông minh hơn.

### Docker - A Containerization Technology

* Docker giúp đóng gói ứng dụng cùng với môi trường chạy và dependencies cần thiết.
* Container nhẹ hơn máy ảo vì không cần mỗi ứng dụng phải chạy trên một hệ điều hành riêng.
* Docker hỗ trợ nguyên tắc “build once, run anywhere”.
* Các khái niệm quan trọng gồm Docker Image, Docker Container, Dockerfile, Layer và Docker command.
* Docker được sử dụng nhiều trong CI/CD, microservices, môi trường development/testing và cloud-native application.
* Bài trình bày giúp hiểu vì sao Docker là kiến thức nền quan trọng cho Cloud và DevOps.

### Combining AWS WAF with Machine Learning for Cyber Attack Detection on AWS

* AWS WAF giúp bảo vệ web application khỏi các tấn công phổ biến như SQL Injection, XSS, bot traffic và request bất thường.
* Cơ chế rule-based của WAF hiệu quả với các mẫu tấn công đã biết nhưng có thể hạn chế trước các tấn công mới.
* Machine Learning có thể hỗ trợ phát hiện hành vi bất thường dựa trên dữ liệu mạng.
* Bài trình bày đề cập đến việc xử lý dataset, làm sạch dữ liệu, huấn luyện mô hình và đánh giá kết quả.
* Kiến trúc AWS có thể kết hợp các dịch vụ như WAF, EC2, ALB, S3, Lambda, CloudWatch, GuardDuty, Security Hub và SNS.
* Nội dung giúp người tham gia hiểu thêm về hướng kết hợp Cloud Security và Machine Learning.

## Những gì học được

### Về AWS Cloud

* AWS không chỉ dùng để tạo server hoặc lưu trữ dữ liệu, mà còn có thể hỗ trợ game realtime, AI, bảo mật và hệ thống phân tán.
* Các dịch vụ như API Gateway, Lambda và DynamoDB có thể kết hợp để tạo backend serverless đơn giản.
* Amazon Neptune hỗ trợ lưu trữ dữ liệu dạng graph, phù hợp với các bài toán cần quan hệ phức tạp.
* AWS WAF, CloudWatch, GuardDuty và Security Hub là những dịch vụ quan trọng khi xây dựng hệ thống có yêu cầu bảo mật.

### Về DevOps và hệ thống

* Docker là công cụ quan trọng giúp ứng dụng chạy ổn định trên nhiều môi trường khác nhau.
* Để đi theo hướng Cloud/DevOps, cần có nền tảng về Linux, Networking, System Administration, Automation và CI/CD.
* Việc học cloud cần kết hợp giữa lý thuyết, lab thực hành và project thực tế.
* Khi triển khai hệ thống, cần chú ý đến monitoring, security, cost và khả năng mở rộng.

### Về AI và dữ liệu

* GraphRAG giúp LLM xử lý tốt hơn các câu hỏi cần hiểu quan hệ giữa nhiều thực thể.
* Machine Learning có thể hỗ trợ phát hiện tấn công mạng bằng cách nhận diện các hành vi bất thường.
* Chất lượng dữ liệu là yếu tố rất quan trọng trong các bài toán AI/ML.
* AI không nên được xem là công cụ độc lập, mà cần được kết hợp với dữ liệu, hạ tầng và quy trình kiểm soát phù hợp.

### Về teamwork và định hướng nghề nghiệp

* Làm việc nhóm hiệu quả cần mục tiêu chung, phân công rõ ràng và trách nhiệm cá nhân.
* Kỹ năng giao tiếp và lắng nghe quan trọng không kém kỹ năng kỹ thuật.
* Lộ trình từ IT Helpdesk đến Sysadmin và Cloud/DevOps cần thời gian, thực hành và nền tảng kiến thức vững.
* Portfolio và project thực tế có giá trị lớn trong quá trình phát triển nghề nghiệp.

## Ứng dụng vào công việc

* Khi học AWS, có thể thử kết hợp nhiều dịch vụ nhỏ để hiểu cách hệ thống cloud hoạt động end-to-end.
* Có thể áp dụng Docker để đóng gói các project cá nhân, giúp dễ triển khai và kiểm thử hơn.
* Khi làm project nhóm, cần chia nhiệm vụ rõ ràng, cập nhật tiến độ thường xuyên và thống nhất mục tiêu từ đầu.
* Với các bài toán AI, cần chú ý đến nguồn dữ liệu, cách tổ chức dữ liệu và cách đánh giá kết quả.
* Khi học bảo mật cloud, cần quan tâm đến nhiều lớp bảo vệ như WAF, logging, monitoring và cảnh báo.
* Các kiến thức về Sysadmin, DevOps và Cloud có thể hỗ trợ định hướng nghề nghiệp sau khi ra trường.

## Trải nghiệm trong sự kiện

Sự kiện ngày 06/06 mang lại nhiều nội dung đa dạng, không chỉ tập trung vào một dịch vụ AWS cụ thể mà mở rộng sang nhiều hướng như game realtime, DevOps, AI, GraphRAG, Docker và Cybersecurity. Các bài trình bày giúp tôi thấy rõ hơn cách AWS được ứng dụng trong các tình huống thực tế, từ backend cho game, xây dựng knowledge base, đến phát hiện tấn công mạng.

Điểm tôi thấy hữu ích là các chủ đề đều có liên hệ thực tế với lộ trình học của sinh viên công nghệ thông tin. Ví dụ, bài về IT Helpdesk đến Sysadmin giúp tôi hiểu hơn về nền tảng cần có trước khi học Cloud/DevOps. Bài về Docker giúp tôi nhận ra containerization là kỹ năng quan trọng nếu muốn triển khai ứng dụng hiện đại. Các bài về GraphRAG và AWS WAF kết hợp Machine Learning cũng mở rộng góc nhìn về cách AI có thể được áp dụng trong dữ liệu và bảo mật.

## Kết nối và trao đổi

* Có cơ hội tiếp cận nhiều chủ đề khác nhau trong cùng một sự kiện.
* Hiểu thêm kinh nghiệm học tập và định hướng nghề nghiệp từ các diễn giả.
* Có thêm ý tưởng để áp dụng vào quá trình học AWS, làm project cá nhân và chuẩn bị cho định hướng Cloud/DevOps.
* Nhận ra rằng kỹ năng kỹ thuật cần đi kèm với kỹ năng teamwork, giao tiếp và tư duy giải quyết vấn đề.

## Bài học rút ra

* AWS là một hệ sinh thái rộng, có thể hỗ trợ nhiều loại ứng dụng khác nhau từ web, game, dữ liệu đến AI và bảo mật.
* Muốn học Cloud hiệu quả cần hiểu nền tảng về networking, system, database, security và deployment.
* Docker là kỹ năng quan trọng trong hướng Cloud Native và DevOps.
* AI/ML có thể tạo ra giá trị lớn khi được kết hợp đúng với dữ liệu và hạ tầng cloud.
* Bảo mật không chỉ dựa vào rule cố định mà cần kết hợp monitoring, logging và các phương pháp phát hiện thông minh hơn.
* Làm việc nhóm tốt giúp project được triển khai hiệu quả hơn và giảm rủi ro trong quá trình phát triển.

## Một số hình ảnh khi tham gia sự kiện

![Hình ảnh sự kiện 1](/cloud/images/4-EventParticipated/event2-01.jpg)

![Hình ảnh sự kiện 2](/cloud/images/4-EventParticipated/event2-02.jpg)

![Hình ảnh sự kiện 3](/cloud/images/4-EventParticipated/event2-03.jpg)

![Hình ảnh sự kiện 4](/cloud/images/4-EventParticipated/event2-04.jpg)

![Hình ảnh sự kiện 5](/cloud/images/4-EventParticipated/event2-05.jpg)