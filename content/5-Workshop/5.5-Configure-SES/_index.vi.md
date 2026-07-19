---
title : "Cấu hình Amazon SES & SNS"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

Trong dự án học tiếng Anh online, **Amazon SES** được dùng để gửi email thông báo như xác nhận tài khoản hoặc cập nhật bài học, còn **Amazon SNS** được dùng để phát các thông báo theo mô hình Publish/Subscribe.

### 1. Cấu hình Amazon SES

Đăng nhập vào **AWS Management Console**, tìm kiếm **Amazon SES** và mở **Configuration → Identities**.

Chọn **Create identity**, sau đó chọn **Email address** và nhập địa chỉ sẽ dùng để gửi thông báo từ hệ thống.

![Amazon SES Identity](/cloud/images/5-Workshop/5.1-Workshop-overview/SES.png)

Sau khi tạo, AWS sẽ gửi một email xác minh đến địa chỉ đó. Mở email và nhấn **Verify email address** để hoàn tất.

---

### 2. Cấu hình Amazon SNS

Mở **AWS Management Console**, tìm kiếm **Amazon SNS** và vào mục **Topics**.

Chọn **Create topic**, chọn loại **Standard**, rồi đặt tên cho topic:

```text
english-study-notification
```

Sau đó nhấn **Create topic**.

![Amazon SNS Topic](/cloud/images/5-Workshop/5.1-Workshop-overview/SNS.png)

Sau khi topic được tạo, AWS sẽ cấp một **Topic ARN** để backend sử dụng để phát thông báo.

---

### 3. Cấu hình Backend

Cập nhật file `application.yml` của backend với các giá trị cần thiết:

```yaml
aws:
  region: ${AWS_REGION}

  ses:
    sender-email: ${AWS_SES_SENDER_EMAIL}

  sns:
    topic-arn: ${AWS_SNS_TOPIC_ARN}
```

Trong đó:

- `AWS_SES_SENDER_EMAIL`: Địa chỉ email đã được xác minh trên Amazon SES.
- `AWS_SNS_TOPIC_ARN`: ARN của topic SNS đã tạo ở bước trước.

Sau khi cấu hình xong và khởi động lại backend, hệ thống sẽ sẵn sàng gửi email qua Amazon SES và phát thông báo qua Amazon SNS.