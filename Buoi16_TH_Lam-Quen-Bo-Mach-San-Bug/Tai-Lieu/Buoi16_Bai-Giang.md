# Bài giảng – Buổi 16: Làm quen bo mạch, săn Bug trên giấy

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 8: Thầy-robot ngốc nghếch · Tuần 8

Mục tiêu của buổi: các Kỹ sư cắm đúng linh kiện vào bo mạch, thấy bo mạch điều khiển xe chạy theo chương trình, và tìm được lỗi trong 3 chương trình viết trên giấy. Kết buổi mở Hộp Bí Ẩn số 2.

## Ôn lý thuyết 5 phút

Thầy hỏi nhanh, cả lớp trả lời đồng thanh hoặc giơ thẻ.

| Câu hỏi | Đáp án |
| --- | --- |
| Thuật toán là gì? | Công thức các bước để làm xong một việc. |
| Ba điều của thuật toán? | Rõ ràng, đúng thứ tự, có lúc xong. |
| Bác Bug hay trốn ở đâu? | Chỗ thiếu bước, sai thứ tự, nói không rõ. |
| Bộ não của robot tên là gì? | Bo mạch điều khiển. |
| Động cơ cắm vào cửa nghe tin hay cửa gửi lệnh? | Cửa gửi lệnh (cổng ra). |
| Bo mạch có tự nghĩ ra việc không? | Không, nó làm theo chương trình. |

> **Thầy:** "Hôm nay Bộ não sẽ thức dậy. Và 3 phong bì của Bác Bug đang chờ các Kỹ sư."

## Hướng dẫn thực hành từng bước

### Trước khi bắt đầu: an toàn

- Cầm bo mạch ở hai mép, không chạm vào chân kim loại và con chip.
- Cắm và rút dây bằng cách **cầm đầu cắm, không kéo dây**.
- Tắt nguồn (tắt công tắc hộp pin) trước khi cắm hoặc rút linh kiện.
- Không để nước, bút dạ, kẹp kim loại trên bàn làm việc.
- Thầy hoặc trợ giảng thay pin.

### Bước 1 – Chiến thắng nhỏ: Bộ não thức dậy (10 phút)

**Làm gì:** Mỗi đội nhận một bo mạch đã được thầy nạp sẵn chương trình nháy đèn. Nối hộp pin, bật công tắc.

**Vì sao:** Các em thấy ngay bo mạch "sống": nó làm một việc mà không ai bấm gì cả. Đó là chương trình đang chạy.

**Đạt khi:** Đèn trên bo nháy đều. Cả đội đếm to số lần nháy trong 10 giây.

> **Thầy:** "Ai bảo đèn nháy? Không ai bấm cả. Chương trình bên trong Bộ não bảo nó nháy."

### Bước 2 – Nhìn, Sờ, Đoán, Thử, Kể với bo mạch (15 phút)

**Làm gì:**

1. **Nhìn:** tìm trên bo mạch các cổng có màu hoặc có số. Đánh dấu đâu là cổng vào, đâu là cổng ra (thầy đã dán nhãn màu: ví dụ xanh dương là cổng ra, cam là cổng vào; theo bộ kit của trường).
2. **Sờ:** cầm đầu cắm của dây đèn LED, cảm nhận chiều cắm (thường có rãnh hoặc mặt phẳng).
3. **Đoán:** "Đèn LED là giác quan hay tay chân? Vậy cắm vào cổng màu nào?"
4. **Thử:** tắt nguồn, cắm LED vào cổng ra, bật nguồn. Thầy đổi chương trình nháy để đèn ngoài cũng nháy.
5. **Kể:** mỗi em nói một câu: "Em cắm đèn vào cổng ... vì đèn là ...".

**Vì sao:** Đây là bước tập nối tay chân vào Bộ não. Cắm đúng cổng thì Bộ não mới gửi lệnh đến đúng nơi.

**Đạt khi:** Đèn LED ngoài nháy cùng nhịp với chương trình.

### Bước 3 – Gắn Bộ não lên xe cứu hộ (20 phút)

**Làm gì:**

