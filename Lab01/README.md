# BÁO CÁO THỰC HÀNH - MÔN IE213.Q21

## 1. Thông tin chung
* **Họ và tên:** Lê Trung Hải  
* **MSSV:** 21522033
* **Lớp:** IE213.O21
* **Môn học:** Kỹ thuật phát triển hệ thống Web

---

## 2. Cấu trúc thư mục bài nộp
Toàn bộ nội dung bài làm được tổ chức trong thư mục `lab01` để đảm bảo tính gọn gàng:

lab01/
├── screenshots/           # Thư mục chứa các ảnh minh chứng kết quả
├── script.txt             # File chứa toàn bộ mã lệnh MONGOSH (2.1 -> 2.10)
└── README.md              # File báo cáo này
---

## 3. Chi tiết Lab 01

### 3.1. Mục tiêu bài thực hành
* Cấu hình và triển khai thành công MongoDB Atlas Cluster.
* Nắm vững cách kết nối cơ sở dữ liệu bằng chuỗi Connection String qua MongoDB Compass.
* Sử dụng thành thạo công cụ MONGOSH để thực thi các câu lệnh truy vấn dữ liệu NoSQL (Create, Read, Update, Delete) và thống kê (Aggregation).

### 3.2. Công cụ / môi trường sử dụng
* **Môi trường Cloud:** MongoDB Atlas (Gói Free M0).
* **Phần mềm quản lý:** MongoDB Compass.
* **Môi trường thực thi lệnh:** MongoDB Shell (MONGOSH) tích hợp sẵn trong Compass.
* **AI:** Gemini hỗ trợ tổ chức README và xây dựng code.

### 3.3. Cách chạy chương trình
1. Mở phần mềm **MongoDB Compass**.
2. Dán chuỗi kết nối (Connection String) của Cluster vào ô URI và nhấn **Connect**.
3. Mở Terminal **MONGOSH** ở góc dưới màn hình giao diện Compass.
4. Chạy lệnh chỉ định cơ sở dữ liệu: `use 21522033-IE213`.
5. Sao chép lần lượt các câu lệnh trong file `script.txt` đính kèm trong thư mục nộp bài và dán vào Shell để thực thi.

### 3.4. Giải thích ngắn gọn phần chính đã thực hiện
Trong bài tập này (từ câu 2.1 đến 2.10), em đã áp dụng các kỹ thuật chính sau:
* **Ràng buộc dữ liệu (Câu 2.3):** Dùng `createIndex({ id: 1 }, { unique: true })` để đảm bảo trường `id` không bị trùng lặp.
* **Truy vấn với điều kiện (Câu 2.4 - 2.6):** Sử dụng các toán tử lọc như `$and`, `$gt` (lớn hơn), `$lt` (nhỏ hơn) để tìm kiếm theo độ tuổi; và `$exists: true` để tìm các document có chứa trường `middle name`.
* **Cập nhật dữ liệu (Câu 2.7 - 2.9):** Dùng `updateMany()` kết hợp `$unset` để xóa trường dữ liệu thừa, và `$set` để thêm/sửa dữ liệu hàng loạt dựa trên điều kiện `$in`.
* **Thống kê dữ liệu (Câu 2.10):** Dùng Aggregation Framework (`aggregate`). Cụ thể là sử dụng `$group` để nhóm nhân viên theo `organization`, kết hợp bộ tích lũy `$sum` để tính tổng tuổi và `$avg` để tính tuổi trung bình.

### 3.5. Kết quả thực hiện & Hình ảnh minh họa
Các câu lệnh đều chạy thành công và trả về dữ liệu chuẩn xác theo yêu cầu đề bài. Hình ảnh các câu lệnh chạy thành công được đính kèm trong thư mục `screenshots`.

---

## 4. Tình trạng hoàn thành
* **Những nội dung đã hoàn thành:** 100% các yêu cầu từ câu 2.1 đến câu 2.10.
* **Những nội dung chưa hoàn thành:** Không có.