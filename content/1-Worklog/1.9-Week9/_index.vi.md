---

title: "Worklog Tuần 9"
date: 2026-06-22
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
----------------------

### Mục tiêu tuần 9:

* Tìm hiểu Elastic Load Balancing và vai trò của Load Balancer trong hệ thống AWS.
* Hiểu khái niệm Target Group, Listener và Health Check.
* Tìm hiểu Auto Scaling Group và cách AWS tự động điều chỉnh số lượng EC2 Instance.
* Làm quen với Launch Template và các chính sách scaling cơ bản.

### Các công việc cần triển khai trong tuần này:

| Thứ   | Công việc                                                                                                                                                                                                          | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                     |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ------------------------------------------------------------------ |
| Thứ 2 | - Tìm hiểu tổng quan về Elastic Load Balancing <br> - Hiểu vai trò của Load Balancer trong việc phân phối traffic <br> - Ghi chú các loại Load Balancer phổ biến trên AWS                                          | 22/06/2026   | 22/06/2026      | https://cloudjourney.awsstudygroup.com/                            |
| Thứ 3 | - Tìm hiểu Application Load Balancer (ALB) <br> - Làm quen với Listener, Target Group và Health Check <br> - Quan sát giao diện Load Balancer trên AWS Console                                                     | 23/06/2026   | 23/06/2026      | https://docs.aws.amazon.com/elasticloadbalancing/                  |
| Thứ 4 | - Tìm hiểu Auto Scaling Group <br> - Hiểu Min Capacity, Desired Capacity và Max Capacity <br> - Ghi chú cách Auto Scaling hỗ trợ hệ thống khi traffic thay đổi                                                     | 24/06/2026   | 24/06/2026      | https://docs.aws.amazon.com/autoscaling/                           |
| Thứ 5 | - Tìm hiểu Launch Template <br> - Liên hệ Launch Template với kiến thức EC2 đã học trước đó <br> - Tìm hiểu Scaling Policy và CloudWatch Metrics dùng cho Auto Scaling                                             | 25/06/2026   | 25/06/2026      | https://docs.aws.amazon.com/autoscaling/ec2/userguide/             |
| Thứ 6 | - Tổng hợp mô hình cơ bản: User → Load Balancer → Target Group → EC2 Instances <br> - Kiểm tra các lưu ý về chi phí khi dùng Load Balancer và Auto Scaling <br> - Cập nhật Worklog tuần 9 lên website Hugo cá nhân | 26/06/2026   | 26/06/2026      | https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/ |

### Kết quả đạt được tuần 9:

* Hiểu được Elastic Load Balancing là dịch vụ giúp phân phối traffic đến nhiều tài nguyên backend như EC2 Instance.

* Nắm được vai trò của Load Balancer trong việc tăng khả năng chịu tải và cải thiện độ sẵn sàng của hệ thống.

* Làm quen với các khái niệm cơ bản trong Application Load Balancer:

  * Listener
  * Target Group
  * Target
  * Health Check
  * Routing Rule

* Hiểu được Health Check giúp Load Balancer xác định tài nguyên backend nào còn hoạt động bình thường.

* Hiểu được Auto Scaling Group giúp tự động điều chỉnh số lượng EC2 Instance dựa trên nhu cầu sử dụng.

* Nắm được ý nghĩa của các thông số cơ bản trong Auto Scaling Group:

  * Minimum Capacity
  * Desired Capacity
  * Maximum Capacity

* Hiểu được Launch Template dùng để định nghĩa cấu hình EC2 Instance khi Auto Scaling cần khởi tạo instance mới.

* Liên hệ được kiến thức Auto Scaling với các nội dung đã học trước đó như EC2, VPC, Security Group và CloudWatch.

* Biết được CloudWatch Metrics có thể được dùng làm cơ sở cho các chính sách scaling.

* Hình dung được mô hình triển khai cơ bản có Load Balancer đứng trước nhiều EC2 Instance.

* Nhận thức được Load Balancer và Auto Scaling có thể phát sinh chi phí, cần kiểm tra tài nguyên sau khi thực hành.

* Hoàn thành Worklog tuần 9 và cập nhật nội dung lên website Hugo cá nhân.
