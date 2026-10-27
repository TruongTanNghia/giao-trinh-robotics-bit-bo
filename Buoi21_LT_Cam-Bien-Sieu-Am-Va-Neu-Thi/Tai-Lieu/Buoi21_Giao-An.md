# Giáo án – Buổi 21: Cảm biến siêu âm và Nếu – Thì

> **Lý thuyết · 60 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 11: Robot biết "nhìn thấy" · Tuần 11


Lý thuyết và lời giảng chi tiết: [Buoi21_Bai-Giang.md](Buoi21_Bai-Giang.md)

| Mục | Nội dung |
| --- | --- |
| Linh kiện · Nấc code | Cảm biến siêu âm · Nấc 5 |
| Sĩ số | 12–16 em, 4 đội; 1 giáo viên + 1 trợ giảng |

## Mục tiêu

- Hiểu cảm biến cho robot biết khoảng cách.
- Hiểu câu Nếu – Thì (nấc 5).

## Chuẩn bị

- [ ] Xe mẫu đã cài chương trình tự dừng
- [ ] Khăn bịt mắt, vật cản mềm
- [ ] Cảm biến siêu âm mẫu
- [ ] Thẻ đỏ, thẻ xanh

Hướng dẫn dựng demo: thư mục `Demo`. Phiếu học sinh: thư mục `Bai-Tap`.

## Tiến trình

| Thời gian | Hoạt động | Nội dung |
| --- | --- | --- |
| 5' | Tín hiệu từ Bít-Bô | Xe tự dừng trước tường mà không ai chạm. "Phép thuật hay khoa học?" |
| 5' | Đoán trước, cược Xu | Các em đoán lời giải cho bí ẩn, đặt cược Xu. |
| 15' | Trò chơi không cần máy | Hoạt động 1–2 |
| 20' | Khám phá và giải thích | Hoạt động 3–4 |
| 10' | Đố nhanh, nhận Thẻ bài | Làm Phiếu bài tập (thư mục Bai-Tap). |
| 5' | Cliffhanger | "Xe của đội mình sắp có đôi tai dơi." |

## Mở màn

Xe tự dừng trước tường mà không ai chạm. "Phép thuật hay khoa học?"

## Hoạt động chi tiết

1. Bài mẫu: bịt mắt một bé và nhờ bé né vật cản, bé khó làm vì thiếu thông tin. Rồi báo "phía trước 5 bước có vật cản, hãy rẽ trái": bé biết đường.
2. Hỏi "Làm sao robot biết có vật cản?" Gặp nhân vật Dơi: dơi biết đường nhờ tiếng vọng. Cả lớp vỗ tay gần tường để nghe tiếng vọng.
3. Chuỗi: Cảm biến cho khoảng cách → Chương trình quyết định → Động cơ thực hiện.
4. Trò "Đèn giao thông": Nếu thầy giơ thẻ đỏ thì đứng yên, nếu thẻ xanh thì đi. Đổi ngược luật để thấy "điều kiện đặt ngược".

## Chương trình mẫu

```text
khi bắt đầu
  lặp mãi
    nếu khoảng cách < 15 cm thì
      dừng
    không thì
      tiến
```

Tên khối thay theo phần mềm lập trình khối của trường.

## Bác Bug hay gặp

Điều kiện đặt ngược.

## Kết buổi

"Xe của đội mình sắp có đôi tai dơi."

## Đánh giá trong buổi

- Hoàn thành nhiệm vụ: +10 Xu
- Bắt được Bác Bug (tự tìm, tự sửa): +10 Xu
- Làm thêm, sáng tạo vượt yêu cầu: +10 Xu
- Dám thử cách mới, giúp bạn mà không làm hộ, đội dọn gọn: +5 Xu
- Hỏi một câu hỏi hay: +3 Xu
