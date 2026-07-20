---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---
# Triển khai Website English Study Online trên AWS

#### Tổng quan

Trong workshop này, tôi sẽ trình bày quá trình triển khai **Website English Study Online** trên nền tảng điện toán đám mây **Amazon Web Services (AWS)**.

Dự án được xây dựng nhằm **giải quyết các hạn chế trong quản lý học tập và đăng ký khóa học trực tuyến theo phương pháp truyền thống**, như:
- Quản lý đăng ký khóa học bằng giấy hoặc bảng tính, gây khó khăn trong theo dõi và cập nhật tiến độ.
- Học viên phải liên hệ thủ công để đăng ký khóa học, gây mất thời gian cho cả học viên và nhân viên.
- Khó quản lý thông tin khóa học, bài giảng, giáo viên và học viên trên cùng một hệ thống.
- Thiếu khả năng theo dõi tiến độ học tập, nhận thông báo và đánh giá hiệu suất học viên khi số lượng người dùng tăng lên.
- Khó mở rộng và triển khai khi sử dụng hạ tầng máy chủ truyền thống.

Để khắc phục các vấn đề trên, hệ thống được xây dựng theo kiến trúc **3-Tier Architecture**, sử dụng **ReactJS** cho Frontend, **Spring Boot** cho Backend và **Amazon DynamoDB** làm cơ sở dữ liệu NoSQL. Việc triển khai trên AWS giúp hệ thống có khả năng mở rộng linh hoạt, tăng tính sẵn sàng, đảm bảo bảo mật và giảm chi phí quản lý hạ tầng.

Trong workshop này, người đọc sẽ được hướng dẫn từng bước triển khai hệ thống trên AWS, từ chuẩn bị môi trường, triển khai Frontend và Backend, cấu hình cơ sở dữ liệu, thiết lập các dịch vụ bảo mật, giám sát hoạt động cho đến kiểm thử và tối ưu ứng dụng.

Các dịch vụ AWS được sử dụng trong workshop gồm:

- Amazon EC2
- AWS Amplify
- Amazon DynamoDB
- Amazon S3
- Amazon CloudFront
- Amazon Route 53
- AWS WAF
- AWS Secrets Manager
- AWS KMS
- Amazon CloudWatch
- Amazon SNS
- Amazon SES
- IAM

#### Nội dung

1. [Giới thiệu](5.1-Workshop-overview/)
2. [Các bước chuẩn bị](5.2-Prerequiste/)
3. [Cấu hình DynamoDB](5.3-Configure-RDS-Database/)
4. [Cấu hình Amazon S3](5.4-Configure-S3/)
5. [Cấu hình Amazon SES & SNS](5.5-Configure-SES/)
6. [Triển khai Backend trên EC2](5.6-Deploy-EC2/)
7. [Kiểm tra hệ thống](5.7-System-Testing/)
8. [Dọn dẹp tài nguyên](5.8-Cleanup/)