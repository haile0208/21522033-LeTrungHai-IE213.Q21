# BÁO CÁO THỰC HÀNH - MÔN IE213.Q21

## 1. Thông tin chung
* **Họ và tên:** Lê Trung Hải
* **MSSV:** 21522033
* **Lớp:** IE213.O21
* **Môn học:** Kỹ thuật phát triển hệ thống Web

---

## 2. Cấu trúc thư mục bài nộp
Toàn bộ nội dung bài làm được tổ chức trong thư mục `lab02` để đảm bảo tính gọn gàng:

movie-reviews/
├── backend/
│   ├── api/
│   │   ├── movies.controller.js
│   │   └── movies.route.js
│   ├── dao/
│   │   └── moviesDAO.js
│   ├── .env
│   ├── index.js
│   ├── package.json
│   └── server.js
├── screenshots/           # Thư mục chứa các ảnh minh chứng kết quả
├── script.txt             # File tổng hợp lệnh cài đặt và mã nguồn (Bài 1 & Bài 2)
└── README.md              # File báo cáo này
---

## 3. Chi tiết Lab 02

### 3.1. Mục tiêu bài thực hành
* Thiết lập môi trường phát triển Node.js và các công cụ liên quan.
* Cài đặt và cấu hình máy chủ web bằng Express.
* Kết nối máy chủ Node.js với cơ sở dữ liệu MongoDB Atlas thông qua Driver.
* Tổ chức mã nguồn theo mô hình MVC (Routes, Controllers, DAO) để xây dựng API truy xuất dữ liệu phim.

### 3.2. Công cụ / môi trường sử dụng
* **Môi trường Server:** Node.js (với npm).
* **Framework:** Express.js.
* **Cơ sở dữ liệu:** MongoDB Atlas (gói Free) và thư viện `mongodb`.
* **Công cụ hỗ trợ:** `nodemon` (tự động khởi động lại server), `dotenv` (quản lý biến môi trường), `cors`.
* **Phần mềm soạn thảo:** Visual Studio Code.
* **AI:** Gemini hỗ trợ rà soát lỗi và tổ chức mã nguồn.

### 3.3. Cách chạy chương trình
1. Mở Terminal tại thư mục `backend`.
2. Chạy lệnh `npm install` để tải và cài đặt các dependencies dựa trên `package.json`.
3. Đảm bảo file `.env` đã chứa đúng `MOVIEREVIEWS_DB_URI` với tên đăng nhập, mật khẩu và địa chỉ cluster cá nhân.
4. Khởi động máy chủ bằng lệnh: `npm run dev` (sử dụng nodemon).
5. Mở trình duyệt hoặc Postman truy cập đường dẫn: `http://localhost:3000/api/v1/movies/` để kiểm tra kết quả trả về.

### 3.4. Giải thích ngắn gọn phần chính đã thực hiện
Trong Lab 02 này (gồm Bài 1 và Bài 2), em đã thực hiện:
* **Bài 1 (Thiết lập môi trường):** Khởi tạo dự án bằng lệnh `npm init`, cài đặt các thư viện cần thiết (`express`, `mongodb`, `cors`, `dotenv`) và công cụ `nodemon`. Định cấu hình `package.json` để sử dụng ES Modules (`"type": "module"`).
* **Bài 2 (Xây dựng Backend):**
  * **Cấu hình Server (2.1, 2.2):** Tạo `server.js` khởi tạo Express app, cấu hình Middleware (CORS, JSON parse), và xử lý lỗi 404 phù hợp với Express 5. Tạo file `.env` chứa thông tin bảo mật.
  * **Kết nối DB & Khởi chạy (2.3):** Tạo `index.js` sử dụng `MongoClient` để kết nối tới MongoDB Atlas và gọi app lắng nghe trên cổng 3000.
  * **Truy xuất dữ liệu (2.5):** Xây dựng lớp `MoviesDAO` tiêm (inject) kết nối DB và viết hàm `getMovies` truy vấn danh sách phim có hỗ trợ phân trang và bộ lọc theo `title` hoặc `rated`.
  * **Xử lý logic (2.6):** Xây dựng lớp `MoviesController` tiếp nhận yêu cầu từ client, lấy thông số từ URL query, gọi logic trong `MoviesDAO` và định dạng trả về chuỗi JSON.
  * **Định tuyến (2.4, 2.7):** Thiết lập tệp `movies.route.js` để định tuyến yêu cầu HTTP GET tại gốc (`/`) tới hàm `apiGetMovies` của Controller.

### 3.5. Kết quả thực hiện & Hình ảnh minh họa
Máy chủ đã khởi động thành công và kết nối tới CSDL. API trả về chuẩn xác danh sách phim từ MongoDB dưới định dạng JSON. Hình ảnh Terminal báo khởi chạy thành công và kết quả gọi API trên trình duyệt được đính kèm trong thư mục `screenshots`.

---

## 4. Tình trạng hoàn thành
* **Những nội dung đã hoàn thành:** 100% các yêu cầu từ Bài 1 và Bài 2.
* **Những nội dung chưa hoàn thành:** Không có.