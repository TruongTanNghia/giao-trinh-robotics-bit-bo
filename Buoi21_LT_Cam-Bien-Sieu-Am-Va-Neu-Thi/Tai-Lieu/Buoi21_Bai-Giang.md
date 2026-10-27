# Bài giảng – Buổi 21: Cảm biến siêu âm và Nếu – Thì

> **Lý thuyết · 60 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 11: Robot biết "nhìn thấy" · Tuần 11

Đây là buổi then chốt của khóa học. Từ trước đến nay, robot chỉ làm theo các bước cố định, không biết gì về xung quanh. Hôm nay robot có **giác quan** đầu tiên – cảm biến siêu âm – và biết **quyết định** bằng câu Nếu – Thì (nấc 5).

## Kiến thức nền cho giáo viên

### Âm thanh và siêu âm

- Âm thanh là dao động truyền trong không khí. Tai người nghe được khoảng 20 Hz đến 20.000 Hz.
- **Siêu âm** là âm có tần số cao hơn 20.000 Hz. Người không nghe được, nhưng dơi, cá heo, chó nghe được một phần.
- Cảm biến siêu âm phổ biến trong các bộ kit giáo dục phát sóng khoảng **40.000 Hz (40 kHz)**.

### Cảm biến siêu âm hoạt động thế nào

Cảm biến có hai "mắt" tròn: một cái **phát** (loa), một cái **thu** (micro). Chu trình đo:

1. Bộ phát bắn ra một chùm siêu âm rất ngắn.
2. Sóng bay đi, gặp vật cản, dội lại (tiếng vọng).
3. Bộ thu nghe thấy tiếng vọng.
4. Cảm biến đo **thời gian** từ lúc phát đến lúc thu.
5. Tính khoảng cách:

```text
khoảng cách = (thời gian × tốc độ âm thanh) ÷ 2
```

- Tốc độ âm thanh trong không khí khoảng **343 m/s** (ở khoảng 20°C), tức là 0,0343 cm mỗi micro-giây.
- **Chia 2** vì sóng đi tới vật rồi quay về, tức là đi hai lần quãng đường.
- Ví dụ: tiếng vọng về sau 0,001 giây (1 mili-giây). Quãng đường cả đi lẫn về = 343 × 0,001 = 0,343 m. Khoảng cách tới vật = 0,343 ÷ 2 ≈ 0,17 m = 17 cm.

Bo mạch làm phép tính này tự động và cho ra con số khoảng cách (thường bằng cm). Học sinh không cần tính.

### Tầm đo và giới hạn

| Đặc điểm | Giá trị thường gặp | Ghi chú |
| --- | --- | --- |
| Tầm đo gần nhất | Khoảng 2–3 cm | Gần hơn thì sóng về quá nhanh, cảm biến không phân biệt được |
| Tầm đo xa nhất | Vài mét (thường 2–4 m) | Xa hơn tiếng vọng quá yếu |
| Góc "nhìn" | Một hình nón hẹp phía trước | Vật lệch sang bên có thể không thấy |

Thông số cụ thể xem tài liệu cảm biến của bộ kit trường.

### Vì sao có lúc đo sai

| Tình huống | Hiện tượng | Lý do |
| --- | --- | --- |
| Vật mềm, xốp (gối bông, rèm, áo len) | Đo xa hơn thật hoặc không đo được | Vật mềm hút âm, tiếng vọng yếu |
| Vật đặt xiên, nghiêng | Không thấy vật hoặc đo sai | Sóng dội lệch sang hướng khác, không quay về bộ thu (như bóng ném vào tường xiên) |
| Vật quá nhỏ, mảnh (chân bàn, dây) | Lúc thấy lúc không | Bề mặt phản xạ quá nhỏ |
| Vật quá gần (dưới 2–3 cm) | Số lạ | Dưới tầm đo |
| Hai cảm biến gần nhau cùng đo | Số nhảy lung tung | Nghe nhầm tiếng vọng của nhau |

Vật tốt nhất để đo: phẳng, cứng, đứng thẳng, quay mặt về cảm biến (hộp giấy, tấm bìa, bức tường).

### Câu lệnh điều kiện Nếu – Thì – Không thì

Câu lệnh điều kiện cho chương trình chọn một trong hai đường đi:

```text
nếu <điều kiện> thì
  <làm việc A>
không thì
  <làm việc B>
```

- **Điều kiện** là một câu chỉ có thể đúng hoặc sai. Ví dụ: "khoảng cách < 15".
- Điều kiện đúng → làm A. Điều kiện sai → làm B. Không bao giờ làm cả hai.
- Phép so sánh: `<` (nhỏ hơn), `>` (lớn hơn), `=` (bằng).
- **Ngưỡng** là con số mốc để so sánh, ví dụ 15 cm. Chọn ngưỡng bằng cách thử.

