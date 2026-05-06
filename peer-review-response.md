# Peer Review Response

## Thông tin nhóm
- Thành viên 1: Phạm Ánh Tuyết
- Thành viên 2: Dương Thị Huyền Trang

## Thành viên 1 góp ý cho thành viên 2
Receiver xử lý đúng luồng dữ liệu nhưng phần kiểm tra lỗi ban đầu còn chưa đầy đủ (chưa xử lý tốt khi thiếu ciphertext).
Log rõ ràng, dễ theo dõi, tuy nhiên nên bổ sung thông báo cụ thể hơn cho từng loại lỗi (header sai, padding sai).
Phần test cần thêm case kiểm tra mất kết nối đột ngột.

## Thành viên 2 góp ý cho thành viên 1
Sender hoạt động đúng và mã hóa chính xác, tuy nhiên phần hiển thị log còn hơi ít thông tin. Cần bổ sung log chi tiết hơn về key, IV và độ dài ciphertext để dễ debug. Code rõ ràng nhưng có thể thêm chú thích để dễ hiểu hơn.

## Nhóm đã sửa gì sau góp ý
Nhóm đã bổ sung kiểm tra lỗi khi nhận thiếu dữ liệu và xử lý trường hợp kết nối bị ngắt.Thêm log chi tiết cho từng bước gửi và nhận dữ liệu, bao gồm header và trạng thái lỗi. Bổ sung thêm test case cho các trường hợp padding sai và mất kết nối. Cập nhật lại code với chú thích rõ ràng hơn để dễ đọc và bảo trì.
