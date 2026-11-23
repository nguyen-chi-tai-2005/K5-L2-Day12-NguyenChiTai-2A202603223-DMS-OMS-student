# Khai báo dùng AI — Nguyen Chi Tai

| # | Công cụ | Bạn hỏi gì (tóm tắt) | Bạn dùng kết quả thế nào | Bạn có kiểm lại không? Bằng gì? |
|---|---|---|---|---|
| 1 | ChatGPT/Codex điều khiển CVAT | Hỏi cách dùng CVAT/ý nghĩa nhãn và nhờ AI thao tác chuột gán hoặc chỉnh một số nhãn | AI đã xem một số ảnh cabin trong CVAT và tạo/chỉnh nhãn | Người học đã rà và sửa nhãn. RULES.md §3 cấm AI xem ảnh cabin và tự gán nhãn; việc này được khai báo trung thực |
| 2 | ChatGPT/Codex | Nhờ kiểm tra export sau khi coach cho phép agent đánh giá | Chạy `cabin_check.py` trên export; kiểm tra cấu trúc/thuộc tính, không tạo peer diff | Có; `check_final.txt` báo 0 lỗi, 0 cảnh báo |
| 3 | ChatGPT/Codex | Nhờ soạn/biên tập tài liệu nộp, diễn đạt E4 từ quan sát do người học gửi và đồng bộ schema theo thông tin coach | Tạo/biên tập bản nháp `class_list_v0.md`, `exit_ticket.md`, `TEAM.md`, `self_review.md`, `ir_log.csv`; cập nhật hướng dẫn và validator | Người học đã rà lại/chỉnh các tài liệu; E4 dựa trên các quan sát người học cung cấp |
