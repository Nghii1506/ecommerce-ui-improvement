# E-commerce UI Improvement

## 1. Giới thiệu
Dự án nhỏ nhằm cải tiến giao diện hiển thị danh sách sản phẩm và bảng tóm tắt chi phí giỏ hàng minh bạch trên trang thương mại điện tử, giúp người dùng dễ so sánh giá và không bị nhầm lẫn bởi các khoản phí/voucher [source 3].

## 2. Website tham khảo
- **Tên website:** Shopee Việt Nam [source 3]
- **URL:** https://shopee.vn [source 3]
- **Khu vực đã khảo sát:** Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng [source 3].

## 3. Chức năng
- Hiển thị danh sách sản phẩm dạng thẻ (Product Card) chuẩn responsive [source 3].
- Thể hiện rõ giá gốc, giá khuyến mãi và phần trăm giảm giá [source 3].
- Bảng tổng kết chi phí tính toán rõ ràng các khoản giảm giá và tổng thanh toán thực tế [source 3].
- Tương thích tốt trên cả màn hình máy tính và điện thoại [source 3].

## 4. Công nghệ
- HTML5 [source 3]
- CSS3 (Flexbox & CSS Grid, Media Queries) [source 3]

## 5. Cách chạy
Mở file `index.html` trực tiếp bằng trình duyệt web (Chrome, Edge, Firefox) [source 3].

## 6. Cải tiến đã thực hiện
- **Vấn đề ban đầu:** Trên Shopee, giá gốc/giá giảm đôi khi rối mắt, phần tính tổng chi phí tại giỏ hàng bị ẩn nhiều cấp voucher khiến người dùng khó tính tổng tiền thực tế [source 3].
- **Thay đổi thực hiện:** 
  - Thiết kế thẻ sản phẩm nổi bật phần trăm giảm giá và nhãn vận chuyển [source 3].
  - Xây dựng bảng "Tóm tắt chi phí minh bạch" hiển thị rõ ràng từng dòng: Tiền hàng - Giảm giá shop - Mã ship + Phí ship = Tổng tiền cuối cùng [source 3].

## 7. Hỗ trợ từ AI
- AI hỗ trợ phân tích ưu/nhược điểm UX của Shopee và gợi ý cấu trúc HTML/CSS responsive [source 3].
- Bản thân tự tinh chỉnh màu sắc, khoảng cách padding/margin và viết bảng tính tổng chi phí minh bạch [source 3].

---

## 📋 Danh Sách Câu Trả Lời Báo Cáo

### 1. Thẻ Semantic HTML5 đã sử dụng và lý do lựa chọn

Trong dự án, các phần tử HTML5 Semantic được sắp xếp và lựa chọn theo mục đích cụ thể:

* `<header>`: Đóng gói phần đầu trang, chứa thương hiệu (Logo) và thanh điều hướng.
* `<nav>`: Định vị khu vực chứa các liên kết điều hướng chính của website.
* `<main>`: Bao bọc khu vực nội dung chính và duy nhất của trang web (không lặp lại ở các trang khác).
* `<section>`: Gom nhóm khu vực danh sách sản phẩm nổi bật thành một khối logic riêng biệt.
* `<article>`: Đóng gói từng thẻ sản phẩm. Mỗi sản phẩm là một đơn vị nội dung độc lập, có thể tái sử dụng hoặc chia sẻ riêng lẻ.
* `<figure>` & `<img>`: Bao bọc hình ảnh sản phẩm kèm theo mô tả ngữ nghĩa rõ ràng.
* `<footer>`: Chứa thông tin chân trang và bản quyền website.

> **Lý do lựa chọn:** Việc áp dụng Semantic HTML5 giúp tối ưu hóa **SEO** (giúp công cụ tìm kiếm hiểu rõ cấu trúc dữ liệu trang) và nâng cao tính **Accessibility (a11y)** cho trình đọc màn hình của người thị lực kém.

---

### 2. Phân biệt `margin` và `padding` trong Thẻ Sản Phẩm

| Tiêu chí | `margin` (Lề ngoài) | `padding` (Đệm trong) |
| :--- | :--- | :--- |
| **Định nghĩa** | Vùng không gian nằm **bên ngoài** đường viền (border). | Vùng không gian nằm **bên trong** đường viền, giữa border và nội dung. |
| **Tác dụng** | Tạo khoảng cách đẩy phần tử ra xa các phần tử xung quanh. | Tạo khoảng không gian đệm giúp nội dung không bị dính vào viền. |
| **Ví dụ thực tế** | `margin: 8px` trên `.product-card` tạo khoảng cách đẩy các thẻ sản phẩm tách rời nhau. | `padding: 16px` trên `.product-card` tạo khoảng trống giữa viền khung và hình ảnh/chữ bên trong. |