1. Gắn bo mạch lên khung xe đã làm ở Chặng 2 bằng ốc hoặc dây rút, tránh chỗ bánh xe quay.
2. Tắt nguồn. Cắm dây động cơ vào cổng ra theo nhãn.
3. Thầy nạp chương trình "chạy 2 giây rồi dừng" cho từng xe.
4. Đặt xe trên sàn, đánh dấu vạch xuất phát. Bật nguồn và chạy.
5. Đo xem xe đi được bao xa trong 2 giây. Ghi vào phiếu.

**Vì sao:** Ở Chặng 2, xe chạy khi bật công tắc và chỉ dừng khi tắt. Bây giờ Bộ não tự đếm 2 giây rồi tự dừng. Đó là sức mạnh của chương trình.

**Đạt khi:** Xe chạy thẳng khoảng 2 giây rồi tự dừng, không cần ai chạm vào.

> **Thầy:** "Công tắc giống cái cửa: chỉ mở và đóng. Bộ não thì biết đếm giờ, biết làm theo thứ tự. Xe của các em vừa lên cấp."

### Bước 4 – Săn Bug trên giấy (25 phút)

**Làm gì:** Mở 3 phong bì của Bác Bug. Mỗi phong bì có một chương trình in bằng thẻ lệnh, kèm "điều mong muốn". Đội đọc, chạy thử bằng "xe người" trên thảm ô, khoanh chỗ sai và viết cách sửa.

| Phong bì | Điều mong muốn | Chương trình của Bác Bug | Loại Bug |
| --- | --- | --- | --- |
| 1 | Đi đến kho báu ở ô 3 rồi rẽ phải 1 ô | ↑ ↑ ↑ ↑ | Thiếu bước rẽ phải, thừa bước tiến |
| 2 | Xe chạy 2 giây rồi dừng | Dừng → Chạy 2 giây | Sai thứ tự |
| 3 | Đi đến cửa ở bên trái | ↑ ↑ → ↑ | Sai hướng: phải là ← |

**Vì sao:** Săn Bug trên giấy giúp các em tập đọc chương trình từng dòng trước khi viết trên máy.

**Đạt khi:** Đội tìm đúng chỗ sai của cả 3 phong bì và viết được bản sửa.

### Bước 5 – Báo cáo căn cứ và dọn dẹp (15 phút)

- Mỗi đội cử một em báo cáo: "Bác Bug ở phong bì số ... trốn ở bước ... Chúng em sửa bằng cách ..."
- Tắt nguồn, rút pin, cất bo mạch vào hộp chống tĩnh điện hoặc túi riêng.
- Mở Hộp Bí Ẩn số 2. Tô thêm một vùng sáng trên Bản đồ Hành trình.

## Giải thích chương trình từng khối

Chương trình mẫu thầy nạp cho xe (tên khối thay theo phần mềm của trường):

```text
khi bắt đầu
  bật động cơ tiến
  chờ 2 giây
  tắt động cơ
```

| Dòng | Ý nghĩa | Giải thích cho trẻ |
| --- | --- | --- |
| `khi bắt đầu` | Sự kiện mở đầu. Các khối bên dưới chạy khi bo mạch được bật hoặc khi bấm Chạy. | "Đây là tiếng còi xuất phát. Có nó thì mọi thứ bên dưới mới chạy." |
| `bật động cơ tiến` | Gửi lệnh qua cổng ra, cho động cơ quay theo chiều tiến. | "Bộ não bảo Cơ bắp: chạy!" |
| `chờ 2 giây` | Bo mạch đứng yên 2 giây. Động cơ vẫn đang quay vì chưa có lệnh tắt. | "Bộ não đếm một, hai. Trong lúc đếm, xe vẫn chạy." |
| `tắt động cơ` | Gửi lệnh dừng động cơ. Hết chương trình. | "Bộ não bảo Cơ bắp: dừng!" |

Điểm quan trọng: lệnh "chờ" **không** làm xe dừng. Nó chỉ làm Bộ não chờ trước khi đọc lệnh tiếp theo. Xe dừng là nhờ lệnh "tắt động cơ".

### Các biến thể của Bác Bug để so sánh

**Bug 1 – Sai thứ tự:**

```text
khi bắt đầu
  tắt động cơ
  chờ 2 giây
  bật động cơ tiến
```

Kết quả: xe đứng yên 2 giây, rồi chạy mãi không dừng (vì không còn lệnh tắt nào sau đó). Bài học: thứ tự quyết định kết quả.

