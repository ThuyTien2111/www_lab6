# Lab6 Spring Boot Project

Lab6 là một ứng dụng Spring Boot mẫu, được thiết kế để cung cấp các chức năng cơ bản liên quan đến quản lý người dùng, bài viết và bình luận. Ứng dụng này sử dụng cơ sở dữ liệu MariaDB để lưu trữ thông tin người dùng và nội dung bài viết.

## Các Package

### 1. Package "entity"
   - Chứa các đối tượng thực thể như User, Post, PostComment.

### 2. Package "dao"
   - Chứa các lớp dao như UserDao, PostDao, PostCommentDao.
   - **UserDao:** Chứa các hàm như addUser, logIn, getUserByMobile.
   - **PostDao:** Chứa các hàm như addPost, updatePost, deletePost, activePost, getAllPostByUser, getAll, getPost.
   - **PostCommentDao:** Chứa hàm getPostCommentByPostID.

### 3. Package "controllers"
   - Chứa các lớp controller như UserController, PostController.

### 4. Package "convert"
   - Chứa các lớp đảm nhiệm chuyển đổi dữ liệu như PostForm, UserForm.

## Lab6Application

```java
@SpringBootApplication
public class Lab6Application {
    public static void main(String[] args) {
        ConfigurableApplicationContext context = SpringApplication.run(Lab6Application.class, args);
        UserDao userDao = context.getBean(UserDao.class);
        PostDao postDao = context.getBean(PostDao.class);

        // ... Các demo chức năng của UserDao và PostDao
    }
}
```

## Cấu hình Ứng dụng

Cấu hình kết nối database được thực hiện thông qua file `application.properties` trong thư mục "resources". Dưới đây là các thông số cấu hình:

```properties
spring.datasource.driver-class-name=org.mariadb.jdbc.Driver
spring.datasource.url=jdbc:mariadb://localhost:3306/week6
spring.datasource.username=root
spring.datasource.password=sapass
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.port=8082
spring.jpa.hibernate.naming.implicit-strategy=org.hibernate.boot.model.naming.ImplicitNamingStrategyLegacyJpaImpl
spring.jpa.hibernate.naming.physical-strategy=org.hibernate.boot.model.naming.PhysicalNamingStrategyStandardImpl
```

## Chạy Ứng dụng

- Chạy class `Lab6Application` để khởi động ứng dụng Spring Boot. 
- Sau đó, truy cập http://localhost:8082 để xem kết quả.

## Lưu ý

- Trước khi chạy ứng dụng, đảm bảo rằng đã cấu hình đúng kết nối database trong file `application.properties`.

## Thư viện và Công nghệ sử dụng

- Spring Boot
- MariaDB
- Thymeleaf (được sử dụng trong thư mục "templates")

## Đóng góp

Nếu bạn muốn đóng góp vào dự án Lab 6 Spring Boot, bạn có thể thực hiện các bước sau:

1. Fork dự án trên [GitHub](https://github.com/ThuyTien2111/www_lab6).
2. Tạo một nhánh mới cho các tính năng hoặc sửa đổi bạn muốn thêm vào.
3. Thực hiện các thay đổi và thêm các testcase liên quan.
4. Tạo một pull request để xem xét và hợp nhất thay đổi của bạn vào dự án gốc.

Tôi hoan nghênh sự đóng góp từ cộng đồng để cải thiện dự án này.

## Tác giả

- [Thuy Tien](https://github.com/ThuyTien2111): Sinh viên năm cuối đang học tập tại IUH (Đại học Công nghiệp TPHCM).

## Hình ảnh sản phẩm

![Ảnh mô tả sản phẩm](https://i.imgur.com/rGLZIgi.png)

![Ảnh mô tả sản phẩm](https://i.imgur.com/wtzOXPc.png)

![Ảnh mô tả sản phẩm](https://i.imgur.com/3ljBjh3.png)

![Ảnh mô tả sản phẩm](https://i.imgur.com/m7vLMM8.png)

![Ảnh mô tả sản phẩm](https://i.imgur.com/NBFWYc0.png)

![Ảnh mô tả sản phẩm](https://i.imgur.com/DyEppoD.png)

![Ảnh mô tả sản phẩm](https://i.imgur.com/fEuXcbY.png)

![Ảnh mô tả sản phẩm](https://i.imgur.com/Yx199cA.png)




---
