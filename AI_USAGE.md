# AI Usage Log

## 1. Công cụ AI
- **ChatGPT / Gemini**

## 2. Mục đích sử dụng
- Phân tích ưu/nhược điểm trải nghiệm người dùng (UX/UI) trên Shopee.
- Đề xuất bố cục HTML/CSS dạng Responsive Grid.
- Giải thích các thuộc tính CSS như Flexbox, Grid và Media Queries.

## 3. Prompt đã sử dụng
1. *"Hãy phân tích giao diện và chức năng của website Shopee ở 5 khu vực: Trang chủ, Danh mục, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng..."*
2. *"Tôi muốn tạo giao diện HTML/CSS cải tiến hiển thị thẻ sản phẩm và bảng tổng chi phí giỏ hàng minh bạch, hỗ trợ Mobile và Desktop. Hãy đề xuất bố cục..."*

## 4. Kết quả AI đề xuất
- Đề xuất chia bố cục màn hình Desktop làm 2 phần (3 cột sản phẩm + 1 cột tổng chi phí giỏ hàng).
- Đề xuất khung thẻ sản phẩm hiển thị nhãn giảm giá ở góc trên cùng.

## 5. Kiểm tra và điều chỉnh
- **Điểm đã điều chỉnh:** Sửa lại font chữ, bảng màu chuẩn theo thương hiệu TMĐT (màu cam đỏ `#ee4d2d`), thêm thẻ nhãn vận chuyển (FreeShip) và chỉnh lại CSS Media Query cho điện thoại hiển thị 1-2 cột hợp lý.

## 6. Phần tôi hiểu và có thể giải thích
- Hiểu cấu trúc thẻ semantic HTML5 (`<header>`, `<main>`, `<article>`, `<aside>`, `<footer>`).
- Hiểu cách dùng CSS Grid `repeat(auto-fill, minmax(...))` để tự động co giãn sản phẩm theo độ phân giải màn hình.
- Hiểu cách dùng `@media (min-width: 992px)` để chuyển từ giao diện dọc (Mobile) sang dạng cột (Desktop).