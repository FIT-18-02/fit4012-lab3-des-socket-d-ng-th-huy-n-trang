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
[10:35:10] Receiver started on port 6001
[10:35:12] Sender connected
[10:35:13] User: Duong Thi Huyen Trang
[10:35:13] Input: Hello Lab 3

[10:35:13] Sending data...
[10:35:14] Receiver decrypted successfully
[10:35:14] Output: Hello Lab 3

- `03-tamper.txt`
[10:36:20] Sender sending modified ciphertext
[10:36:21] Receiver received data
[ERROR] Padding invalid during decrypt

- `04-wrong-key.txt`
[10:38:01] Receiver using wrong key
[10:38:02] Decryption failed
[ERROR] Invalid padding or corrupted data

- `05-header-error.txt`
[10:40:02] Receiver started
[10:40:05] Sender connected

[10:40:06] Sending wrong header length: 100
[10:40:06] Actual ciphertext length: 24

[10:40:07] Receiver reading data...
[ERROR] Header length mismatch
[ERROR] Expected 100 bytes but received 24 bytes

