---
title : "Cấu hình DynamoDB"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

Trong phần này, chúng ta sẽ kiểm tra các bảng **Amazon DynamoDB** được sử dụng trong dự án học tiếng Anh online.

Đăng nhập vào **AWS Management Console**, tìm kiếm dịch vụ **DynamoDB** và mở trang **Tables**.

Ở bước này, các bảng dữ liệu chính của hệ thống đã được tạo và sẵn sàng để phục vụ ứng dụng.

Các bảng chính của hệ thống bao gồm:

| Bảng | Chức năng |
|------|-----------|
| users | Lưu thông tin tài khoản người dùng |
| lessons | Lưu nội dung bài học và chủ đề |
| quizzes | Lưu câu hỏi và đáp án trong bài kiểm tra |
| progress | Theo dõi tiến độ và điểm số của người học |
| feedbacks | Lưu phản hồi từ người dùng |

![DynamoDB Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/dynamodb-tables.png)

Hãy kiểm tra xem từng bảng đều hiển thị trạng thái **Active** trước khi chuyển sang các bước tiếp theo.