# Giáo án – Buổi 18: Đưa xe tới kho báu

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 9: Bản đồ kho báu · Tuần 9


Lý thuyết và lời giảng chi tiết: [Buoi18_Bai-Giang.md](Buoi18_Bai-Giang.md)

| Mục | Nội dung |
| --- | --- |
| Linh kiện · Nấc code | Còi · Nấc 1–3 trên máy |
| Sĩ số | 12–16 em, 4 đội; 1 giáo viên + 1 trợ giảng |

## Mục tiêu

- Ghép 1–5 khối để xe đi tới đích.
- Dự đoán trước mỗi lần chạy.

## Chuẩn bị

- [ ] Mỗi đội: xe có bo mạch, còi, 1 máy tính
- [ ] Thảm ô có kho báu và vật cản
- [ ] Phiếu dự đoán

Hướng dẫn dựng demo: thư mục `Demo`. Phiếu học sinh: thư mục `Bai-Tap`.

## Tiến trình

| Thời gian | Hoạt động | Nội dung |
| --- | --- | --- |
| 10' | Nhắc lại bí ẩn, luật an toàn, chia vai | Kho báu đã đặt trên thảm. Xe của đội nào tới trước? |
| 10' | Chiến thắng nhỏ | Hoạt động 1 |
| 45' | Nhiệm vụ theo đội | Hoạt động 2–4; đổi vai bằng đồng hồ cát |
| 10' | Săn Bác Bug | Quên nối máy hoặc bấm Chạy; số quá lớn nên xe tông tường. |
| 10' | Báo cáo căn cứ | Mỗi đội kể: đã làm gì, gặp Bug nào, sửa thế nào. Làm Phiếu bài tập. |
| 5' | Dọn dẹp, tô Bản đồ Hành trình, cliffhanger | Đội bắt được Bác Bug được thưởng điểm. "Có cách nào viết ít khối hơn không?" |

## Mở màn

Kho báu đã đặt trên thảm. Xe của đội nào tới trước?

## Hoạt động chi tiết

1. Chiến thắng nhỏ: 1 khối bật đèn, 1 khối cho còi kêu.
2. Chuyển kế hoạch trên giấy thành khối trên máy. Mỗi lần bấm Chạy, ghi một dự đoán trước.
3. Xe tới kho báu thì còi kêu và đèn sáng.
4. Thử thách sao vàng: đường có 1 vật cản phải vòng qua.

## Chương trình mẫu

```text
khi bắt đầu
  tiến 2 giây
  rẽ phải 0,5 giây
  tiến 1 giây
  bật đèn
  phát tiếng bíp
```

Tên khối thay theo phần mềm lập trình khối của trường.

## Bác Bug hay gặp

Quên nối máy hoặc bấm Chạy; số quá lớn nên xe tông tường.

## Kết buổi

Đội bắt được Bác Bug được thưởng điểm. "Có cách nào viết ít khối hơn không?"

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
