# NoVarAI — Website giới thiệu sản phẩm công nghệ

- **Sinh viên:** Đinh Trung Hiếu
- **MSSV:** 125000193
- **Tên repository theo đề:** `Hieu_DinhTrung_125000193` (dùng ASCII để tránh lỗi ký tự có dấu)
- **Công nghệ:** HTML5 và CSS3; không có tệp `.js`
- **Font:** Roboto

## 1. Cấu trúc dự án

- `index.html` — trang web, cấu trúc Semantic HTML5, 16 sản phẩm, danh mục và biểu mẫu liên hệ minh họa.
- `style.css` — CSS Variables, Flexbox/Grid, responsive, hover/focus, chuyển động và menu hamburger bằng CSS.
- `PROMPT_LOG.md` — nhật ký Prompt Engineering theo khung đề thi.
- `TEST_RESULTS.md` — kết quả kiểm tra tĩnh và checklist kiểm thử thủ công.

## 2. Nội dung và giao diện

NoVarAI là website giới thiệu sản phẩm công nghệ với phong cách xanh đen/cyan, font Roboto, hình ảnh sản phẩm, danh mục liên kết đến sản phẩm tương ứng, phần giới thiệu thương hiệu, ưu điểm và liên hệ. Lưới sản phẩm có 4 cột trên desktop rộng, 3 cột trên màn hình vừa, 2 cột trên tablet và 1 cột trên điện thoại. Giá, thông tin sản phẩm và địa chỉ/email trong bản demo là nội dung minh họa, không phải dữ liệu bán hàng thật.

## 3. Chạy website

Mở `index.html` bằng Chrome hoặc Edge. Font, Animate.css và hình ảnh Unsplash được tải từ Internet. Khi không có Internet, một số tài nguyên bên ngoài có thể không hiển thị. Biểu mẫu liên hệ chỉ là giao diện HTML, chưa gửi dữ liệu đến máy chủ.

## 4. Hiệu ứng và giới hạn thư viện

- **Animate.css:** được nạp bằng stylesheet CDN và dùng các class `animate__...` trong phần hero.
- **Hiệu ứng cuộn:** website dùng CSS scroll-driven animations (`animation-timeline: view()`) trong trình duyệt hỗ trợ; nếu không hỗ trợ, nội dung vẫn hiển thị bình thường. `data-aos` chỉ được dùng làm dấu đánh dấu.
- **AOS chính thức:** chưa tích hợp runtime/khởi tạo AOS. Đề thi yêu cầu Animate.css và AOS; do bản này được giới hạn ở HTML/CSS, hiệu ứng cuộn hiện tại là giải pháp CSS thay thế chứ không được tính là AOS chính thức. Nếu giảng viên chấm bắt buộc AOS, cần hỏi giảng viên có cho phép runtime JavaScript của thư viện hay không. Không nên ghi rằng AOS chính thức đã tích hợp thành công.
- **Hiệu ứng chữ:** chỉ tên thương hiệu `NoVarAI` trong phần mở đầu có hiệu ứng kiểu gõ chữ.

## 5. Kiểm thử trước khi nộp

Các kiểm tra tĩnh được ghi trong `TEST_RESULTS.md`. Chưa thể khẳng định website đã được kiểm thử trực quan trên mọi trình duyệt hoặc đã có GitHub Pages live cho đến khi tự mở trang và triển khai repository.

## 6. Nộp bài bằng GitHub Pages

1. Tạo repository **Public** tên `Hieu_DinhTrung_125000193`.
2. Đưa `index.html`, `style.css`, `README.md`, `PROMPT_LOG.md`, `TEST_RESULTS.md` vào thư mục gốc repository. Không cần tạo thư mục `assets/` vì ảnh đang được gọi bằng URL bên ngoài.
3. Commit với thông điệp rõ ràng, ví dụ `Complete NoVarAI midterm website`.
4. Vào **Settings → Pages → Build and deployment**. Chọn **Deploy from a branch**, branch `main`, folder `/(root)`, rồi nhấn **Save**.
5. Chờ GitHub Pages triển khai xong, mở URL mà GitHub hiển thị và kiểm tra website bằng chính URL đó.
6. Cập nhật URL GitHub và URL GitHub Pages thật vào README và PROMPT_LOG, commit/push lần cuối.
7. Nộp cả link repository công khai và link live preview theo hướng dẫn giảng viên.

## Website trực tuyến

- **GitHub Repository:** https://github.com/TheBill0907/Hieu_DinhTrung_125000193
- **Live Demo:** https://thebill0907.github.io/Hieu_DinhTrung_125000193/

Website NoVarAI được xây dựng bằng HTML5 và CSS3, có giao diện responsive cho máy tính và thiết bị di động.
