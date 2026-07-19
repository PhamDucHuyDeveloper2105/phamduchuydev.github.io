---
title : "Kết nối Backend"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.3.2. </b> "
---

Trong phần này, chúng ta sẽ cấu hình backend Spring Boot để kết nối an toàn với **Amazon DynamoDB** bằng AWS SDK for Java. Đây là bước quan trọng để ứng dụng học tiếng Anh online có thể lưu trữ người dùng, bài học, kết quả làm bài và phản hồi.

### 1. Cấu hình thông tin xác thực

Backend cần có Access Key, Secret Key và vùng AWS để truy cập DynamoDB. Thay vì ghi trực tiếp vào mã nguồn, dự án sẽ đọc các giá trị này từ file `application.yml` thông qua biến môi trường:

```yaml
aws:
  credentials:
    access-key-id: ${AWS_ACCESS_KEY_ID}
    secret-access-key: ${AWS_SECRET_ACCESS_KEY}
  region: ${AWS_REGION}
```

Hãy đảm bảo các biến môi trường này đã được thiết lập trước khi chạy ứng dụng.

### 2. Kiểm tra kết nối DynamoDB

Sau khi cấu hình xong, hãy khởi động backend bằng lệnh:

```bash
mvn spring-boot:run
```

Khi ứng dụng bắt đầu chạy, lớp `DynamoDbTableInitializer` sẽ tự động kiểm tra xem các bảng cần thiết đã tồn tại chưa. Nếu đã có, hệ thống sẽ in ra thông báo `Table already exists`.

```text
Checking and creating DynamoDB tables if they do not exist...
Table already exists: users
Table already exists: lessons
Table already exists: quizzes
Table already exists: progress
Table already exists: feedbacks
```

Nếu terminal hiển thị các dòng này, nghĩa là backend đã kết nối thành công với Amazon DynamoDB và sẵn sàng làm việc với cơ sở dữ liệu NoSQL.

![DynamoDB Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/connetdb.png)