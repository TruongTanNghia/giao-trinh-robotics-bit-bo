# Giáo án – Buổi 20: Xe chạy hình vuông, đèn nhạc theo vòng lặp

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 10: Phép thuật "Lặp" · Tuần 10


Lý thuyết và lời giảng chi tiết: [Buoi20_Bai-Giang.md](Buoi20_Bai-Giang.md)

| Mục | Nội dung |
| --- | --- |
| Linh kiện · Nấc code | Nấc 4: vòng lặp |
| Sĩ số | 12–16 em, 4 đội; 1 giáo viên + 1 trợ giảng |

## Mục tiêu

- Dùng khối lặp để lập trình xe và đèn.

## Chuẩn bị

- [ ] Mỗi đội: xe có bo mạch, máy tính
- [ ] Hình vuông dán sàn

Hướng dẫn dựng demo: thư mục `Demo`. Phiếu học sinh: thư mục `Bai-Tap`.

## Tiến trình

| Thời gian | Hoạt động | Nội dung |
| --- | --- | --- |
| 10' | Nhắc lại bí ẩn, luật an toàn, chia vai | Giải "Kỹ sư lười thông minh" bắt đầu! |
| 10' | Chiến thắng nhỏ | Hoạt động 1 |
| 45' | Nhiệm vụ theo đội | Hoạt động 2–4; đổi vai bằng đồng hồ cát |
| 10' | Săn Bác Bug | Lặp mãi không dừng, đặt khối ra ngoài vòng lặp. |
| 10' | Báo cáo căn cứ | Mỗi đội kể: đã làm gì, gặp Bug nào, sửa thế nào. Làm Phiếu bài tập. |
| 5' | Dọn dẹp, tô Bản đồ Hành trình, cliffhanger | Biểu diễn đèn và nhạc. Thầy hỏi: "Xe có tự biết dừng trước bức tường không?" |

## Mở màn

Giải "Kỹ sư lười thông minh" bắt đầu!

## Hoạt động chi tiết

1. Chiến thắng nhỏ: đèn nháy 5 lần bằng 1 khối lặp.
2. Xe chạy hình vuông bằng vòng lặp. Chỉnh số giây rẽ cho góc đúng.
3. Giải "Kỹ sư lười thông minh": đội có chương trình ít khối nhất mà vẫn đúng.
4. Mỗi đội soạn một điệu nhảy đèn và còi có điệp khúc.

## Chương trình mẫu

```text
khi bắt đầu
  lặp 4 lần
    tiến 1 giây
    rẽ phải 0,5 giây
  phát tiếng bíp
```

Tên khối thay theo phần mềm lập trình khối của trường.

## Bác Bug hay gặp

Lặp mãi không dừng, đặt khối ra ngoài vòng lặp.

## Kết buổi

Biểu diễn đèn và nhạc. Thầy hỏi: "Xe có tự biết dừng trước bức tường không?"

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
