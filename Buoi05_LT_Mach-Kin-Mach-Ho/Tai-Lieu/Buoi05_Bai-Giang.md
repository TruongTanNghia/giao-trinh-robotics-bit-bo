# Bài giảng – Buổi 5: Mạch kín và mạch hở

> **Lý thuyết · 60 phút** · Chặng 1: Đánh thức Bít-Bô · Nhiệm vụ 3: Bí ẩn bóng đèn không sáng · Tuần 3

Đây là buổi lý thuyết điện quan trọng nhất của khóa học. Các em hiểu vì sao đèn sáng, vì sao đèn không sáng, và biết ba luật an toàn với pin. Hai nhân vật mới xuất hiện: **Pin** (Bình sữa năng lượng) và **đèn LED** (Đom đóm). Mọi bài về động cơ, bo mạch, cảm biến sau này đều dựa trên ý tưởng mạch kín của buổi hôm nay.

---

## Kiến thức nền cho giáo viên

### 1. Pin là gì

- Pin là nguồn điện, tạo ra **hiệu điện thế** (điện áp) giữa hai cực nhờ phản ứng hóa học bên trong.
- Một viên pin AA hoặc AAA kiềm (alkaline) mới có điện áp danh định **1,5 V**. Pin sạc NiMH cùng cỡ có điện áp khoảng **1,2 V**.
- Hộp pin 2 viên mắc **nối tiếp** cho khoảng **3 V**; hộp 4 viên cho khoảng **6 V**. Nối tiếp nghĩa là cực dương viên này nối cực âm viên kia, điện áp cộng lại.
- **Cực dương (+)**: đầu có núm lồi trên pin AA. **Cực âm (−)**: đầu phẳng. Trên hộp pin, cực âm thường là lò xo, cực dương là miếng kim loại phẳng. Dây ra từ hộp pin theo quy ước: **đỏ là dương, đen là âm**.
- Khi pin dùng dần, điện áp giảm, đèn sáng yếu đi, động cơ quay chậm lại. Đây là "robot đói".

### 2. Dòng điện và mạch điện

- Dòng điện chỉ chạy trong **mạch kín**: từ cực dương của nguồn, qua dây dẫn và thiết bị tiêu thụ điện (đèn, động cơ), về cực âm.
- Theo quy ước, chiều dòng điện đi từ **+ sang −** bên ngoài nguồn. (Thực tế electron trong dây kim loại chuyển động theo chiều ngược lại. Thầy không cần nói điều này với học sinh tiểu học, nhưng nên biết nếu học sinh lớp 5 đọc sách và hỏi.)
- **Mạch hở**: có chỗ đứt (dây tuột, dây đứt trong vỏ, công tắc tắt). Không có dòng điện ở **bất kỳ đâu** trong mạch đơn đó.

### 3. Đèn LED

- LED là viết tắt của *Light Emitting Diode*: điốt phát quang. **Điốt** là linh kiện chỉ cho dòng điện đi theo **một chiều**.
- Vì vậy LED **chỉ sáng khi lắp đúng chiều**. Lắp ngược, LED không sáng, nhưng thường không hỏng nếu điện áp thấp như pin 3 V.
- Nhận biết chân LED rời:
  - **Chân dài** là **cực dương** (anode, A, +).
  - **Chân ngắn** là **cực âm** (cathode, K, −).
  - Viền nhựa của LED có một **mép vát phẳng** ở phía cực âm.
- LED đỏ cần khoảng **1,8–2,2 V** để sáng, dòng điện thường dùng **10–20 mA**. LED xanh dương hoặc trắng cần khoảng **2,8–3,3 V**.
- **Điện trở hạn dòng:** LED rời luôn phải mắc nối tiếp với một điện trở. Không có điện trở, dòng điện tăng rất nhanh và LED có thể cháy. Ví dụ với nguồn 3 V và LED đỏ 2 V, muốn dòng khoảng 15 mA thì điện trở cần khoảng (3 − 2) ÷ 0,015 ≈ 67 Ω, chọn giá trị chuẩn **100 Ω**. Nhiều mô-đun LED trong bộ học tập đã gắn sẵn điện trở; thầy kiểm tra kit của mình trước buổi học.

### 4. Vì sao không được nối thẳng hai đầu pin (đoản mạch)

