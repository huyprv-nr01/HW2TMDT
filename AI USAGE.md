# Báo cáo sử dụng AI (AI Usage Report)

## 1. Công cụ AI sử dụng
- **Tên công cụ:** Google Gemini
- **Phạm vi áp dụng:** Hỗ trợ phân tích nghiệp vụ UX/UI, đề xuất kiến trúc giao diện HTML5/CSS3, hỗ trợ gỡ lỗi hiển thị trên trình duyệt và biên tập tài liệu dự án (`README.md`, `AI_USAGE.md`).

## 2. Mục đích sử dụng AI
- Hệ thống hóa khung tiêu chí khảo sát giao diện và chức năng cho website thương mại điện tử.
- Đề xuất phương án cải tiến trải nghiệm người dùng (UX/UI) cho khu vực **Chi tiết sản phẩm** phù hợp với thói quen mua sắm trực tuyến tại Việt Nam.
- Hỗ trợ tạo mã nguồn mẫu HTML5 ngữ nghĩa và CSS3 thuần (không sử dụng thư viện ngoài hay backend) đáp ứng hiển thị đa thiết bị (Responsive).
- Hỗ trợ kiểm tra nguyên nhân lỗi liên kết tệp, đặt tên phần mở rộng (`.html`, `.css`) trên Visual Studio Code và cách kiểm thử giao diện di động trên trình duyệt Opera GX.

## 3. Quá trình tương tác và triển khai (Workflow)
1. **Giai đoạn 1 – Khảo sát giao diện và chức năng:**
   - **Yêu cầu đặt ra:** Yêu cầu AI đóng vai trò chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng để lập bảng đánh giá 5 khu vực cốt lõi (*Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng*) trên website **CellphoneS**, đảm bảo không khẳng định các tính năng chưa kiểm chứng.
   - **Kết quả thu được:** Bảng phân tích chi tiết gồm mục đích chức năng, thành phần giao diện, điểm thuận tiện, vấn đề phát sinh (trang chi tiết quá dài, người dùng phải cuộn nhiều để đối chiếu giá và thông số) và đề xuất cải tiến.
2. **Giai đoạn 2 – Đề xuất phương án thiết kế cải tiến:**
   - **Yêu cầu đặt ra:** Xác định các ý tưởng cải tiến cụ thể cho trang Chi tiết sản phẩm và phương án tổ chức HTML5/CSS3 trên cả máy tính và điện thoại.
   - **Kết quả thu được:** Đề xuất bố cục 3 tầng gồm vùng chốt đơn đầu trang (Buy Box), thanh điều hướng neo cố định (`Sticky Sub-navigation`), bảng thông số kỹ thuật tóm tắt 6 tiêu chí trọng tâm và thanh hành động cố định dưới đáy màn hình điện thoại.
3. **Giai đoạn 3 – Xây dựng mã nguồn HTML5 & CSS3:**
   - **Yêu cầu đặt ra:** Viết mã nguồn giao diện tách biệt tệp HTML và CSS, có tối thiểu 4 sản phẩm mẫu (đầy đủ hình ảnh, tên, giá, nút thao tác) và tự động cập nhật giá tiền khi người dùng chọn các phiên bản dung lượng khác nhau (`256GB`, `512GB`, `1TB`).
   - **Kết quả thu được:** Bộ mã nguồn hoàn chỉnh gồm tệp HTML5 (sử dụng hình ảnh vector SVG tích hợp sẵn) và tệp `style.css` (sử dụng CSS Grid, Flexbox, `position: sticky` và bộ chọn `:has()` để đồng bộ giá bán theo phiên bản mà không cần JavaScript).
4. **Giai đoạn 4 – Gỡ lỗi và hoàn thiện cấu trúc dự án GitHub:**
   - **Yêu cầu đặt ra:** Khắc phục tình trạng trang trắng khi mở trên trình duyệt, điều chỉnh tên tệp và tổ chức cấu trúc thư mục chuẩn để đẩy lên GitHub.
   - **Kết quả thu được:** Hướng dẫn sửa tên tệp đúng phần mở rộng (`giaodien.html` / `index.html` và `style.css`), kiểm tra mã nguồn trang (`Ctrl + U`) và chuẩn hóa các tệp tài liệu dự án.

## 4. Phân định phần AI hỗ trợ và phần sinh viên tự thực hiện
- **Phần AI hỗ trợ:**
  - Gợi ý cấu trúc bảng khảo sát UX/UI và các phương án cải tiến bố cục trang chi tiết sản phẩm.
  - Cung cấp mã nguồn khung HTML5, CSS3 và kỹ thuật xử lý đổi giá bằng bộ chọn `:has()`.
- **Phần sinh viên tự thực hiện và kiểm thử:**
  - Trực tiếp lựa chọn đối tượng khảo sát (CellphoneS), quan sát và đối chiếu các vấn đề trải nghiệm thực tế trên trang web gốc.
  - Tự thiết lập thư mục làm việc trên Visual Studio Code, quản lý tên tệp và đường dẫn liên kết giữa HTML và CSS.
  - Trực tiếp chạy kiểm thử giao diện trên trình duyệt **Opera GX** ở cả màn hình máy tính và chế độ mô phỏng điện thoại (`Ctrl + Shift + I` → `Ctrl + Shift + M`), kiểm tra hoạt động của thanh điều hướng neo, hiệu ứng đổi giá khi bấm chọn dung lượng và khả năng hiển thị của 4 sản phẩm gợi ý.
  - Rà soát, chỉnh sửa nội dung các tệp `README.md` và `AI_USAGE.md` cho phù hợp với cấu trúc thư mục thực tế trước khi công khai trên GitHub.

## 5. Cam kết
Tôi xác nhận đã trực tiếp kiểm tra, chạy thử nghiệm và hiểu rõ toàn bộ cấu trúc mã nguồn HTML5, CSS3 cũng như các giải pháp thiết kế giao diện được trình bày trong bài tập này.
