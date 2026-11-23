# Danh sách lớp v0 — Nguyen Chi Tai · G09

## DMS

| # | Lớp / thuộc tính | Giá trị | Để làm gì (chức năng DMS) | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | `face` + `eye_left/eye_right` | open / closed / unknown | Phát hiện buồn ngủ hoặc nhắm mắt kéo dài | Thường thấy; phản xạ kính có thể che mắt |
| 2 | `face13` | 13 mốc mặt, kèm cờ occluded/outside | Theo dõi tư thế và hình học khuôn mặt | Có thể thấy; điểm bị che cần gắn cờ, không đoán |
| 3 | `gaze_zone` | road, mirror_l/r/c, cluster, center, lap, other | Phát hiện tài xế nhìn khỏi đường | Có thể thấy qua hướng đầu/mắt; kính phản xạ làm giảm độ tin cậy |
| 4 | `glasses` | none / clear / sun / unknown | Nhận biết kính và diễn giải độ tin cậy của mắt | Gọng thường thấy; kính râm có thể trông trong suốt trên NIR |
| 5 | `hand` + `on_wheel` | yes / no / unknown | Theo dõi tay tài xế có đang chạm vô lăng | Thường thấy theo hình dạng/vị trí; có thể bị khuất |
| 6 | `phone` + `state` | held / mounted / lap | Phát hiện dùng điện thoại khi lái xe | Thường thấy theo hình dạng; không gán nếu chỉ thấy vật tối không rõ là điện thoại |

## OMS

| # | Lớp / thuộc tính | Giá trị | Để làm gì (chức năng OMS) | Nhìn thấy được trên IR? |
|---|---|---|---|---|
| 1 | `person` + `seat` | rear_left / rear_middle / rear_right | Xác định người ngồi ở ghế nào để theo dõi an toàn | Thường thấy theo hình dáng và vị trí |
| 2 | `person` + `seatbelt` | worn_correct / worn_incorrect / not_worn / unknown | Kiểm tra tình trạng thắt dây an toàn | Dây có thể thấy nếu tương phản đủ; nếu không rõ chọn unknown |
| 3 | `infant_seat` + `seat` | vị trí ghế | Nhận biết ghế dành cho trẻ nhỏ và vị trí lắp | Thường thấy theo hình dáng |
| 4 | `child_seat` + `occupied` | yes / no / unknown theo schema trong CVAT | Nhận biết ghế trẻ em và việc có người/vật trong ghế | Ghế thường thấy; tình trạng bên trong có thể khó thấy |
| 5 | `object` + `seat` | loại vật theo guideline / vị trí ghế | Nhận biết vật để quên hoặc vật cản trong cabin | Có thể thấy nếu hình dáng và tương phản đủ |
| 6 | `frame_meta` | modality, light, camera_blocked | Giúp diễn giải nguồn ảnh và điều kiện quan sát | Bản thân là metadata; không phải vật thể trong ảnh |

## 2 câu hỏi leo thang

1. Câu hỏi: Khi chỉ thấy một phần vật tối nằm trong tay nhưng không thấy cạnh, góc hay màn hình đặc trưng, có cần tạo nhãn `phone` không?
   Khung ví dụ: D01.
   Tạm gán: Không tạo `phone` nếu chưa thấy dấu hiệu hình dạng của điện thoại, theo quy tắc GUIDE §4.7.
2. Câu hỏi: Nếu hai thành phần của một ghế trẻ em bị che một phần, khi nào `occupied` là `unknown` thay vì `yes`?
   Khung ví dụ: S02_rgb.
   Tạm gán: Chỉ chọn `yes` khi thấy rõ người/vật bên trong; nếu không thể kết luận thì dùng giá trị unknown được schema CVAT cho phép và hỏi coach.

Ghi chú: Coach đã cấp schema mới cho task này, trong đó `child_seat.occupied` nhận `yes`, `no`, `unknown`. Validator và `labels_cabin_v1.json` trong bản nộp đã được cập nhật để khớp schema đó.