**Bug 2 – Thiếu bước:**

```text
khi bắt đầu
  bật động cơ tiến
  tắt động cơ
```

Kết quả: xe gần như không nhúc nhích. Động cơ vừa bật đã bị tắt ngay, vì Bộ não đọc lệnh nhanh hơn chớp mắt. Bài học: thiếu bước "chờ" thì không có thời gian để chạy.

**Bug 3 – Thiếu sự kiện mở đầu:**

```text
bật động cơ tiến
chờ 2 giây
tắt động cơ
```

Kết quả: các khối nằm rời, không gắn dưới "khi bắt đầu", nên không chạy. Bài học: phải gắn khối vào sự kiện.

## Bảng xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
| --- | --- | --- |
| Bật nguồn mà không đèn nào sáng | Hết pin, lắp ngược pin, công tắc hộp pin chưa bật | Kiểm tra theo thứ tự: pin – công tắc – dây nguồn |
| Đèn trên bo sáng nhưng LED ngoài không sáng | Cắm LED vào cổng vào, hoặc cắm sai cổng mà chương trình điều khiển | So nhãn màu, cắm vào đúng cổng ra mà chương trình dùng |
| Động cơ không quay | Dây động cơ lỏng, cắm sai cổng, chưa nạp chương trình | Lắc nhẹ đầu cắm, đổi đúng cổng, nhờ thầy nạp lại |
| Xe chạy lùi thay vì tiến | Động cơ lắp ngược chiều hoặc cắm đảo đầu dây | Đổi chiều cắm, hoặc đổi khối "tiến" thành "lùi" trong chương trình |
| Xe chạy mãi không dừng | Chương trình thiếu lệnh tắt, hoặc lệnh tắt đặt sai chỗ | Đọc lại chương trình, đặt "tắt động cơ" ở cuối |
| Xe chạy chéo | Một bánh lỏng hoặc bo mạch đè lệch một bên | Siết bánh, gắn bo mạch vào giữa khung |
| Dây tuột khi rút | Kéo dây thay vì cầm đầu cắm | Nhắc luật "cầm đầu cắm, không kéo dây"; thay dây nếu đứt |
| Bo mạch nóng bất thường | Chập mạch do vật kim loại chạm chân bo | Tắt nguồn ngay, báo thầy, dọn vật kim loại khỏi bàn |

## Thử thách mở rộng

1. **Sao vàng 1:** Sửa chương trình để xe chạy 1 giây, dừng 1 giây, rồi chạy tiếp 1 giây. (Gợi ý: cần thêm "chờ" sau "tắt động cơ".)
2. **Sao vàng 2:** Viết trên giấy chương trình cho xe chạy tiến 2 giây rồi lùi về 2 giây. Dự đoán xe có về đúng vạch không. Thầy nạp thử.
3. **Lớp 4–5:** Đo quãng đường xe đi trong 1 giây, 2 giây, 3 giây. Có phải gấp đôi thời gian thì gấp đôi quãng đường không? Vì sao giây đầu có thể ngắn hơn? (Xe cần một chút để tăng tốc.)

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Lệnh "chờ 2 giây" làm xe dừng hay chạy tiếp? | Xe chạy tiếp, Bộ não chỉ chờ trước khi đọc lệnh sau. |
| Vì sao rút cáp máy tính rồi xe vẫn chạy được? | Bo mạch đã nhớ chương trình sau khi nạp. |
| Phong bì số 2 sai ở đâu? | Sai thứ tự: dừng trước rồi mới chạy. |
| Nếu quên khối "khi bắt đầu" thì sao? | Các khối không chạy. |
| Cách rút dây đúng? | Tắt nguồn, cầm đầu cắm, không kéo dây. |

## Ghi nhớ cuối bài

1. Bo mạch là Bộ não: làm theo chương trình đã nạp, kể cả khi rút cáp.
2. Tay chân (động cơ, đèn) cắm vào cổng ra; giác quan cắm vào cổng vào.
3. Chương trình chạy từ trên xuống, từng khối một, bắt đầu từ "khi bắt đầu".
4. "Chờ" không làm xe dừng; "tắt động cơ" mới làm xe dừng.
5. Săn Bug: đọc từng dòng, tìm dòng đầu tiên làm sai, sửa rồi thử lại.
