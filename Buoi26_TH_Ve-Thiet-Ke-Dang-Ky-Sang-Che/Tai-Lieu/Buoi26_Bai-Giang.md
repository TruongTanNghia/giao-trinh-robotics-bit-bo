# Bài giảng – Buổi 26: Vẽ thiết kế, đăng ký bằng sáng chế

> **Thực hành · 90 phút** · Chặng 4: Chế tạo robot của riêng em · Nhiệm vụ 13: Hội đồng phát minh · Tuần 13

Hôm nay Hội đồng phát minh khai mạc. Mỗi đội biến ý tưởng ở buổi 25 thành một **bản thiết kế** có thể làm được, rồi lắp và thử **món nhỏ đầu tiên**. Cuối buổi, thầy đóng dấu "Đã cấp bằng sáng chế" lên phiếu của từng đội.

Bài thực hành này dạy một điều quan trọng của nghề kỹ sư: **vẽ trước, làm sau**. Bản thiết kế giúp cả đội hiểu giống nhau, chia việc rõ ràng, và biết khi nào robot "đạt".

## Ôn lý thuyết 5 phút

Thầy hỏi nhanh, đội nào trả lời đúng nhận 3 Xu.

| Câu hỏi | Đáp án |
| --- | --- |
| Ba phần của mọi robot là gì? | Giác quan – Bộ não – Tay chân (cảm biến – bo mạch – cơ cấu chấp hành) |
| Nút bấm có mấy trạng thái? | Hai: đang bấm và không bấm |
| Luật khi dùng nút bấm là gì? | Bấm một lần, chờ robot nghe |
| Vì sao chia việc lớn thành món nhỏ? | Để làm và thử từng phần; khi lỗi biết ngay lỗi ở đâu |
| Món "gặp vật thì dừng" dùng nhân vật nào? | Dơi (cảm biến siêu âm) |
| (Lớp 4–5) Đầu chương trình phải làm gì với biến điểm? | Đặt điểm bằng 0 |

## Hướng dẫn thực hành từng bước

Nhắc an toàn trước khi phát kit: không cho linh kiện nhỏ vào miệng; không nối thẳng hai đầu pin; không giữ bánh hoặc trục khi động cơ chạy; thầy hoặc trợ giảng thay pin.

### Bước 1 – Chiến thắng nhỏ: bấm nút cho còi kêu (10 phút)

**Làm gì:** Cắm nút bấm và còi vào bo mạch theo đúng cổng màu. Ghép chương trình ba khối:

```text
khi nút được bấm
  phát tiếng bíp
  tiến 1 giây
```

**Vì sao:** Trước khi làm robot lớn, đội cần chắc rằng linh kiện mới chạy được. Đây cũng là món nhỏ đầu tiên của hầu hết vai trò cứu hộ.

**Đạt khi:** Bấm nút một lần, còi kêu một tiếng và xe tiến khoảng 1 giây rồi dừng. Bấm lại, xe làm lại đúng như vậy.

### Bước 2 – Điền Phiếu bằng sáng chế (20 phút)

**Làm gì:** Mỗi đội nhận phiếu khổ A3 và điền 6 ô:

| Ô | Nội dung cần ghi | Gợi ý cho thầy hỏi |
| --- | --- | --- |
| 1. Tên robot | Tên do đội đặt | "Tên này nói lên robot làm gì không?" |
| 2. Vai trò | Chở thuốc, dọn rác, canh gác, tìm đường hoặc vai trò khác | "Robot giúp ai ở Căn cứ?" |
| 3. Bản vẽ | Robot nhìn từ trên xuống, đánh dấu vị trí từng linh kiện | "Dơi đặt ở đâu để nhìn thấy đường?" |
| 4. Linh kiện | Liệt kê giác quan, bộ não, tay chân | "Thiếu phần nào không?" |
| 5. Món nhỏ | 3–5 món theo thứ tự | "Món nào làm trước?" |
| 6. Đạt khi nào | 1–2 câu đo được | "Làm sao biết robot làm đúng?" |