- Nối trực tiếp cực dương và cực âm bằng một dây gọi là **đoản mạch** (ngắn mạch, chập mạch).
- Dây có điện trở rất nhỏ, nên dòng điện **rất lớn**. Năng lượng biến thành nhiệt: **dây và pin nóng nhanh**, có thể làm bỏng tay, pin phồng, rò rỉ hóa chất. Với pin sạc dung lượng lớn (Li-ion), đoản mạch có thể gây **cháy**.
- Đồng thời pin hết năng lượng rất nhanh.
- Quy tắc với lớp học: **không bao giờ để một dây nối hai cực pin mà không qua thiết bị nào**.

### 5. Vì sao cấm pin cúc áo

- Pin cúc áo (pin đồng xu, pin nút) nhỏ, tròn, trẻ dễ nuốt hoặc nhét vào mũi, tai.
- Nếu bị nuốt và kẹt trong thực quản, pin tạo dòng điện qua mô ẩm, gây **bỏng hóa chất nặng chỉ trong khoảng 2 giờ**. Đây là tình huống **cấp cứu**, phải đưa đi bệnh viện ngay.
- Vì vậy khóa học **không dùng pin cúc áo**, và thầy hoặc trợ giảng là người thay pin.

### 6. Thứ tự tìm lỗi khi đèn không sáng

Đây là quy trình gỡ lỗi đầu tiên của khóa học, dùng lại ở mọi buổi sau:

1. **Pin:** Có pin không? Lắp đúng chiều chưa? Còn điện không?
2. **Công tắc:** Đã bật chưa?
3. **Dây:** Có dây nào lỏng, tuột, đứt không?
4. (Bổ sung từ buổi 5) **Thiết bị:** LED lắp đúng chiều chưa?

---

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Pin là Bình sữa năng lượng

**Nói cho trẻ hiểu:** Pin cho robot năng lượng để chạy, giống sữa cho em bé năng lượng để chơi. Hết sữa thì em bé đói, mệt. Hết pin thì robot "đói", đèn sáng yếu, xe chạy chậm.

**Pin có hai đầu:**
- Đầu có núm lồi là **cực dương**, ký hiệu dấu cộng **+**, dây màu **đỏ**.
- Đầu phẳng là **cực âm**, ký hiệu dấu trừ **−**, dây màu **đen** (hoặc xanh).

**Lời giảng mẫu:**

> **Thầy:** "Đây là Bình sữa năng lượng của robot. Nhìn kỹ: một đầu có cái núm nhỏ, có dấu cộng. Một đầu phẳng, có dấu trừ. Nhớ luật lắp pin: đỏ gặp đỏ, xanh gặp xanh. Dấu cộng của pin gặp dấu cộng của hộp pin."

**Câu hỏi kiểm tra:**
1. Pin cho robot cái gì? *Đáp án: Năng lượng (điện).*
2. Đầu có núm lồi là cực gì? *Đáp án: Cực dương, dấu cộng.*
3. Dây màu đỏ nối với cực nào? *Đáp án: Cực dương.*

### Khái niệm 2: Mạch kín thì sáng, mạch hở thì tắt

**Nói cho trẻ hiểu:** Điện đi ra từ đầu cộng của pin, chạy theo dây, qua đèn, rồi chạy về đầu trừ của pin. Đi đủ một vòng gọi là **mạch kín**, đèn sáng. Đứt một chỗ gọi là **mạch hở**, đèn tắt.

**Ví dụ đời sống:** Đường đua xe đồ chơi hình vòng tròn: thiếu một miếng ray, xe không chạy hết vòng được.

**Lời giảng mẫu:**

> **Thầy:** "Thầy vẽ trên bảng hai mạch. Mạch thứ nhất, con đường liền một vòng. Đèn sáng. Đây là mạch kín. Mạch thứ hai, có một chỗ đứt. Đèn tắt. Đây là mạch hở. Chữ 'kín' giống như cái vòng kín, không có lỗ hở."

**Câu hỏi kiểm tra:**
1. Mạch kín thì đèn thế nào? *Đáp án: Sáng.*
2. Công tắc tắt thì mạch kín hay hở? *Đáp án: Hở.*
3. Dây đứt bên trong lớp vỏ, nhìn bên ngoài vẫn bình thường. Đèn có sáng không? *Đáp án: Không, vì mạch vẫn hở.*

