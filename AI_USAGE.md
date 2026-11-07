# Báo Cáo Sử Dụng AI Có Kiểm Soát (AI Usage Report)

> **Dự án:** RECHIC — Lookbook Studio Minimalist Chic  
> **Môn học:** Phát triển ứng dụng Web / Thương mại Điện tử (UEH)  
> **Công cụ AI hỗ trợ:** Google Gemini  

---

##  1. Nhật Ký Prompt Tiêu Biểu & Kết Quả

| STT | Bước thực hiện | Prompt dán cho AI | Kết quả AI phản hồi | Điều chỉnh thực tế của Sinh viên |
| :---: | :--- | :--- | :--- | :--- |
| **1** | Rà soát bài Buổi 1 | *"Phân tích mã HTML cửa hàng thời trang của tôi, chỉ ra 3 lỗi bố cục và đề xuất thẻ HTML5 ngữ nghĩa phù hợp."* | AI gợi ý thay thế các thẻ `div` tràn lan bằng `<header>`, `<nav>`, `<article>`, `<aside>`. | Chấp nhận đề xuất, tái cấu trúc toàn bộ phân vùng trang theo chuẩn HTML5. |
| **2** | Bố cục CSS Grid | *"Hướng dẫn viết CSS Grid cho danh sách 4 cột sản phẩm tự động co giãn 2 cột trên điện thoại."* | AI cung cấp đoạn mã CSS Grid với `grid-template-columns` và media query. | Tự tinh chỉnh lại tham số `gap: 30px` và thêm `aspect-ratio: 3/4` để giữ tỷ lệ ảnh chuẩn Lookbook. |
| **3** | Phong cách RECHIC | *"Thiết kế đồ theo style thương hiệu RECHIC đơn giản, tạo modal xem chi tiết sản phẩm và ảnh studio chuẩn."* | AI tạo bộ sản phẩm gồm Đầm Origami, Set Gile Halter, Áo Lụa Satin và khung Modal chi tiết. | Yêu cầu AI cập nhật mã màu Crimson Red (`#B8192C`), tối giản chi tiết thừa và bổ sung bảng hướng dẫn chọn size theo kg. |
| **4** | Tài liệu Báo cáo | *"Tạo file README.md và AI_USAGE.md chuẩn bài tập Buổi 2 UEH chứa đáp án 7 câu hỏi và bảng test."* | AI tổng hợp báo cáo Markdown hoàn chỉnh theo yêu cầu đề bài. | Rà soát thông tin cá nhân (MSSV, Lớp) và đối chiếu với mã nguồn trước khi push lên GitHub. |

---

##  2. Đánh Giá Năng Lực Kiểm Soát Mã Nguồn Của Sinh Viên

Trong suốt quá trình làm bài, sinh viên đảm bảo vai trò chủ đạo trong việc kiểm soát mã nguồn:

1. **Tuân thủ yêu cầu đề bài:** AI có xu hướng gợi ý các thư viện bên ngoài (như Tailwind CSS hay Bootstrap). Sinh viên đã chủ động yêu cầu chuẩn hóa về CSS thuần (Pure CSS3), Flexbox và CSS Grid đúng mục tiêu bài tập Buổi 2.
2. **Tối ưu hóa hình ảnh & trải nghiệm:** Tự chọn lọc bộ ảnh Lookbook studio sắc nét chuẩn tỷ lệ 3:4, viết đầy đủ thuộc tính `alt` cho từng hình ảnh.
3. **Kiểm thử tính năng tương tác:** Kiểm tra kỹ lưỡng logic JavaScript tính chi phí minh bạch trong Giỏ hàng trượt Drawer, đảm bảo các khoản giảm giá Shop Voucher (-50k) và FreeShip (-30k) được tính toán chính xác.
