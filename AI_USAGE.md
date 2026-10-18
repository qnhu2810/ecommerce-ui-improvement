# AI Usage Log

## 1. Công cụ AI

Tên công cụ: Claude (Anthropic)  

## 2. Mục đích sử dụng

- Phân tích giao diện website Cocoon theo 5 khu vực (trang chủ, danh mục, chi tiết sản phẩm, tìm kiếm, giỏ hàng).
- Đề xuất bố cục và cấu trúc HTML/CSS cho khối giá trên thẻ sản phẩm.
- Tạo mã nguồn HTML/CSS cho trang web mẫu.
- Hỗ trợ chỉnh sửa CSS/HTML theo nhận xét của tôi và giải thích cách xem, chạy trang web.

## 3. Prompt đã sử dụng

(Tóm tắt, bạn thay bằng nội dung prompt thật của mình)  

1. Prompt 1 – Phân tích website Cocoon: mục đích, thành phần giao diện, điểm thuận tiện, vấn đề có thể phát sinh và đề xuất cải tiến cho 5 khu vực.
2. Prompt 2 – Đề xuất giao diện cải tiến khối giá (giá gốc, giá khuyến mãi, tỷ lệ giảm giá): bố cục, thẻ HTML, cách tổ chức CSS, hiển thị trên máy tính và điện thoại, các điểm cần kiểm tra.
3. Prompt 3 – Tạo mã nguồn HTML/CSS với ít nhất 4 sản phẩm, có hình, tên, giá, nút "Thêm vào giỏ" và hướng dẫn chạy.
4. Prompt 4 – Sửa mã theo nhận xét: làm khối giá gọn hơn, giữ giá khuyến mãi nổi bật, nhãn % cạnh giá, giá gốc nhỏ xám gạch ngang, giữ số tiền tiết kiệm với khoảng cách dòng nhỏ, nút thêm vào giỏ đồng đều; đổi tên thương hiệu thành Cocoon.

## 4. Kết quả AI đề xuất

- Bảng phân tích 5 khu vực của website Cocoon.
- Ý tưởng khối giá hai hàng: hàng 1 gồm giá khuyến mãi và nhãn %, hàng 2 gồm giá gốc và số tiền tiết kiệm.
- Mã HTML5 ngữ nghĩa (`<ins>`, `<del>`, `<data>`) và CSS theo quy ước BEM, dùng biến CSS, Grid, Flexbox, mobile-first.
- Bản chỉnh sửa khối giá gọn hơn: gom giá gốc và tiết kiệm vào một dòng (`.price__meta`), bỏ nền hồng và viền đỏ.

## 5. Kiểm tra và điều chỉnh

- Đối chiếu kết quả phân tích của AI với website Cocoon thực tế; giữ phần đúng, sửa phần chỉ đúng một phần và bỏ các nhận định chưa đủ căn cứ (ví dụ chưa kết luận website thiếu bộ lọc hay tìm kiếm không dấu).
- Mở trang trong trình duyệt, kiểm tra giao diện 3 cột trên máy tính và 2 cột trên điện thoại.
- Phát hiện khối giá chiếm nhiều diện tích làm thẻ giảm giá cao hơn thẻ không giảm giá, từ đó tự đề ra hướng điều chỉnh.
- Kiểm tra sau chỉnh sửa: giá khuyến mãi vẫn nổi bật, nhãn % cạnh giá, nút thêm vào giỏ thẳng hàng giữa các thẻ.
- Đổi tên thương hiệu từ "Lá Xanh" thành "Cocoon" trong tiêu đề, logo và chân trang.
- Không dùng phần AI gợi ý thêm như thanh giá cố định (sticky) ở trang chi tiết, vì bài chỉ làm trang danh sách sản phẩm. 
## 6. Phần tôi hiểu và có thể giải thích

- `display: grid` và `grid-template-columns`: chia thẻ sản phẩm thành 2 cột trên điện thoại, 3 cột từ 768px.
- `@media (min-width: 768px)` và `@media (max-width: 480px)`: đổi bố cục và cỡ chữ theo chiều rộng màn hình.
- `.product-card`: thẻ sản phẩm xếp theo chiều dọc (hình, tên, giá, nút) bằng Flexbox, các thẻ có chiều cao bằng nhau.
- `.price__current`: giá khuyến mãi chữ đậm, lớn, màu đỏ; dùng `clamp()` để cỡ chữ co giãn.
- `.price__row` và `.price__badge`: đặt giá khuyến mãi và nhãn % cùng một hàng.
- `.price__meta`, `.price__original` và thẻ `<del>`: giá gốc gạch ngang nằm cùng dòng với số tiền tiết kiệm.
- `.btn` và `margin-top: auto`: đẩy nút xuống đáy thẻ, giúp các nút thẳng hàng và đồng đều.
- `.visually-hidden`: chữ ẩn dành cho trình đọc màn hình ("Giá khuyến mãi", "Giá gốc").
- Biến CSS ở `:root`: thay đổi màu và khoảng cách tại một nơi.