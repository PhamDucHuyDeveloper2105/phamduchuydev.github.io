---
title : "Cấu hình Amazon S3"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

Trong dự án học tiếng Anh online, **Amazon S3** được sử dụng để lưu trữ các tệp hình ảnh như ảnh minh họa bài học, ảnh đại diện người dùng và các file media được tải lên.

### 1. Tạo S3 Bucket

Đăng nhập vào **AWS Management Console**, tìm kiếm **Amazon S3** và mở trang **Buckets**.

Chọn **Create bucket** và nhập các thông tin cần thiết:

- **Bucket name:** `english-study-online-images-huy`
- **AWS Region:** `Asia Pacific (Singapore) - ap-southeast-1`

Sau khi hoàn tất thiết lập, nhấn **Create bucket**.

![Amazon S3 Bucket](/cloud/images/5-Workshop/5.1-Workshop-overview/S3.png)

Sau khi tạo thành công, bucket sẽ xuất hiện trong danh sách và sẵn sàng để sử dụng.

---

### 2. Cấu hình S3 trong Backend

Sau khi tạo bucket, hãy thêm thông tin cấu hình vào file `application.yml` của backend:

```yaml
aws:
  region: ${AWS_REGION}

  s3:
    bucket-name: ${AWS_S3_BUCKET_NAME}
```

Trong đó:

- `AWS_REGION`: Vùng AWS được sử dụng để triển khai dịch vụ.
- `AWS_S3_BUCKET_NAME`: Tên của bucket S3, ví dụ `english-study-online-images-huy`.

Backend sẽ dùng các giá trị này để kết nối với Amazon S3 và thực hiện các thao tác upload, download và quản lý file.

Sau khi cấu hình xong và ứng dụng chạy, hệ thống có thể lưu trữ và lấy lại các tệp trực tiếp từ S3.