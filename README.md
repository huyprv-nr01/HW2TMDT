# E-commerce UI Improvement

## 1. Giới thiệu
Dự án thực hành phân tích nghiệp vụ, đánh giá trải nghiệm người dùng (UX/UI) và thiết kế lại giao diện khu vực **Chi tiết sản phẩm (Product Detail Page)** cho website thương mại điện tử bán lẻ công nghệ tại Việt Nam. Mục tiêu của bản cải tiến là giảm tình trạng quá tải thông tin, tối ưu hóa khả năng đối chiếu giá – thông số kỹ thuật và giữ nút hành động mua hàng luôn trong tầm mắt người dùng trên cả máy tính lẫn điện thoại.

## 2. Website tham khảo
- **Tên website:** CellphoneS
- **URL:** https://cellphones.com.vn
- **Khu vực đã khảo sát:** 5 khu vực chức năng cốt lõi (Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng). Trong đó, khu vực được chọn để thiết kế cải tiến giao diện là **Chi tiết sản phẩm**.

## 3. Chức năng
- Hiển thị đầy đủ thông tin sản phẩm chính: thư viện hình ảnh, đánh giá, giá bán (giá hiện tại, giá gốc gạch ngang, phần trăm giảm), khung ưu đãi và bảng thông số kỹ thuật trọng tâm.
- Cho phép chọn phiên bản dung lượng (`256GB`, `512GB`, `1TB`) và màu sắc với hiệu ứng phản hồi trực quan, đồng thời **tự động cập nhật giá tiền đồng bộ** trên toàn trang bằng CSS3 thuần.
- Tích hợp thanh điều hướng neo cố định (`Sticky Sub-navigation`) giúp chuyển nhanh giữa các phần *Tổng quan*, *Thông số kỹ thuật*, *Đánh giá* và *Sản phẩm gợi ý*.
- Hiển thị khu vực 4 sản phẩm gợi ý/mua kèm đầy đủ hình ảnh, tên sản phẩm, giá bán và nút thao tác.
- Bố cục đáp ứng (Responsive) linh hoạt trên màn hình máy tính (Desktop), máy tính bảng (Tablet) và điện thoại di động (Mobile) kèm thanh chốt đơn cố định dưới đáy màn hình điện thoại.

## 4. Công nghệ
- **HTML5:** Sử dụng các thẻ ngữ nghĩa chuẩn (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<figure>`, `<fieldset>`) và hình ảnh minh họa vector (SVG) tích hợp trực tiếp.
- **CSS3:** Tổ chức tách biệt trong tệp `style.css`, ứng dụng CSS Variables (`:root`), CSS Grid, Flexbox, `position: sticky`, bộ chọn hiện đại `:has()` để xử lý đổi giá theo biến thể và Media Queries cho giao diện đa thiết bị.

## 5. Cách chạy
1. Tải toàn bộ thư mục dự án về máy tính (đảm bảo tệp HTML và tệp `style.css` nằm cùng thư mục).
2. Mở trực tiếp tệp `giaodien.html` (hoặc `index.html`) bằng trình duyệt web bất kỳ (Chrome, Opera GX, Edge, Safari) hoặc chạy thông qua tiện ích **Live Server** trên Visual Studio Code.

## 6. Cải tiến đã thực hiện
- **Vấn đề ban đầu:** Trang chi tiết sản phẩm thực tế có chiều dài lớn do chứa nhiều khối nội dung nối tiếp nhau (ưu đãi, phụ kiện, bài viết đánh giá, thông số chi tiết, hỏi đáp), buộc người dùng phải cuộn trang lên xuống nhiều lần để đối chiếu giá bán với thông số kỹ thuật hoặc quay lại bấm nút mua hàng.
- **Thay đổi đã thực hiện:**
  1. **Tập trung hóa vùng chốt đơn đầu trang (Buy Box):** Bố cục 2 cột rõ ràng giúp người dùng nắm bắt ngay hình ảnh, giá bán, biến thể dung lượng/màu sắc, khung khuyến mãi tóm tắt và cụm nút *Mua ngay / Thêm vào giỏ* ngay trong khung nhìn đầu tiên.
  2. **Bổ sung thanh điều hướng neo cố định (Sticky Sub-navigation):** Tự động ghim ở mép trên khi cuộn trang, cung cấp liên kết chuyển nhanh tới từng mục nội dung kèm giá bán và nút *Mua ngay* thu gọn.
  3. **Rút gọn bảng thông số kỹ thuật:** Trình bày 6 thông số cốt lõi nhất đặt song song với phần mô tả để dễ đối chiếu.
  4. **Tối ưu thao tác trên điện thoại:** Chuyển bố cục sang 1 cột dọc dễ đọc và ghim thanh hành động *Thêm giỏ | Mua ngay* cố định ở cạnh dưới màn hình cho thao tác bằng ngón tay cái.

## 7. Hỗ trợ từ AI
- **Phần AI hỗ trợ:**
  - Hệ thống hóa khung tiêu chí khảo sát UX/UI cho 5 khu vực trên website thương mại điện tử và đề xuất các phương án cải tiến trang chi tiết sản phẩm.
  - Hỗ trợ xây dựng cấu trúc HTML5 ngữ nghĩa, tách tệp CSS3 chuẩn Responsive và gợi ý kỹ thuật dùng bộ chọn `:has()` để tự động cập nhật giá theo phiên bản mà không cần thư viện ngoài.
- **Phần sinh viên tự thực hiện và kiểm tra:**
  - Trực tiếp khảo sát, đối chiếu giao diện thực tế trên website CellphoneS để xác định vấn đề trải nghiệm người dùng.
  - Tổ chức thư mục dự án trên Visual Studio Code, quản lý tên tệp và đường dẫn liên kết giữa HTML và CSS.
  - Kiểm thử trực tiếp giao diện trên trình duyệt Opera GX ở cả chế độ máy tính và chế độ mô phỏng điện thoại (`DevTools`), kiểm tra hoạt động của thanh điều hướng neo, hiệu ứng đổi giá khi chọn dung lượng và khả năng hiển thị của khu vực 4 sản phẩm mẫu.
