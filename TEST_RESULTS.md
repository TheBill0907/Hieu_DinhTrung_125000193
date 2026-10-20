# TEST_RESULTS — NoVarAI

- **Sinh viên:** Đinh Trung Hiếu
- **MSSV:** 125000193
- **Phạm vi:** kiểm tra tĩnh mã nguồn HTML/CSS và đối chiếu tài liệu. Chưa phải kiểm thử trình duyệt trực quan.

## Kết quả kiểm tra tĩnh

| Hạng mục | Kết quả |
|---|---|
| HTML được parser đọc thành công | ĐẠT |
| `header`, `nav`, `main`, `section`, `article`, `footer` | ĐẠT |
| Số thẻ `article` tổng cộng | 20 |
| Số thẻ sản phẩm `.product-card` | 16 |
| Ảnh có thuộc tính `alt` | 16/16 |
| Liên kết neo nội bộ trỏ đến ID tồn tại | ĐẠT |
| CSS Variables trong `:root` | ĐẠT |
| CSS Grid/Flexbox và media queries responsive | ĐẠT; sản phẩm 4 cột desktop rộng, 3 cột ≤1100px, 2 cột ≤820px, 1 cột ≤600px |
| Trạng thái `:hover`, `:focus-visible` | ĐẠT về mặt mã nguồn |
| `prefers-reduced-motion` | ĐẠT về mặt mã nguồn |
| Animate.css stylesheet và class animation | ĐẠT về mặt mã nguồn |
| Hiệu ứng cuộn CSS có fallback hiển thị nội dung | ĐẠT về mặt mã nguồn |
| Thẻ `<script>` / tệp `.js` | Không có |
| AOS chính thức | CHƯA TÍCH HỢP — không có runtime/khởi tạo AOS |
| Kiểm thử giao diện trực tiếp bằng trình duyệt | CHƯA THỰC HIỆN |
| GitHub Pages live preview | CHƯA TRIỂN KHAI / XÁC MINH |

## Kiểm thử thủ công bắt buộc trước khi nộp

- [ ] Mở `index.html` bằng Chrome hoặc Edge và cuộn từ đầu đến cuối.
- [ ] Xác nhận font Roboto và 16 ảnh tải được khi có Internet.
- [ ] Bấm từng liên kết điều hướng và danh mục; xác nhận nhảy đến đúng phần.
- [ ] Kiểm tra menu nằm ngang trên desktop và hamburger ở màn hình rộng 760px trở xuống.
- [ ] Thử độ rộng 1440px, 1024px, 768px, 390px và 320px; kiểm tra chữ tràn, ảnh méo và thanh cuộn ngang.
- [ ] Thử biểu mẫu: đây chỉ là form minh họa HTML, không có backend xử lý dữ liệu.
- [ ] Triển khai GitHub Pages, mở URL công khai và kiểm tra lại bằng URL đó.

## Giới hạn quan trọng đối với rubric

Đề thi yêu cầu tích hợp Animate.css và AOS. Animate.css đã được nạp qua stylesheet. Hiệu ứng cuộn hiện tại được tự viết bằng CSS; `data-aos` không tự làm AOS chạy và không thay thế runtime chính thức. Vì gói này giữ giới hạn HTML/CSS, tiêu chí AOS chính thức chưa được đáp ứng đầy đủ. Cần hỏi giảng viên nếu tiêu chí này bắt buộc.

Không ghi website đã chạy tốt trên mọi trình duyệt hoặc đã có GitHub Pages cho đến khi tự kiểm tra trực tiếp.