**Vì sao:** Ô 6 là **yêu cầu** của robot. Kỹ sư thật luôn viết rõ "thế nào là đạt" trước khi làm. Ví dụ tốt: "Robot dừng trước hộp mà không chạm hộp." Ví dụ chưa tốt: "Robot chạy hay."

**Ràng buộc** (điều kiện bắt buộc phải tuân theo) thầy đọc cho cả lớp:

- Chỉ dùng linh kiện trong bộ kit của đội.
- Robot phải vừa trong một ô thảm (hoặc khổ giấy A4).
- Làm xong trong 3 buổi tới.

**Đạt khi:** Phiếu đủ 6 ô, bản vẽ có đánh dấu vị trí cảm biến, ô "đạt khi nào" đo được.

### Bước 3 – Chia vai trong đội (5 phút)

**Làm gì:** Mỗi đội chia ba vai, đổi vai mỗi khi đồng hồ cát chảy hết (khoảng 10 phút):

- **Kỹ sư cơ khí:** lắp khung, gắn cảm biến, kiểm tra "lắc nhẹ".
- **Kỹ sư lập trình:** ghép khối trên máy, bấm Chạy.
- **Thư ký ghi Bug:** ghi lại mỗi lần chạy: dự đoán, kết quả, Bug gặp được.

Đội 4 em thêm vai **Người thử**: đặt vật cản, đo khoảng cách, đếm giờ.

**Vì sao:** Đổi vai giúp em nào cũng được làm mọi việc và giảm tranh giành điều khiển.

### Bước 4 – Lắp và thử món nhỏ đầu tiên (35 phút)

**Làm gì:**

1. Chọn món nhỏ số 1 trên phiếu.
2. Lắp phần cứng cho món đó (ví dụ gắn Dơi phía trước xe).
3. Ghép chương trình chỉ cho món đó.
4. Thư ký ghi dự đoán trước khi bấm Chạy.
5. Chạy, so sánh với dự đoán, sửa, chạy lại.
6. Khi món 1 đạt, đánh dấu ✓ trên phiếu. Còn thời gian thì sang món 2.

**Vì sao:** Đây là bài học "thử từng món". Một món chạy thật tốt có giá trị hơn năm món chạy nửa vời.

**Đạt khi:** Ít nhất món 1 đạt 3 lần chạy liên tiếp.

### Bước 5 – Lớp 4–5: biến đếm số lần bấm (lồng trong bước 4)

Đội nào xong món 1 sớm thử chương trình đếm:

```text
khi bắt đầu
  đặt số_lần = 0
  hiện số_lần
khi nút được bấm
  đổi số_lần thêm 1
  hiện số_lần
  chờ 0,3 giây
```

**Đạt khi:** Bấm 5 lần, màn hình hiện đúng 5. Tắt rồi bật lại, màn hình về 0.

### Bước 6 – Báo cáo và đóng dấu (10 phút)

Mỗi đội đọc tên robot, vai trò và ô "đạt khi nào". Thầy hỏi một câu, rồi đóng dấu "Đã cấp bằng sáng chế".

Còn lại 5 phút: dọn dẹp, tô Bản đồ Hành trình.

## Giải thích chương trình từng khối

### Chương trình chiến thắng nhỏ

| Khối | Robot hiểu là | Nếu thiếu khối này |
| --- | --- | --- |
| khi nút được bấm | Đứng chờ đến khi Chuông cửa reo | Chương trình không có điểm bắt đầu, không bao giờ chạy |
| phát tiếng bíp | Báo cho mọi người biết "tôi nghe rồi" | Robot vẫn chạy nhưng không ai biết nó đã nhận lệnh |
| tiến 1 giây | Bật động cơ tiến trong 1 giây rồi dừng | Robot kêu nhưng đứng yên |

Hỏi các em: "Đổi 1 giây thành 3 giây thì sao?" → Xe đi xa hơn gấp khoảng 3 lần. "Đặt khối tiến lên trước khối bíp thì sao?" → Xe đi trước rồi mới kêu: thứ tự thay đổi thì hành động thay đổi.