### Khái niệm 3: LED là Đom đóm, chỉ sáng khi đúng chiều

**Nói cho trẻ hiểu:** Đèn LED giống con đom đóm báo hiệu trong đêm. Nhưng đom đóm này hơi khó tính: điện phải đi vào **đúng cửa**. LED có hai chân. **Chân dài là chân cộng**, **chân ngắn là chân trừ**. Lắp ngược thì LED không sáng.

**Ví dụ đời sống:** Cửa xoay một chiều ở siêu thị: đi vào được, nhưng đi ngược thì bị chặn.

**Lời giảng mẫu:**

> **Thầy:** "Nhìn con Đom đóm này. Hai chân dài ngắn khác nhau. Chân dài là chân cộng. Mẹo nhớ: 'Dài thì Dương', cùng chữ D. Điện chỉ đi vào Đom đóm theo một chiều thôi. Lắp ngược, Đom đóm không chịu sáng."

**Câu hỏi kiểm tra:**
1. Chân dài của LED là chân gì? *Đáp án: Chân cộng (dương).*
2. Lắp LED ngược chiều thì sao? *Đáp án: Không sáng.*
3. Mẹo nhớ chân LED là gì? *Đáp án: Dài thì Dương.*

### Khái niệm 4: Ba luật an toàn với pin

**Nói cho trẻ hiểu và giải thích lý do:**

| Luật | Vì sao (nói cho trẻ) |
| --- | --- |
| Không nối thẳng hai đầu pin bằng một sợi dây | Điện chạy quá nhanh, không qua đèn, nên dây và pin nóng lên, có thể làm bỏng tay. |
| Không dùng pin cúc áo, không cho pin vào miệng | Pin cúc áo nhỏ, nếu nuốt phải sẽ làm bỏng bên trong cổ, rất nguy hiểm. |
| Thầy thay pin, các em không tự thay, không tự sạc | Lắp sai pin có thể làm nóng, hỏng mạch. |

**Lời giảng mẫu:**

> **Thầy:** "Điện thích đường tắt. Nếu mình nối thẳng hai đầu pin, điện không thèm đi qua đèn nữa mà chạy vèo một vòng. Chạy nhanh quá nên nóng lên, như mình chạy thật nhanh thì người nóng ran. Nóng quá thì bỏng tay. Vì vậy luật số 1: không bao giờ nối thẳng hai đầu pin."

**Câu hỏi kiểm tra:**
1. Nối thẳng hai đầu pin bằng dây thì chuyện gì xảy ra? *Đáp án: Dây và pin nóng lên, có thể bỏng.*
2. Ai được thay pin? *Đáp án: Thầy hoặc trợ giảng.*
3. Thấy pin hoặc dây nóng lên, em làm gì? *Đáp án: Tắt công tắc, báo thầy ngay.*

---

## Kịch bản giảng theo khung 60 phút

### 0'–5': Tín hiệu từ Bít-Bô

Thầy cầm mạch có dây đứt giấu bên trong vỏ. Bật công tắc. Đèn không sáng.

> **Thầy:** "Bít-Bô gửi tới mạch đèn này. Pin còn mới. Công tắc đã bật. Dây nhìn bình thường. Vậy mà đèn không sáng! Bác Bug đã giấu gì ở đây? Ai là thám tử giỏi nhất?"

### 5'–10': Đoán trước, cược Xu

Ghi 4 khả năng lên bảng: *Pin hết · Công tắc hỏng · Dây đứt · Đèn hỏng*. Các em cược Xu. Thầy không công bố đáp án ngay.

**Câu chuyển ý:** "Muốn bắt Bác Bug, thám tử phải hiểu điện đi thế nào. Mời hai nhân vật mới."

### 10'–25': Trò chơi không cần máy (Hoạt động 1–2)

