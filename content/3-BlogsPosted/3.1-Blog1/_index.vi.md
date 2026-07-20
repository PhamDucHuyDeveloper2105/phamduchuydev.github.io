---
title: "Blog 1"
date: 2024-01-02
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# AWS LAMBDA: XÂY DỰNG ỨNG DỤNG MÀ KHÔNG CẦN QUẢN LÝ MÁY CHỦ

Trong quá trình phát triển các ứng dụng trên nền tảng điện toán đám mây, việc quản lý máy chủ luôn là một trong những công việc tốn nhiều thời gian và chi phí. Nhà phát triển không chỉ cần viết mã nguồn mà còn phải cấu hình hệ điều hành, cài đặt môi trường, giám sát tài nguyên và đảm bảo hệ thống luôn hoạt động ổn định.

AWS Lambda được AWS giới thiệu nhằm giải quyết vấn đề này thông qua mô hình **Serverless Computing (Điện toán không máy chủ)**. Với Lambda, lập trình viên chỉ cần tập trung vào việc xây dựng chức năng của ứng dụng, còn toàn bộ việc quản lý hạ tầng, mở rộng tài nguyên và vận hành hệ thống sẽ do AWS tự động xử lý.

Điều này giúp rút ngắn thời gian phát triển, giảm chi phí vận hành và giúp ứng dụng dễ dàng mở rộng khi số lượng người dùng tăng lên.

## CÁC TÍNH NĂNG NỔI BẬT

<br>&emsp;• **Không cần quản lý máy chủ:**  
<br>&emsp;Người dùng chỉ cần tải mã nguồn lên AWS Lambda, dịch vụ sẽ tự động thực thi khi có sự kiện kích hoạt mà không cần tạo hay quản lý EC2.

<br>&emsp;• **Tự động mở rộng (Auto Scaling):**  
<br>&emsp;Lambda có khả năng tự động mở rộng số lượng phiên thực thi khi lưu lượng truy cập tăng, đáp ứng hàng nghìn yêu cầu cùng lúc mà không cần cấu hình thủ công.

<br>&emsp;• **Tính phí theo thời gian sử dụng:**  
<br>&emsp;Thay vì phải trả chi phí cho máy chủ hoạt động 24/7, AWS Lambda chỉ tính phí khi hàm được thực thi, giúp tối ưu chi phí cho các ứng dụng có lưu lượng truy cập không ổn định.

<br>&emsp;• **Hoạt động theo sự kiện (Event-Driven):**  
<br>&emsp;Lambda có thể được kích hoạt bởi nhiều dịch vụ AWS như Amazon S3, Amazon API Gateway, Amazon DynamoDB, Amazon EventBridge, Amazon SNS hoặc Amazon SQS.

<br>&emsp;• **Hỗ trợ nhiều ngôn ngữ lập trình:**  
<br>&emsp;AWS Lambda hỗ trợ Python, Node.js, Java, C#, Go, Ruby và nhiều môi trường chạy khác thông qua Container Image.

<br>&emsp;• **Tích hợp với nhiều dịch vụ AWS:**  
<br>&emsp;Lambda có thể kết hợp với API Gateway, DynamoDB, S3, CloudWatch, Step Functions và nhiều dịch vụ khác để xây dựng các ứng dụng hiện đại theo kiến trúc Serverless.

<br>&emsp;• **Giám sát và ghi nhật ký:**  
<br>&emsp;Mọi thông tin về quá trình thực thi, lỗi phát sinh và hiệu năng đều được ghi nhận thông qua Amazon CloudWatch, giúp dễ dàng theo dõi và xử lý sự cố.

## KẾT LUẬN

Theo mình, AWS Lambda là một trong những dịch vụ quan trọng nhất khi bắt đầu học AWS vì nó thể hiện rõ cách AWS đơn giản hóa việc phát triển và triển khai ứng dụng trên nền tảng đám mây.

Thay vì dành nhiều thời gian để cấu hình và quản lý máy chủ, lập trình viên chỉ cần tập trung xây dựng các chức năng của ứng dụng. AWS sẽ tự động xử lý việc cấp phát tài nguyên, mở rộng hệ thống và đảm bảo khả năng sẵn sàng của dịch vụ.

Khi tìm hiểu về AWS Lambda, mình cũng hiểu rõ hơn một số câu hỏi quan trọng trong quá trình thiết kế hệ thống như:

<br>&emsp;Ứng dụng có thể chia thành bao nhiêu chức năng độc lập?

<br>&emsp;Sự kiện nào sẽ kích hoạt mỗi hàm Lambda?

<br>&emsp;Làm thế nào để tối ưu thời gian thực thi và chi phí?

<br>&emsp;Cách kết hợp Lambda với API Gateway, DynamoDB hoặc S3 để xây dựng hệ thống hoàn chỉnh?

<br>&emsp;Làm sao để theo dõi lỗi và hiệu năng của ứng dụng thông qua CloudWatch?

Qua quá trình tìm hiểu, mình nhận thấy AWS Lambda không chỉ giúp giảm chi phí vận hành mà còn tạo điều kiện để xây dựng các ứng dụng có khả năng mở rộng cao, linh hoạt và hiện đại theo mô hình Serverless. Đây là một dịch vụ rất đáng để tìm hiểu đối với bất kỳ ai đang học và phát triển ứng dụng trên nền tảng AWS.

**Tài liệu tham khảo:**

https://docs.aws.amazon.com/lambda/latest/dg/welcome.html

![Picture](/cloud/images/3-BlogsPosted/Blog1.jpg)