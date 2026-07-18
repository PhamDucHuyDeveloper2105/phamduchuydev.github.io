---
title: "Bản đề xuất"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

-- English Study Online System
## Nền tảng học tiếng Anh trực tuyến trên AWS Cloud

### 1. Tóm tắt điều hành

**English Study Online System** là một ứng dụng web cho phép học viên đăng ký các khóa học tiếng Anh trực tuyến, duyệt qua các khóa học có sẵn, theo dõi tiến độ học tập và nhận thông báo. Hệ thống cũng hỗ trợ giáo viên và quản trị viên trong việc quản lý khóa học, bài học, hồ sơ học viên và các hoạt động hàng ngày của nền tảng.

Hệ thống được xây dựng trên **Kiến trúc Cloud Native** sử dụng các dịch vụ của AWS để cung cấp tính sẵn sàng cao, bảo mật, khả năng mở rộng và hiệu suất. Frontend được triển khai bằng **AWS Amplify**, trong khi backend được phát triển bằng **Spring Boot** và được lưu trữ trên **Amazon EC2**. Dữ liệu ứng dụng được lưu trữ trong **Amazon DynamoDB**, tài liệu học tập và các tệp tải lên được lưu trữ trong **Amazon S3**, và các dịch vụ như **CloudWatch, SNS, SES, AWS WAF, IAM, Secrets Manager và AWS KMS** được tích hợp để đảm bảo hoạt động đáng tin cậy và an toàn.

---

### 2. Tuyên bố vấn đề

#### Vấn đề hiện tại

Nhiều trung tâm ngoại ngữ vẫn quản lý việc đăng ký khóa học theo cách thủ công qua điện thoại hoặc hồ sơ giấy, dẫn đến một số vấn đề:

- Khó quản lý việc đăng ký.
- Xung đột lịch học và sai sót.
- Quản lý thông tin học viên không hiệu quả.
- Thiếu hệ thống thông báo tự động.
- Khó mở rộng khi số lượng học viên tăng.

#### Giải pháp

**English Study Online System** cung cấp một nền tảng học tập điện tử dựa trên đám mây hoạt động trên AWS Cloud.

Học viên có thể:

- Đăng ký, đăng nhập.
- Đăng ký khóa học tiếng Anh.
- Xem lịch sử đăng ký.
- Hủy đăng ký.
- Duyệt các khóa học tiếng Anh có sẵn.
- Theo dõi tiến độ học tập.

Giáo viên có thể:

- Xem lịch làm việc.
- Quản lý tiến độ của học viên.
- Cập nhật trạng thái bài học.

Quản trị viên có thể:

- Quản lý người dùng.
- Quản lý giáo viên.
- Quản lý các khóa học và bài học.
- Quản lý đăng ký.
- Theo dõi hoạt động hệ thống.

#### Lợi ích

- Giảm thời gian xử lý đăng ký.
- Tự động hóa việc lên lịch học.
- Cải thiện trải nghiệm của học viên.
- Dễ dàng mở rộng hệ thống.
- Tăng tính bảo mật dữ liệu.
- Giảm chi phí vận hành nhờ sử dụng dịch vụ AWS.

---

### 3. Kiến trúc giải pháp

Hệ thống được xây dựng theo mô hình Cloud Native trên AWS.

Frontend được triển khai bằng **AWS Amplify**, cùng với **Amazon Route 53**, **Amazon CloudFront** và **AWS WAF** để cải thiện hiệu suất và bảo vệ ứng dụng.

Backend được triển khai trên **Amazon EC2** sau một **Application Load Balancer (ALB)** để xử lý các yêu cầu đến một cách hiệu quả.

Dữ liệu ứng dụng được lưu trữ trong **Amazon DynamoDB**, trong khi tài liệu học tập và các tệp tải lên được lưu trữ trong **Amazon S3**.

Dữ liệu cấu hình nhạy cảm được quản lý an toàn bằng **AWS Secrets Manager** và được mã hóa bằng **AWS KMS**.

**Amazon CloudWatch** giám sát tài nguyên hệ thống, trong khi **Amazon SNS** và **Amazon SES** gửi cảnh báo và email xác nhận đăng ký.

![English Study Online Architecture](/cloud/images/2-Proposal/drawio.jpg)

### Dịch vụ AWS sử dụng

