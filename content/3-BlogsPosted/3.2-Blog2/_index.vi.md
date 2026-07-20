---
title: "Blog 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# AMAZON CLOUDFRONT: TĂNG TỐC WEBSITE VÀ CẢI THIỆN TRẢI NGHIỆM NGƯỜI DÙNG TOÀN CẦU

Khi xây dựng một website hoặc ứng dụng trực tuyến, tốc độ tải trang luôn là một trong những yếu tố quan trọng quyết định trải nghiệm của người dùng. Nếu nội dung được lưu trữ tại một máy chủ ở một khu vực duy nhất, người dùng ở các quốc gia khác sẽ phải mất nhiều thời gian hơn để truy cập do khoảng cách địa lý và độ trễ của mạng.

Để giải quyết vấn đề này, AWS cung cấp **Amazon CloudFront** – dịch vụ Content Delivery Network (CDN) giúp phân phối nội dung đến người dùng thông qua mạng lưới các máy chủ biên (Edge Locations) được đặt tại nhiều quốc gia trên thế giới.

Thay vì luôn lấy dữ liệu từ máy chủ gốc (Origin Server), CloudFront sẽ lưu trữ tạm thời (Cache) các nội dung như hình ảnh, video, CSS, JavaScript hoặc tài liệu tĩnh tại các Edge Location gần người dùng nhất. Điều này giúp giảm thời gian phản hồi, giảm tải cho máy chủ và nâng cao hiệu năng của hệ thống.

## CÁC TÍNH NĂNG NỔI BẬT

<br>&emsp;• **Phân phối nội dung với tốc độ cao**

<br>&emsp;CloudFront sử dụng mạng lưới hàng trăm Edge Locations trên toàn thế giới để cung cấp nội dung từ vị trí gần người dùng nhất, giúp giảm đáng kể độ trễ khi truy cập.

<br>&emsp;• **Giảm tải cho máy chủ gốc**

<br>&emsp;Các nội dung tĩnh sẽ được lưu trong bộ nhớ đệm của CloudFront. Khi người dùng tiếp theo truy cập cùng một nội dung, dữ liệu sẽ được trả về trực tiếp từ Edge Location mà không cần gửi yêu cầu đến máy chủ gốc.

<br>&emsp;• **Tăng cường bảo mật**

<br>&emsp;CloudFront hỗ trợ HTTPS, SSL/TLS, AWS Shield Standard và có thể tích hợp với AWS WAF để bảo vệ website khỏi các cuộc tấn công phổ biến.

<br>&emsp;• **Tích hợp với nhiều dịch vụ AWS**

<br>&emsp;CloudFront hoạt động hiệu quả cùng Amazon S3, Elastic Load Balancer (ELB), Amazon EC2, API Gateway và AWS Lambda để xây dựng các ứng dụng hiện đại.

<br>&emsp;• **Theo dõi hiệu năng**

<br>&emsp;CloudFront có thể tích hợp với Amazon CloudWatch để giám sát số lượng yêu cầu, tỷ lệ cache, băng thông sử dụng và nhiều chỉ số quan trọng khác.

## TÌNH HUỐNG THỰC TẾ

Giả sử một doanh nghiệp xây dựng website giới thiệu sản phẩm và lưu trữ toàn bộ hình ảnh trên Amazon S3.

Nếu người dùng tại Việt Nam, Nhật Bản, Mỹ và Châu Âu đều truy cập trực tiếp vào S3 thì thời gian tải hình ảnh có thể khác nhau do khoảng cách địa lý.

Khi triển khai Amazon CloudFront, kiến trúc sẽ như sau:

**Người dùng → Amazon CloudFront → Amazon S3**

Trong mô hình này:

<br>&emsp;+ Người dùng gửi yêu cầu đến CloudFront.

<br>&emsp;+ CloudFront kiểm tra xem nội dung đã được lưu trong bộ nhớ đệm hay chưa.

<br>&emsp;+ Nếu dữ liệu đã tồn tại, CloudFront trả kết quả ngay từ Edge Location gần nhất.

<br>&emsp;+ Nếu chưa có, CloudFront sẽ lấy dữ liệu từ Amazon S3, lưu vào bộ nhớ đệm và gửi về cho người dùng.

Nhờ đó, các lần truy cập tiếp theo sẽ có tốc độ nhanh hơn, giảm lượng truy cập trực tiếp đến máy chủ gốc và tiết kiệm chi phí băng thông.

## KẾT LUẬN

Theo mình, Amazon CloudFront là một trong những dịch vụ quan trọng khi xây dựng các ứng dụng có lượng người dùng lớn hoặc phục vụ khách hàng ở nhiều khu vực khác nhau.

Không chỉ giúp tăng tốc độ tải trang, CloudFront còn giảm tải cho máy chủ, cải thiện khả năng mở rộng và tăng cường bảo mật khi kết hợp với AWS WAF và AWS Shield.

Qua quá trình tìm hiểu dịch vụ này, mình hiểu rõ hơn về cách AWS sử dụng mạng lưới CDN để tối ưu hiệu năng cho website và ứng dụng trên phạm vi toàn cầu. Đây là một dịch vụ rất phù hợp để học khi tìm hiểu về Cloud Computing, đặc biệt trong các chủ đề như tối ưu hiệu năng, phân phối nội dung và kiến trúc hệ thống hiện đại.

## Tài liệu tham khảo

https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html

![Picture](/cloud/images/3-BlogsPosted/Blog2.jpg)