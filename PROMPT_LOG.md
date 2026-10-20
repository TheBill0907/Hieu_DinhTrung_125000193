# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** Đinh Trung Hiếu
- **MSSV:** 125000193
- **Tên đề tài Website:** NoVarAI — Website giới thiệu sản phẩm công nghệ
- **Công cụ AI đã sử dụng:** ChatGPT và Google Antigravity
- **Repository dự kiến:** `Hieu_DinhTrung_125000193`

## 1. Yêu cầu ban đầu (System/Initial Prompt)

> Hãy xem bạn là một chuyên viên thiết kế UI/UX cho thương hiệu công nghệ hiện đại và thiết kế cho tôi website NoVarAI giới thiệu nhiều sản phẩm công nghệ. Tôi là sinh viên làm bài kiểm tra giữa kỳ môn Thiết kế Web. Tạo website tiếng Việt, dùng font Roboto, bảng màu xanh đen/cyan, tiêu đề nổi bật, ảnh sản phẩm rõ, nội dung dễ đọc và bố cục responsive cho desktop, tablet, điện thoại. Bắt buộc có `header`, `nav`, `main`, `section`, `article`, `footer`; CSS Variables trong `:root`; Flexbox/Grid; trạng thái `:hover`, `:focus-visible`; danh mục sản phẩm, phần ưu điểm, giới thiệu thương hiệu, liên hệ và footer. Chỉ sử dụng HTML/CSS, không tạo tệp `.js`. Tổ chức mã rõ ràng và không khẳng định đã kiểm thử khi chưa có bằng chứng.

## 2. Quá trình tinh chỉnh và giải quyết vấn đề

### Lần 1: Dựng khung Semantic HTML5 và CSS Variables

**Prompt đã dùng:**

> Hãy rà soát cấu trúc HTML của NoVarAI. Sử dụng đúng `header`, `nav`, `main`, `section`, `article`, `footer`; mỗi sản phẩm phải là một `article`. Quản lý màu sắc, font và khoảng cách bằng CSS Variables; kiểm tra các liên kết neo nội bộ; chỉ sửa HTML/CSS.

**Kết quả:** Trang có các vùng ngữ nghĩa chính, 16 thẻ `article` sản phẩm và các section cho nội dung chính.

**Nhận xét của sinh viên:** Cần làm rõ nhóm sản phẩm và giúp người dùng đến đúng loại thiết bị nhanh hơn.

### Lần 2: Hoàn thiện giao diện và responsive

**Prompt đã dùng:**

> Hãy nâng cấp UI/UX NoVarAI theo phong cách website công nghệ hiện đại. Làm nổi bật sản phẩm, giữ khoảng cách hợp lý, thống nhất thẻ sản phẩm, căn giá và liên kết ở cuối thẻ, thêm trạng thái hover/focus và tối ưu lưới theo desktop/tablet/mobile. Giữ nhận diện NoVarAI và chỉ dùng HTML/CSS.

**Kết quả:** Bổ sung dải thông tin, liên kết danh mục, thẻ sản phẩm, trạng thái tương tác, breakpoint responsive và quy tắc giảm chuyển động. Lưới sản phẩm cuối cùng dùng 4 cột trên desktop rộng, 3 cột ở màn hình vừa, 2 cột trên tablet và 1 cột trên điện thoại.

**Nhận xét của sinh viên:** Cần tránh khoảng trắng dư, ảnh bị nhảy và thẻ có chiều cao không đồng đều. Vì vậy ảnh được giữ hiển thị bình thường lúc tải trang, dùng `object-fit: cover`, còn hiệu ứng cuộn chỉ tác động nhẹ lên thẻ khi trình duyệt hỗ trợ.

### Lần 3: Animate.css và hiệu ứng cuộn

**Prompt đã dùng:**

> Hãy thêm Animate.css qua stylesheet cho các thành phần chính ở phần hero. Tạo hiệu ứng xuất hiện khi cuộn bằng CSS hiện đại nếu trình duyệt hỗ trợ; không được ẩn nội dung mặc định; tôn trọng `prefers-reduced-motion`. Chỉ dùng HTML/CSS, không thêm tệp JavaScript.

**Kết quả:** `index.html` nạp stylesheet Animate.css và dùng class `animate__...`; `style.css` có CSS scroll-driven animations.

**Thách thức kỹ thuật:** Đề thi yêu cầu cả Animate.css và AOS. AOS chính thức cần runtime/khởi tạo JavaScript để theo dõi cuộn. Do giới hạn chỉ HTML/CSS, bản này không tích hợp AOS chính thức; `data-aos` là thuộc tính đánh dấu, còn hiệu ứng thực tế do CSS tự xử lý.

**Prompt sửa lỗi:**

> Hãy đảm bảo hiệu ứng cuộn không đặt `opacity: 0` làm ẩn nội dung khi trình duyệt không hỗ trợ `animation-timeline: view()`. Tắt/giảm chuyển động theo `prefers-reduced-motion`, không tạo tệp `.js`, và ghi rõ giới hạn AOS trong tài liệu.

### Lần 4: Chỉnh tên thương hiệu và điều hướng

**Prompt đã dùng:**

