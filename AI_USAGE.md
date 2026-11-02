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

# BÁO CÁO SỬ DỤNG AI – BUỔI 2

## 1. Công cụ AI đã sử dụng

- Công cụ: ChatGPT.
- Mục đích: Hỗ trợ phân tích mã nguồn HTML/CSS hiện có, giải thích các thuộc tính CSS và đề xuất phương án cải thiện giao diện website Cocoon.
- Phạm vi sử dụng: Cấu trúc HTML5, CSS Selector, Box Model, Flexbox, CSS Grid, hiệu ứng hover/focus và kiểm tra giao diện responsive.

## 2. Các prompt đã sử dụng

### Prompt 1 – Phân tích mã nguồn hiện tại

Nhờ AI phân tích các vấn đề trong giao diện website hiện tại, tập trung vào cấu trúc trang, cách trình bày thẻ sản phẩm và menu điều hướng. Đề xuất hướng cải thiện phù hợp nhưng không viết lại toàn bộ mã nguồn.

**Kết quả sử dụng:** Xác định các vấn đề về cấu trúc HTML, khoảng cách trong thẻ sản phẩm và cách bố trí menu.

### Prompt 2 – Kiểm tra cấu trúc HTML5

Nhờ AI kiểm tra cấu trúc HTML hiện tại, đánh giá việc sử dụng các phần tử ngữ nghĩa như header, nav, main, section, article và footer; đồng thời kiểm tra thứ bậc tiêu đề, thuộc tính alt và cách tổ chức danh sách sản phẩm.

**Kết quả sử dụng:** Rà soát cấu trúc HTML và bổ sung các thuộc tính cần thiết cho hình ảnh, nút thao tác và khu vực sản phẩm.

### Prompt 3 – Tạo CSS cơ bản

Nhờ AI hướng dẫn cách liên kết tệp CSS riêng với HTML và giải thích các quy tắc CSS cơ bản như font-family, color, background-color, line-height và kích thước hình ảnh.

**Kết quả sử dụng:** Hoàn thiện việc liên kết tệp css/style.css và thiết lập các định dạng cơ bản cho website.

### Prompt 4 – Thực hành CSS Selector và Box Model

Nhờ AI giải thích cách sử dụng Element Selector, Class Selector và Descendant Selector để định dạng thẻ sản phẩm. Đồng thời, hướng dẫn áp dụng margin, padding, border, border-radius và box-sizing.

**Kết quả sử dụng:** Điều chỉnh tên sản phẩm, giá bán, nút thao tác và đường viền thẻ sản phẩm.

### Prompt 5 – Thực hành Flexbox

Nhờ AI hướng dẫn sử dụng display: flex, flex-direction, justify-content, align-items và gap để sắp xếp logo và menu điều hướng trong khu vực header.

**Kết quả sử dụng:** Căn chỉnh logo và các liên kết điều hướng theo hàng ngang, tạo khoảng cách hợp lý giữa các thành phần.

### Prompt 6 – Thực hành CSS Grid

Nhờ AI đề xuất cách sử dụng CSS Grid để bố trí danh sách sáu sản phẩm thành các cột có kích thước phù hợp. Đồng thời, giải thích sự khác nhau giữa object-fit: cover và object-fit: contain.

**Kết quả sử dụng:** Áp dụng display: grid, grid-template-columns và gap để bố trí danh sách sản phẩm. Lựa chọn object-fit: contain để hiển thị đầy đủ hình ảnh sản phẩm.

### Prompt 7 – Bổ sung hiệu ứng tương tác

Nhờ AI hướng dẫn bổ sung các hiệu ứng hover, transition và focus-visible cho nút thao tác nhằm giúp người dùng nhận biết trạng thái khi rê chuột hoặc điều hướng bằng bàn phím.

**Kết quả sử dụng:** Bổ sung hiệu ứng thay đổi màu nền, dịch chuyển nhẹ và đường viền focus cho nút hiện có.

### Prompt 8 – Kiểm tra và cải thiện giao diện responsive

Nhờ AI hỗ trợ phân tích các quy tắc CSS Grid và Media Query, xác định nguyên nhân khiến các thẻ sản phẩm bị thu hẹp trên màn hình điện thoại. Đề xuất cách điều chỉnh số cột và khoảng cách hiển thị.

**Kết quả sử dụng:** Kiểm tra lại quy tắc .product-grid và Media Query, sau đó điều chỉnh số cột để cải thiện khả năng hiển thị trên màn hình nhỏ.

### Prompt 9 – Kiểm tra README

Nhờ AI đề xuất cấu trúc README ngắn gọn, bao gồm giới thiệu bài tập, website tham khảo, khu vực cải tiến, kỹ thuật HTML5/CSS3, hướng dẫn chạy website, thay đổi đã thực hiện và công cụ AI sử dụng.

**Kết quả sử dụng:** Xây dựng nội dung README.md để giới thiệu repository và hướng dẫn sử dụng dự án.

## 3. Cách kiểm tra kết quả AI

Các đề xuất từ AI không được áp dụng một cách máy móc. Trong quá trình thực hiện, em đã:

- Đối chiếu đề xuất với cấu trúc HTML và CSS hiện có.
- Chỉnh sửa mã nguồn trong Visual Studio Code.
- Lưu tệp và kiểm tra giao diện trực tiếp trên trình duyệt.
- Sử dụng Chrome DevTools để kiểm tra các kích thước màn hình 1366px, 768px và 390px.
- Kiểm tra hiệu ứng hover bằng chuột và focus-visible bằng phím Tab.
- Tự điều chỉnh Media Query khi phát hiện bố cục sản phẩm chưa phù hợp trên màn hình nhỏ.

## 4. Đánh giá việc sử dụng AI

AI hỗ trợ giải thích cú pháp HTML5 và CSS3, đề xuất cách tổ chức giao diện và giúp xác định một số vấn đề trong quá trình chỉnh sửa mã nguồn.

Tuy nhiên, các đề xuất vẫn cần được kiểm tra và điều chỉnh dựa trên cấu trúc website thực tế. Ví dụ, em đã kiểm tra và lựa chọn object-fit: contain để hình ảnh sản phẩm không bị cắt mất nội dung; đồng thời điều chỉnh CSS Grid và Media Query để cải thiện bố cục trên màn hình điện thoại.

Qua đó, AI đóng vai trò là công cụ hỗ trợ tham khảo, còn việc lựa chọn giải pháp, chỉnh sửa mã nguồn và kiểm tra kết quả được thực hiện trực tiếp trong Visual Studio Code và trình duyệt.
