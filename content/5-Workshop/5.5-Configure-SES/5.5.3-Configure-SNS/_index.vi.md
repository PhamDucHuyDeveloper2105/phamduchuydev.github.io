---
title : "Cấu hình SNS gửi thông báo"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.5.3. </b> "
---

Trong phần này, chúng ta sẽ cấu hình **Amazon SNS** để tự động gửi email thông báo như cảnh báo hệ thống hoặc báo cáo đến địa chỉ Gmail của bạn.

### 1. Tạo SNS Topic

1. Truy cập **AWS Management Console**, tìm kiếm **Amazon SNS** và chọn **Topics**.
2. Nhấn **Create topic**.
3. Ở phần **Type**, chọn **Standard**.
4. Nhập **Name** như `english-study-alerts`.
5. Giữ nguyên các cài đặt mặc định và nhấn **Create topic**.

### 2. Đăng ký Gmail nhận thông báo

Sau khi topic được tạo, hãy thêm địa chỉ email sẽ nhận thông báo:

1. Mở topic vừa tạo và chuyển sang tab **Subscriptions**.
2. Nhấn **Create subscription**.
3. Ở **Protocol**, chọn **Email**.
4. Ở **Endpoint**, nhập địa chỉ Gmail của bạn.
5. Nhấn **Create subscription**.

### 3. Xác nhận đăng ký

1. AWS SNS sẽ gửi một email xác nhận đến địa chỉ Gmail bạn vừa nhập.
2. Mở hộp thư và tìm email có tiêu đề **AWS Notification - Subscription Confirmation**.
3. Nhấn vào liên kết **Confirm subscription**.
4. Quay lại AWS Console, kiểm tra trạng thái sẽ chuyển từ *Pending confirmation* sang **Confirmed**.

### 4. Gửi thử thông báo

1. Trên giao diện topic, nhấn **Publish message**.
2. Nhập **Subject** như *Test Alert from English Study System*.
3. Nhập nội dung tin nhắn, ví dụ: *The system is working normally!*.
4. Nhấn **Publish message**.
5. Kiểm tra hộp thư Gmail để xác nhận tin nhắn đã đến.

Sau khi hoàn tất, hệ thống SNS đã sẵn sàng để tích hợp với CloudWatch hoặc backend để gửi thông báo tự động.
