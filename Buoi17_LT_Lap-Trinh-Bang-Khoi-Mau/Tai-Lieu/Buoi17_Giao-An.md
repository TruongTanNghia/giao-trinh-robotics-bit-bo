# Giáo án – Buổi 17: Lập trình bằng khối màu

> **Lý thuyết · 60 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 9: Bản đồ kho báu · Tuần 9


Lý thuyết và lời giảng chi tiết: [Buoi17_Bai-Giang.md](Buoi17_Bai-Giang.md)

| Mục | Nội dung |
| --- | --- |
| Linh kiện · Nấc code | Còi · Nấc 1–3 trên máy |
| Sĩ số | 12–16 em, 4 đội; 1 giáo viên + 1 trợ giảng |

## Mục tiêu

- Biết các phần của giao diện lập trình khối.
- Hiểu số bước và số giây trong lệnh (nấc 3).

## Chuẩn bị

- [ ] Máy chiếu, máy tính có phần mềm lập trình khối, xe mẫu có bo mạch
- [ ] Còi (buzzer) mẫu
- [ ] Giấy ô và thẻ lệnh

Hướng dẫn dựng demo: thư mục `Demo`. Phiếu học sinh: thư mục `Bai-Tap`.

## Tiến trình

| Thời gian | Hoạt động | Nội dung |
| --- | --- | --- |
| 5' | Tín hiệu từ Bít-Bô | Thầy kéo một khối "bật đèn", bấm Chạy, đèn xe sáng, cả lớp "ồ" lên. |
| 5' | Đoán trước, cược Xu | Các em đoán lời giải cho bí ẩn, đặt cược Xu. |
| 15' | Trò chơi không cần máy | Hoạt động 1–2 |
| 20' | Khám phá và giải thích | Hoạt động 3–4 |
| 10' | Đố nhanh, nhận Thẻ bài | Làm Phiếu bài tập (thư mục Bai-Tap). |
| 5' | Cliffhanger | "Kho báu đang ở trên thảm. Buổi sau xe sẽ tự đi tìm." |

## Mở màn

Thầy kéo một khối "bật đèn", bấm Chạy, đèn xe sáng, cả lớp "ồ" lên.

## Hoạt động chi tiết

1. Trên máy chiếu: kho khối, vùng ghép khối, nút Chạy, nút Dừng. Mỗi màu khối là một nhóm việc.
2. Gặp nhân vật Chú chim hót (còi), giống chuông cửa. Luật "giờ hót" 10 giây mỗi lượt.
3. Trò đếm nhịp: "tiến 3 bước" khác "tiến 3 giây". Cả lớp thử bằng cơ thể.
4. Mỗi đội vẽ đường đến kho báu trên giấy ô và viết sẵn chuỗi 1–5 lệnh.

## Chương trình mẫu

```text
khi bắt đầu
  bật đèn
  phát tiếng bíp
  chờ 1 giây
  tắt đèn
```

Tên khối thay theo phần mềm lập trình khối của trường.

## Bác Bug hay gặp

Số quá lớn nên xe đi quá xa.

## Kết buổi

"Kho báu đang ở trên thảm. Buổi sau xe sẽ tự đi tìm."

## Đánh giá trong buổi

- Hoàn thành nhiệm vụ: +10 Xu
- Bắt được Bác Bug (tự tìm, tự sửa): +10 Xu
- Làm thêm, sáng tạo vượt yêu cầu: +10 Xu
- Dám thử cách mới, giúp bạn mà không làm hộ, đội dọn gọn: +5 Xu
- Hỏi một câu hỏi hay: +3 Xu
