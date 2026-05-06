# Logs minh chứng
Thư mục này lưu lại log chạy thực tế của hệ thống Sender/Receiver trong các ca kiểm thử.
Danh sách file log
- `01-happy-path-member1.txt`
[10:30:12] Receiver started on port 6001
[10:30:15] Sender connected to 127.0.0.1:6001
[10:30:16] User: Pham Anh Tuyet
[10:30:16] Input: Xin chao FIT4012

[10:30:16] Generated Key: b'12345678'
[10:30:16] Generated IV: b'abcdefgh'
[10:30:16] Sending header length: 24
[10:30:16] Ciphertext sent

[10:30:17] Receiver received data
[10:30:17] Decrypting...
[10:30:17] Output: Xin chao FIT4012
- `02-happy-path-member2.txt`
- `03-tamper.txt`
- `04-wrong-key.txt`
- `05-header-error.txt`
[10:40:02] Receiver started
[10:40:05] Sender connected

[10:40:06] Sending wrong header length: 100
[10:40:06] Actual ciphertext length: 24

[10:40:07] Receiver reading data...
[ERROR] Header length mismatch
[ERROR] Expected 100 bytes but received 24 bytes

