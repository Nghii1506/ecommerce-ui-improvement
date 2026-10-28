# E-commerce UI Improvement

## BUOI 1

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

## BUOI 2

1. **Các phần tử HTML5 ngữ nghĩa đã dùng:** `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`. Dùng để phân chia cấu trúc trang rõ ràng, dễ bảo trì và tối ưu cho SEO.
2. **Khác biệt Margin vs Padding:** `padding` là khoảng cách bên trong (từ nội dung tới viền). `margin` là khoảng cách bên ngoài (từ viền tới phần tử khác). Ví dụ: `.product-card` dùng `padding: 12px` để nội dung không dính sát viền.
3. **Ứng dụng Flexbox:** Dùng ở `.header-content` và `.nav-menu`. `justify-content: space-between` giúp đẩy Logo sang trái, Menu sang phải; `align-items: center` căn giữa theo chiều dọc.
4. **CSS Grid vs Flexbox:** Flexbox tối ưu bố cục 1 chiều, Grid tối ưu 2 chiều (hàng & cột). Dùng Grid cho `.product-grid` giúp tự động chia cột sản phẩm đều đặn và co giãn linh hoạt.
5. **Nếu xóa `display: grid`:** Các thẻ sản phẩm `<article>` sẽ trở về dạng khối mặc định (`block`) và xếp chồng thành 1 cột dọc từ trên xuống.
6. **Tác dụng của thuộc tính `alt`:** Mô tả hình ảnh khi ảnh bị lỗi không hiển thị, hỗ trợ trình đọc màn hình cho người khiếm thị và giúp Google hiểu nội dung ảnh.
7. **Đề xuất AI đã điều chỉnh:** AI đề xuất dùng kích thước ảnh cố định `height: 200px`, em đã đổi thành `aspect-ratio: 1/1` kết hợp `object-fit: cover` để ảnh hiển thị chuẩn tỷ lệ vuông và không bị móp méo.