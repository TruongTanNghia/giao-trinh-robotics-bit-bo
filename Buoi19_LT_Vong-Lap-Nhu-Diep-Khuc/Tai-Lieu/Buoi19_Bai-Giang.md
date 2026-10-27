# Bài giảng – Buổi 19: Vòng lặp như điệp khúc

> **Lý thuyết · 60 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 10: Phép thuật "Lặp" · Tuần 10

Buổi này dạy nấc 4 của bậc thang lập trình: **vòng lặp**. Các em sẽ nhận ra phần lặp lại trong một chuỗi lệnh, viết gọn nó bằng "Lặp n lần", và hiểu khác biệt giữa "lặp n lần" và "lặp mãi".

## Kiến thức nền cho giáo viên

### Vòng lặp là gì

Vòng lặp là cấu trúc cho máy làm lại một nhóm lệnh nhiều lần mà không phải viết lại. Nhóm lệnh nằm bên trong vòng lặp gọi là **thân vòng lặp**.

```text
lặp 4 lần            ← vòng lặp, số 4 là số lần lặp
  tiến 1 giây        ← thân vòng lặp
  rẽ phải 0,5 giây   ← thân vòng lặp
phát tiếng bíp       ← nằm ngoài, chạy 1 lần sau khi lặp xong
```

Chương trình trên tương đương 8 lệnh viết thẳng (tiến, rẽ, tiến, rẽ, tiến, rẽ, tiến, rẽ) rồi 1 lệnh bíp.

### Hai loại vòng lặp dùng trong khóa

| Loại | Chạy bao nhiêu lần | Khi nào dùng | Ví dụ |
| --- | --- | --- | --- |
| Lặp n lần | Đúng n lần rồi đi tiếp | Biết trước số lần | Vẽ hình vuông: lặp 4 lần |
| Lặp mãi | Không bao giờ tự dừng, đến khi tắt nguồn hoặc bấm Dừng | Robot phải liên tục làm việc hoặc liên tục kiểm tra cảm biến | Đèn nháy cảnh báo; xe dò đường (tuần 11–12) |

Một số phần mềm còn có "lặp cho đến khi ...". Khóa này chưa dùng loại đó.

### Vì sao vòng lặp quan trọng

1. **Ngắn gọn:** ít khối hơn, dễ đọc hơn.
2. **Dễ sửa:** muốn đổi cạnh hình vuông dài hơn, chỉ sửa một chỗ thay vì bốn chỗ.
3. **Ít Bug:** viết lặp tay 8 lệnh dễ gõ nhầm một số. Vòng lặp tránh được điều đó.
4. **Nền tảng cho cảm biến:** robot muốn "để ý" xung quanh thì phải kiểm tra cảm biến liên tục, tức là cần "lặp mãi".

### Hình dạng và số lần lặp

Xe chạy "tiến – rẽ" lặp lại sẽ vẽ ra đa giác. Tổng các góc xe quay khi đi hết một vòng khép kín là 360 độ. Vì vậy:

| Số lần lặp | Góc mỗi lần rẽ để khép kín | Hình |
| --- | --- | --- |
| 3 | 120° | Tam giác đều |
| 4 | 90° | Hình vuông |
| 6 | 60° | Lục giác |

Với lớp 1–3, thầy chỉ cần dạy hình vuông. Bảng này dành cho câu hỏi mở rộng của lớp 4–5. Lưu ý: nếu giữ nguyên góc 90° mà đổi số lần thành 3, xe đi 3 cạnh của hình vuông, không khép kín. Đây là câu "đoán" trong bài.

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Tìm phần lặp lại

**Định nghĩa cho trẻ:** Khi một nhóm lệnh xuất hiện nhiều lần giống hệt nhau, đó là phần lặp lại.

**Ví dụ đời sống:** Đánh răng: chải trái – chải phải – chải trái – chải phải. Đi cầu thang: bước – bước – bước. Hình hoa văn trên áo: hoa – lá – hoa – lá.

**Ẩn dụ nhân vật:** Bác Bug rất thích các chương trình dài lê thê, vì càng dài càng dễ trốn.

