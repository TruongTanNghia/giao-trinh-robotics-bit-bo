# Bài giảng – Buổi 11: Động cơ – cơ bắp của robot

> **Lý thuyết · 60 phút** · Chặng 2: Chế tạo xe cứu hộ · Nhiệm vụ 6: Thổi hồn cho chiếc xe · Tuần 6

**Mục tiêu buổi học**

- Học sinh biết động cơ nhận điện từ pin và biến điện thành chuyển động quay.
- Học sinh biết đảo hai dây của động cơ thì động cơ quay ngược chiều.
- Học sinh biết động cơ quay nhanh nhưng yếu, nên cần bánh răng giúp sức.
- Học sinh nắm luật an toàn: không giữ trục, kẹt thì tắt ngay.
- Nấc 2 không máy: chuỗi lệnh phải đúng thứ tự.

**Nhân vật linh kiện của buổi:** Cơ bắp (động cơ).

---

## Kiến thức nền cho giáo viên

### 1. Động cơ điện một chiều làm việc thế nào

Động cơ dùng trong xe robot giáo dục thường là **động cơ điện một chiều** (động cơ DC), chạy bằng pin. Nó biến **điện năng** thành **chuyển động quay**.

Bên trong có ba phần chính:

| Bộ phận | Vị trí | Nhiệm vụ |
| --- | --- | --- |
| Nam châm vĩnh cửu | Gắn vào vỏ, đứng yên | Tạo từ trường cố định |
| Cuộn dây quấn trên lõi sắt (rô-to) | Gắn vào trục, quay được | Khi có dòng điện chạy qua, trở thành nam châm điện |
| Cổ góp và chổi than | Ở một đầu trục | Đưa điện vào cuộn dây đang quay và đổi chiều dòng điện mỗi nửa vòng |

Nguyên lý: dòng điện chạy qua cuộn dây biến nó thành nam châm điện. Nam châm điện bị nam châm vĩnh cửu hút và đẩy, nên quay đi. Đúng lúc nó sắp dừng lại ở vị trí hút nhau, cổ góp đổi chiều dòng điện, cực của nam châm điện đổi, và nó lại bị đẩy quay tiếp. Cứ thế trục quay liên tục.

### 2. Vì sao đảo dây thì quay ngược

Đảo hai dây nối pin làm dòng điện chạy ngược chiều trong cuộn dây. Cực bắc và cực nam của nam châm điện đổi chỗ cho nhau. Lực hút đẩy đổi hướng, nên trục quay ngược lại. Đây là cách xe robot đi lùi: mạch điều khiển đảo chiều dòng điện vào động cơ.

### 3. Tốc độ và điện áp

- Điện áp càng cao, động cơ quay càng nhanh (trong giới hạn cho phép của động cơ).
- Pin yếu thì điện áp tụt, động cơ quay chậm và yếu. Đây là nguyên nhân rất hay gặp khi xe "tự nhiên chạy chậm".
- Không cắm động cơ 3 V vào nguồn quá cao: động cơ nóng và nhanh hỏng.

### 4. Vì sao động cơ cần hộp giảm tốc

Động cơ nhỏ quay rất nhanh, thường vài nghìn vòng mỗi phút khi không tải, nhưng lực xoắn rất yếu. Nếu gắn thẳng bánh xe vào trục, xe sẽ không đủ sức chạy, hoặc chạy giật cục.

Vì vậy động cơ xe robot thường đi kèm **hộp giảm tốc**: một chuỗi bánh răng nhỏ dẫn bánh to (đúng kiến thức buổi 9). Ví dụ tỉ số 48 : 1 nghĩa là trục động cơ quay 48 vòng thì trục ra bánh xe quay 1 vòng. Bánh xe quay chậm lại 48 lần nhưng khỏe lên nhiều lần.

### 5. Vì sao bóp trục gây nóng và kẹt

Khi động cơ quay tự do, chính chuyển động quay sinh ra một điện áp ngược (sức điện động ngược) làm giảm dòng điện chạy qua cuộn dây. Khi trục bị giữ chặt, không còn điện áp ngược này. Dòng điện tăng vọt, có thể gấp nhiều lần lúc chạy bình thường. Hậu quả:

- Cuộn dây nóng lên nhanh, có thể cháy lớp cách điện.
- Pin tụt nhanh và nóng.
- Bánh răng trong hộp giảm tốc có thể gãy răng.
- Ngón tay, tóc, dây buộc có thể bị cuốn vào trục hoặc bánh răng.

Đây là lý do luật an toàn: **không giữ bánh xe hay trục khi động cơ chạy; xe kẹt thì tắt công tắc ngay**.