> Chỉ áp dụng hiệu ứng gõ chữ cho tên thương hiệu `NoVarAI`, không áp dụng cho tiêu đề chính. Trên desktop, menu nằm ngang và không có dấu chấm; trên màn hình nhỏ mới hiện hamburger, mở/đóng bằng CSS. Các nút danh mục phải nhảy đến đúng sản phẩm đầu tiên của từng nhóm và không bị header che.

**Kết quả:** Hiệu ứng gõ chữ giới hạn ở tên thương hiệu; menu responsive dùng checkbox/label và CSS; liên kết danh mục trỏ đến `#product-laptop`, `#product-display`, `#product-audio`, `#product-lifestyle`, `#product-accessory`.

### Lần 5: Rà soát cuối và đồng bộ tài liệu

**Prompt đã dùng:**

> Hãy kiểm tra lại HTML, CSS, README, prompt log và test results để số lượng sản phẩm, breakpoint, hiệu ứng, file thực tế và giới hạn kỹ thuật khớp nhau. Không bịa kết quả browser testing hay GitHub Pages. Nêu rõ mục nào đã kiểm tra tĩnh và mục nào tôi phải tự kiểm tra trước khi nộp.

**Kết quả kiểm tra tĩnh:** Có 16 thẻ sản phẩm, đủ vùng Semantic HTML5, liên kết neo nội bộ không trỏ đến ID bị thiếu, không có thẻ `script` hoặc tệp `.js`; có CSS Variables, Grid/Flexbox, responsive và trạng thái hover/focus. Chi tiết ở `TEST_RESULTS.md`.

### Lần 6: Tối ưu typography Roboto, cân đối phân cấp chữ và xử lý hiệu ứng gõ chữ

**Prompt đã dùng:**

> Chỉnh lại cho tôi chữ phải cân đối, nhìn đẹp mắt bằng font chữ Roboto; hiệu ứng đầu vào mượt mà, không để chỗ chạy hiệu ứng chỗ không; bỏ khối gõ chữ NoVarAI đứng riêng trơ trọi; sửa lỗi gõ chữ NoVarAI bị nhảy xuống hàng thành một hàng cố định mượt mà.

**Kết quả:** 
1. Loại bỏ thẻ `<p class="brand-typewriter">` đứng tách rời gây thừa thãi; tích hợp hiệu ứng gõ chữ trực tiếp vào `<span class="brand-typewriter">NoVarAI</span>` trong tiêu đề `h1`.
2. Khắc phục triệt để lỗi nhảy dòng ("gõ rồi xuống hàng") bằng cách bọc cụm `cùng NoVarAI` trong `white-space: nowrap` và chuyển cơ chế hoạt hình sang `clip-path: inset()`, giữ nguyên độ rộng cố định trong suốt quá trình gõ.
3. Đồng bộ hóa chuỗi chuyển động Hero (eyebrow, h1, lead, buttons, promises, laptop visual) bằng độ trễ stagger tự nhiên; loại bỏ hiện tượng giảm opacity gây "mất chữ/mờ chữ" khi cuộn trang.
4. Tái cấu trúc toàn bộ Typography theo thang đo tỷ lệ chuẩn quốc tế với font Roboto: tăng độ cao dòng tránh đè dấu thanh tiếng Việt (`line-height: 1.22` cho tiêu đề, `1.65` cho văn bản), loại bỏ khoảng cách âm gây dính chữ, đồng nhất chiều cao 16 thẻ sản phẩm.

## 3. Đánh giá cá nhân về quá trình Vibe Coding

**AI đã giúp tiết kiệm thời gian ở đâu?**

AI hỗ trợ tôi phác thảo cấu trúc website, tạo thẻ sản phẩm nhất quán, đề xuất CSS responsive và rà soát liên kết. Tôi vẫn cần kiểm tra kết quả thật trên trình duyệt và tự xác nhận website đã hoạt động trước khi nộp.

**Bài học rút ra khi viết prompt:**

Tôi học được cách mô tả rõ vai trò, mục tiêu, cấu trúc bắt buộc, giới hạn công nghệ và tiêu chí kiểm tra. Khi giao diện chưa đúng, prompt cần nêu chính xác lỗi nhìn thấy và kết quả mong muốn. Tôi cũng nhận ra phải phân biệt hiệu ứng CSS tự viết với thư viện AOS chính thức; không nên báo cáo tính năng chưa tích hợp hoặc chưa kiểm thử là đã hoàn thành.

## 4. Việc tôi cần tự hoàn thành trước khi nộp

- [ ] Mở `index.html` bằng Chrome/Edge và kiểm tra toàn trang.
- [ ] Kiểm tra menu desktop/mobile, năm liên kết danh mục, ảnh và hiệu ứng cuộn.
- [ ] Thử độ rộng 1440px, 1024px, 768px, 390px và 320px; kiểm tra chữ tràn và thanh cuộn ngang.
- [ ] Tạo repository công khai tên `Hieu_DinhTrung_125000193`.
- [ ] Bật GitHub Pages và kiểm tra URL live.
- [ ] Cập nhật URL thật ở README và nhật ký này.
- [ ] Nếu giảng viên yêu cầu AOS chính thức, hỏi rõ có được phép dùng runtime JavaScript của thư viện hay không.

**URL GitHub Pages: https://thebill0907.github.io/Hieu_DinhTrung_125000193/
