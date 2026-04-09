# FIT4012 - Report 1 Page
## Lab 01 - CIA & Risk: Hệ thống lưu điểm

### 1. Mục tiêu bài lab
- Nhận diện tài sản cần bảo vệ trong một hệ thống thông tin đơn giản.
- Phân biệt Confidentiality, Integrity, Availability.
- Xác định threat, vulnerability, mitigation.
- Thực hành workflow GitHub cơ bản để nhận và nộp bài.

### 2. Cách làm
- Đọc bối cảnh và xác định các thành phần quan trọng của hệ thống.
- Phân tích từng sự cố theo bộ ba CIA.
- Chọn sự cố B để phân tích sâu hơn theo threat - vulnerability - mitigation.
- Hoàn thiện bài làm trong repo và commit/push lên GitHub.

### 3. Kết quả chính
**Assets:**
- Cơ sở dữ liệu thông tin hành khách (thông tin cá nhân, lịch sử đặt chỗ).
- Cổng thanh toán và hệ thống quản lý giá vé.
- Máy chủ (Server) vận hành website và ứng dụng.

**CIA mapping:**
- Sự cố A -> Sự cố A (Thông tin hành khách bị lộ cho bên thứ ba) -> Confidentiality (Tính bí mật)
- Sự cố B -> Sự cố B (Dữ liệu giá vé bị sửa đổi trái phép) -> Integrity (Tính toàn vẹn)
- Sự cố C -> Sự cố C (Hệ thống không thể phục vụ khách hàng khi cần đặt vé) -> Availability (Tính sẵn sàng)

**Phân tích sự cố B:**
- Threat: Kẻ tấn công (hoặc người dùng có ý đồ xấu) cố ý can thiệp vào quy trình đặt vé để thay đổi giá trị thanh toán.
- Vulnerability: Ứng dụng web thiếu bước kiểm tra, xác thực dữ liệu đầu vào (Input validation) hoặc cơ chế kiểm soát logic kinh doanh, phân quyền ở phía backend (máy chủ) không chặt chẽ.
- Mitigation: Thực hiện kiểm tra tính hợp lệ của dữ liệu (Data validation) nghiêm ngặt từ phía máy chủ (Server-side); áp dụng nguyên tắc đặc quyền tối thiểu (Principle of Least Privilege) đối với các module liên quan đến tính toán giá cả và giao dịch.

### 4. Kết luận ngắn
(4-6 dòng: em học được gì từ bài lab này, phần nào khó nhất, điều gì cần chú ý khi phân tích một sự cố an toàn thông tin.)
Qua bài lab, em hiểu rõ cách áp dụng mô hình C.I.A để bảo vệ các tài sản cốt lõi của hệ thống. Khó khăn nhất là việc phân biệt chính xác giữa Mối đe dọa (Threat) và Lỗ hổng (Vulnerability) để đề xuất biện pháp khắc phục hiệu quả. Bài học rút ra khi phân tích sự cố là phải nhìn nhận toàn diện: không chỉ tập trung vào lỗi kỹ thuật mà còn phải đánh giá tác động đến tài chính và uy tín của doanh nghiệp.
