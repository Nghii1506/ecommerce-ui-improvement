# 👗 RECHIC — Lookbook Studio Minimalist Chic

> **Trường Đại học Kinh tế TP. Hồ Chí Minh (UEH)**  
> **Môn học:** Phát triển ứng dụng Web / Thương mại Điện tử  
> **Bài tập:** Cá nhân - Buổi 2: Củng cố HTML5 & Áp dụng CSS3  
> **Giảng viên hướng dẫn:** TS. Nguyễn Mạnh Tuấn  

---

## 📋 Thông Tin Sinh Viên

- **Họ và tên:** Nguyễn Hoàng Bảo Nghi
- **Mã số sinh viên (MSSV):** 31231022898
- **Lớp:** K50 - EE0001
- **GitHub Repository:** `https://github.com/username/rechic-chic-store`

---

## 🎯 1. Giới Thiệu Dự Án & Website Tham Khảo

### 1.1 Website tham khảo
Dự án được xây dựng lấy cảm hứng từ thương hiệu thời trang nữ cao cấp **RECHIC Vietnam** (`rechicbrand.com`).

### 1.2 Trọng tâm giao diện cải tiến
Website tập trung tối ưu trải nghiệm mua sắm trực tuyến cho dòng sản phẩm thời trang nữ thiết kế (Lookbook Studio):
- **Header & Navigation:** Thanh điều hướng 4 trang chính (*Trang chủ, Sản phẩm, Blog, Liên hệ*) phối hợp nhận diện thương hiệu Rechic Crimson Red (`#B8192C`).
- **Danh sách sản phẩm dạng Grid:** Hiển thị mượt mà các thiết kế đầm Origami chiết eo, set gile peplum, áo lụa satin viền ren, quần ống rộng với nhãn giảm giá.
- **Chi tiết sản phẩm (Product Detail Modal):** Cửa sổ xem nhanh chất liệu (*Taffeta, Tuyết mưa, Satin*), hướng dẫn chọn size theo kg, bộ chọn màu sắc và chính sách bảo quản.
- **Giỏ hàng trượt Minh bạch Chi phí (Cart Drawer):** Tự động tính toán Tổng tiền hàng, Giảm giá Shop Voucher (-50.000đ), Mã Miễn phí vận chuyển (-30.000đ) và Tổng thanh toán thực tế ở mọi thao tác.
- **Blog thời trang (Blog Reader Modal):** Tích hợp cửa sổ đọc bài viết chuyên sâu về mẹo phối đồ tôn dáng khi ấn nút *"Xem thêm"*.

---

## 📁 2. Cấu Trúc Thư Mục Dự Án

```text
rechic-chic-store/
├── index.html             # Mã nguồn trang web chính (HTML5 + JS logic)
├── css/
│   └── style.css          # Tệp định dạng giao diện CSS3
├── images/                # Thư mục hình ảnh Lookbook Studio
│   ├── dam-origami.jpg
│   ├── set-gile.jpg
│   ├── ao-lua-satin.jpg
│   └── set-peplum.jpg
├── README.md              # Báo cáo tổng quan dự án (File này)
└── AI_USAGE.md            # Báo cáo nhật ký sử dụng AI có kiểm soát
```

---

## 🛠️ 3. Kỹ Thuật HTML5 & CSS3 Đã Áp Dụng

