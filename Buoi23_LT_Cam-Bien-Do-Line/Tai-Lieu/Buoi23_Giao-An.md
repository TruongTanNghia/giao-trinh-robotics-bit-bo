# Giáo án – Buổi 23: Cảm biến dò line

> **Lý thuyết · 60 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 12: Mê cung đen · Tuần 12


Lý thuyết và lời giảng chi tiết: [Buoi23_Bai-Giang.md](Buoi23_Bai-Giang.md)

| Mục | Nội dung |
| --- | --- |
| Linh kiện · Nấc code | Cảm biến dò line · Nấc 5 nâng cao |
| Sĩ số | 12–16 em, 4 đội; 1 giáo viên + 1 trợ giảng |

## Mục tiêu

- Biết cảm biến dò line phân biệt đen và trắng.
- Lập được 2 trường hợp Nếu – Thì để đi theo vạch (nấc 5 nâng cao).

## Chuẩn bị

- [ ] Mê cung băng dính đen trên sàn sáng màu
- [ ] Đèn pin, giấy đen, giấy trắng
- [ ] Ống giấy (lõi giấy vệ sinh)
- [ ] Cảm biến dò line mẫu

Hướng dẫn dựng demo: thư mục `Demo`. Phiếu học sinh: thư mục `Bai-Tap`.

## Tiến trình

| Thời gian | Hoạt động | Nội dung |
| --- | --- | --- |
| 5' | Tín hiệu từ Bít-Bô | Mê cung đen kẻ trên sàn: "Bít-Bô bị lạc, chỉ robot biết nhìn đường mới cứu được." |
| 5' | Đoán trước, cược Xu | Các em đoán lời giải cho bí ẩn, đặt cược Xu. |
| 15' | Trò chơi không cần máy | Hoạt động 1–2 |
| 20' | Khám phá và giải thích | Hoạt động 3–4 |
| 10' | Đố nhanh, nhận Thẻ bài | Làm Phiếu bài tập (thư mục Bai-Tap). |
| 5' | Cliffhanger | "Con Bug to nhất đang chờ ở cuối mê cung." |

## Mở màn

Mê cung đen kẻ trên sàn: "Bít-Bô bị lạc, chỉ robot biết nhìn đường mới cứu được."

## Hoạt động chi tiết

1. Gặp nhân vật Mắt mèo: phân biệt tối và sáng. Soi đèn pin lên giấy đen và giấy trắng để thấy ánh sáng phản lại khác nhau.
2. Trò "Người dò line": một em chỉ được nhìn xuống chân qua ống giấy, đi theo vạch đen.
3. Cả lớp rút ra luật: Nếu thấy đen thì đi thẳng, nếu thấy trắng thì rẽ về phía vạch.
4. Mỗi đội viết luật lên thẻ trước khi làm trên máy.

## Chương trình mẫu

```text
khi bắt đầu
  lặp mãi
    nếu cảm biến thấy đen thì
      tiến chậm
    không thì
      rẽ về phía vạch
```

Tên khối thay theo phần mềm lập trình khối của trường.

## Bác Bug hay gặp

Ánh sáng thay đổi làm cảm biến nhìn sai.

## Kết buổi

"Con Bug to nhất đang chờ ở cuối mê cung."

## Đánh giá trong buổi

- Hoàn thành nhiệm vụ: +10 Xu
- Bắt được Bác Bug (tự tìm, tự sửa): +10 Xu
- Làm thêm, sáng tạo vượt yêu cầu: +10 Xu
- Dám thử cách mới, giúp bạn mà không làm hộ, đội dọn gọn: +5 Xu
- Hỏi một câu hỏi hay: +3 Xu