- **Amazon Route 53:** Quản lý tên miền và định tuyến người dùng đến hệ thống thông qua DNS.
- **Amazon CloudFront:** Phân phối nội dung (CDN), tăng tốc độ truy cập và giảm độ trễ cho website.
- **AWS WAF:** Bảo vệ ứng dụng web trước các cuộc tấn công phổ biến như SQL Injection, Cross-Site Scripting (XSS) và giới hạn lưu lượng truy cập bất thường.
- **AWS Amplify:** Triển khai và lưu trữ ứng dụng Frontend React, tự động build và triển khai khi có thay đổi từ GitHub.
- **Application Load Balancer (ALB):** Tiếp nhận và phân phối lưu lượng truy cập đến máy chủ Backend, giúp tăng tính sẵn sàng và khả năng mở rộng.
- **Amazon EC2:** Chạy ứng dụng Backend được xây dựng bằng Spring Boot, xử lý các API và nghiệp vụ của hệ thống.
- **Amazon DynamoDB:** Lưu trữ người dùng, giáo viên, khóa học, bài học, đăng ký và dữ liệu ứng dụng khác.
- **Amazon S3:** Lưu trữ hình ảnh giáo viên, hình ảnh khóa học, các tệp tải lên của người dùng và các tệp tĩnh.
- **AWS Secrets Manager:** Quản lý và lưu trữ an toàn các thông tin nhạy cảm như JWT Secret, Access Key và các thông số kết nối.
- **AWS Key Management Service (KMS):** Mã hóa dữ liệu và quản lý khóa bảo mật nhằm tăng cường an toàn thông tin.
- **Amazon CloudWatch:** Giám sát tài nguyên AWS, thu thập log và theo dõi hiệu năng của hệ thống.
- **Amazon SNS:** Gửi thông báo khi xảy ra sự kiện hoặc cảnh báo hệ thống đến quản trị viên.
- **Amazon SES:** Gửi email xác nhận đăng ký, lời nhắc và thông báo qua email.
- **AWS Identity and Access Management (IAM):** Quản lý người dùng, vai trò và phân quyền truy cập các tài nguyên AWS theo nguyên tắc bảo mật.
### Thiết kế thành phần

**Frontend**

- ReactJS
- AWS Amplify
- CloudFront
- Route53
- AWS WAF

**Backend**

- Spring Boot
- Amazon EC2
- Application Load Balancer

**Database**

- Amazon DynamoDB

**Storage**

- Amazon S3

**Security**

- IAM
- Secrets Manager
- AWS KMS

**Monitoring**

- CloudWatch
- SNS
- SES

---

### 4. Triển khai kỹ thuật

#### Các giai đoạn triển khai

Dự án được chia thành 4 giai đoạn chính, từ phân tích yêu cầu đến triển khai hệ thống trên nền tảng AWS Cloud.

1. **Phân tích yêu cầu và thiết kế hệ thống:** Phân tích các yêu cầu của nền tảng học trực tuyến, xác định các tính năng cốt lõi như quản lý người dùng, quản lý giáo viên, đăng ký khóa học và quản lý bài học, sau đó thiết kế cơ sở dữ liệu, giao diện người dùng và kiến trúc AWS Cloud.

2. **Xây dựng và phát triển hệ thống:** Phát triển Frontend bằng ReactJS và Backend bằng Java Spring Boot theo mô hình RESTful API. Đồng thời xây dựng cơ sở dữ liệu trên Amazon DynamoDB, lưu trữ hình ảnh trên Amazon S3 và hoàn thiện các chức năng nghiệp vụ của hệ thống.

3. **Triển khai hệ thống trên AWS:** Triển khai ứng dụng Frontend bằng AWS Amplify, triển khai Backend trên Amazon EC2, cấu hình Application Load Balancer (ALB), Route 53, CloudFront và AWS WAF để đảm bảo khả năng truy cập, bảo mật và hiệu năng của hệ thống.

4. **Kiểm thử, tối ưu và vận hành:** Thực hiện kiểm thử chức năng, kiểm thử bảo mật và hiệu năng. Giám sát hệ thống bằng Amazon CloudWatch, cấu hình Amazon SNS và Amazon SES để gửi thông báo và email xác nhận, đồng thời tối ưu chi phí và hiệu năng hệ thống trước khi triển khai sản xuất.

---

#### Yêu cầu kỹ thuật

**Frontend**

- Phát triển bằng **ReactJS** kết hợp **Tailwind CSS** để xây dựng giao diện người dùng hiện đại và thân thiện.
- Sử dụng **Axios** để giao tiếp với RESTful API.
- Triển khai ứng dụng trên **AWS Amplify**.
- Tăng tốc truy cập thông qua **Amazon CloudFront** và định tuyến tên miền bằng **Amazon Route 53**.
- Bảo vệ ứng dụng bằng **AWS WAF** nhằm hạn chế các cuộc tấn công phổ biến như SQL Injection và Cross-Site Scripting (XSS).

**Backend**

- Phát triển bằng **Java Spring Boot** theo mô hình RESTful API.
- Xác thực và phân quyền người dùng bằng **JWT Authentication**.
- Triển khai Backend trên **Amazon EC2**.
- Sử dụng **Application Load Balancer (ALB)** để phân phối lưu lượng truy cập và tăng tính sẵn sàng của hệ thống.
- Quản lý thông tin bảo mật bằng **AWS Secrets Manager** và mã hóa dữ liệu với **AWS KMS**.

**Cơ sở dữ liệu và lưu trữ**

- **Amazon DynamoDB** cho dữ liệu ứng dụng.
- **Amazon S3** để lưu trữ tài liệu học tập và các tệp tải lên.

**Giám sát và thông báo**

