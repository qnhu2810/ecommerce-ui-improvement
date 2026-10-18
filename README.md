# E-commerce UI Improvement

Phát triển ứng dụng WEB/TMĐT

TS Nguyễn Mạnh Tuấn – tuannm@ueh.edu.vn

Sinh viên: Hà Quỳnh Như – MSSV: 31241026992

## 1. Giới thiệu

Đây là trang web mẫu thương mại điện tử mỹ phẩm, xây dựng bằng HTML5 và CSS3 để cải tiến khu vực hiển thị giá trên thẻ sản phẩm của website Cocoon. Giao diện mới làm nổi bật giá khuyến mãi, tỷ lệ giảm giá, giá gốc và số tiền tiết kiệm, đồng thời giữ thẻ sản phẩm gọn gàng và nhất quán. Trang chỉ là bản minh họa, không có backend hay chức năng thanh toán.

## 2. Website tham khảo

- Tên website: Cocoon
- URL: https://cocoonvietnam.com
- Khu vực đã khảo sát: Trang chủ, danh mục sản phẩm, chi tiết sản phẩm, tìm kiếm và giỏ hàng. Khu vực chọn cải tiến: hiển thị giá gốc, giá khuyến mãi và tỷ lệ giảm giá trên thẻ sản phẩm.

## 3. Chức năng

- Hiển thị danh sách 6 sản phẩm (5 sản phẩm giảm giá, 1 sản phẩm không giảm giá).
- Hiển thị hình ảnh, tên, giá và nút "Thêm vào giỏ" cho từng sản phẩm.
- Hiển thị giá khuyến mãi, nhãn phần trăm giảm giá, giá gốc gạch ngang và số tiền tiết kiệm.
- Bố cục hỗ trợ nhiều kích thước màn hình: 1 cột (dưới 360px), 2 cột (điện thoại), 3 cột (từ 768px).

## 4. Công nghệ

- HTML5
- CSS3 (Grid, Flexbox, biến CSS, media query)

## 5. Cách chạy

Mở file `index.html` bằng trình duyệt (Chrome, Edge hoặc Firefox). Cần giữ nguyên các thư mục `css` và `images` cùng cấp với `index.html`.

## 6. Cải tiến đã thực hiện

**Vấn đề ban đầu:** Bản giao diện đầu tiên có đủ giá bán, tỷ lệ giảm giá, giá gốc và số tiền tiết kiệm nhưng mỗi thông tin nằm ở một dòng riêng, nền hồng và viền đỏ bao quanh. Khối giá chiếm nhiều diện tích, thẻ sản phẩm giảm giá cao hơn thẻ không giảm giá.

**Thay đổi đã thực hiện:**
- Giữ giá khuyến mãi nổi bật: chữ đậm, cỡ lớn, màu đỏ.
- Đặt nhãn phần trăm giảm giá cùng hàng với giá khuyến mãi.
- Hiển thị giá gốc chữ nhỏ, màu xám, gạch ngang; đặt cùng dòng với số tiền tiết kiệm.
- Bỏ nền hồng và viền đỏ của khối giá, giảm khoảng cách giữa các dòng.
- Nút "Thêm vào giỏ" luôn nằm sát đáy thẻ, cao tối thiểu 44px, thẳng hàng và đồng đều giữa các thẻ.
- Đổi tên thương hiệu của trang mẫu thành Cocoon.

## 7. Hỗ trợ từ AI

AI (Claude) hỗ trợ phân tích website, đề xuất bố cục khối giá, viết mã HTML/CSS ban đầu và gợi ý cách chỉnh sửa. Tôi tự khảo sát website Cocoon, đối chiếu kết quả AI với website thực tế, tự quan sát giao diện, phát hiện vấn đề khối giá quá chiếm diện tích, quyết định hướng điều chỉnh, kiểm tra kết quả trên trình duyệt và đổi tên thương hiệu. Chi tiết xem trong file [AI_USAGE.md](AI_USAGE.md).