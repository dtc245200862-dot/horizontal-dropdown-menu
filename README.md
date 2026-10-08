# [Thực hành] Tạo menu ngang (Horizontal Dropdown Menu)

## 📌 Giới thiệu & Mục tiêu
Bài thực hành kỹ thuật xây dựng **trình đơn hàng ngang có khả năng thả xuống (Horizontal Dropdown Menu)** hoàn toàn bằng **HTML & CSS thuần**:
- Hiểu cách sắp xếp các phần tử danh sách thành hàng ngang bằng thuộc tính `float: left`.
- Sử dụng cặp thuộc tính `position: relative` (ở mục cha `li`) và `position: absolute` (ở danh sách con `ul ul`) để kiểm soát chính xác vị trí hiển thị thả xuống ngay bên dưới thanh menu.
- Xử lý trạng thái ẩn mặc định bằng `visibility: hidden` và kích hoạt hiển thị khi hover bằng `:hover > ul`.
- Chuyển màu nền sang **màu Đỏ (`background-color: red`)** khi rê chuột theo đúng yêu cầu đề bài.

---

## 🛠️ Chi tiết các bộ chọn CSS theo từng bước hướng dẫn

1. **Bộ chọn phân vùng cho trình đơn (`#menu`)**:
   - `height: 50px;`: Cố định chiều cao thanh menu ngang.
   - `background-color: #000000;`: Màu nền đen đồng bộ.
2. **Bộ chọn cho các phần tử danh sách (`#menu ul li`)**:
   - `float: left;`: Đưa các phần tử danh sách xếp kề nhau thành hàng ngang.
   - `position: relative;`: Làm điểm mốc tọa độ tương đối cho menu con.
   - `list-style: none;`: Bỏ dấu chấm bullet mặc định.
3. **Bộ chọn cho các liên kết trong menu (`#menu ul li a`)**:
   - `display: block;`: Mở rộng vùng bấm bao phủ toàn bộ ô menu.
   - `width: 160px;` & `height: 50px;`: Cố định độ rộng và chiều cao cho từng mục chọn.
   - `line-height: 50px;`: Căn văn bản nằm chính giữa theo chiều dọc.
   - `text-align: center;`: Căn giữa chữ theo chiều ngang.
   - `text-decoration: none;` & `color: #ffffff;`: Bỏ gạch chân và đổi chữ sang màu trắng.
4. **Bộ chọn khi di chuột qua liên kết (`a:hover`)**:
   - `background-color: red;`: Đổi màu nền sang màu đỏ nổi bật khi con trỏ đưa qua.
5. **Bộ chọn cho danh sách con (`#menu ul ul`)**:
   - `position: absolute;`: Cố định vị trí menu con theo mục cha.
   - `top: 50px;` & `left: 0;`: Đặt menu con xuất hiện ngay phía dưới chân mục cha tương ứng.
   - `visibility: hidden;`: Ẩn danh sách con khi ở trạng thái bình thường.
6. **Bộ chọn ngắt float cho các mục con (`#menu ul ul li`)**:
   - `float: none;`: Đảm bảo các mục trong menu thả xuống được xếp thành cột dọc, không bị dạt sang ngang.
7. **Bộ chọn kích hoạt hiển thị (`#menu ul li:hover > ul`)**:
   - `visibility: visible;`: Hiển thị menu con tương ứng khi rê chuột vào mục cha.

---

## 📂 Cấu trúc thư mục dự án

```
horizontal-dropdown-menu/
├── index.html          # Trang HTML chứa cấu trúc menu ngang hai cấp
├── style.css           # Mã nguồn CSS định dạng và điều khiển hiệu ứng dropdown
├── .gitignore          # Cấu hình bỏ qua file rác hệ thống
└── README.md           # Tài liệu giải thích chi tiết các bộ chọn
```

---

## 🚀 Hướng dẫn mở và kiểm tra giao diện

1. Clone kho lưu trữ về máy:
   ```bash
   git clone https://github.com/dtc245200862-dot/horizontal-dropdown-menu.git
   ```
2. Mở file `index.html` bằng trình duyệt Chrome, Edge hoặc Firefox.
3. Rê chuột vào các mục **"Khóa học"**, **"Dịch vụ"** hoặc **"Tài liệu"** trên thanh menu ngang để kiểm tra menu con buông xuống phía dưới và màu nền đổi sang màu đỏ!
