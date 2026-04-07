# BÁO CÁO THỰC HÀNH - MÔN IE213.Q21 (LAB 03)

## 1. Thông tin chung
* **Họ và tên:** Lê Trung Hải
* **MSSV:** 21522033
* **Lớp:** IE213.O21
* **Môn học:** Kỹ thuật phát triển hệ thống Web
* **Nội dung:** Hoàn thiện Back-end cho ứng dụng Movie Reviews (Lab 03)

---

## 2. Cấu trúc thư mục cập nhật
Dự án được mở rộng thêm các tệp tin để quản lý Review:

movie-reviews/
├── backend/
│   ├── api/
│   │   ├── movies.controller.js (Cập nhật GetById, Ratings)
│   │   ├── movies.route.js      (Cập nhật Route Review & Movie Details)
│   │   └── reviews.controller.js (MỚI - Xử lý logic CRUD Review)
│   ├── dao/
│   │   ├── moviesDAO.js         (Cập nhật Aggregate & Distinct)
│   │   └── reviewsDAO.js        (MỚI - Tương tác DB Reviews)
│   ├── .env
│   ├── index.js                 (Cập nhật Inject ReviewsDAO)
│   └── server.js
└── README.md
---

## 3. Chi tiết nội dung thực hiện (Lab 03)

### 3.1. Mục tiêu
* Xây dựng đầy đủ các chức năng CRUD (Create, Read, Update, Delete) cho hệ thống đánh giá phim.
* Sử dụng MongoDB Aggregation Framework để gộp dữ liệu từ nhiều collection (Movies và Reviews).
* Quản lý bảo mật cơ bản: Chỉ người dùng tạo review mới có quyền chỉnh sửa hoặc xóa review đó.

### 3.2. Các chức năng chính đã hoàn thành
1. **Quản lý Review:**
   - **POST:** Cho phép người dùng gửi đánh giá mới vào cơ sở dữ liệu.
   - **PUT:** Cập nhật nội dung đánh giá dựa trên `review_id` và xác thực `user_id`.
   - **DELETE:** Xóa đánh giá nếu người dùng gửi đúng ID của mình.
2. **Nâng cao truy vấn Movie:**
   - **Get Movie By ID:** Sử dụng `$match` và `$lookup` để lấy thông tin chi tiết một bộ phim kèm theo toàn bộ danh sách các đánh giá liên quan.
   - **Get Ratings:** Sử dụng phương thức `distinct` để lấy danh sách các phân loại phim hiện có trong hệ thống.

### 3.3. Công cụ kiểm thử
* **Insomnia / Postman:** Dùng để giả lập các request POST/PUT/DELETE với dữ liệu JSON trong Body.
* **MongoDB Compass:** Kiểm tra sự thay đổi dữ liệu trực tiếp trong các collections `movies` và `reviews`.

### 3.4. Cách chạy chương trình
1. Di chuyển vào thư mục `backend`.
2. Chạy lệnh: `npm run dev`.
3. Kiểm tra API Get Movie Details: `http://localhost:3000/api/v1/movies/id/[MOVIE_ID]`.
4. Kiểm tra API Ratings: `http://localhost:3000/api/v1/movies/ratings`.

---

## 4. Tình trạng hoàn thành
* **Nội dung đã hoàn thành:** 100% (Từ Bài 1 đến Bài 4 của Hướng dẫn 3.2.2).
* **Kết quả:** Hệ thống Back-end đã sẵn sàng để kết nối với Front-end, các API hoạt động ổn định và trả về đúng dữ liệu yêu cầu.