### 6. Chuỗi lệnh – nấc 2

Chuỗi lệnh là danh sách việc robot làm lần lượt từ trên xuống. Cùng các lệnh nhưng đổi thứ tự thì kết quả khác:

| Chuỗi | Kết quả |
| --- | --- |
| Chạy – Quay phải – Dừng | Xe chạy thẳng, rẽ phải, rồi dừng |
| Quay phải – Chạy – Dừng | Xe rẽ phải trước, chạy theo hướng mới, rồi dừng |
| Dừng – Chạy – Quay phải | Xe đứng yên một lúc, chạy, rồi quay mãi vì không có lệnh dừng ở cuối |

Trò "Xe người" giúp học sinh cảm nhận điều này bằng cơ thể trước khi lập trình trên máy ở buổi 17.

---

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Động cơ – Cơ bắp của robot

**Định nghĩa cho trẻ:** Động cơ là bộ phận nhận điện từ pin rồi quay tròn. Nhờ động cơ quay mà bánh xe quay, robot chạy được.

**Ví dụ đời sống:** Quạt điện, máy sấy tóc, máy xay sinh tố, bàn chải đánh răng điện, xe điện đồ chơi đều có động cơ.

**Ẩn dụ nhân vật:** Cơ bắp. Người ăn cơm thì có sức để chạy. Robot "ăn" điện từ Bình sữa năng lượng (pin) thì Cơ bắp có sức để quay.

**Lời giảng mẫu:**

> **Thầy:** "Bên trong Cơ bắp có một nam châm và một cuộn dây. Khi điện chạy vào cuộn dây, cuộn dây biến thành nam châm. Hai nam châm hút nhau, đẩy nhau, đẩy mãi, đẩy mãi, và thế là trục quay tít. Không có điện thì Cơ bắp nằm im."

**Câu hỏi kiểm tra:**
1. Động cơ cần gì để quay? → *Cần điện (từ pin).*
2. Kể hai đồ vật trong nhà có động cơ. → *Quạt, máy xay, máy giặt...*
3. Pin yếu thì động cơ quay thế nào? → *Chậm và yếu hơn.*

### Khái niệm 2: Đảo dây thì quay ngược

**Định nghĩa cho trẻ:** Động cơ có hai dây. Đổi chỗ hai dây khi nối vào pin thì động cơ quay theo chiều ngược lại.

**Ví dụ đời sống:** Xe điện đồ chơi có nút tiến và nút lùi. Bên trong, nút lùi chính là đảo chiều điện vào động cơ.

**Ẩn dụ nhân vật:** Cơ bắp nghe theo hướng của dòng điện. Điện chảy một hướng thì Cơ bắp xoay phải, điện chảy hướng ngược lại thì Cơ bắp xoay trái.

**Lời giảng mẫu:**

> **Thầy:** "Thầy dán cánh quạt giấy lên trục. Nối dây đỏ với cực đỏ, dây đen với cực đen: cánh quạt quay sang phải. Bây giờ các Kỹ sư đoán: thầy đổi chỗ hai dây thì sao? Đội nào cược quay ngược?"

**Câu hỏi kiểm tra:**
1. Muốn động cơ quay ngược, em làm gì? → *Đổi chỗ hai dây nối với pin.*
2. Xe robot đi lùi nhờ đâu? → *Nhờ động cơ quay ngược chiều.*
3. Đảo dây thì động cơ có quay nhanh hơn không? → *Không, chỉ đổi chiều.*

### Khái niệm 3: Cơ bắp nhanh nhưng yếu, cần Anh em răng cưa giúp sức

**Định nghĩa cho trẻ:** Động cơ nhỏ quay rất nhanh nhưng không khỏe. Người ta gắn bánh răng để bánh xe quay chậm lại nhưng khỏe hơn, đủ sức chở xe.

**Ví dụ đời sống:** Xe đạp leo dốc phải chuyển sang líp to để nhẹ chân.

**Lời giảng mẫu:**

> **Thầy:** "Nhớ buổi trước không? Bánh nhỏ dẫn bánh to thì quay chậm mà khỏe. Cơ bắp của robot quay nhanh như chớp nhưng yếu. Nên trong hộp động cơ có Anh em răng cưa đứng sẵn để biến nhanh thành khỏe."

**Câu hỏi kiểm tra:**
1. Động cơ nhỏ quay nhanh hay chậm? Khỏe hay yếu? → *Nhanh nhưng yếu.*
2. Bộ phận nào giúp động cơ khỏe hơn? → *Bánh răng (bánh nhỏ dẫn bánh to).*

### Khái niệm 4: An toàn với Cơ bắp

