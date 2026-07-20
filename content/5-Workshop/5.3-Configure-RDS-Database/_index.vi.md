---
title : "Cấu hình Amazon RDS"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

Trong phần này, chúng ta sẽ kiểm tra cơ sở dữ liệu **Amazon RDS** được sử dụng trong dự án học tiếng Anh trực tuyến.

Đăng nhập vào **AWS Management Console**, tìm kiếm dịch vụ **Amazon RDS** và mở trang **Databases**.

Chọn Database Instance đã tạo cho dự án và kiểm tra trạng thái của cơ sở dữ liệu. Trước khi ứng dụng hoạt động, hãy đảm bảo trạng thái của Database Instance là **Available**.

Sau khi kết nối đến cơ sở dữ liệu bằng **MySQL Workbench**, **DBeaver** hoặc **SQL Server Management Studio (SSMS)** (tùy theo hệ quản trị cơ sở dữ liệu được sử dụng), kiểm tra các bảng đã được tạo tự động bởi ứng dụng.

Các bảng chính của hệ thống bao gồm:

| Bảng | Chức năng |
|------|-----------|
| users | Lưu thông tin tài khoản người dùng |
| courses | Lưu thông tin các khóa học |
| lessons | Lưu nội dung bài học |
| quizzes | Lưu câu hỏi và đáp án của bài kiểm tra |
| progress | Theo dõi tiến độ và kết quả học tập của người học |
| feedbacks | Lưu phản hồi của người dùng |

Thực hiện câu lệnh SQL sau để hiển thị danh sách các bảng trong cơ sở dữ liệu:

```sql
SHOW TABLES;
```

Nếu danh sách các bảng được hiển thị đầy đủ, điều đó chứng tỏ ứng dụng đã kết nối thành công với Amazon RDS và cơ sở dữ liệu đã sẵn sàng để sử dụng.

![Amazon RDS Database](/cloud/images/5-Workshop/5.1-Workshop-overview/rds-database.png)

Cuối cùng, hãy xác nhận rằng **Database Instance** đang ở trạng thái **Available** và các bảng đã được tạo đầy đủ trước khi tiếp tục các bước triển khai tiếp theo.