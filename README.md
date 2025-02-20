SampleAPI - Ứng dụng Web API đơn giản với MongoDB
Giới thiệu
Dự án này sử dụng ASP.NET Core để xây dựng một Web API thực hiện các thao tác CRUD trên cơ sở dữ liệu MongoDB cho hệ thống quản lý sách (BookStore).
API hỗ trợ các chức năng cơ bản như thêm, sửa, xóa và truy xuất thông tin sách (Book).
Cấu trúc dự án
Controllers
Chứa lớp BooksController đảm nhận việc xử lý các yêu cầu từ phía client.
Các endpoint chính:
GET /api/books: Lấy danh sách tất cả các sách.
GET /api/books/{id}: Truy vấn thông tin chi tiết của một cuốn sách dựa trên ID.
POST /api/books: Thêm sách mới vào cơ sở dữ liệu.
PUT /api/books/{id}: Cập nhật thông tin sách theo ID.
DELETE /api/books/{id}: Xóa sách khỏi cơ sở dữ liệu dựa trên ID.
Models
Bao gồm hai lớp quan trọng:
Book:
Đại diện cho một sách trong cơ sở dữ liệu.
Các thuộc tính chính:
Id: Mã định danh duy nhất (được MongoDB tự động tạo).
Name: Tên sách.
Price: Giá sách.
Category: Danh mục sách.
Author: Tác giả của sách.
BookStoreDatabaseSettings:
Chứa thông tin cấu hình để kết nối với MongoDB:
ConnectionString: Chuỗi kết nối đến MongoDB.
DatabaseName: Tên cơ sở dữ liệu sử dụng.
BooksCollectionName: Tên collection lưu trữ dữ liệu sách.
Services
Chứa lớp BooksService thực hiện các thao tác tương tác trực tiếp với MongoDB.
Chức năng bao gồm:
Lấy danh sách toàn bộ sách hoặc thông tin cụ thể của một sách.
Thêm mới, cập nhật và xóa sách trong hệ thống.
Sử dụng thư viện MongoDB.Driver để làm việc với cơ sở dữ liệu NoSQL MongoDB.
Hướng dẫn cài đặt và chạy dự án
Yêu cầu
Cài đặt .NET SDK 6.0 hoặc mới hơn.
Cài đặt MongoDB và đảm bảo nó đang chạy.
Cách chạy
Cấu hình kết nối MongoDB trong appsettings.json:

{
  "BookStoreDatabaseSettings": {
    "ConnectionString": "mongodb://localhost:27017",
    "DatabaseName": "BookStore",
    "BooksCollectionName": "Books"
  }
}
Chạy ứng dụng:

dotnet run
Truy cập Swagger UI tại: http://localhost:5000/swagger

Kết quả đạt được
Tích hợp thành công MongoDB vào ASP.NET Core Web API.
Xây dựng một hệ thống API đơn giản hỗ trợ đầy đủ chức năng CRUD.
Nắm vững cách sử dụng dependency injection và công cụ Swagger để tài liệu hóa API. GET ALL image GET THEO ID image POST image DELETE THEO ID image PUT image