**Định nghĩa cho trẻ:** Khi động cơ đang chạy mà bị giữ lại, nó sẽ nóng lên và có thể hỏng. Tay hoặc tóc có thể bị cuốn vào.

**Ví dụ đời sống:** Không thò tay vào quạt đang quay. Quạt bị kẹt sẽ nóng và có mùi khét.

**Lời giảng mẫu:**

> **Thầy:** "Khi Cơ bắp bị giữ, nó cố hết sức mà không quay được, nên nóng như người bị sốt. Luật của căn cứ: không giữ bánh xe, không giữ trục khi động cơ chạy. Xe kẹt thì việc đầu tiên là tắt công tắc, sau đó mới gỡ."

**Câu hỏi kiểm tra:**
1. Xe đang chạy bị kẹt vào chân ghế, em làm gì đầu tiên? → *Tắt công tắc.*
2. Vì sao không được bóp trục động cơ? → *Động cơ nóng, có thể hỏng; tay có thể bị kẹp.*
3. Bạn tóc dài phải làm gì khi làm với động cơ? → *Buộc tóc gọn.*

### Khái niệm 5: Chuỗi lệnh – thứ tự rất quan trọng

**Định nghĩa cho trẻ:** Chuỗi lệnh là các lệnh xếp thành hàng. Robot làm từng lệnh từ đầu đến cuối. Đổi thứ tự thì robot làm khác đi.

**Ví dụ đời sống:** Đi giày rồi mới đi tất thì không được. Mặc áo rồi mới cài cúc.

**Lời giảng mẫu:**

> **Thầy:** "Xe người của đội Xanh có ba thẻ: Chạy, Quay, Dừng. Bây giờ thầy đổi thành Dừng, Chạy, Quay. Xe người sẽ làm gì? Đứng yên, chạy, rồi quay mãi không dừng! Thứ tự sai một chút là xe đi sai cả đường."

**Câu hỏi kiểm tra:**
1. Robot làm lệnh nào trước? → *Lệnh ở đầu chuỗi.*
2. Chuỗi "Chạy – Quay" và "Quay – Chạy" có giống nhau không? → *Không, xe đi theo hướng khác.*
3. Nếu quên thẻ Dừng ở cuối thì sao? → *Xe làm mãi lệnh cuối cùng, không dừng.*

---

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

Thầy giơ động cơ lên cao, nối nhanh với pin cho cánh quạt giấy quay vù vù rồi tắt.

> **Thầy:** "Đây là Cơ bắp của robot. Xe của các Kỹ sư đã có Đôi chân, nhưng vẫn phải đẩy bằng tay. Hôm nay mình tìm hiểu Cơ bắp. Vì sao nó quay được?"

### 5' – Đoán trước, cược Xu

Câu hỏi cược: "Thầy đổi chỗ hai dây, cánh quạt sẽ: quay nhanh hơn, quay ngược lại, hay đứng yên?" Mỗi đội cược 1–3 Xu.

### 15' – Trò chơi không cần máy

1. **Nam châm đẩy nhau (5 phút):** Mỗi đội cầm hai thanh nam châm, thử cho hai đầu cùng cực lại gần nhau để cảm nhận lực đẩy. Thầy liên hệ: "Bên trong Cơ bắp có nam châm đẩy nhau như vậy."
2. **Xe người (10 phút):** Một em làm "xe", các bạn xếp thẻ Chạy (đi 3 bước), Quay trái, Quay phải, Dừng. Mỗi đội chạy hai chuỗi có cùng thẻ nhưng khác thứ tự, quan sát kết quả khác nhau.

### 20' – Khám phá và giải thích

1. Nhìn – Sờ – Đoán với động cơ (5 phút): nhìn hai dây, hai cực; sờ vỏ động cơ khi chưa chạy; đoán xem bên trong có gì.
2. Giảng Khái niệm 1 bằng hình vẽ đơn giản: nam châm, cuộn dây, trục (5 phút).
3. Thầy làm thí nghiệm đảo dây, công bố kết quả cược, giảng Khái niệm 2 (4 phút).
4. Giảng Khái niệm 3: cho xem hộp giảm tốc thật (nếu tháo được nắp) hoặc hình vẽ (3 phút).
5. Giảng Khái niệm 4 và đọc to luật an toàn, cả lớp nhắc lại (3 phút).

### 10' – Đố nhanh, nhận Thẻ bài

Học sinh làm Phiếu bài tập buổi 11. Thầy đố:
- "Cơ bắp ăn gì để có sức?"
- "Xe kẹt, việc đầu tiên là gì?"