### Vì sao điều kiện phải nằm trong "lặp mãi"

Nếu chỉ kiểm tra một lần lúc bắt đầu, robot "nhìn" đúng một lần rồi thôi. Muốn robot luôn để ý, phải đặt câu Nếu – Thì trong **lặp mãi**: nhìn – quyết định – làm – nhìn lại – quyết định lại..., hàng chục lần mỗi giây.

```text
khi bắt đầu
  lặp mãi
    nếu khoảng cách < 15 cm thì
      dừng
    không thì
      tiến
```

Đây là chu trình **cảm biến → chương trình quyết định → động cơ thực hiện** mà các em sẽ dùng đến hết khóa học.

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Robot cần thông tin để quyết định

**Định nghĩa cho trẻ:** Muốn quyết định đúng, phải biết xung quanh có gì. Robot cũng vậy.

**Ví dụ đời sống:** Bịt mắt đi trong phòng: em sẽ va vào bàn ghế. Có bạn nói "phía trước 5 bước có ghế, rẽ trái", em đi được.

**Ẩn dụ nhân vật:** Bác Bug đã giấu đi đôi mắt của robot. Hôm nay mình tìm lại cho nó.

**Lời giảng mẫu:**

> **Thầy:** "Lúc bịt mắt, bạn Lan đi khó khăn vì thiếu thông tin. Khi được báo có ghế, bạn Lan biết rẽ. Robot của chúng ta đến giờ vẫn đang bịt mắt. Nó chạy 2 giây là chạy 2 giây, có tường cũng đâm vào. Làm sao để robot biết có vật cản?"

**Câu hỏi kiểm tra:**

1. Vì sao bịt mắt thì khó né vật cản? → Vì không có thông tin về vật cản.
2. Robot hiện nay có biết phía trước có tường không? → Không.

### Khái niệm 2: Dơi – cảm biến siêu âm

**Định nghĩa cho trẻ:** Cảm biến siêu âm phát ra tiếng kêu rất cao mà tai người không nghe được. Tiếng kêu đập vào vật rồi dội lại. Tiếng dội về càng nhanh thì vật càng gần.

**Ví dụ đời sống:** Hét to trong hang hay trong phòng trống, em nghe tiếng vọng. Đứng gần vách thì tiếng vọng về nhanh, đứng xa thì về chậm.

**Ẩn dụ nhân vật:** Dơi. Dơi bay trong đêm tối không va vào cây vì dơi kêu và nghe tiếng vọng. Cảm biến có hai con mắt tròn: một cái là miệng dơi (phát), một cái là tai dơi (nghe).

**Lời giảng mẫu:**

> **Thầy:** "Đây là đôi tai dơi của robot. Mắt tròn bên này kêu 'chíp' – tiếng cao đến nỗi tai các em không nghe được. Tiếng 'chíp' bay đi, đập vào tường, bay về mắt tròn bên kia. Bộ não đếm xem tiếng đi rồi về mất bao lâu. Về nhanh là tường gần. Về chậm là tường xa."

**Câu hỏi kiểm tra:**

1. Cảm biến có mấy mắt tròn, mỗi cái làm gì? → Hai: một cái phát tiếng, một cái nghe tiếng vọng.
2. Tiếng vọng về nhanh nghĩa là vật gần hay xa? → Gần.
3. Vì sao mình không nghe cảm biến kêu? → Vì tiếng quá cao, tai người không nghe được.

### Khái niệm 3: Vật nào đo tốt, vật nào đo kém

**Định nghĩa cho trẻ:** Tiếng vọng dội tốt trên vật cứng, phẳng, đứng thẳng. Vật mềm thì "nuốt" mất tiếng. Vật xiên thì làm tiếng dội đi chỗ khác.

**Ví dụ đời sống:** Ném bóng vào tường thẳng, bóng bật về tay em. Ném vào tường xiên, bóng bật đi hướng khác. Ném vào đống gối, bóng không bật lại.

**Lời giảng mẫu:**

> **Thầy:** "Tiếng của dơi giống quả bóng. Gặp tường phẳng, nó bật về. Gặp gối bông, nó bị nuốt mất. Gặp tấm bìa xiên, nó bật đi chỗ khác. Khi đó robot tưởng không có gì phía trước."

**Câu hỏi kiểm tra:**

1. Cảm biến đo tốt hộp giấy hay gối bông? → Hộp giấy.
2. Vì sao tấm bìa đặt xiên có thể không đo được? → Tiếng dội đi hướng khác, không về tai dơi.

### Khái niệm 4: Nếu – Thì như đèn giao thông

**Định nghĩa cho trẻ:** Nếu – Thì là cách robot chọn việc. **Nếu** điều này đúng **thì** làm việc này, **không thì** làm việc kia.

