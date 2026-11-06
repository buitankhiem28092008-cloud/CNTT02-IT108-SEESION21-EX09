# Bài 9: Xây Dựng Prompt 3 Thành Phần Giải Mã Thông Báo Lỗi Trạm Sạc Cùng Trợ Lý AI
## Phần 1 thiết kế prompt 3 thành phần chuẩn hóa 
**Nguyên nhân AI trả lời sai lệch ` hiện tượng hallucination`
- [x] Thiếu ngữ cảnh cụ thể: câu hỏi cụt ngủn không nói rõ thiết bị gì, phần mềm nào, lỗi ra sao khiến AI phải tự đoán mò 
- [x] bẫy ảo giác `hallucination` vì không có thông tin thực tế, Ai tưởng tượng ra kịch bản phần cứng bị hỏng *khuyên tháo vỏ máy* để trả lời cho nó , dẫn đến lời khuyên cực kì nguy hiểm    
## PHẦN 2: LÀM SAO ĐỂ SỬA LỖI NÀY?
1. Nguyên nhân thực tế là gì?
Phần mềm trạm sạc muốn ghi lại lịch sử hoạt động vào thư mục bảo vệ của Windows (Program Files), nhưng vì bạn đang mở phần mềm bằng tài khoản thường nên bị hệ thống chặn lại (báo lỗi Access is denied).
**2. 3 bước xử lý nhanh tại hiện trường**
**Chạy phần mềm với quyền Quản trị viên**
2 phút 
*Nhấp chuột phải vào biểu tượng ứng dụng VoltCharge trên màn hình, chọn Run as administrator.
Verification: Bảng thông báo hiện ra, bấm Yes để mở quyền cao nhất*
**Cấp quyền ghi file cho thư mục dữ liệu**
3 phút 
*Vào đường dẫn C:\Program Files\VoltCharge, bấm chuột phải vào thư mục data ➔ chọn Properties ➔ vào thẻ Security ➔ bấm Edit rồi tích chọn Full control.
Verification: Các quyền đọc/ghi được tích xanh đầy đủ.*
**khởi động lại phần mền**
1 phút 
* tắt chương cũ đang lỗi và bật lại phần mềm quản lí trạm sạc 
**lưu ý quan trọng về bảo mật**
- [x] trước khi dán đoạn mã lỗi cho AI xem luôn luôn xóa hoặc che mờ các đoạn mã bí mật *như khóa API, mật khẩu* 
- [X] lý do: trách việc làm rò rỉ dữ liệu nhạy cảm của hệ thống ra ngoài lịch sử chat của AI 