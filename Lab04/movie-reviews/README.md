# BÁO CÁO THỰC HÀNH - MÔN IE213.Q21 (LAB 04)

## 1. Thông tin chung
* **Họ và tên:** Lê Trung Hải
* **MSSV:** 21522033
* **Lớp:** IE213.O21
* **Môn học:** Kỹ thuật phát triển hệ thống Web
* **Nội dung:** Thiết lập Frontend với ReactJS cho ứng dụng Movie Reviews (Lab 04)

---

## 2. Cấu trúc thư mục cập nhật

movie-reviews/
├── backend/               # (Đã hoàn thiện ở Lab 03)
├── frontend/              # MỚI - Mã nguồn ứng dụng ReactJS
│   ├── public/            # Chứa các tài nguyên tĩnh
│   ├── src/
│   │   ├── components/    # Chứa các thành phần giao diện (UI Components)
│   │   │   ├── add-review.js
│   │   │   ├── login.js
│   │   │   ├── movie.js
│   │   │   └── movies-list.js
│   │   ├── App.js         # Thành phần chính, quản lý Định tuyến (Routing) và Trạng thái (State)
│   │   ├── App.css
│   │   ├── index.js       # Điểm đầu vào của ứng dụng
│   │   └── ...
│   ├── package.json       # Quản lý thư viện và script của dự án
│   └── node_modules/
└── README.md
---

## 3. Chi tiết nội dung thực hiện (Lab 04)
3.1. Mục tiêu
* Khởi tạo dự án Frontend sử dụng thư viện ReactJS thông qua công cụ create-react-app.
* Thiết lập hệ thống điều hướng (Routing) cho ứng dụng phía Client.
* Xây dựng giao diện cơ bản bằng Bootstrap và quản lý trạng thái người dùng (Authentication state).

## 3.2. Các công việc đã hoàn thành
** Khởi tạo môi trường:
Sử dụng lệnh npx create-react-app frontend để tạo khung dự án.
Cài đặt các thư viện bổ trợ: react-bootstrap, bootstrap, và react-router-dom (hỗ trợ định tuyến).
Xây dựng cấu trúc điều hướng (App.js):
Thiết lập thanh điều hướng (Navbar) bằng React-Bootstrap với các liên kết: Movies, Login/Logout.
** Sử dụng Switch và Route để phân tách các trang:
/: Danh sách phim (MoviesList).
/movies/:id/review: Thêm đánh giá (AddReview).
/movies/:id: Chi tiết phim (Movie).
/login: Đăng nhập (Login).
** Quản lý trạng thái người dùng:
Sử dụng React.useState(null) để lưu trữ thông tin user.
Viết các hàm xử lý login và logout để cập nhật trạng thái hiển thị trên thanh Menu (hiển thị "Login" hoặc "Logout User").

## 3.3. Thư viện sử dụng
React Router Dom: Quản lý chuyển trang mà không cần tải lại trình duyệt (SPA).
React Bootstrap: Cung cấp các Component UI có sẵn như Navbar, Nav, giúp xây dựng giao diện nhanh và chuyên nghiệp.

## 3.4. Cách chạy chương trình
Di chuyển vào thư mục frontend: cd frontend.
Cài đặt các thư viện (nếu chưa có): npm install.
Khởi chạy ứng dụng: npm start.
Truy cập giao diện tại: http://localhost:3000.
---

## 4. Tình trạng hoàn thành
* **Nội dung đã hoàn thành:** 100% (Từ Bài 1 đến Bài 4 của Hướng dẫn 3.2.2).
* **Kết quả:** Hệ thống Back-end đã sẵn sàng để kết nối với Front-end, các API hoạt động ổn định và trả về đúng dữ liệu yêu cầu.