1. **Gặp Pin và LED (8').** Phát mỗi đội một viên pin AA (không có hộp) và một LED mẫu. **Nhìn:** tìm dấu + và −, tìm chân dài chân ngắn. **Sờ:** đầu lồi, đầu phẳng; chân LED cứng hay mềm. **Đoán:** "Chân nào nối với dấu cộng?" Giới thiệu biệt danh và mẹo "Dài thì Dương".
2. **Luật "đỏ gặp đỏ, xanh gặp xanh" (7').** Thầy chiếu ảnh hộp pin có ký hiệu + và −. Mời 2 em lên bảng nối hình pin vào hộp pin đúng chiều. Cả lớp kiểm tra bằng luật "đỏ gặp đỏ".

**Câu chuyển ý:** "Pin đúng chiều rồi. Giờ xem điện đi đâu."

### 25'–45': Khám phá và giải thích (Hoạt động 3–5)

3. **Mạch kín, mạch hở (10').** Thầy vẽ hai mạch trên bảng. Cả lớp chơi lại "Con đường điện": lần 1 cả vòng liền, bóng đi hết, "đèn sáng". Lần 2, thầy giấu một chỗ đứt **ở sau lưng một em** (em đó chỉ giả vờ nắm tay). Bóng dừng ở đó. Hỏi: "Nhìn từ xa có thấy chỗ đứt không?" Liên hệ với mạch bí ẩn: dây đứt bên trong vỏ, nhìn ngoài không thấy.
4. **Luật an toàn (7').** Giảng 3 luật ở Khái niệm 4. Thầy cầm một sợi dây và hộp pin, giơ lên nhưng **không nối**: "Nếu ai làm thế này, chuyện gì xảy ra?" Cả lớp trả lời. Treo bảng luật an toàn lên tường.
5. **Ôn thẻ lệnh nấc 0–1 (3').** Thầy đọc nhanh 4 lệnh, các em giơ thẻ: rõ ràng hay mơ hồ, một việc hay hai việc.

**Giải bí ẩn mở màn:** Thầy thay một dây khác vào mạch bí ẩn: đèn sáng. "Bác Bug trốn trong dây! Dây bị đứt bên trong lớp vỏ." Ai cược "Dây đứt" được giữ Xu.

### 45'–55': Đố nhanh, nhận Thẻ bài

| Câu đố | Đáp án |
| --- | --- |
| Đèn chỉ sáng khi mạch... | Kín |
| Chân dài của LED là... | Dương (+) |
| Dây đỏ nối cực... | Dương |
| Tìm lỗi theo thứ tự nào? | Pin – Công tắc – Dây |
| Thấy pin nóng thì làm gì? | Tắt công tắc, báo thầy |

Làm Phiếu bài tập buổi 5. Phát Thẻ bài "Bình sữa năng lượng" và "Đom đóm".

### 55'–60': Cliffhanger

> **Thầy:** "Bác Bug tức lắm vì bị bắt. Nó đã lẻn vào phá 3 mạch nữa, mỗi mạch một kiểu khác nhau. Buổi sau, đội nào bắt đủ 3 con Bác Bug?"

---

## Học sinh hay hỏi gì và trả lời thế nào

| Câu hỏi | Gợi ý trả lời |
| --- | --- |
| Pin ở trong có gì? | Có các chất hóa học. Chúng phản ứng với nhau tạo ra điện. Vì vậy không được cắn, đập hay mở pin. |
| Vì sao điện trong ổ cắm nguy hiểm mà pin thì không? | Ổ cắm có điện rất mạnh, khoảng 220 vôn, mạnh hơn pin AA hơn 100 lần. Pin nhỏ trong lớp chỉ 3 vôn, an toàn. Nhưng tuyệt đối không chạm ổ cắm. |
| LED lắp ngược có bị cháy không? | Với pin nhỏ trong lớp thì thường không cháy, chỉ không sáng. Lắp lại đúng chiều là sáng. |
| Đèn LED khác bóng đèn tròn ở nhà thế nào? | LED tốn ít điện hơn, bền hơn, ít nóng hơn. Bóng đèn sợi đốt cũ sáng nhờ sợi dây nóng đỏ lên, nên rất nóng. |
| Pin hết thì vứt đâu? | Không vứt vào thùng rác thường, vì hóa chất trong pin làm bẩn đất và nước. Bỏ vào thùng thu gom pin cũ. |
| Sao pin hết mà nhìn vẫn như cũ? | Năng lượng hết nằm ở bên trong, hóa chất đã dùng hết. Vỏ ngoài vẫn như cũ. Muốn biết, mình thử lắp vào mạch xem đèn có sáng không. |

---

## Hiểu lầm thường gặp

| Hiểu lầm | Cách sửa |
| --- | --- |
| "Chỉ cần một dây từ pin tới đèn là đèn sáng." | Điện cần đi một vòng. Vẽ mạch chỉ có một dây, hỏi: "Điện quay về pin bằng đường nào?" |
| "Dây nhìn bình thường thì chắc chắn tốt." | Dây có thể đứt bên trong lớp vỏ. Dùng mạch bí ẩn mở màn để chứng minh. |
| "Pin mới thì không bao giờ là lỗi." | Pin mới vẫn có thể lắp ngược. Luôn kiểm tra pin đầu tiên. |
| "Lắp LED chiều nào cũng sáng." | LED là đom đóm một chiều. Cho các em thử ở buổi 6. |
| "Pin càng nhiều càng tốt, cứ thêm pin." | Thêm pin là tăng điện áp. Quá nhiều có thể làm cháy LED, hỏng động cơ. Kỹ sư dùng đúng số pin. |
| "Pin nóng là pin đang chạy tốt." | Pin nóng là dấu hiệu nguy hiểm (thường do nối tắt). Tắt và báo thầy. |

---

## Phân hóa

### Lớp 1–3

- Chỉ dùng từ "đầu cộng", "đầu trừ", "chân dài", "chân ngắn". Chưa cần từ "cực dương", "cực âm" nếu các em chưa quen.
- Dùng màu thay cho ký hiệu: dán chấm đỏ lên đầu cộng của pin và chân dài của LED.
- Luật an toàn dạy bằng tranh: tranh "đúng" có dấu tích xanh, tranh "sai" có dấu nhân đỏ.
- Mẹo nhớ: "Dài thì Dương", "Đỏ gặp đỏ".

### Lớp 4–5

- Dùng đúng thuật ngữ: **cực dương, cực âm, mạch kín, mạch hở, đoản mạch, điốt**.
- Giới thiệu số liệu: pin AA 1,5 V; hai viên nối tiếp 3 V. Hỏi: "Bốn viên nối tiếp được bao nhiêu vôn?" (6 V).
- Giải thích điện trở bằng ẩn dụ: "Điện trở như cái van làm nước chảy chậm lại, để Đom đóm không bị 'uống' quá nhiều điện mà cháy."
- Vẽ sơ đồ mạch bằng ký hiệu đơn giản: pin (hai vạch dài ngắn), công tắc, đèn.
- Câu hỏi suy nghĩ: "Nếu mắc hai đèn nối tiếp nhau trong một vòng, tháo một đèn thì đèn còn lại thế nào?" (Tắt, vì mạch hở.)

---

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Pin (Bình sữa năng lượng) | Đồ ăn của robot | Nguồn điện hóa học, tạo hiệu điện thế giữa hai cực |
| Cực dương (+) | Đầu cộng, dây đỏ | Cực có điện thế cao hơn của nguồn |
| Cực âm (−) | Đầu trừ, dây đen | Cực có điện thế thấp hơn của nguồn |
| Mạch kín | Con đường liền một vòng, đèn sáng | Mạch có đường dẫn liên tục, có dòng điện |
| Mạch hở | Con đường bị đứt, đèn tắt | Mạch bị ngắt, không có dòng điện |
| LED (Đom đóm) | Đèn nhỏ chỉ sáng khi đúng chiều | Điốt phát quang, chỉ dẫn điện theo một chiều |
| Đoản mạch | Nối thẳng hai đầu pin, rất nóng | Nối hai cực nguồn qua điện trở rất nhỏ, dòng điện lớn bất thường |
| Vôn (V) | Sức đẩy của điện | Đơn vị đo hiệu điện thế |

---

## Ghi nhớ cuối bài

1. Pin là Bình sữa năng lượng, có đầu cộng và đầu trừ.
2. Đỏ gặp đỏ, xanh gặp xanh.
3. Mạch kín thì đèn sáng, mạch hở thì đèn tắt.
4. Đom đóm LED: dài thì dương, lắp ngược không sáng.
5. Không bao giờ nối thẳng hai đầu pin.
6. Tìm Bác Bug theo thứ tự: pin – công tắc – dây.