- **Amazon CloudWatch** theo dõi log, tài nguyên và hiệu năng của hệ thống.
- **Amazon SNS** gửi cảnh báo khi xảy ra sự cố hoặc các sự kiện quan trọng.
- **Amazon SES** gửi email xác nhận đăng ký và nhắc nhở.

**Bảo mật hệ thống**

- **AWS IAM** quản lý người dùng, vai trò và phân quyền truy cập tài nguyên AWS.
- **AWS Secrets Manager** lưu trữ các thông tin nhạy cảm như Access Key, JWT Secret và các thông số kết nối.
- **AWS KMS** mã hóa dữ liệu nhằm đảm bảo an toàn thông tin trong quá trình lưu trữ và truyền tải.

**Môi trường triển khai**

- Frontend: ReactJS + AWS Amplify.
- Backend: Java Spring Boot chạy trên Amazon EC2.
- Database: Amazon DynamoDB.
- Storage: Amazon S3.
- Domain: Amazon Route 53.
- CDN: Amazon CloudFront.
- Security: AWS WAF, IAM, Secrets Manager và AWS KMS.
- Monitoring: Amazon CloudWatch.
- Notification: Amazon SNS và Amazon SES.

---

### 5. Lộ trình & Mốc triển khai

**Tháng 1**

- Phân tích yêu cầu.
- Thiết kế giao diện.
- Thiết kế cơ sở dữ liệu.
- Thiết kế kiến trúc AWS.

**Tháng 2**

- Phát triển Backend.
- Phát triển Frontend.
- Kết nối DynamoDB.
- Kết nối S3.

**Tháng 3**

- Triển khai hệ thống lên AWS.
- Kiểm thử.
- Tối ưu.
- Hoàn thiện báo cáo.

---

### 6. Ước tính ngân sách

Có thể xem chi phí bằng **AWS Pricing Calculator** để ước tính chi phí triển khai hệ thống.

#### Chi phí hạ tầng

- **Amazon EC2:** 0,30 USD/tháng (01 máy chủ t3.micro chạy Backend Spring Boot trong môi trường thử nghiệm).
- **Application Load Balancer (ALB):** 0,06 USD/tháng (cân bằng tải cho Backend với lưu lượng thấp).
- **Amazon DynamoDB:** 0,08 USD/tháng (lưu trữ dữ liệu người dùng, giáo viên, khóa học và đăng ký).
- **Amazon S3:** 0,10 USD/tháng (02 bucket lưu trữ hình ảnh, tài liệu và dữ liệu tĩnh).
- **AWS Amplify:** 0,15 USD/tháng (triển khai và lưu trữ ứng dụng React).
- **Amazon CloudFront:** 0,05 USD/tháng (phân phối nội dung và tăng tốc truy cập).
- **Amazon Route 53:** 0,04 USD/tháng (quản lý tên miền và DNS).
- **AWS WAF:** 0,10 USD/tháng (bảo vệ hệ thống trước các cuộc tấn công phổ biến).
- **Amazon CloudWatch:** 0,05 USD/tháng (theo dõi log, hiệu năng và tài nguyên hệ thống).
- **Amazon SNS:** 0,02 USD/tháng (gửi thông báo khi có sự kiện hoặc cảnh báo).
- **Amazon SES:** 0,04 USD/tháng (gửi email xác nhận đăng ký và thông báo).
- **AWS Secrets Manager:** 0,03 USD/tháng (quản lý thông tin bảo mật như API Key và Database Secret).
- **AWS KMS:** 0,02 USD/tháng (mã hóa dữ liệu và khóa bảo mật).

#### Tổng chi phí

**Tổng:** **1,04 USD/tháng**, tương đương khoảng **12,48 USD/12 tháng** *(ước tính đối với môi trường demo, quy mô nhỏ và tận dụng AWS Free Tier khi có thể).*

---

### 7. Đánh giá rủi ro

#### Ma trận rủi ro

- EC2 gặp sự cố.
- Người dùng truy cập tăng đột biến.
- Mất kết nối Internet.
- Sai cấu hình AWS.
- Lộ thông tin đăng nhập.

#### Chiến lược giảm thiểu

- Sử dụng CloudWatch để giám sát.
- Sử dụng WAF chống tấn công.
- Lưu Secret bằng Secrets Manager.
- Phân quyền bằng IAM.
- Sao lưu dữ liệu định kỳ.

#### Kế hoạch dự phòng

- Khôi phục dữ liệu từ S3.
- Khởi tạo lại EC2.
- Theo dõi log bằng CloudWatch.
- Gửi cảnh báo qua SNS và Email.

---

### 8. Kết quả kỳ vọng

- Phát triển thành công một nền tảng học tiếng Anh trực tuyến.
- Triển khai một ứng dụng ổn định và an toàn trên AWS Cloud.
- Cải thiện hiệu quả quản lý khóa học.
- Nâng cao trải nghiệm của học viên.
- Cung cấp một kiến trúc đám mây có khả năng mở rộng cho việc mở rộng trong tương lai.
- Hỗ trợ các tính năng trong tương lai như thanh toán trực tuyến, chatbot AI và phân tích học tập.