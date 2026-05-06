# Report 1 page - Lab 3

## Thông tin nhóm
- Thành viên 1:Phạm Ánh Tuyết (MSSV: 1871020643)
- Thành viên 2: Dương Thị Huyền Trang (MSSV: 1871020579)

## Mục tiêu
Bài lab xây dựng hệ thống truyền dữ liệu qua socket TCP, trong đó dữ liệu được mã hóa bằng DES-CBC. Sinh viên cần hiểu luồng gửi–nhận giữa Sender và Receiver (key, IV, header, ciphertext). Đồng thời rèn luyện kiểm thử với các tình huống lỗi và phân tích rủi ro bảo mật. Qua đó nâng cao kỹ năng làm việc nhóm và trình bày kết quả.

## Phân công thực hiện
Phạm Ánh Tuyết: Phụ trách chính phần Sender.Hỗ trợ viết test cho happy path. 
Dương Thị Huyền Trang: Phụ trách chính phần Receiver.
Phụ trách tests, logs và threat model.
làm chung:Thiết kế cấu trúc gói tin (key + IV + header + ciphertext). Viết README và hoàn thiện báo cáo.

## Cách làm
Nhóm xây dựng hai chương trình Sender và Receiver giao tiếp qua socket TCP.
Sender tạo key, IV, mã hóa dữ liệu bằng DES-CBC với padding PKCS#7 rồi gửi theo thứ tự: key → IV → header → ciphertext. 
Receiver mở cổng chờ kết nối, nhận dữ liệu theo thứ tự, kiểm tra độ dài và giải mã để lấy plaintext.
Nhóm thực hiện kiểm thử với các trường hợp: chạy đúng (happy path), header sai, thiếu dữ liệu, padding lỗi và mất kết nối.

## Kết quả
Hệ thống hoạt động đúng, Receiver nhận và giải mã chính xác dữ liệu từ Sender.
Log thể hiện rõ quá trình kết nối, gửi và nhận dữ liệu thành công.
Các ca kiểm thử lỗi đều được phát hiện và xử lý, không gây treo chương trình.
Có đầy đủ log minh chứng cho cả trường hợp đúng và lỗi.

## Kết luận
Bài lab giúp hiểu rõ cách hoạt động của socket TCP và quy trình mã hóa DES-CBC.
Nhóm nhận thấy việc truyền key dạng plaintext là không an toàn trong thực tế.
Qua đó nâng cao kỹ năng kiểm thử, xử lý lỗi và phân tích rủi ro bảo mật.
