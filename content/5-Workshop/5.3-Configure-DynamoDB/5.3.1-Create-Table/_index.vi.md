---
title : "Tạo các bảng DynamoDB"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.3.1. </b> "
---

Trong dự án học tiếng Anh online này, các bảng **Amazon DynamoDB** không được tạo thủ công trên AWS Console. Thay vào đó, chúng sẽ được khởi tạo tự động khi backend Spring Boot bắt đầu chạy.

Backend sử dụng lớp `DynamoDbTableInitializer` để kiểm tra xem các bảng cần thiết đã tồn tại hay chưa, rồi tạo chúng nếu chưa có.

```java
@Configuration
public class DynamoDbTableInitializer {

    private final DynamoDbEnhancedClient enhancedClient;

    public DynamoDbTableInitializer(DynamoDbEnhancedClient enhancedClient) {
        this.enhancedClient = enhancedClient;
    }

    @PostConstruct
    public void createTables() {
        createTableIfNotExists("users", User.class);
        createTableIfNotExists("lessons", Lesson.class);
        createTableIfNotExists("quizzes", Quiz.class);
        createTableIfNotExists("progress", Progress.class);
        createTableIfNotExists("feedbacks", Feedback.class);
    }
}
```

Khi ứng dụng Spring Boot khởi động, annotation `@PostConstruct` sẽ tự động gọi phương thức `createTables()`. Phương thức này đảm bảo các bảng DynamoDB cần thiết đã sẵn sàng trước khi hệ thống bắt đầu phục vụ người dùng.

Các bảng được tạo tự động gồm:

| Bảng | Mục đích |
|------|----------|
| users | Lưu thông tin tài khoản người dùng |
| lessons | Lưu nội dung bài học và chủ đề |
| quizzes | Lưu câu hỏi và đáp án trong bài kiểm tra |
| progress | Theo dõi tiến độ và điểm số của người học |
| feedbacks | Lưu phản hồi từ người dùng |

Sau khi ứng dụng khởi động thành công, hãy mở **AWS Console → DynamoDB → Tables** để kiểm tra các bảng đã được tạo.

![DynamoDB Tables](/cloud/images/5-Workshop/5.1-Workshop-overview/dynamodb-tables.png)

Nếu các bảng hiển thị trạng thái **Active**, quá trình khởi tạo DynamoDB đã hoàn tất.