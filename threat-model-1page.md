# Threat Model - Lab 3

## Thông tin nhóm
- Thành viên 1: Phạm Ánh Tuyết
- Thành viên 2: Dương Thị Huyền Trang

## Assets
Plaintext (dữ liệu gốc của người dùng)
DES key
IV (Initialization Vector)
Ciphertext
Log hệ thống
Địa chỉ IP và cổng dịch vụ

## Attacker model
Kẻ tấn công có thể:
Nghe lén dữ liệu trên cùng mạng (sniffing)
Chặn và sửa đổi dữ liệu khi đang truyền (tampering)
Gửi gói tin giả hoặc dữ liệu lỗi tới Receiver
Làm gián đoạn kết nối (disconnect, DoS đơn giản)
## Threats
Lộ DES key do được gửi dưới dạng plaintext qua mạng
Ciphertext bị sửa đổi dẫn đến lỗi giải mã hoặc sai dữ liệu
Header độ dài bị giả mạo khiến Receiver đọc sai dữ liệu
Padding không hợp lệ gây lỗi khi giải mã
Kết nối bị đóng đột ngột làm chương trình treo hoặc lỗi

## Mitigations
Không truyền key dạng plaintext, sử dụng cơ chế trao đổi khóa an toàn (ví dụ: TLS)
Kiểm tra tính toàn vẹn dữ liệu (MAC hoặc hash)
Xác thực độ dài dữ liệu trước khi xử lý
Thêm kiểm tra padding hợp lệ khi giải mã
Thiết lập timeout và xử lý exception khi mất kết nối

## Residual risks
Nếu máy người dùng bị tấn công (malware), dữ liệu vẫn có thể bị lộ
Log có thể chứa thông tin nhạy cảm nếu không kiểm soát
Trong môi trường mạng nội bộ, vẫn có nguy cơ bị sniffing