**Ví dụ đời sống:** Nếu trời mưa thì mang áo mưa, không thì đội mũ. Nếu đèn đỏ thì dừng, nếu đèn xanh thì đi.

**Ẩn dụ nhân vật:** Đèn giao thông của Căn cứ.

**Lời giảng mẫu:**

> **Thầy:** "Bộ não của robot giờ có thể hỏi: 'Có vật ở gần hơn 15 cm không?' Câu trả lời chỉ có Đúng hoặc Sai. Đúng thì dừng. Sai thì đi tiếp. Con số 15 gọi là ngưỡng – cái mốc để so sánh. Và robot phải hỏi câu này liên tục, nên ta đặt nó trong Lặp mãi."

**Câu hỏi kiểm tra:**

1. Điều kiện "khoảng cách < 15" đúng khi nào? → Khi vật ở gần hơn 15 cm.
2. Nếu điều kiện sai thì robot làm phần nào? → Phần "không thì".
3. Vì sao đặt Nếu – Thì trong lặp mãi? → Để robot kiểm tra liên tục, không chỉ một lần.

### Khái niệm 5: Chuỗi Cảm biến – Bộ não – Động cơ

**Định nghĩa cho trẻ:** Cảm biến cho biết khoảng cách. Chương trình quyết định. Động cơ thực hiện.

**Lời giảng mẫu:**

> **Thầy:** "Tai dơi nghe: còn 10 cm. Bộ não hỏi: 10 có nhỏ hơn 15 không? Có. Vậy ra lệnh: Dừng! Cơ bắp dừng lại. Ba bạn làm việc cùng nhau: Dơi, Bộ não, Cơ bắp."

**Câu hỏi kiểm tra:**

1. Ai đo, ai quyết định, ai làm? → Cảm biến đo, chương trình (bộ não) quyết định, động cơ làm.

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

Thầy đặt xe mẫu (đã cài chương trình tự dừng) cách tường 1 m. Bấm Chạy. Xe chạy rồi tự dừng trước tường. Thầy không chạm vào.

> **Thầy:** "Không ai chạm. Không ai bấm. Xe tự biết dừng. Phép thuật hay khoa học?"

### 5' – Đoán trước, cược Xu

> **Thầy:** "Xe dừng nhờ cái gì? Đoán: A. nó nhìn thấy bằng mắt; B. nó nghe tiếng vọng; C. thầy điều khiển từ xa. Đặt 2 Xu."

### 15' – Trò chơi không cần máy

1. **Bịt mắt né vật cản (5 phút):** Bịt mắt một em, đặt 3 vật cản mềm. Lần 1 không ai nói gì: em khó đi. Lần 2 cả lớp báo "phía trước 5 bước có vật, rẽ trái": em đi được. Hỏi: "Thiếu gì? Thêm gì thì đi được?"
2. **Nghe tiếng vọng (4 phút):** Cả lớp vỗ tay một cái thật to khi đứng gần bức tường lớn hoặc hành lang. Nói nhỏ: "Âm thanh đi tới tường rồi quay về."
3. **Đèn giao thông (6 phút):** Thầy giơ thẻ đỏ/xanh. Luật: Nếu đỏ thì đứng yên, không thì đi tại chỗ. Chơi 1 phút. Sau đó thầy bí mật đổi luật thành "Nếu xanh thì đứng yên" mà không nói rõ – cả lớp lộn xộn. Hỏi: "Bác Bug ở đâu?" (Điều kiện đặt ngược.)

### 20' – Khám phá và giải thích

**7 phút: Gặp nhân vật Dơi.** Chuyền tay cảm biến (không cắm điện). Nhìn – Sờ – Đoán: "Hai mắt tròn này làm gì?" Vẽ lên bảng: cảm biến → sóng đi → tường → sóng về. Giải thích tiếng đi rồi về. Cho trả lời cược Xu (đáp án B).

**5 phút: Vật nào đo tốt.** Thầy cắm cảm biến xe mẫu, chiếu số khoảng cách. Đưa lần lượt hộp giấy phẳng, gối bông, tấm bìa xiên trước cảm biến. Cả lớp xem số thay đổi và nhận xét.

**8 phút: Nếu – Thì.** Chiếu chương trình mẫu. Đọc chậm từng dòng. Vẽ sơ đồ hai nhánh trên bảng:

```text
           Có vật gần hơn 15 cm?
             /            \
          Đúng            Sai
           |               |
         Dừng            Tiến
             \            /
              quay lại hỏi tiếp
```

> **Thầy:** "Robot hỏi câu này hàng chục lần mỗi giây. Vì thế ta đặt nó trong Lặp mãi."

### 10' – Đố nhanh, nhận Thẻ bài

Làm Phiếu bài tập buổi 21. Đố miệng:

- "Dơi biết đường nhờ gì?" → Tiếng vọng.
- "Nếu thấy vật ở gần thì...?" → Dừng.
- "Cảm biến – ? – Động cơ?" → Chương trình quyết định.

