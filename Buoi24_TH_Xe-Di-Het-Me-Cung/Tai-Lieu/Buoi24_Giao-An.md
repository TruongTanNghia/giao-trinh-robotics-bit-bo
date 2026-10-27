# Giáo án – Buổi 24: Xe đi hết mê cung đen

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 12: Mê cung đen · Tuần 12


Lý thuyết và lời giảng chi tiết: [Buoi24_Bai-Giang.md](Buoi24_Bai-Giang.md)

| Mục | Nội dung |
| --- | --- |
| Linh kiện · Nấc code | Cảm biến dò line · Nấc 5 nâng cao |
| Sĩ số | 12–16 em, 4 đội; 1 giáo viên + 1 trợ giảng |

## Mục tiêu

- Lắp cảm biến dò line và lập trình xe đi hết mê cung.

## Chuẩn bị

- [ ] Mỗi đội: cảm biến dò line, xe có bo mạch, máy tính
- [ ] Mê cung đen
- [ ] Sổ đội ghi Bug
- [ ] Hộp Bí Ẩn số 3, huy hiệu Thợ Săn Bug

Hướng dẫn dựng demo: thư mục `Demo`. Phiếu học sinh: thư mục `Bai-Tap`.

## Tiến trình

| Thời gian | Hoạt động | Nội dung |
| --- | --- | --- |
| 10' | Nhắc lại bí ẩn, luật an toàn, chia vai | Con Bug to nhất đang chờ. Đội nào cứu được Bít-Bô khỏi mê cung? |
| 10' | Chiến thắng nhỏ | Hoạt động 1 |
| 45' | Nhiệm vụ theo đội | Hoạt động 2–5; đổi vai bằng đồng hồ cát |
| 10' | Săn Bác Bug | Ánh sáng đổi làm lệch kết quả; xe chạy quá nhanh vượt khỏi vạch. |
| 10' | Báo cáo căn cứ | Mỗi đội kể: đã làm gì, gặp Bug nào, sửa thế nào. Làm Phiếu bài tập. |
| 5' | Dọn dẹp, tô Bản đồ Hành trình, cliffhanger | Mở Hộp Bí Ẩn số 3, trao huy hiệu Thợ Săn Bug. |

## Mở màn

Con Bug to nhất đang chờ. Đội nào cứu được Bít-Bô khỏi mê cung?

## Hoạt động chi tiết

1. Chiến thắng nhỏ: đưa cảm biến qua vạch đen, đèn trên cảm biến đổi.
2. Đo lại cảm biến trên sàn thật trước mỗi lần chạy.
3. Chuyển luật trên thẻ thành khối Nếu – Thì trong vòng lặp. Chạy đoạn thẳng, rồi đoạn cong, rồi cả mê cung.
4. Thử và sửa nhiều lần; ghi mỗi con Bug bắt được vào sổ đội.
5. Kiểm tra cuối chặng 3: mỗi em chỉ đúng khối điều kiện trong chương trình.

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

Ánh sáng đổi làm lệch kết quả; xe chạy quá nhanh vượt khỏi vạch.

## Kết buổi

Mở Hộp Bí Ẩn số 3, trao huy hiệu Thợ Săn Bug.

## Đánh giá trong buổi

- Hoàn thành nhiệm vụ: +10 Xu
- Bắt được Bác Bug (tự tìm, tự sửa): +10 Xu
- Làm thêm, sáng tạo vượt yêu cầu: +10 Xu
- Dám thử cách mới, giúp bạn mà không làm hộ, đội dọn gọn: +5 Xu
- Hỏi một câu hỏi hay: +3 Xu

## An toàn

- Không cho linh kiện nhỏ vào miệng, mũi, tai.
- Không nối thẳng hai đầu pin.
- Không giữ bánh xe hoặc trục khi động cơ chạy.
- Thầy hoặc trợ giảng thay pin.
- Plan B không cần máy: dùng thẻ lệnh và "xe người" trên thảm ô.
