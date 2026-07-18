---

title: "Worklog Tuần 6"
date: 2026-06-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
----------------------

### Mục tiêu tuần 6:

* Tìm hiểu dịch vụ Amazon Relational Database Service (Amazon RDS).
* Hiểu vai trò của cơ sở dữ liệu quan hệ trong hệ thống cloud.
* Làm quen với các Database Engine phổ biến như MySQL, PostgreSQL và Amazon Aurora.
* Tìm hiểu các thiết lập cơ bản khi triển khai RDS như Instance Class, Storage, Backup, Security Group và VPC.

### Các công việc cần triển khai trong tuần này:

| Thứ   | Công việc                                                                                                                                                                                                                  | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                                         |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | -------------------------------------------------------------------------------------- |
| Thứ 2 | - Tìm hiểu tổng quan về Amazon RDS <br> - Hiểu vai trò của RDS trong nhóm dịch vụ Database <br> - So sánh RDS với việc tự cài database trên EC2                                                                            | 01/06/2026   | 01/06/2026      | https://cloudjourney.awsstudygroup.com/                                                |
| Thứ 3 | - Tìm hiểu các Database Engine được hỗ trợ bởi RDS <br> - Ghi chú các engine phổ biến: MySQL, PostgreSQL, MariaDB, SQL Server, Oracle và Amazon Aurora <br> - Tìm hiểu điểm khác biệt cơ bản của Amazon Aurora             | 02/06/2026   | 02/06/2026      | https://docs.aws.amazon.com/rds/                                                       |
| Thứ 4 | - Quan sát quy trình tạo RDS Database trên AWS Console <br> - Tìm hiểu các cấu hình như DB Instance Class, Storage Type và Free Tier <br> - Ghi chú các thông tin cần chú ý trước khi tạo database                         | 03/06/2026   | 03/06/2026      | https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/                                |
| Thứ 5 | - Tìm hiểu cách RDS kết nối với VPC và Security Group <br> - Phân biệt Public Access và Private Access ở mức cơ bản <br> - Tìm hiểu Backup, Snapshot và Multi-AZ Deployment                                                | 04/06/2026   | 04/06/2026      | https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html |
| Thứ 6 | - Kiểm tra giao diện RDS và Aurora trên AWS Console <br> - Xem trạng thái tài nguyên database trong tài khoản <br> - Tìm hiểu các lưu ý về chi phí khi sử dụng RDS <br> - Cập nhật Worklog tuần 6 lên website Hugo cá nhân | 05/06/2026   | 05/06/2026      | https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ManagingCosts.html         |

### Kết quả đạt được tuần 6:

* Hiểu được Amazon RDS là dịch vụ cơ sở dữ liệu quan hệ được quản lý bởi AWS.

* Nắm được lợi ích của RDS so với việc tự cài đặt và quản trị database thủ công trên EC2.

* Hiểu được các Database Engine phổ biến mà RDS hỗ trợ:

  * MySQL
  * PostgreSQL
  * MariaDB
  * Microsoft SQL Server
  * Oracle Database
  * Amazon Aurora

* Làm quen với Amazon Aurora và hiểu đây là dịch vụ cơ sở dữ liệu quan hệ được tối ưu hóa cho môi trường AWS.

* Biết các thông tin cần quan tâm khi cấu hình RDS Database:

  * DB Engine
  * DB Instance Class
  * Storage
  * Username và Password
  * VPC
  * Security Group
  * Backup

* Hiểu được vai trò của Security Group trong việc kiểm soát kết nối đến database.

* Phân biệt được Public Access và Private Access ở mức cơ bản khi cấu hình database trên AWS.

* Tìm hiểu được ý nghĩa của Backup, Snapshot và Multi-AZ trong việc bảo vệ dữ liệu và tăng độ sẵn sàng.

* Biết cách truy cập khu vực Amazon RDS và Amazon Aurora trên AWS Management Console để kiểm tra trạng thái tài nguyên.

* Nhận thức được RDS là dịch vụ có thể phát sinh chi phí nếu cấu hình không phù hợp hoặc quên xóa tài nguyên sau khi thực hành.

* Biết cần kiểm tra Billing Dashboard và trạng thái tài nguyên sau khi tìm hiểu các dịch vụ Database.

* Hoàn thành Worklog tuần 6 và cập nhật nội dung lên website Hugo cá nhân.
