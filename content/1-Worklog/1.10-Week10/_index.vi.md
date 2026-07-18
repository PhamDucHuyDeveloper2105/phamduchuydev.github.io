---

title: "Worklog Tuần 10"
date: 2026-06-29
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
-----------------------

### Mục tiêu tuần 10:

* Tìm hiểu mô hình Serverless Computing trên AWS.
* Làm quen với AWS Lambda và cách chạy code mà không cần quản lý server.
* Hiểu các thành phần cơ bản của Lambda như Function, Runtime, Handler, Trigger và Execution Role.
* Tìm hiểu Amazon API Gateway và cách API Gateway kết nối với Lambda.

### Các công việc cần triển khai trong tuần này:

| Thứ   | Công việc                                                                                                                                                                                                                                        | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                    |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ----------------------------------------------------------------- |
| Thứ 2 | - Tìm hiểu tổng quan về Serverless Computing <br> - Hiểu sự khác nhau giữa EC2 và Lambda <br> - Ghi chú các trường hợp sử dụng phổ biến của AWS Lambda                                                                                           | 29/06/2026   | 29/06/2026      | https://cloudjourney.awsstudygroup.com/                           |
| Thứ 3 | - Khám phá giao diện AWS Lambda trên AWS Console <br> - Tìm hiểu Function, Runtime, Handler và Execution Role <br> - Quan sát các bước tạo một Lambda Function cơ bản                                                                            | 30/06/2026   | 30/06/2026      | https://docs.aws.amazon.com/lambda/                               |
| Thứ 4 | - Thực hành tạo Lambda Function đơn giản <br> - Kiểm tra kết quả chạy thử bằng Test Event <br> - Xem log thực thi của Lambda trong CloudWatch Logs                                                                                               | 01/07/2026   | 01/07/2026      | https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html |
| Thứ 5 | - Tìm hiểu Amazon API Gateway <br> - Hiểu khái niệm REST API, Resource, Method và Endpoint <br> - Tìm hiểu cách API Gateway có thể gọi Lambda Function                                                                                           | 02/07/2026   | 02/07/2026      | https://docs.aws.amazon.com/apigateway/                           |
| Thứ 6 | - Tổng hợp mô hình cơ bản: Client → API Gateway → Lambda → CloudWatch Logs <br> - Kiểm tra lại các tài nguyên đã tạo trong tuần <br> - Xóa tài nguyên không cần thiết sau khi thực hành <br> - Cập nhật Worklog tuần 10 lên website Hugo cá nhân | 03/07/2026   | 03/07/2026      | https://docs.aws.amazon.com/lambda/latest/dg/welcome.html         |

### Kết quả đạt được tuần 10:

* Hiểu được Serverless Computing là mô hình cho phép chạy ứng dụng mà không cần trực tiếp quản lý máy chủ.

* Nắm được sự khác nhau cơ bản giữa Amazon EC2 và AWS Lambda:

  * EC2 cần quản lý máy chủ ảo
  * Lambda chạy code theo sự kiện và AWS quản lý hạ tầng phía sau

* Hiểu được vai trò của AWS Lambda trong việc xử lý các tác vụ nhỏ, tự động hóa hoặc xử lý theo sự kiện.

* Làm quen với các thành phần cơ bản trong Lambda:

  * Function
  * Runtime
  * Handler
  * Trigger
  * Execution Role
  * Test Event

* Thực hành tạo Lambda Function đơn giản trên AWS Management Console.

* Biết cách chạy thử Lambda Function bằng Test Event.

* Hiểu được Lambda có thể ghi log thực thi vào Amazon CloudWatch Logs.

* Tìm hiểu Amazon API Gateway và vai trò của API Gateway trong việc tạo endpoint để client gọi đến backend.

* Nắm được các khái niệm cơ bản của API Gateway như REST API, Method, Resource và Endpoint.

* Hình dung được cách API Gateway kết nối với Lambda để tạo một API serverless đơn giản.

* Nhận thức được cần kiểm tra và xóa tài nguyên không cần thiết sau khi thực hành để tránh phát sinh chi phí.

* Hoàn thành Worklog tuần 10 và cập nhật nội dung lên website Hugo cá nhân.
