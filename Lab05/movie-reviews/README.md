BÁO CÁO THỰC HÀNH - MÔN IE213.Q21 (LAB 05)
1. Thông tin chung
* **Họ và tên:** Lê Trung Hải
* **MSSV:** 21522033
* **Lớp:** IE213.O21
* **Môn học:** Kỹ thuật phát triển hệ thống Web

Nội dung: Kết nối Frontend với Backend và Hoàn thiện ứng dụng Movie Reviews (Lab 05)

2. **Cấu trúc thư mục cập nhật**
Trong bài thực hành này, thư mục frontend được bổ sung thêm tầng dịch vụ (services) để quản lý các lời gọi API và hoàn thiện các Component chức năng:

movie-reviews/
├── backend/               # (Đã hoàn thiện ở các Lab trước)
├── frontend/
│   ├── src/
│   │   ├── components/    # Cập nhật logic hiển thị và xử lý dữ liệu
│   │   │   ├── add-review.js
│   │   │   ├── login.js
│   │   │   ├── movie.js
│   │   │   └── movies-list.js
│   │   ├── services/      # MỚI - Quản lý kết nối API
│   │   │   └── movies.js  # Lớp MovieDataService (sử dụng axios)
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json       # Bổ sung thư viện axios
│   └── ...
└── README.md

3. Chi tiết Lab 05
**3.1. Mục tiêu bài thực hành**
Kết nối thành công ứng dụng Frontend (ReactJS) với Backend (Node.js/Express) thông qua thư viện Axios.

Xây dựng lớp dịch vụ MovieDataService để tập trung quản lý các yêu cầu HTTP.

Thực hiện các chức năng CRUD hoàn chỉnh trên giao diện: Xem danh sách phim, tìm kiếm phim, xem chi tiết và quản lý đánh giá (Thêm/Sửa/Xóa).

Áp dụng React Hooks (useState, useEffect) để quản lý dữ liệu động từ API.

**3.2. Các chức năng chính đã hoàn thành**
Thiết lập kết nối (MovieDataService):
Triển khai các phương thức: getAll(), get(id), find(), getRatings().
Triển khai các phương thức CRUD Review: createReview(), updateReview(), deleteReview().

Trang danh sách phim (MoviesList):
Hiển thị danh sách phim dưới dạng Card.
Chức năng tìm kiếm phim theo Tên (Title) hoặc Phân loại (Rating).
Phân trang cơ bản dựa trên kết quả trả về từ API.

Trang chi tiết phim (Movie):
Hiển thị thông tin chi tiết phim và danh sách các đánh giá liên quan.
Logic kiểm tra quyền sở hữu: Chỉ hiển thị nút "Edit" và "Delete" nếu người dùng hiện tại là tác giả của đánh giá đó.

Trang quản lý đánh giá (AddReview):
Xử lý biểu mẫu (Form) để gửi nội dung đánh giá mới.
Hỗ trợ chế độ "Edit" khi người dùng nhấn sửa đánh giá cũ (truyền dữ liệu qua location.state).
Chức năng Đăng nhập (Login):
Cho phép người dùng nhập Name và ID để giả lập trạng thái đăng nhập, làm cơ sở để thực hiện viết đánh giá.

**3.3. Thư viện và Công nghệ sử dụng**

Axios: Thư viện chính để thực hiện các yêu cầu HTTP (GET, POST, PUT, DELETE).
React Hooks: * useEffect: Tự động gọi API khi Component được render.
useState: Quản lý danh sách phim, thông tin chi tiết và trạng thái form.
React Bootstrap: Sử dụng Card, Button, Form, Media để xây dựng giao diện người dùng.

**3.4. Cách chạy chương trình**
Khởi chạy Backend:
    - Di chuyển vào thư mục backend và chạy: npm start.

Khởi chạy Frontend:
    - Di chuyển vào thư mục frontend.
    - Cài đặt: npm install.
    - Chạy ứng dụng: npm start.

Kiểm tra kết nối tại địa chỉ: http://localhost:3000.

4. **Tình trạng hoàn thành**
Nội dung đã hoàn thành: 100% (Từ Bài 1 đến Bài 4 theo tài liệu hướng dẫn HDBT 5.2.2).

Kết quả: Ứng dụng Movie Reviews đã hoạt động hoàn chỉnh từ giao diện đến cơ sở dữ liệu. Người dùng có thể tìm kiếm phim, đăng nhập và thực hiện đầy đủ các thao tác quản lý đánh giá phim một cách mượt mà.