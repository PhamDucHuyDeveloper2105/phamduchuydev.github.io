---
title : "Kết nối Backend"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.3.2. </b> "
---

Trong phần này, chúng ta sẽ cấu hình backend Spring Boot để kết nối an toàn với **Amazon RDS**. Amazon RDS được sử dụng làm cơ sở dữ liệu quan hệ để lưu trữ thông tin người dùng, khóa học, bài học, bài kiểm tra và kết quả học tập của hệ thống học tiếng Anh trực tuyến.

### 1. Cấu hình kết nối cơ sở dữ liệu

Backend kết nối đến Amazon RDS thông qua thông tin Endpoint, Username và Password được khai báo trong file `application.yml`.

```yaml
spring:
  datasource:
    url: jdbc:mysql://${RDS_ENDPOINT}:3306/english_learning
    username: ${DB_USERNAME}
    password: ${DB_PASSWORD}

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
```

Trong đó:

- `RDS_ENDPOINT`: Địa chỉ Endpoint của Amazon RDS.
- `DB_USERNAME`: Tên đăng nhập cơ sở dữ liệu.
- `DB_PASSWORD`: Mật khẩu cơ sở dữ liệu.
- `ddl-auto=update`: Hibernate sẽ tự động tạo hoặc cập nhật các bảng dựa trên các lớp Entity.

Hãy đảm bảo các biến môi trường trên đã được thiết lập trước khi khởi động ứng dụng.

### 2. Kiểm tra kết nối Amazon RDS

Sau khi hoàn tất cấu hình, khởi động backend bằng lệnh:

```bash
mvn spring-boot:run
```

Khi ứng dụng khởi động, Spring Boot sẽ tự động kết nối đến Amazon RDS. Đồng thời, Hibernate sẽ kiểm tra các Entity và tạo hoặc cập nhật các bảng trong cơ sở dữ liệu nếu cần.

Terminal sẽ hiển thị các thông báo tương tự:

```text
HikariPool-1 - Start completed.

Hibernate:
create table users (...)

Hibernate:
create table courses (...)

Hibernate:
create table lessons (...)

Hibernate:
create table quizzes (...)

Hibernate:
create table progress (...)

Hibernate:
create table feedbacks (...)
```

Nếu các thông báo trên xuất hiện mà không có lỗi kết nối, điều đó chứng tỏ backend đã kết nối thành công với Amazon RDS và sẵn sàng phục vụ hệ thống.

### 3. Kiểm tra cơ sở dữ liệu

Đăng nhập vào **AWS Console → Amazon RDS**, chọn Database Instance đang sử dụng và kết nối bằng một công cụ quản lý cơ sở dữ liệu như **MySQL Workbench**, **DBeaver** hoặc **SQL Server Management Studio (SSMS)** (tùy theo loại cơ sở dữ liệu đã triển khai).

Sau đó thực hiện câu lệnh:

```sql
SHOW TABLES;
```

Kết quả sẽ hiển thị các bảng được tạo tự động, ví dụ:

- users
- courses
- lessons
- quizzes
- progress
- feedbacks

Nếu các bảng xuất hiện đầy đủ, quá trình kết nối backend với Amazon RDS đã hoàn tất thành công.

![Amazon RDS Connection](/cloud/images/5-Workshop/5.1-Workshop-overview/connect-rds.png)