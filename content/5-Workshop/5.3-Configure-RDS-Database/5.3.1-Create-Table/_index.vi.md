---
title : "Tạo các bảng Amazon RDS"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.3.1. </b> "
---

Trong dự án học tiếng Anh online này, hệ thống sử dụng **Amazon RDS** làm cơ sở dữ liệu quan hệ để lưu trữ thông tin người dùng, khóa học, bài học và kết quả học tập.

Các bảng trong cơ sở dữ liệu không được tạo thủ công trên Amazon RDS. Thay vào đó, chúng được **tự động khởi tạo khi ứng dụng Spring Boot khởi động** thông qua **Spring Data JPA** và **Hibernate**.

Cấu hình kết nối đến Amazon RDS trong file `application.properties` như sau:

```properties
spring.datasource.url=jdbc:mysql://<rds-endpoint>:3306/english_learning
spring.datasource.username=admin
spring.datasource.password=********

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Trong đó:

- `spring.datasource.url` dùng để kết nối đến Amazon RDS.
- `spring.jpa.hibernate.ddl-auto=update` cho phép Hibernate tự động tạo hoặc cập nhật các bảng dựa trên các lớp Entity.
- `spring.jpa.show-sql=true` hiển thị các câu lệnh SQL trong quá trình khởi động ứng dụng.

Ví dụ về một Entity:

```java
@Entity
@Table(name = "users")
public class User {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String fullName;

    private String email;

    private String password;
}
```

Khi ứng dụng Spring Boot khởi động, Hibernate sẽ tự động quét tất cả các lớp Entity và tạo các bảng tương ứng trong Amazon RDS nếu chúng chưa tồn tại.

Các bảng được tạo tự động gồm:

| Bảng | Mục đích |
|------|----------|
| users | Lưu thông tin tài khoản người dùng |
| courses | Lưu thông tin khóa học |
| lessons | Lưu nội dung bài học |
| quizzes | Lưu câu hỏi và đáp án trong bài kiểm tra |
| progress | Theo dõi tiến độ và điểm số của người học |
| feedbacks | Lưu phản hồi từ người dùng |

Sau khi ứng dụng khởi động thành công, mở **AWS Console → Amazon RDS**, chọn cơ sở dữ liệu đang sử dụng và kết nối bằng công cụ như **MySQL Workbench**, **DBeaver** hoặc **SQL Server Management Studio (SSMS)** (tùy theo hệ quản trị cơ sở dữ liệu).

Thực hiện câu lệnh sau để kiểm tra các bảng đã được tạo:

```sql
SHOW TABLES;
```

Nếu danh sách các bảng xuất hiện đúng như mong đợi, quá trình khởi tạo cơ sở dữ liệu trên Amazon RDS đã hoàn tất.

![Amazon RDS Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/rds-tables.png)