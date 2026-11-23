# Tự đánh giá — Nguyen Chi Tai · G09

## 1. Tự rà soát 4 cảnh

| Ảnh | Đối tượng | Loại lỗi | Ghi chú | Đã sửa? |
|---|---|---|---|---|
| S02_rgb | `child_seat.occupied` | schema | `occupied=yes` được coach xác nhận có trong schema mới. | Đã rà theo schema coach |
| S06_rgb | `person.seatbelt` | wrong attribute | Bản đầu bị cảnh báo `worn_incorrect`; export mới dùng `not_worn` theo hướng dẫn SVIRO. | Đã sửa |
| D02 | `frame_meta` | missing | Export đầu thiếu tag; export mới đã có `modality=ir`. | Đã sửa |
| D06 | `face.eye_left` / `face13` | flag/state | Đã rà lại trạng thái mắt và cờ điểm; export mới không còn cảnh báo validator. | Đã sửa |

## 2. Lỗi mình lặp lại nhiều nhất hôm nay

Lỗi: Bỏ sót `frame_meta` ở nhiều ảnh DMS trong export đầu.

Vì sao mình mắc: Mình chưa rà tag theo từng ảnh sau khi hoàn thành các box DMS.

Lần sau tránh bằng cách: Dùng checklist từng ảnh để xác nhận có đúng một `frame_meta`, rồi chạy kiểm tra đủ 22 ảnh trước khi nộp.

## 3. Ghi chú về review chéo

Coach đã miễn review chéo; không có disagreement log/nhận xét peer để ghi ở mục này.
