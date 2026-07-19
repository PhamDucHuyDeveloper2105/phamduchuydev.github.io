---
title : "Xác minh Email"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.5.1. </b> "
---

Trong phần này, chúng ta sẽ cấu hình **Amazon SNS** để gửi email thông báo từ hệ thống học tiếng Anh online.

### 1. Tạo SNS Topic

Đăng nhập vào **AWS Management Console**, tìm kiếm **Amazon SNS** và mở trang **Topics**.

Chọn **Create topic** và thiết lập các thông tin sau:

- **Type:** Standard
- **Name:** `english-study-notification`

Giữ nguyên các tùy chọn mặc định và nhấn **Create topic**.

---

### 2. Tạo Subscription

Sau khi topic được tạo, hãy thêm địa chỉ email sẽ nhận thông báo.

1. Mở topic vừa tạo.
2. Nhấn **Create subscription**.
3. Trong **Protocol**, chọn **Email**.
4. Trong **Endpoint**, nhập địa chỉ email cần nhận thông báo.
5. Nhấn **Create subscription**.

---

### 3. Xác nhận đăng ký

AWS SNS sẽ gửi một email xác nhận đến địa chỉ bạn vừa nhập.

Mở email và nhấn **Confirm subscription** để hoàn tất thiết lập.

Sau khi xác nhận, trạng thái subscription sẽ chuyển sang **Confirmed**.

---

### 4. Kiểm tra thông báo

Trên giao diện topic, chọn **Publish message**.

Nhập thông tin kiểm tra:

- **Subject:** English Study Notification
- **Message:** Đây là thông báo thử từ hệ thống học tiếng Anh online.

Sau đó nhấn **Publish message**.

Nếu cấu hình đúng, địa chỉ email đã đăng ký sẽ nhận được thông báo.

Đến đây, Amazon SNS đã sẵn sàng để kết nối với backend để gửi cảnh báo và thông báo.
