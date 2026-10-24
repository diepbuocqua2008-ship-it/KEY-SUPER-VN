KEYVN website starter
=====================
Mở index.html bằng trình duyệt để xem bản demo.

Có sẵn:
- Giao diện responsive lấy cảm hứng từ ảnh tham khảo
- Danh sách sản phẩm mẫu, tìm kiếm, sắp xếp
- Giỏ hàng, tăng/giảm số lượng
- Màn hình thanh toán demo

Chưa có:
- Backend/database, tài khoản thật, quản trị
- Cổng thanh toán thật, webhook xác minh giao dịch
- Giao key tự động và email gửi key

Để triển khai thanh toán tự động:
1. Chọn nhà cung cấp thanh toán phù hợp tại Việt Nam (ví dụ VietQR qua nhà cung cấp hỗ trợ webhook, hoặc cổng thanh toán như VNPay/MoMo theo điều kiện tài khoản).
2. Backend tạo đơn và mã tham chiếu duy nhất; không tạo giao dịch từ HTML thuần.
3. Xác minh chữ ký/webhook phía máy chủ trước khi đánh dấu đã thanh toán.
4. Chỉ sau khi xác minh thành công mới trừ kho và giao key; xử lý giao dịch lặp để tránh giao key nhiều lần.
5. Lưu secret API ở biến môi trường phía server, tuyệt đối không nhúng vào HTML/JS frontend.

Sản phẩm và ảnh trong file là dữ liệu minh họa; thay bằng sản phẩm/ảnh bạn có quyền sử dụng.