**Lời giảng mẫu:**

> **Thầy:** "Các Kỹ sư đọc chuỗi thẻ này: tiến, rẽ, tiến, rẽ, tiến, rẽ, tiến, rẽ. Có gì lặp lại không? Đúng rồi, 'tiến, rẽ' lặp lại 4 lần. Khi thấy điều gì lặp lại, Kỹ sư thông minh sẽ dùng phép thuật Lặp."

**Câu hỏi kiểm tra:**

1. Trong "vỗ – dậm – vỗ – dậm – vỗ – dậm", phần nào lặp lại? Mấy lần? → "vỗ – dậm", 3 lần.
2. Tìm phần lặp trong "↑ → ↑ → ↑ → ↑ →". → "↑ →", 4 lần.

### Khái niệm 2: Vòng lặp như điệp khúc

**Định nghĩa cho trẻ:** Vòng lặp là cái hộp. Bỏ các lệnh vào hộp, ghi số lần, robot sẽ làm lại đủ số lần đó.

**Ví dụ đời sống:** Điệp khúc bài hát. Lời bài hát chỉ in điệp khúc một lần, ghi "hát lại 2 lần", nhưng cả lớp vẫn hát đủ.

**Ẩn dụ nhân vật:** Phép thuật "Lặp". Câu thần chú: "Lặp 4 lần!"

**Lời giảng mẫu:**

> **Thầy:** "Bài hát không in điệp khúc 3 lần. Người ta in 1 lần và ghi 'lặp lại'. Robot cũng vậy. Thầy bỏ 'tiến, rẽ' vào hộp Lặp, ghi số 4. Hai khối bên trong, nhưng robot làm đủ 8 việc. 8 lệnh thành 2 lệnh. Đó là phép thuật Lặp!"

**Câu hỏi kiểm tra:**

1. Các lệnh bên trong hộp Lặp gọi là gì? → Thân vòng lặp (phần bên trong hộp).
2. "Lặp 3 lần [vỗ tay]" thì vỗ mấy cái? → 3 cái.
3. Lệnh nằm bên dưới, ngoài hộp Lặp, chạy mấy lần? → 1 lần, sau khi lặp xong.

### Khái niệm 3: Lặp n lần và lặp mãi

**Định nghĩa cho trẻ:** "Lặp 4 lần" làm 4 lần rồi thôi. "Lặp mãi" làm hoài, không bao giờ tự dừng.

**Ví dụ đời sống:** Đèn giao thông đổi màu cả ngày, không bao giờ "xong". Đó là lặp mãi. Còn đánh răng 2 phút rồi xong, đó là lặp có số lần.

**Ẩn dụ nhân vật:** Bác Bug thích nhất là "lặp mãi" đặt nhầm chỗ: xe chạy vòng vòng không bao giờ dừng.

**Lời giảng mẫu:**

> **Thầy:** "Khi biết trước phải làm mấy lần, ta dùng 'lặp n lần'. Khi robot phải làm suốt, như đèn báo hiệu hay xe canh gác, ta dùng 'lặp mãi'. Muốn dừng 'lặp mãi' thì phải bấm Dừng hoặc tắt nguồn."

**Câu hỏi kiểm tra:**

1. Đèn giao thông dùng loại lặp nào? → Lặp mãi.
2. Vẽ hình vuông dùng loại nào? → Lặp 4 lần.
3. Lệnh đặt bên dưới "lặp mãi" có bao giờ chạy không? → Không, vì lặp mãi không bao giờ xong.

### Khái niệm 4: Đổi số lần lặp, đổi hình

**Định nghĩa cho trẻ:** Cùng một thân vòng lặp, đổi số lần thì robot đi ra hình khác.

**Ví dụ đời sống:** Đi một vòng quanh sân trường có 4 góc thì rẽ 4 lần. Nếu chỉ rẽ 3 lần, em chưa về chỗ cũ.

**Lời giảng mẫu:**