### Chương trình đếm (lớp 4–5)

| Khối | Ý nghĩa |
| --- | --- |
| đặt số_lần = 0 | Đổ hộp về 0 mỗi lần bắt đầu |
| hiện số_lần | Cho mọi người xem số trong hộp |
| đổi số_lần thêm 1 | Bỏ thêm 1 viên bi vào hộp |
| chờ 0,3 giây | Cho nút hết "nấc cụt" trước khi nghe lần bấm tiếp |

Tên khối thật thay theo phần mềm lập trình khối của trường.

## Bảng xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
| --- | --- | --- |
| Bấm nút không có gì xảy ra | Nút cắm sai cổng hoặc cắm lỏng | Cầm đầu cắm, rút ra, cắm lại đúng cổng màu |
| Bấm nút không có gì xảy ra | Chưa nạp chương trình hoặc chưa bấm Chạy | Kiểm tra máy đã nối, bấm Chạy hoặc nạp lại |
| Còi kêu nhưng xe không chạy | Động cơ chưa cắm hoặc pin yếu | Kiểm tra dây động cơ; nhờ thầy thay pin |
| Bấm một lần, xe chạy hai ba lần | Nút bị "nấc cụt" (dội phím) hoặc bấm giữ quá lâu | Thêm khối chờ ngắn; bấm dứt khoát rồi nhả |
| Số đếm không về 0 khi chạy lại | Thiếu khối "đặt = 0" ở đầu | Thêm "đặt số_lần = 0" dưới "khi bắt đầu" |
| Số đếm nhảy 2–3 mỗi lần bấm | Dội phím | Thêm khối chờ 0,3 giây sau khi cộng |
| Xe chạy lệch sang một bên | Bánh lỏng hoặc khung lệch | Lắc nhẹ kiểm tra bánh; siết lại |
| Bản vẽ và robot thật khác nhau | Đội đổi ý khi lắp mà không ghi lại | Sửa bản vẽ bằng bút màu khác; đây là cải tiến, không phải lỗi |

## Thử thách mở rộng

- **Sao vàng 1:** Bấm nút một lần thì xe tiến, bấm lần nữa thì xe dừng. (Gợi ý: cần nhớ xe đang chạy hay đang dừng.)
- **Sao vàng 2:** Thêm đèn LED nháy 3 lần khi bắt đầu, báo robot đã sẵn sàng.
- **Sao vàng 3 (lớp 4–5):** Đếm đủ 5 lần bấm thì còi kêu dài báo "đầy".
- **Sáng tạo:** Trang trí robot theo vai trò (hộp thuốc, xô rác, mũ bảo vệ…).

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Robot của đội tên gì, làm vai trò gì? | Tên và vai trò trên phiếu |
| Món nhỏ đầu tiên là gì, đã đạt chưa? | Ví dụ: "Chờ bấm nút rồi còi kêu – đã đạt 3 lần" |
| Robot "đạt" khi nào? | Một câu đo được, ví dụ "dừng trước hộp mà không chạm" |
| Hôm nay đội bắt được Bác Bug nào? | Ví dụ: cắm sai cổng, quên bấm Chạy, nút nấc cụt |
| (Lớp 4–5) Vì sao phải đặt biến về 0? | Để không còn số của lần chạy trước |
| Món tiếp theo đội sẽ làm là gì? | Món 2 trên phiếu |

## Ghi nhớ cuối bài

1. Kỹ sư vẽ thiết kế trước, rồi mới lắp.
2. Bản thiết kế phải ghi rõ "robot đạt khi nào".
3. Làm và thử từng món nhỏ; món này đạt mới sang món kia.
4. Bấm một lần, chờ robot nghe.
5. Đổi vai đúng lượt để ai cũng được làm.
6. Robot thay đổi so với bản vẽ là chuyện bình thường; nhớ ghi lại thay đổi.
