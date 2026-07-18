---

title: "Worklog Tuần 3"
date: 2026-05-11
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
----------------------

### Mục tiêu tuần 3:

* Tìm hiểu dịch vụ Amazon EC2 và vai trò của EC2 trong nhóm Compute trên AWS.
* Hiểu các thành phần cơ bản khi khởi tạo EC2 Instance như AMI, Instance Type, Key Pair, Security Group và EBS.
* Thực hành tạo EC2 Instance ở mức cơ bản trong phạm vi Free Tier.
* Tìm hiểu cách kết nối EC2 thông qua SSH và kiểm tra trạng thái tài nguyên sau khi thực hành.

### Các công việc cần triển khai trong tuần này:

| Thứ   | Công việc                                                                                                                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                  |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------------------- |
| Thứ 2 | - Tìm hiểu tổng quan về Amazon EC2 <br> - Hiểu vai trò của EC2 trong việc cung cấp máy chủ ảo trên cloud <br> - Ghi chú các trường hợp sử dụng phổ biến của EC2                                                               | 11/05/2026   | 11/05/2026      | https://cloudjourney.awsstudygroup.com/                                         |
| Thứ 3 | - Tìm hiểu các thành phần khi tạo EC2 Instance <br> - Phân biệt AMI, Instance Type, Key Pair và Security Group <br> - Xem qua các lựa chọn Free Tier phù hợp cho môi trường học tập                                           | 12/05/2026   | 12/05/2026      | https://docs.aws.amazon.com/ec2/                                                |
| Thứ 4 | - Thực hành tạo EC2 Instance bằng AWS Management Console <br> - Chọn Amazon Linux làm hệ điều hành thử nghiệm <br> - Cấu hình Security Group cho phép kết nối SSH cơ bản                                                      | 13/05/2026   | 13/05/2026      | https://docs.aws.amazon.com/ec2/                                                |
| Thứ 5 | - Tìm hiểu cách kết nối SSH vào EC2 Instance <br> - Kiểm tra Public IPv4 Address và Key Pair <br> - Quan sát trạng thái Instance sau khi khởi tạo                                                                             | 14/05/2026   | 14/05/2026      | https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-linux-inst-ssh.html |
| Thứ 6 | - Tìm hiểu EBS Volume gắn với EC2 Instance <br> - Kiểm tra trạng thái tài nguyên sau khi thực hành <br> - Dừng hoặc xóa tài nguyên không cần thiết để tránh phát sinh chi phí <br> - Cập nhật Worklog tuần 3 lên website Hugo | 15/05/2026   | 15/05/2026      | https://docs.aws.amazon.com/ebs/                                                |

### Kết quả đạt được tuần 3:

* Hiểu được Amazon EC2 là dịch vụ cung cấp máy chủ ảo trên AWS, thuộc nhóm dịch vụ Compute.

* Nắm được vai trò của EC2 trong việc triển khai ứng dụng, thử nghiệm môi trường server và học các kiến thức nền tảng về hạ tầng cloud.

* Hiểu được các thành phần quan trọng khi tạo EC2 Instance:

  * Amazon Machine Image (AMI)
  * Instance Type
  * Key Pair
  * Security Group
  * Elastic Block Store (EBS)

* Biết cách chọn Instance Type phù hợp cho mục đích học tập, đặc biệt là các lựa chọn nằm trong phạm vi Free Tier.

* Thực hành tạo EC2 Instance cơ bản bằng AWS Management Console.

* Hiểu được vai trò của Security Group trong việc kiểm soát traffic inbound và outbound cho EC2 Instance.

* Biết cách kiểm tra thông tin Public IPv4 Address để chuẩn bị kết nối đến EC2.

* Tìm hiểu cách kết nối SSH vào EC2 Instance bằng Key Pair.

* Quan sát được trạng thái hoạt động của Instance trên AWS Console và biết cách kiểm tra tài nguyên theo từng Region.

* Hiểu được EBS là dịch vụ lưu trữ dạng block storage được sử dụng kèm với EC2 Instance.

* Biết cách dừng hoặc xóa tài nguyên sau khi thực hành để hạn chế phát sinh chi phí không cần thiết.

* Hoàn thành Worklog tuần 3 và cập nhật nội dung lên website Hugo cá nhân.
