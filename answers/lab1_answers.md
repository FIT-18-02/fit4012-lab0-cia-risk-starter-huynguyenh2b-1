# Lab 01 Answers
## CIA & Risk: Hệ thống lưu điểm

**Họ và tên:** Nguyễn Văn Huy

**MSSV:** 1871020313

**Lớp/Nhóm:** CNTT18-02

## 1. Assets
Liệt kê ít nhất 2 assets cần bảo vệ. (bán vé máy bay)

- Asset 1: Cơ sở dữ liệu thông tin hành khách (thông tin cá nhân, lịch sử đặt chỗ).
- Asset 2: Cổng thanh toán và hệ thống giá vé.
- Asset 3 (nếu có): Máy chủ (Server) vận hành website

---

## 2. Mapping CIA
Ghép từng sự cố với CIA.

- Sự cố A -> C (Confidentiality - Tính bí mật): Thông tin hành khách bị lộ cho bên thứ ba.
- Sự cố B -> I (Integrity - Tính toàn vẹn): Dữ liệu giá vé bị sửa đổi trái phép.
- Sự cố C -> A (Availability - Tính sẵn sàng): Hệ thống không thể phục vụ khách hàng khi họ cần đặt vé.

---

## 3. Phân tích sự cố B
- Threat: Kẻ tấn công (hoặc khách hàng có ý đồ xấu) cố ý can thiệp vào quy trình đặt vé để thay đổi giá.
- Vulnerability: Ứng dụng web thiếu bước kiểm tra, xác thực dữ liệu đầu vào (Input validation) hoặc phân quyền không chặt chẽ ở phía backend.
- Mitigation: Thực hiện kiểm tra tính hợp lệ của dữ liệu (Data validation) nghiêm ngặt từ phía máy chủ (Server-side); áp dụng nguyên tắc đặc quyền tối thiểu (Principle of Least Privilege) cho các tác vụ liên quan đến giá cả.

---

## 4. Reflection
Viết 5-7 dòng.
Qua việc phân tích các sự cố trên hệ thống bán vé máy bay, có thể thấy việc đảm bảo an toàn thông tin không chỉ là vấn đề kỹ thuật mà còn ảnh hưởng trực tiếp đến doanh thu và uy tín của doanh nghiệp. Nếu không bảo vệ tốt tính bí mật (C), khách hàng sẽ mất niềm tin khi lộ dữ liệu. Việc mất tính toàn vẹn (I) gây thiệt hại trực tiếp về tài chính, trong khi mất tính sẵn sàng (A) làm gián đoạn dịch vụ. Do đó, việc xác định rõ tài sản (Asset) và các điểm yếu (Vulnerability) để có biện pháp phòng ngừa (Mitigation) kịp thời là vô cùng cấp thiết.



---

## 5. Bonus Flag
`FIT4012{A-?-B-?-C-?}`

Flag của em: FIT4012{A-C-B-I-C-A}

