# Khai báo dùng AI — Nguyen Chi Tai

| # | Công cụ | Bạn hỏi gì (tóm tắt) | Bạn dùng kết quả thế nào | Bạn có kiểm lại không? Bằng gì? |
|---|---|---|---|---|
| 1 | ChatGPT/Codex điều khiển CVAT | Hỏi cách dùng CVAT/ý nghĩa nhãn và nhờ AI thao tác chuột gán/chỉnh một số nhãn cabin | AI đã xem ảnh trong CVAT và tạo/chỉnh một số nhãn; người học sau đó rà soát và sửa nhãn | Đã đối chiếu lại trong CVAT và chạy validator. RULES.md cấm AI xem ảnh cabin và tự gán nhãn; việc này được khai báo để coach quyết định cách xử lý |
| 2 | ChatGPT/Codex | Nhờ agent kiểm tra export sau khi coach cho phép tự đánh giá bằng agent | Chạy `cabin_check.py` trên export XML/metadata; không làm peer diff | Có; `check_final.txt` báo 0 lỗi, 0 cảnh báo trên export mới |
| 3 | ChatGPT/Codex | Nhờ hỗ trợ chuẩn bị tài liệu nộp, E4 và cập nhật schema theo thông tin coach | AI soạn/biên tập bản nháp `class_list_v0.md`, `exit_ticket.md`, `TEAM.md`, `self_review.md`; biên tập câu chữ E4 từ bốn quan sát do người học cung cấp; cập nhật `GUIDE.md`, `scripts/cabin_schema.py`, `labels_cabin_v1.json` để nhận `child_seat.occupied=yes` theo schema coach xác nhận | Người học đã rà lại các tài liệu; E4 được đối chiếu với ghi chép quan sát do người học gửi. Các phần phản ánh cá nhân được người học kiểm tra/chỉnh sửa |
