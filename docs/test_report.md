# Báo cáo kiểm thử

- Phiên bản: v1.0
- Ngày kiểm thử: 2026-10-27
- Phạm vi: trang portfolio `index.html`, mở trực tiếp bằng trình duyệt ở viewport 1049 × 645.
- Kết luận chung: trang tĩnh tải được và các ảnh giao diện hiện có đều hiển thị. Còn lỗi liên kết email, vùng liên hệ chồng lên footer, cùng các chức năng gửi form/liên kết ngoài chưa hoàn thiện.

## Kết quả theo tiêu chí

| Tiêu chí | Trạng thái | Kết quả và minh chứng |
| --- | --- | --- |
| Tính đúng đắn | Đạt một phần | Các mục nội dung và điều hướng tới `#projects` hoạt động; cả 5 ảnh trong trang tải thành công. Email hiển thị `trannin028@gmail.com` nhưng liên kết lại trỏ tới `mailto:an.nguyen@example.com`. Sáu liên kết dự án, GitHub và LinkedIn vẫn dùng `#`. Xem [ảnh toàn trang](screenshots/desktop.png) và [ảnh dự án](screenshots/projects.png). |
| UI/UX | Chưa đạt | Bố cục desktop và thẻ dự án hiển thị; tuy nhiên danh sách liên hệ chồng lên vùng footer. CSS có breakpoint cho tablet/desktop nhưng chưa xác minh trên viewport mobile vì môi trường trình duyệt không áp dụng được kích thước mobile. Xem [ảnh khu vực liên hệ](screenshots/contact.png). |
| Khả năng vận hành - xử lý lỗi | Đạt một phần | Trang mở trực tiếp từ tệp HTML, không cần bước build. Form mới chỉ có giao diện, chưa có xử lý gửi, xác thực dữ liệu hoặc trạng thái lỗi; chưa thể xác nhận luồng gửi liên hệ đầu-cuối. |
| Bảo mật | Đánh giá tĩnh, chưa kiểm thử chuyên sâu | Trong mã trang không thấy JavaScript, xử lý dữ liệu phía máy chủ hoặc script bên ngoài; do đó bề mặt xử lý dữ liệu hiện tại nhỏ. Chưa chạy công cụ quét bảo mật và chưa đánh giá HTTPS, security headers hay cấu hình máy chủ triển khai. |
| Chất lượng mã nguồn | Đạt một phần | Có cấu trúc HTML ngữ nghĩa, CSS tách riêng, alt cho ảnh, breakpoint responsive, focus-visible và hỗ trợ reduced-motion. Cần thay tiêu đề tab `ABCDEF`; các ô form chưa có label gắn với input và email dùng `type="text"`. CSS dùng float trong vùng liên hệ, góp phần gây lỗi chồng lấn đã ghi nhận. |
| Khả năng triển khai | Đạt với static hosting; chưa xác minh production | Trang và tài nguyên tương đối tải được khi mở tại máy; cấu trúc hiện tại không cần build hay dependency. Có thể triển khai trên static hosting, nhưng chưa kiểm thử URL production, HTTPS, cấu hình hosting hoặc quy trình CI/CD. |

## Minh chứng

- [Toàn trang desktop](screenshots/desktop.png)
- [Khu vực dự án](screenshots/projects.png)
- [Khu vực liên hệ và footer](screenshots/contact.png)

## Ghi chú phạm vi

Kiểm thử giao diện được thực hiện trên trình duyệt tích hợp ở desktop. Mobile, gửi form tới dịch vụ thật, quét bảo mật và triển khai production chưa được kiểm thử; các mục này không được xem là đã đạt chỉ dựa trên việc đọc mã nguồn.