> **Thầy:** "Lặp 4 lần [tiến, rẽ góc vuông] thì về đúng chỗ cũ: hình vuông. Lặp 3 lần thì sao? Các em đoán đi rồi thầy cho một bạn đi thử."

**Câu hỏi kiểm tra:**

1. Lặp 3 lần [tiến, rẽ góc vuông] thì xe về chỗ cũ không? → Không, chỉ đi 3 cạnh của hình vuông.
2. Lặp 8 lần [tiến, rẽ góc vuông] thì sao? → Đi hình vuông 2 vòng.

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

Thầy dán 8 thẻ lệnh lên bảng thành một hàng dài: tiến, rẽ, tiến, rẽ, tiến, rẽ, tiến, rẽ.

> **Thầy:** "Bác Bug bảo: muốn vẽ hình vuông phải dùng 8 lệnh. Thầy nói: thầy chỉ cần 2 lệnh. Các em tin ai?"

### 5' – Đoán trước, cược Xu

Mỗi đội cược Xu: "Thầy làm được hay không?" Ghi kết quả lên bảng.

### 15' – Trò chơi không cần máy

1. **Robot đi hình vuông (5 phút):** Một em làm robot, đi trên hình vuông dán sàn theo 8 thẻ. Cả lớp đọc to từng thẻ. Thầy hỏi: "Phần nào lặp lại?"
2. **Điệp khúc (5 phút):** Cả lớp hát một bài quen có điệp khúc. Mỗi lần điệp khúc vang lên, cả lớp vỗ tay. Đếm điệp khúc lặp mấy lần.
3. **Nhảy theo vòng lặp (5 phút):** Thầy giơ thẻ "Lặp 3 lần [nhảy – vỗ tay]". Cả lớp làm. Đổi thành "Lặp 5 lần". Rồi "Lặp mãi" và để cả lớp làm một lúc, thầy hô "Dừng!". Hỏi: "Nếu thầy không hô Dừng thì sao?"

### 20' – Khám phá và giải thích

**8 phút: Phép thuật Lặp.** Thầy gỡ 8 thẻ, thay bằng một thẻ to "Lặp 4 lần" có ô trống bên trong, đặt 2 thẻ "tiến, rẽ" vào ô. Mời em làm robot đi lại. Robot vẫn đi đúng hình vuông. Trả Xu cho các đội cược "thầy làm được".

Giảng khái niệm thân vòng lặp: chỉ tay vào ô bên trong.

**6 phút: Đoán hình.** Thầy đổi số thành 3. Các đội vẽ dự đoán lên giấy rồi cho robot đi thử. Thầy đổi thành 8: robot đi 2 vòng.

**6 phút: Lặp n lần và lặp mãi.** Chiếu khối "lặp n lần" và khối "lặp mãi" của phần mềm. So sánh hình dạng. Kể ví dụ đèn giao thông, đèn báo cháy, quạt trần.

> **Thầy:** "Khối nằm ngoài, bên dưới hộp Lặp, chỉ chạy một lần sau khi lặp xong. Nhưng nếu là Lặp mãi, khối bên dưới sẽ chờ mãi mãi. Bác Bug rất thích trốn ở đó."

### 10' – Đố nhanh, nhận Thẻ bài

Làm Phiếu bài tập buổi 19. Đố miệng:

- "Viết gọn ↑ → ↑ → ↑ → ↑ →." → Lặp 4 lần [↑ →].
- "Lặp 2 lần [nhảy, nhảy, vỗ tay] thì nhảy mấy cái?" → 4 cái.
- "Đèn nhấp nháy cảnh báo dùng lặp gì?" → Lặp mãi.

Trao Thẻ bài "Phép thuật Lặp".

### 5' – Cliffhanger

> **Thầy:** "Buổi sau có giải 'Kỹ sư lười thông minh'. Đội nào viết chương trình ít khối nhất mà xe vẫn chạy đúng hình vuông sẽ thắng. Lười đúng cách cũng là giỏi!"

## Học sinh hay hỏi gì và trả lời thế nào