Phát Thẻ bài "Cơ bắp".

### 5' – Cliffhanger

> **Thầy:** "Buổi sau, chiếc xe của mỗi đội sẽ có Cơ bắp và tự chạy lần đầu tiên. Mỗi đội nghĩ sẵn một cái tên thật hay để làm lễ khai sinh nhé."

---

## Học sinh hay hỏi gì và trả lời thế nào

1. **"Động cơ có bị hết sức không?"** → Động cơ không tự hết sức. Pin hết điện thì động cơ yếu đi và dừng. Thay pin mới là động cơ khỏe lại.
2. **"Cắm nhiều pin hơn thì quay nhanh hơn à?"** → Đúng là nhanh hơn, nhưng quá nhiều thì động cơ nóng và hỏng. Phải dùng đúng số pin thầy cho.
3. **"Ô tô thật có động cơ này không?"** → Ô tô xăng dùng động cơ đốt xăng, khác loại. Ô tô điện thì dùng động cơ điện, to và khỏe hơn rất nhiều.
4. **"Vì sao động cơ kêu ro ro?"** → Do các bánh răng trong hộp giảm tốc cọ vào nhau và trục quay nhanh.
5. **"Nối một dây thôi được không?"** → Không. Điện phải đi một vòng kín: từ pin ra, qua động cơ, rồi về pin. Thiếu một dây là mạch hở, như buổi 5.
6. **"Động cơ quay ngược có hỏng không?"** → Không hỏng. Động cơ được làm để quay được cả hai chiều.

---

## Hiểu lầm thường gặp

| Hiểu lầm | Cách sửa |
| --- | --- |
| "Đảo dây làm động cơ hỏng hoặc chạy nhanh hơn." | Làm thí nghiệm trực tiếp: chỉ đổi chiều quay. |
| "Động cơ tự có điện bên trong." | Rút pin ra cho học sinh thấy động cơ đứng yên. |
| "Giữ bánh xe một chút cũng không sao." | Cho sờ (qua thầy) vỏ động cơ sau khi bị kẹt vài giây thấy ấm; giải thích nguy cơ. |
| "Động cơ càng nhanh thì xe càng khỏe." | Nhắc lại bánh răng: nhanh thì yếu, cần giảm tốc để khỏe. |
| "Thứ tự lệnh không quan trọng, miễn đủ lệnh." | Chạy hai chuỗi Xe người cùng thẻ khác thứ tự để so sánh. |

---

## Phân hóa

**Lớp 1–3**
- Chỉ cần nhớ: điện vào thì quay; đảo dây thì quay ngược; kẹt thì tắt.
- Học nam châm bằng cảm nhận tay, không giải thích cổ góp.
- Xe người với chuỗi 3 thẻ.

**Lớp 4–5**
- Vẽ sơ đồ động cơ: nam châm, cuộn dây, trục, hai dây ra.
- Giải thích hộp giảm tốc bằng tỉ số truyền đã học ở buổi 9.
- Xe người với chuỗi 5–6 thẻ, có thử thách "tìm chuỗi ngắn nhất để đến đích".

---

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Động cơ | Cơ bắp của robot, nhận điện thì quay | Thiết bị biến điện năng thành cơ năng, ở đây là chuyển động quay |
| Trục động cơ | Que nhỏ thò ra, quay tít | Trục quay của rô-to, nơi truyền chuyển động ra ngoài |
| Nam châm điện | Cuộn dây có điện thì thành nam châm | Cuộn dây dẫn có dòng điện chạy qua tạo ra từ trường |
| Đảo chiều | Đổi hai dây để quay ngược | Đổi chiều dòng điện qua động cơ làm đổi chiều quay |
| Hộp giảm tốc | Bánh răng giúp động cơ khỏe hơn | Bộ truyền bánh răng làm giảm tốc độ và tăng mô-men xoắn ở trục ra |
| Kẹt | Động cơ bị giữ không quay được | Trạng thái rô-to bị chặn, dòng điện tăng cao gây nóng |
| Chuỗi lệnh | Các lệnh xếp hàng, làm lần lượt | Dãy câu lệnh thực hiện tuần tự theo thứ tự viết |

---

## Ghi nhớ cuối bài

1. Động cơ là Cơ bắp của robot, nhận điện từ pin thì quay.
2. Đảo hai dây thì động cơ quay ngược chiều.
3. Động cơ nhanh nhưng yếu, bánh răng giúp nó khỏe hơn.
4. Không giữ bánh xe hay trục khi động cơ chạy; kẹt thì tắt ngay.
5. Robot làm lệnh theo đúng thứ tự; đổi thứ tự là đổi kết quả.
