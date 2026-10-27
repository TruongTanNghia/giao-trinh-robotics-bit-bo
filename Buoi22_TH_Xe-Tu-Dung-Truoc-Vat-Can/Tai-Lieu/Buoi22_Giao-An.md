# Giáo án – Buổi 22: Xe tự dừng trước vật cản

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 11: Robot biết "nhìn thấy" · Tuần 11


Lý thuyết và lời giảng chi tiết: [Buoi22_Bai-Giang.md](Buoi22_Bai-Giang.md)

| Mục | Nội dung |
| --- | --- |
| Linh kiện · Nấc code | Cảm biến siêu âm · Nấc 5 |
| Sĩ số | 12–16 em, 4 đội; 1 giáo viên + 1 trợ giảng |

## Mục tiêu

- Đọc được khoảng cách từ cảm biến.
- Viết được lệnh Nếu – Thì cho xe dừng.

## Chuẩn bị

- [ ] Mỗi đội: cảm biến siêu âm, xe có bo mạch, máy tính
- [ ] Hộp giấy phẳng làm vật cản, thước đo

Hướng dẫn dựng demo: thư mục `Demo`. Phiếu học sinh: thư mục `Bai-Tap`.

## Tiến trình

| Thời gian | Hoạt động | Nội dung |
| --- | --- | --- |
| 10' | Nhắc lại bí ẩn, luật an toàn, chia vai | Lắp đôi tai dơi cho xe cứu hộ! |
| 10' | Chiến thắng nhỏ | Hoạt động 1 |
| 45' | Nhiệm vụ theo đội | Hoạt động 2–4; đổi vai bằng đồng hồ cát |
| 10' | Săn Bác Bug | Đo sai với vật mềm (dùng vật phẳng, đứng thẳng); điều kiện đặt ngược nên xe chỉ chạy khi gần tường. |
| 10' | Báo cáo căn cứ | Mỗi đội kể: đã làm gì, gặp Bug nào, sửa thế nào. Làm Phiếu bài tập. |
| 5' | Dọn dẹp, tô Bản đồ Hành trình, cliffhanger | Hé lộ con Bug to nhất đang trốn ở mê cung cuối. |

## Mở màn

Lắp đôi tai dơi cho xe cứu hộ!

## Hoạt động chi tiết

1. Chiến thắng nhỏ: cắm cảm biến, đưa tay lại gần, xem số trên màn hình thay đổi.
2. Đọc 3 khoảng cách gần, vừa, xa, ghi vào phiếu.
3. Viết "Nếu thấy vật ở gần hơn … thì dừng". Chọn con số bằng cách thử nhiều lần.
4. Lớp 4–5: nếu gần thì lùi lại và rẽ, không chỉ dừng.

## Chương trình mẫu

```text
khi bắt đầu
  lặp mãi
    nếu khoảng cách < 15 cm thì
      dừng
      lùi 0,5 giây      (lớp 4–5)
      rẽ trái 0,5 giây  (lớp 4–5)
    không thì
      tiến
```

Tên khối thay theo phần mềm lập trình khối của trường.

## Bác Bug hay gặp

Đo sai với vật mềm (dùng vật phẳng, đứng thẳng); điều kiện đặt ngược nên xe chỉ chạy khi gần tường.

## Kết buổi

Hé lộ con Bug to nhất đang trốn ở mê cung cuối.

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