| Câu hỏi | Gợi ý trả lời |
| --- | --- |
| "Lặp mãi thì robot có mệt không?" | Robot không mệt, nhưng pin sẽ hết. Hết pin thì robot dừng. |
| "Lặp 1 lần có khác không lặp không?" | Kết quả giống nhau. Lặp 1 lần không có ích gì. |
| "Lặp 0 lần thì sao?" | Thân vòng lặp không chạy lần nào, robot bỏ qua hộp đó. |
| "Bỏ hộp Lặp vào trong hộp Lặp được không?" | Được. Đó là vòng lặp lồng nhau, mình sẽ thử ở thử thách sao vàng. |
| "Sao lặp 3 lần không ra tam giác?" | Vì góc rẽ vẫn là góc vuông. Muốn tam giác thì phải rẽ nhiều hơn mỗi lần. |
| "Muốn dừng lặp mãi thì làm sao?" | Bấm Dừng trên máy hoặc tắt nguồn. Sau này, mình sẽ cho cảm biến quyết định khi nào dừng xe. |

## Hiểu lầm thường gặp

- **"Lặp 4 lần thì chỉ lệnh đầu tiên được lặp."** Toàn bộ các khối trong thân vòng lặp đều được lặp.
- **"Khối đặt dưới vòng lặp cũng được lặp."** Chỉ khối nằm bên trong hộp mới lặp. Khối bên dưới chạy một lần sau đó.
- **"Lặp mãi sẽ tự dừng khi xe tới nơi."** Không. Lặp mãi không biết "tới nơi" là gì nếu không có cảm biến và điều kiện.
- **"Đổi số lần lặp thì hình to hơn."** Số lần lặp đổi số cạnh. Độ dài cạnh do số giây "tiến" quyết định.
- **"Vòng lặp chỉ để cho ngắn."** Ngắn là một lợi ích. Còn giúp dễ sửa và giúp robot làm việc liên tục.

## Phân hóa

### Lớp 1–3

- Chỉ dùng "Lặp n lần" với n từ 2 đến 5.
- Hoạt động chính bằng cơ thể và thẻ.
- Không cần thuật ngữ "thân vòng lặp", có thể nói "bên trong hộp".
- Chỉ dạy hình vuông.

### Lớp 4–5

- Dùng thuật ngữ "thân vòng lặp".
- Thử "Lặp mãi" và giải thích vì sao khối dưới nó không chạy.
- Câu hỏi mở rộng: tổng góc quay hết một vòng là 360°. Tam giác đều cần rẽ 120° mỗi lần, lục giác cần 60°.
- Thử thách: viết "Lặp 2 lần [Lặp 4 lần [tiến, rẽ]]" và đoán kết quả (2 vòng hình vuông).

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Vòng lặp | Hộp phép thuật làm lại nhiều lần | Cấu trúc điều khiển thực hiện lặp lại một khối lệnh |
| Thân vòng lặp | Các lệnh bên trong hộp | Tập lệnh được thực hiện ở mỗi lần lặp |
| Lặp n lần | Làm đúng n lần rồi thôi | Vòng lặp với số lần lặp xác định trước |
| Lặp mãi | Làm hoài không ngừng | Vòng lặp vô hạn, chỉ dừng khi chương trình bị dừng hoặc mất nguồn |
| Điệp khúc | Đoạn hát lại trong bài | Ẩn dụ cho phần lệnh lặp lại |
| Lặp lồng nhau | Hộp Lặp trong hộp Lặp | Vòng lặp nằm trong thân của vòng lặp khác |

## Ghi nhớ cuối bài

1. Thấy phần lặp lại thì dùng vòng lặp để viết gọn.
2. Các lệnh bên trong hộp Lặp được làm lại đủ số lần.
3. Lệnh nằm ngoài, bên dưới hộp Lặp, chỉ chạy một lần sau khi lặp xong.
4. "Lặp n lần" dùng khi biết trước số lần; "lặp mãi" dùng khi robot phải làm suốt.
5. Lặp mãi không tự dừng: phải bấm Dừng, tắt nguồn, hoặc cho cảm biến quyết định.
