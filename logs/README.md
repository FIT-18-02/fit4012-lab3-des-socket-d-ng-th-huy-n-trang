# Logs minh chứng
Thư mục này lưu lại log chạy thực tế của hệ thống Sender/Receiver trong các ca kiểm thử.
Danh sách file log
- `01-happy-path-member1.txt`
Thời gian: 2026-05-06
Người thực hiện: Phạm Ánh Tuyết
Tình huống: Gửi bản tin hợp lệ
Input: "Xin chao FIT4012"
Kết quả:
Sender gửi thành công key, IV, header, ciphertext
Receiver nhận đủ dữ liệu và giải mã đúng
Output: "Xin chao FIT4012"
- `02-happy-path-member2.txt`
- `03-tamper.txt`
- `04-wrong-key.txt`
- `05-header-error.txt`

