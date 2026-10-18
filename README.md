# Thực Hành: Dựng Layout Blog Cổ Điển Bằng CSS Grid

## 1. Mục tiêu
- Sử dụng `display: grid` để biến thẻ `<body>` thành container lưới 2 chiều.
- Định nghĩa phân chia cột và hàng bằng `grid-template-columns: 2fr 1fr;` và `grid-template-rows: auto 1fr auto;`.
- Sử dụng thuộc tính `grid-column: 1 / 3;` để mở rộng Header và Footer trải dài trên toàn bộ chiều rộng (2 cột).
- Định vị tường minh vùng nội dung chính (`main`) và thanh bên (`sidebar`).

---

## 2. Các bước thực hiện tóm tắt
1. **Khởi tạo tệp HTML (`blog-layout.html` & `index.html`):**
   - Đặt class `.grid-container` cho thẻ `<body>`.
   - Tạo các thẻ ngữ nghĩa: `<header class="header">`, `<main class="main">`, `<aside class="sidebar">`, `<footer class="footer">`.
2. **Cấu hình Grid Container trong CSS (`style.css`):**
   - Kích hoạt lưới: `display: grid;`.
   - Chia 2 cột: `grid-template-columns: 2fr 1fr;` (Main Content chiếm 2 phần, Sidebar chiếm 1 phần).
   - Chia 3 hàng: `grid-template-rows: auto 1fr auto;` (Header/Footer tự động theo nội dung, hàng giữa chiếm không gian còn lại).
   - Khoảng cách ô `gap: 20px;` và chiều cao tối thiểu `min-height: 100vh;`.
3. **Sắp xếp vị trí các phần tử bằng `grid-column`:**
   - `.header`: `grid-column: 1 / 3;` chiếm trọn 2 cột từ đường kẻ 1 đến đường kẻ 3.
   - `.footer`: `grid-column: 1 / 3;` chiếm trọn 2 cột tương tự header.
   - `.main`: `grid-column: 1 / 2;` nằm ở cột 1.
   - `.sidebar`: `grid-column: 2 / 3;` nằm ở cột 2.