| Kỹ thuật | Chi tiết triển khai |
| :--- | :--- |
| **HTML5 Semantics** | Sử dụng đúng cấu trúc ngữ nghĩa: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`. |
| **CSS Box Model** | Khai báo `box-sizing: border-box`, tinh chỉnh `margin`, `padding`, `border` và `border-radius` cho toàn bộ thẻ sản phẩm. |
| **CSS Flexbox** | Căn chỉnh Header, menu Nav, bộ chọn Size S/M/L, bộ chọn màu và các hàng tính chi phí trong giỏ hàng (`display: flex`, `justify-content`, `align-items`, `gap`). |
| **CSS Grid** | Bố trí danh sách sản phẩm dạng lưới linh hoạt với `grid-template-columns: repeat(auto-fill, minmax(270px, 1fr))` và `gap: 30px`. |
| **Hover & Focus** | Thêm chuyển động di chuột `:hover` phóng to ảnh `transform: scale(1.05)`, đổi màu nút bấm và trạng thái `:focus-visible` hỗ trợ phím Tab. |
| **Responsive Design** | Đảm bảo giao diện hiển thị tối ưu trên 3 kích thước: Desktop (1366px), Tablet (768px) và Mobile (390px). |

---

## 💻 4. Hướng Dẫn Chạy Dự Án

1. **Clone repository:**
   ```bash
   git clone https://github.com/username/rechic-chic-store.git
   cd rechic-chic-store
   ```
2. **Mở giao diện:**
   - Kích chuột đúp vào tệp `index.html` để chạy trực tiếp trên trình duyệt web.
   - Hoặc mở thư mục bằng **VS Code** và chạy bằng extension **Live Server**.

---

## 🧪 5. Bảng Kiểm Thử Giao Diện (Test Matrix)

| Nội dung kiểm tra | Trạng thái | Ghi chú |
| :--- | :---: | :--- |
| **Hiển thị trang `index.html`** |  Đạt | Logo Rechic & Banner Lookbook hiển thị sắc nét |
| **Liên kết tệp `css/style.css`** |  Đạt | Giao diện chuẩn màu Crimson Red & chuẩn phông chữ |
| **Hình ảnh sản phẩm có thẻ `alt`** |  Đạt | Ảnh hiển thị đúng tỷ lệ 3:4 không bị méo |
| **Thanh điều hướng 4 trang** |  Đạt | Chuyển đổi Trang chủ, Sản phẩm, Blog, Liên hệ mượt mà |
| **Bố cục Flexbox & Grid** |  Đạt | Tự động co giãn theo kích thước màn hình |
| **Hiệu ứng Hover & Transition** |  Đạt | Phóng to ảnh và đổi màu nút khi di chuột |
| **Modal Mô tả Chi tiết Sản phẩm** |  Đạt | Chọn được size/màu và xem thông tin chất liệu |
| **Giỏ hàng trượt Drawer & Tính chi phí** |  Đạt | Tính đúng Tổng tiền = Tiền hàng - Voucher + Phí ship |
| **Modal Đọc Bài Viết Blog** |  Đạt | Nút "Xem thêm" mở bài viết đầy đủ |

---

## ✍️ 6. Trả Lời 7 Câu Hỏi Kiến Thức (Buổi 2)

#### Câu 1: Trong khu vực giao diện của em, em đã sử dụng những phần tử HTML5 nào? Vì sao em chọn chúng?
- **Các phần tử:** `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<h1>`-`<h3>`, `<img>`, `<button>`.
- **Lý do chọn:** Các phần tử ngữ nghĩa giúp mã nguồn chuẩn hóa theo tiêu chuẩn W3C, giúp công cụ tìm kiếm (SEO) dễ dàng thu thập dữ liệu và hỗ trợ trình đọc màn hình cho người khiếm thị.

#### Câu 2: Giải thích sự khác nhau giữa `margin` và `padding`. Cho ví dụ từ thẻ sản phẩm của em.
- **Khác nhau:**
  - `padding` (khoảng cách trong): Tính từ nội dung đến đường viền phần tử.
  - `margin` (khoảng cách ngoài): Khoảng cách đẩy phần tử ra xa các phần tử lân cận.
- **Ví dụ:** Trong `.product-card`, `padding: 16px` giúp chữ và nút cách mép khung thẻ, còn `margin-bottom: 24px` giúp thẻ sản phẩm cách hàng sản phẩm bên dưới.

#### Câu 3: Trong bài của em, Flexbox được sử dụng ở đâu? Giải thích tác dụng của `justify-content` và `align-items`.
- **Vị trí:** Dùng ở Header (`.header-container`), Menu (`.main-nav ul`), Bộ chọn size và các dòng tóm tắt chi phí giỏ hàng.
- **Tác dụng:** `justify-content: space-between` đẩy Logo sang trái và menu/giỏ hàng sang phải; `align-items: center` căn gióng các phần tử thẳng hàng theo trục ngang.

#### Câu 4: CSS Grid khác Flexbox như thế nào? Vì sao em sử dụng Grid cho danh sách sản phẩm?
- **Khác nhau:** Flexbox dàn trang 1 chiều (hàng hoặc cột), CSS Grid dàn trang 2 chiều (vừa hàng vừa cột).
- **Lý do:** CSS Grid giúp tự động chia danh sách sản phẩm thành các cột đều đặn (`repeat(auto-fill, minmax(270px, 1fr))`) và tự động xuống hàng khi thu nhỏ màn hình.

#### Câu 5: Nếu xóa quy tắc CSS `display: grid` khỏi danh sách sản phẩm, giao diện sẽ thay đổi như thế nào?
- Các thẻ sản phẩm `<article>` sẽ trở về hiển thị khối mặc định (`display: block`) và bị xếp chồng lên nhau thành một cột dọc chiếm 100% chiều rộng.

#### Câu 6: Vì sao cần sử dụng thuộc tính `alt` cho hình ảnh sản phẩm?
- Giúp hiển thị văn bản mô tả nếu ảnh bị lỗi đường dẫn.
- Hỗ trợ công cụ tìm kiếm (Google Images) lập chỉ mục sản phẩm.
- Hỗ trợ người dùng khiếm thị đọc nội dung qua trình đọc màn hình.

#### Câu 7: Hãy nêu một đề xuất của AI mà em đã kiểm tra hoặc điều chỉnh trước khi đưa vào bài tập.
- **Điều chỉnh:** AI ban đầu đề xuất giao diện và sản phẩm sặc sỡ không đúng phong cách thương hiệu. Em đã điều chỉnh lại tông màu Crimson Red (`#B8192C`) và phối màu studio tối giản, đồng thời bổ sung thêm Modal Trang Chi tiết sản phẩm để tăng tính trải nghiệm.

---

*© 2026 RECHIC Vietnam — Bài tập Phát triển ứng dụng Web / TMĐT (UEH)*
