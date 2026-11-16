# AI Usage Log

## 1. Công cụ AI
- **Tên công cụ:** Google Gemini

## 2. Mục đích sử dụng
- Phân tích nghiệp vụ và đánh giá trải nghiệm người dùng (UX/UI) trên website thương mại điện tử.
- Đề xuất phương án cải tiến bố cục cho khu vực **Chi tiết sản phẩm** trên cả máy tính và điện thoại.
- Hỗ trợ xây dựng cấu trúc mã nguồn HTML5 ngữ nghĩa, tách tệp CSS3 riêng biệt và xử lý hiệu ứng cập nhật giá theo phiên bản.
- Hỗ trợ gỡ lỗi hiển thị trên trình duyệt, tổ chức cấu trúc thư mục dự án trên Visual Studio Code và biên tập tài liệu GitHub (`README.md`, `AI_USAGE.md`).

## 3. Prompt đã sử dụng
1. **Khảo sát giao diện và chức năng:** *"Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng cho website thương mại điện tử. Tôi đang khảo sát website: CellphoneS. Hãy giúp tôi lập bảng phân tích 5 khu vực (Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng)... Nhớ không được khẳng định những tính năng chưa được kiểm chứng."*
2. **Đề xuất phương án cải tiến:** *"Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử bằng HTML5 và CSS3. Tôi muốn cải tiến khu vực: chi tiết sản phẩm. Đối tượng sử dụng: khách hàng mua sắm trực tuyến tại Việt Nam. Hãy đề xuất bố cục giao diện, thành phần HTML, cách tổ chức CSS, hiển thị đa thiết bị và điểm cần kiểm tra."*
3. **Tạo mã nguồn giao diện:** *"Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện thương mại điện tử bằng HTML5 và CSS3 (tối thiểu 4 sản phẩm mẫu, tách file CSS riêng, không dùng backend hay thư viện ngoài)."*
4. **Cải tiến tương tác & gỡ lỗi:** *"Khi tôi chọn các options khác nhau thì giá tiền không đổi, xem lại code"* và *"Để xem bằng chế độ điện thoại trên Opera GX thì tôi phải làm sao."*

## 4. Kết quả AI đề xuất
- **Bảng phân tích UX/UI:** Chỉ ra ưu nhược điểm của CellphoneS, nổi bật là trang chi tiết sản phẩm dài khiến người dùng phải cuộn nhiều lần để đối chiếu giá và thông số kỹ thuật.
- **Giải pháp bố cục:** Thiết kế vùng chốt đơn đầu trang (Buy Box) 2 cột, bổ sung thanh điều hướng neo cố định (`Sticky Sub-navigation`), rút gọn bảng thông số kỹ thuật 6 tiêu chí trọng tâm và ghim thanh thao tác dưới đáy màn hình điện thoại.
- **Mã nguồn HTML5 & CSS3:** Cung cấp 2 tệp tách biệt (`giaodien.html` / `index.html` và `style.css`), sử dụng hình ảnh vector SVG tích hợp sẵn, bố cục Grid/Flexbox đáp ứng đa màn hình và kỹ thuật CSS `:has()` để tự động đổi giá khi chọn dung lượng (`256GB`, `512GB`, `1TB`).

## 5. Kiểm tra và điều chỉnh
- **Kiểm tra hiển thị và liên kết tệp:** Phát hiện lỗi trang trắng ban đầu do tệp HTML mới tạo chưa được lưu nội dung và đặt thiếu phần mở rộng (`.html`, `.css`) trên Visual Studio Code; đã tự đổi tên chuẩn và kiểm tra mã nguồn trang (`Ctrl + U`).
- **Kiểm tra tương tác thực tế:** Chạy thử trên trình duyệt **Opera GX**, phát hiện giá tiền chưa thay đổi khi bấm chọn dung lượng ở phiên bản đầu tiên nên đã yêu cầu bổ sung quy tắc cập nhật giá đồng bộ.
- **Kiểm thử giao diện di động (Responsive):** Sử dụng công cụ kiểm tra phần tử trên Opera GX (`Ctrl + Shift + I` → `Ctrl + Shift + M`) để kiểm tra độ co giãn của lưới sản phẩm và vị trí thanh mua hàng cố định dưới đáy màn hình.
- **Điều chỉnh cấu trúc thư mục:** Lược bỏ thư mục `images/` không cần thiết (do đã dùng SVG tích hợp) và giữ tệp HTML ngang hàng với `style.css` để tránh lỗi đường dẫn khi đưa lên GitHub.
