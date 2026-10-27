# Giáo án – Buổi 25: Từ ý tưởng đến thiết kế

> **Lý thuyết · 60 phút** · Chặng 4: Chế tạo robot của riêng em · Nhiệm vụ 13: Hội đồng phát minh · Tuần 13


Lý thuyết và lời giảng chi tiết: [Buoi25_Bai-Giang.md](Buoi25_Bai-Giang.md)

| Mục | Nội dung |
| --- | --- |
| Linh kiện · Nấc code | Nút bấm · Nấc 7 (lớp 4–5 thêm nấc 6) |
| Sĩ số | 12–16 em, 4 đội; 1 giáo viên + 1 trợ giảng |

## Mục tiêu

- Ôn lại toàn bộ linh kiện và nấc code đã học.
- Biết chia một việc lớn thành việc nhỏ (nấc 7).

## Chuẩn bị

- [ ] Thẻ bài 12 linh kiện
- [ ] Nút bấm mẫu
- [ ] Phiếu chia việc lớn thành món nhỏ

Hướng dẫn dựng demo: thư mục `Demo`. Phiếu học sinh: thư mục `Bai-Tap`.

## Tiến trình

| Thời gian | Hoạt động | Nội dung |
| --- | --- | --- |
| 5' | Tín hiệu từ Bít-Bô | "Căn cứ cần một robot đặc biệt. Mỗi đội tự nghĩ ra robot của mình." |
| 5' | Đoán trước, cược Xu | Các em đoán lời giải cho bí ẩn, đặt cược Xu. |
| 15' | Trò chơi không cần máy | Hoạt động 1–2 |
| 20' | Khám phá và giải thích | Hoạt động 3–5 |
| 10' | Đố nhanh, nhận Thẻ bài | Làm Phiếu bài tập (thư mục Bai-Tap). |
| 5' | Cliffhanger | Mỗi đội chọn một vai trò, mang ý tưởng về nhà vẽ thêm. |

## Mở màn

"Căn cứ cần một robot đặc biệt. Mỗi đội tự nghĩ ra robot của mình."

## Hoạt động chi tiết

1. Trò "Đố thẻ bài": thầy giơ biệt danh (Dơi, Mắt mèo, Cơ bắp...), các đội nói tên linh kiện và công dụng.
2. Gặp nhân vật Chuông cửa (nút bấm): "bấm một lần, chờ robot nghe".
3. Nấc 7 – nấu cả bữa ăn: chia việc "robot chở thuốc" thành các món nhỏ: chờ bấm nút → đi theo vạch → gặp vật thì dừng → còi báo đến nơi.
4. Lớp 4–5, nấc 6 – biến: giống bảng Xu của lớp, mỗi lần bấm nút cộng 1 điểm. Nhớ đưa điểm về 0 khi bắt đầu.
5. Giới thiệu 4 vai trò cứu hộ: chở thuốc, dọn rác, canh gác, tìm đường. Đội bàn ý tưởng.

## Chương trình mẫu

```text
(lớp 4–5) khi bắt đầu
  đặt điểm = 0
khi nút được bấm
  đổi điểm thêm 1
  hiện điểm
```

Tên khối thay theo phần mềm lập trình khối của trường.

## Bác Bug hay gặp

Chương trình quá dài (chia nhỏ); quên đưa điểm về 0.

## Kết buổi

Mỗi đội chọn một vai trò, mang ý tưởng về nhà vẽ thêm.

## Đánh giá trong buổi

- Hoàn thành nhiệm vụ: +10 Xu
- Bắt được Bác Bug (tự tìm, tự sửa): +10 Xu
- Làm thêm, sáng tạo vượt yêu cầu: +10 Xu
- Dám thử cách mới, giúp bạn mà không làm hộ, đội dọn gọn: +5 Xu
- Hỏi một câu hỏi hay: +3 Xu