---

### 3. Ứng dụng Flexbox & Tác dụng của `justify-content`, `align-items`

Flexbox được ứng dụng tại 2 khu vực chính:
1. **Header (`<header>`):** Sắp xếp Logo và Menu nằm ngang.
2. **Thẻ sản phẩm (`.product-card` & `.product-info`):** Sắp xếp hình ảnh, tên, giá và nút bấm theo hàng dọc.

#### Giải thích thuộc tính:
* `justify-content`: Điều chỉnh phân bổ các phần tử con dọc theo **trục chính (Main Axis)**.
  * *Ứng dụng:* `justify-content: space-between` trong header giúp đẩy Logo sang sát góc trái và Menu sang sát góc phải.
* `align-items`: Căn dóng các phần tử con dọc theo **trục vuông góc (Cross Axis)**.
  * *Ứng dụng:* `align-items: center` trong `.product-info` căn chỉnh tất cả tiêu đề, giá tiền và nút bấm nằm ngay chính giữa theo chiều ngang.

---

### 4. So sánh CSS Grid vs Flexbox & Lý do chọn Grid cho Danh sách Sản phẩm

* **Khác biệt cốt lõi:**
  * **Flexbox:** Bố cục **1 chiều** (1D - theo hàng ngang HOẶC cột dọc). Phù hợp cho các thành phần giao diện nhỏ hoặc dãy phần tử đơn lẻ.
  * **CSS Grid:** Bố cục **2 chiều** (2D - quản lý đồng thời cả hàng ngang VÀ cột dọc).

* **Lý do chọn Grid cho Danh sách Sản phẩm:**
  * Danh sách sản phẩm đòi hỏi chia layout dạng lưới 2 chiều phức tạp (nhiều hàng, nhiều cột).
  * CSS Grid cho phép tự động chia cột linh hoạt với cú pháp:
    ```css
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 24px;
    ```
  * Cách làm này giúp các thẻ sản phẩm tự động co giãn và xuống hàng chuẩn Responsive mà không cần dùng Media Queries hay tính toán `width %` thủ công.

---

### 5. Tác động khi xóa thuộc tính `display: grid`

Nếu xóa dòng `display: grid` khỏi container `.product-grid`:
* Khối chứa sẽ quay về dạng khối mặc định (`display: block`).
* Tất cả các thẻ sản phẩm `<article>` bên trong sẽ **bị vỡ cấu trúc lưới và xếp chồng lên nhau thành 1 cột dọc duy nhất** từ trên xuống dưới.
* Màn hình bị kéo dài theo chiều dọc và làm mất hoàn toàn giao diện dạng lưới ban đầu.

---

### 6. Vai trò của thuộc tính `alt` trong thẻ `<img>`

Thuộc tính `alt` (Alternative Text) cho hình ảnh sản phẩm đóng vai trò quan trọng vì 3 lý do:

1. **Hỗ trợ truy cập (Accessibility - a11y):** Trình đọc màn hình (Screen Reader) sẽ đọc nội dung thẻ `alt` để người khiếm thị hiểu được hình ảnh sản phẩm hiển thị gì.
2. **Hiển thị dự phòng (Fallback):** Khi kết nối mạng yếu hoặc đường dẫn ảnh bị lỗi (404), văn bản trong `alt` sẽ hiển thị thay thế để người dùng không bị mất thông tin.
3. **Tối ưu hóa SEO:** Giúp trình đọc của Google Images quét và hiểu ngữ cảnh của bức ảnh, giúp tăng xếp hạng hình ảnh trên công cụ tìm kiếm.

---

### 7. Đánh giá và điều chỉnh đề xuất của AI

* **Gợi ý ban đầu từ AI:**
  * AI đề xuất chia cột cố định bằng `grid-template-columns: repeat(4, 1fr);`.
  * AI sử dụng các thẻ `<div>` không có ngữ nghĩa để bao bọc thẻ sản phẩm.

* **Kiểm tra & Điều chỉnh thực tế:**
  1. **Tối ưu Responsive:** Thay `repeat(4, 1fr)` thành `repeat(auto-fit, minmax(250px, 1fr))` để giao diện tự động thích ứng trên màn hình di động mà không bị tràn khung.
  2. **Tối ưu HTML Semantic:** Thay các thẻ `<div>` bọc sản phẩm bằng thẻ ngữ nghĩa chuẩn HTML5 là `<article>`.