Trao Thẻ bài "Dơi".

### 5' – Cliffhanger

> **Thầy:** "Xe của đội mình sắp có đôi tai dơi. Buổi sau, chính các em sẽ dạy xe tự dừng. Ai sẽ chọn được con số ngưỡng tốt nhất?"

## Học sinh hay hỏi gì và trả lời thế nào

| Câu hỏi | Gợi ý trả lời |
| --- | --- |
| "Sao mình không nghe tiếng cảm biến?" | Tiếng quá cao, khoảng 40.000 lần rung mỗi giây. Tai người chỉ nghe tới khoảng 20.000. Chó, dơi có thể nghe được. |
| "Cảm biến có phải là mắt không?" | Không hẳn. Nó không thấy màu, không thấy hình. Nó chỉ biết vật ở xa bao nhiêu, giống dơi. |
| "Đo được xa bao nhiêu?" | Thường từ vài cm đến vài mét. Xa quá thì tiếng vọng yếu, không nghe được. |
| "Cảm biến có thấy người không?" | Có, nhưng áo mềm, tóc xù làm tiếng vọng yếu hơn, đo có thể sai. |
| "Xe ô tô thật có cái này không?" | Có. Cảm biến lùi của ô tô kêu bíp bíp khi gần tường chính là cảm biến siêu âm. |
| "Nếu điều kiện vừa đúng vừa sai thì sao?" | Không thể. Điều kiện chỉ đúng hoặc sai, robot chỉ chọn một đường. |

## Hiểu lầm thường gặp

- **"Cảm biến nhìn bằng ánh sáng như mắt."** Cảm biến siêu âm dùng âm thanh, hoạt động được cả trong bóng tối.
- **"Cảm biến đo được mọi thứ."** Vật mềm, xiên, quá nhỏ hoặc quá gần dễ đo sai.
- **"Kiểm tra một lần là đủ."** Robot phải kiểm tra liên tục trong lặp mãi.
- **"Nếu – Thì làm cả hai việc."** Robot chỉ làm một trong hai: phần "thì" hoặc phần "không thì".
- **"Ngưỡng càng nhỏ càng an toàn."** Ngưỡng quá nhỏ thì xe không kịp dừng và đâm vào tường, vì xe cần quãng đường để dừng hẳn.

## Phân hóa

### Lớp 1–3

- Nói "tiếng kêu rất cao" thay cho "siêu âm 40 kHz".
- Chỉ dùng "gần" và "xa"; ngưỡng do thầy cho sẵn.
- Nếu – Thì: chỉ dạy một nhánh "nếu gần thì dừng", phần "không thì tiến" thầy gắn sẵn.

### Lớp 4–5

- Dùng từ "siêu âm", "tần số", "ngưỡng".
- Giới thiệu công thức khoảng cách = thời gian × tốc độ âm thanh ÷ 2, giải thích vì sao chia 2.
- Phân biệt `<` và `>`, tự đọc câu điều kiện.
- Câu hỏi suy luận: "Đổi `<` thành `>` thì xe làm gì?" (Chỉ chạy khi gần vật, dừng khi xa: điều kiện đặt ngược.)

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Cảm biến | Giác quan của robot | Linh kiện đo một đại lượng của môi trường và chuyển thành tín hiệu điện |
| Siêu âm | Tiếng kêu quá cao, tai người không nghe | Sóng âm tần số trên khoảng 20 kHz |
| Tiếng vọng | Tiếng dội lại | Sóng âm phản xạ từ bề mặt vật cản |
| Khoảng cách | Vật ở xa bao nhiêu | Giá trị tính từ thời gian tiếng vọng, thường đơn vị cm |
| Điều kiện | Câu hỏi chỉ có Đúng hoặc Sai | Biểu thức logic cho kết quả đúng/sai |
| Nếu – Thì – Không thì | Chọn một trong hai việc | Cấu trúc rẽ nhánh của chương trình |
| Ngưỡng | Con số mốc để so sánh | Giá trị giới hạn dùng trong phép so sánh |
| Phép so sánh `<` | Nhỏ hơn | Toán tử so sánh trả về đúng khi vế trái nhỏ hơn vế phải |

## Ghi nhớ cuối bài

1. Cảm biến siêu âm giống dơi: phát tiếng kêu rất cao rồi nghe tiếng vọng.
2. Tiếng vọng về càng nhanh, vật càng gần.
3. Vật cứng, phẳng, đứng thẳng thì đo tốt; vật mềm hoặc xiên dễ đo sai.
4. Nếu – Thì giúp robot chọn: điều kiện đúng làm việc này, sai làm việc kia.
5. Cảm biến đo → chương trình quyết định → động cơ làm, lặp lại liên tục trong Lặp mãi.
