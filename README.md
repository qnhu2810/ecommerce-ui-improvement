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
# BÀI TẬP CÁ NHÂN BUỔI 2 – HTML & CSS

## 1. Thông tin sinh viên

- **Họ và tên:** Hà Quỳnh Như
- **MSSV:** 31241026992
- **Môn học:** Phát triển ứng dụng WEB/TMĐT
- **Giảng viên:** TS. Nguyễn Mạnh Tuấn

## 2. Giới thiệu bài tập

Bài tập cá nhân Buổi 2 tiếp tục phát triển website từ sản phẩm đã thực hiện ở Buổi 1. Website được xây dựng dựa trên giao diện tham khảo của thương hiệu Cocoon.

Trong bài tập này, em tập trung rà soát cấu trúc HTML5, thực hành CSS Selector, Box Model, Flexbox và CSS Grid; đồng thời cải thiện giao diện sản phẩm, bổ sung hiệu ứng tương tác và kiểm tra khả năng hiển thị trên các kích thước màn hình khác nhau.

## 3. Website tham khảo và khu vực cải tiến

- **Website tham khảo:** Cocoon Việt Nam
- **Đường dẫn:** https://cocoonvietnam.com/
- **Khu vực cải tiến:** Header, menu điều hướng và danh sách sản phẩm nổi bật.

Các nội dung được cải tiến:
- Điều chỉnh kích thước hình ảnh và khoảng cách trong thẻ sản phẩm.
- Sắp xếp logo và menu bằng Flexbox.
- Bố trí danh sách sản phẩm bằng CSS Grid.
- Điều chỉnh màu sắc, đường viền và khoảng cách bằng CSS Selector và Box Model.
- Bổ sung hiệu ứng hover, transition và focus-visible.
- Điều chỉnh bố cục sản phẩm bằng Media Query để phù hợp với màn hình nhỏ.

## 4. Công nghệ và kỹ thuật đã thực hành

### HTML5
- Sử dụng các phần tử ngữ nghĩa: header, nav, main, section, article và footer.
- Tổ chức danh sách sản phẩm bằng ul và li.
- Sử dụng các thẻ h1, h2, h3 để xây dựng thứ bậc tiêu đề.
- Bổ sung thuộc tính alt cho hình ảnh.
- Sử dụng button, data, del và ins trong khu vực sản phẩm.

### CSS3
- Element Selector, Class Selector và Descendant Selector.
- Box Model: margin, padding, border, border-radius và box-sizing.
- Flexbox: display, flex-direction, justify-content, align-items và gap.
- CSS Grid: display, grid-template-columns và gap.
- Pseudo-class: hover và focus-visible.
- Transition và transform.
- Media Query để điều chỉnh giao diện theo kích thước màn hình.

## 5. Những thay đổi đã thực hiện

| Khu vực | Nội dung cải tiến |
|---|---|
| Cấu trúc HTML | Rà soát và sử dụng các phần tử HTML5 ngữ nghĩa |
| Thẻ sản phẩm | Điều chỉnh khoảng cách, đường viền và hình ảnh |
| Header | Căn chỉnh logo và menu bằng Flexbox |
| Danh sách sản phẩm | Sử dụng CSS Grid để bố trí sản phẩm |
| Nút thao tác | Bổ sung hover, transition và focus-visible |
| Giao diện responsive | Điều chỉnh số cột bằng Media Query |

## 6. Hướng dẫn chạy website

1. Tải repository về máy bằng chức năng Code → Download ZIP hoặc sử dụng Git Clone.
2. Giải nén thư mục dự án nếu tải bằng ZIP.
3. Mở Visual Studio Code.
4. Chọn File → Open Folder và mở thư mục dự án.
5. Mở tệp index.html bằng Live Preview hoặc Live Server.
6. Kiểm tra giao diện website trên trình duyệt.

## 7. Công cụ AI đã sử dụng

- **Công cụ:** ChatGPT.
- **Mục đích:** Hỗ trợ phân tích cấu trúc HTML, giải thích CSS Selector, Box Model, Flexbox, CSS Grid và đề xuất cách kiểm tra, cải thiện giao diện.
- **Cách kiểm tra:** Các đề xuất được đối chiếu với mã nguồn hiện có, điều chỉnh trong Visual Studio Code và kiểm tra trực tiếp trên trình duyệt bằng Chrome DevTools.

Chi tiết các prompt và quá trình sử dụng AI được trình bày trong tệp AI_USAGE.md.

## 8. Kiểm thử

Website được kiểm tra trên trình duyệt ở các kích thước màn hình 1366px, 768px và 390px.

Các nội dung kiểm tra gồm:
- Khả năng mở trang HTML và áp dụng CSS.
- Hiển thị hình ảnh sản phẩm.
- Bố cục danh sách sản phẩm.
- Các liên kết và nút thao tác.
- Hiệu ứng hover và focus-visible.
- Khả năng hiển thị trên màn hình nhỏ.

## 9. Repository và website

- **GitHub Repository:** https://github.com/qnhu2810/ecommerce-ui-improvement
- **Website triển khai:** file:///C:/Users/Quynh%20Nhu/Downloads/ecommerce-ui-improvement/ecommerce-ui-improvement/index.html 
