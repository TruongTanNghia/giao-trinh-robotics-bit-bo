# Bài giảng – Buổi 3: Giác quan – Bộ não – Tay chân

> **Lý thuyết · 60 phút** · Chặng 1: Đánh thức Bít-Bô · Nhiệm vụ 2: Robot cũng cần "giác quan" · Tuần 2

Buổi này trả lời câu hỏi: **robot được làm từ những phần nào, và điện đi đến các phần đó bằng cách nào?** Các em học ba nhóm bộ phận của robot, làm quen với hai linh kiện đầu tiên là **dây nối** và **công tắc**, và lên nấc 1 của bậc thang lập trình: **một lệnh là một việc**.

---

## Kiến thức nền cho giáo viên

### 1. Mô hình Cảm biến – Bộ xử lý – Cơ cấu chấp hành

Mọi robot, từ đồ chơi giáo dục đến robot công nghiệp, đều có thể mô tả bằng ba khối:

| Khối kỹ thuật | Chức năng | Ví dụ | Tương ứng cơ thể người | Tên trong khóa học |
| --- | --- | --- | --- | --- |
| Cảm biến (sensor) | Đổi thông tin từ môi trường (ánh sáng, khoảng cách, lực bấm) thành tín hiệu điện | Cảm biến siêu âm, cảm biến dò line, nút bấm | Mắt, tai, da | Giác quan |
| Bộ xử lý (controller) | Đọc tín hiệu cảm biến, chạy chương trình, quyết định | Bo mạch có vi điều khiển | Não | Bộ não |
| Cơ cấu chấp hành (actuator) | Đổi tín hiệu điện thành chuyển động, ánh sáng, âm thanh | Động cơ, đèn LED, còi | Tay, chân, miệng | Tay chân |

Ngoài ba khối trên, robot còn cần **nguồn điện** (pin) và **đường dẫn điện** (dây nối). Có thể ví nguồn điện như thức ăn, dây nối như mạch máu hoặc dây thần kinh.

**Lưu ý phân loại:** Đèn LED và còi được xếp vào "Tay chân" vì chúng là đầu ra (robot dùng để "nói", "báo hiệu"). Nút bấm là "Giác quan" vì robot dùng nó để nhận thông tin từ người.

### 2. Dòng điện cần một vòng khép kín

- **Dòng điện** là dòng chuyển động có hướng của các hạt mang điện (trong dây kim loại là các electron).
- Dòng điện chỉ chạy khi có **mạch kín**: một vòng liền từ cực dương của pin, qua dây, qua thiết bị (đèn, động cơ), rồi quay về cực âm của pin.
- Nếu vòng bị đứt ở bất kỳ chỗ nào, gọi là **mạch hở**, dòng điện dừng lại ở mọi chỗ trong mạch, không chỉ ở chỗ đứt.

Trò chơi "Con đường điện" (truyền bóng trong vòng tròn) mô phỏng đúng ý này: bóng chỉ đi được khi vòng tay liền. Một em buông tay thì cả vòng dừng.

### 3. Dây nối

- Dây điện gồm **lõi kim loại** (thường là đồng) dẫn điện tốt, và **vỏ nhựa** cách điện bao bên ngoài.
- Vỏ nhựa giúp điện không đi sai đường (chạm sang dây khác) và giúp tay người cầm an toàn.
- Chỉ phần lõi kim loại ở hai đầu dây mới nối điện được. Nếu đầu dây bị lỏng, hoặc lõi bị đứt bên trong lớp vỏ, mạch sẽ hở.

### 4. Công tắc

- Công tắc là bộ phận **đóng hoặc mở** mạch điện theo ý người dùng.
- **Đóng công tắc** (bật): hai tiếp điểm kim loại chạm nhau, mạch kín, điện chạy.
- **Mở công tắc** (tắt): hai tiếp điểm tách ra, mạch hở, điện ngừng.
- Lưu ý ngôn ngữ: trong điện học, "đóng" là bật, "mở" là tắt, ngược với cửa. Với học sinh nhỏ, dùng "bật" và "tắt" để tránh nhầm. Ẩn dụ "Người gác cổng" giúp các em nhớ: cổng đóng lại (nối liền) thì điện đi qua được.

> Với lớp 4–5, thầy có thể nói rõ: "Công tắc đóng giống cây cầu được hạ xuống, xe đi qua được. Công tắc mở giống cầu kéo lên, xe dừng lại."

### 5. Nấc 1: Một lệnh là một việc

Trong lập trình, mỗi câu lệnh (mỗi khối lệnh) thực hiện **một hành động đơn**. Muốn làm nhiều việc thì dùng nhiều lệnh nối tiếp nhau. Một lệnh gộp hai việc ("đi và nhảy") làm người đọc không biết làm việc nào trước, làm đồng thời hay lần lượt. Đây là cơ sở để buổi sau và các nấc sau ghép lệnh thành chuỗi.

---

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Robot cần giác quan để biết xung quanh

**Nói cho trẻ hiểu:** Mắt giúp mình nhìn, tai giúp mình nghe. Robot cũng cần "mắt, tai" để biết phía trước có gì. Mắt tai của robot gọi là **cảm biến**.

**Ví dụ đời sống:**
- Cửa tự động ở siêu thị có cảm biến, thấy người đến thì mở.
- Đèn hành lang tự sáng khi có người đi qua.
- Robot hút bụi có cảm biến để biết sắp đụng tường.

**Lời giảng mẫu:**

> **Thầy:** "Lúc nãy bạn Hà bịt mắt, đi chậm lắm, còn suýt đụng ghế. Vì sao? Vì bạn không thấy đường. Robot không có giác quan cũng giống bạn Hà bịt mắt. Nó không biết phía trước có tường hay không."

**Câu hỏi kiểm tra:**
1. Người dùng gì để nhìn? Robot dùng gì? *Đáp án: Người dùng mắt, robot dùng cảm biến.*
2. Cửa tự động biết có người nhờ đâu? *Đáp án: Nhờ cảm biến.*

### Khái niệm 2: Robot có 3 phần: Giác quan – Bộ não – Tay chân

**Nói cho trẻ hiểu:**
- **Giác quan** (cảm biến) để biết.
- **Bộ não** (bo mạch) để nghĩ và ra lệnh.
- **Tay chân** (động cơ, đèn, còi) để làm.

**Ví dụ đời sống:** Khi em chạm tay vào nồi nóng: **da** cảm thấy nóng (giác quan) → **não** nghĩ "nguy hiểm!" (bộ não) → **tay** rút lại (tay chân). Robot cũng đi theo đúng ba bước này.

**Lời giảng mẫu:**

> **Thầy:** "Robot mẫu của thầy có ba phần. Cái 'mắt' phía trước là Giác quan. Cái bảng mạch bên trong là Bộ não. Bánh xe và đèn là Tay chân. Thiếu một phần, robot không làm việc được. Không có mắt thì không biết đường. Không có não thì không biết nghĩ. Không có chân thì không đi được."

**Câu hỏi kiểm tra:**
1. Bánh xe thuộc phần nào? *Đáp án: Tay chân.*
2. Bo mạch thuộc phần nào? *Đáp án: Bộ não.*
3. Đèn LED thuộc phần nào? *Đáp án: Tay chân (robot dùng đèn để báo hiệu, giống miệng nói).*

### Khái niệm 3: Điện cần một con đường khép kín

**Nói cho trẻ hiểu:** Điện giống nước chảy trong ống. Điện đi từ pin, chạy theo dây, qua đèn, rồi quay về pin. Con đường phải **liền một vòng**. Đứt một chỗ là điện dừng hết.

**Ẩn dụ:** Nhân vật **Dây nối** tên là **"Con đường điện"**, giống ống dẫn nước. Ống thủng một chỗ thì nước không tới vòi.

**Lời giảng mẫu:**

> **Thầy:** "Trò truyền bóng vừa rồi, bóng đi hết vòng khi mọi người nắm tay nhau. Bạn Nam buông tay, bóng dừng luôn. Điện cũng thế. Dây nối là con đường điện. Con đường phải liền, không được đứt."

**Câu hỏi kiểm tra:**
1. Điện đi theo gì? *Đáp án: Theo dây nối.*
2. Dây bị đứt một chỗ thì đèn có sáng không? *Đáp án: Không.*
3. Dây có hai phần: lõi bên trong và vỏ bên ngoài. Phần nào cho điện đi qua? *Đáp án: Lõi kim loại bên trong.*

### Khái niệm 4: Công tắc là Người gác cổng

**Nói cho trẻ hiểu:** Công tắc quyết định điện có được đi qua hay không. Bật công tắc là mở đường cho điện. Tắt công tắc là chặn đường.

**Ẩn dụ:** Nhân vật **Công tắc** là **"Người gác cổng"**, giống công tắc đèn trong nhà em.

**Lời giảng mẫu:**

> **Thầy:** "Ở nhà, muốn đèn sáng em làm gì? Bật công tắc. Người gác cổng cho điện đi qua, đèn sáng. Tắt công tắc, người gác cổng chặn lại, đèn tắt. Trò chơi lúc nãy, bạn buông tay chính là người gác cổng đang chặn."

**Câu hỏi kiểm tra:**
1. Muốn đèn sáng, công tắc phải bật hay tắt? *Đáp án: Bật.*
2. Công tắc giống ai? *Đáp án: Người gác cổng.*

### Khái niệm 5: Một lệnh là một việc (nấc 1)

**Nói cho trẻ hiểu:** Mỗi lệnh chỉ bảo robot làm **một việc**. Muốn làm hai việc thì dùng hai lệnh.

**Ví dụ:** Nốt nhạc: mỗi nốt là một âm. Muốn hát một câu thì ghép nhiều nốt.

**Lời giảng mẫu:**

> **Thầy:** "Thầy giơ thẻ 'Vỗ tay', các em vỗ tay. Thẻ 'Đứng lên', các em đứng lên. Giờ thầy giơ thẻ 'Đứng lên và hát và vỗ tay'. Làm cái nào trước? Rối quá phải không? Robot cũng rối. Mỗi thẻ chỉ một việc thôi."

**Câu hỏi kiểm tra:**
1. Thẻ "Ngồi xuống" có mấy việc? *Đáp án: Một.*
2. Thẻ "Đi và nhảy" nên tách thành mấy thẻ? *Đáp án: Hai thẻ: "Đi" và "Nhảy".*

---

## Kịch bản giảng theo khung 60 phút

### 0'–5': Tín hiệu từ Bít-Bô

Mời một em xung phong, bịt mắt bằng khăn. Đặt 3 vật cản mềm trên đường. Các bạn dẫn đường bằng lời.

> **Thầy:** "Bít-Bô gửi tín hiệu: robot ở đó đi lung tung, đụng hết vào tường. Vì sao nhỉ? Mình thử làm robot bịt mắt xem."

Sau khi bạn đi xong, hỏi bạn: "Đi bịt mắt khó hay dễ? Vì sao?"

### 5'–10': Đoán trước, cược Xu

Ghi lên bảng câu hỏi: "Robot cần những gì để làm việc giỏi?" Ba lựa chọn: *Chỉ cần bánh xe · Cần mắt, não và chân · Chỉ cần pin*. Các em cược Xu.

**Câu chuyển ý:** "Muốn biết đáp án, mình xem cơ thể của chính mình trước đã."

### 10'–25': Trò chơi không cần máy (Hoạt động 1–2)

1. **So sánh cơ thể người và robot (7').** Vẽ hình người bên trái bảng, hình robot bên phải. Nối mắt – cảm biến, não – bo mạch, tay chân – động cơ. Ví dụ chạm tay vào nồi nóng.
2. **Trò "Con đường điện" (8').** Cả lớp đứng thành vòng tròn, nắm tay. Thầy đứng ở một chỗ làm "Pin", cầm quả bóng. Bóng truyền qua từng em, quay về thầy là "điện chạy hết một vòng". Thầy chạm vai một em: em đó buông tay, làm "công tắc tắt". Bóng phải dừng tại chỗ đứt. Thầy hỏi: "Bóng có đi tới các bạn phía sau chỗ đứt không?"

**Câu chuyển ý:** "Trong robot thật, cái gì làm 'con đường', cái gì làm 'người buông tay'? Mời hai nhân vật mới ra mắt."

### 25'–45': Khám phá và giải thích (Hoạt động 3–4)

3. **Gặp Dây nối và Công tắc (12').** Phát mỗi đội 1 dây nối và 1 công tắc mẫu. Đi qua 3 bước đầu của quy trình 5 bước:
   - **Nhìn:** Dây có mấy màu? Hai đầu dây trông thế nào? Công tắc có mấy vị trí?
   - **Sờ:** Vỏ dây mềm hay cứng? Gạt công tắc nghe tiếng gì?
   - **Đoán:** Dây dùng làm gì? Công tắc dùng làm gì?
   Thầy dùng mạch mẫu pin – công tắc – đèn, bật tắt cho cả lớp xem. Giới thiệu biệt danh "Con đường điện" và "Người gác cổng".
4. **Trò "Mỗi thẻ một việc" (8').** Thầy giơ thẻ hành động: Vỗ tay, Ngồi, Đứng, Giơ tay. Cả lớp làm. Rồi giơ thẻ gộp "Đứng lên và hát". Hỏi: làm sao sửa? Tách thành hai thẻ.

### 45'–55': Đố nhanh, nhận Thẻ bài

Đố nhanh bằng thẻ hình bộ phận robot: thầy giơ hình, cả lớp hô "Giác quan", "Bộ não" hoặc "Tay chân".

| Hình | Đáp án |
| --- | --- |
| Cảm biến | Giác quan |
| Bo mạch | Bộ não |
| Động cơ | Tay chân |
| Bánh xe | Tay chân |
| Nút bấm | Giác quan |
| Đèn LED | Tay chân |

Sau đó làm Phiếu bài tập buổi 3.

### 55'–60': Cliffhanger

> **Thầy:** "Người gác cổng có thật không? Thầy bật thì đèn sáng. Nhưng các Kỹ sư tự bật có được không? Buổi sau, các em tự mở cổng cho điện chạy."

---

## Học sinh hay hỏi gì và trả lời thế nào

| Câu hỏi | Gợi ý trả lời |
| --- | --- |
| Điện có nhìn thấy được không? | Không nhìn thấy điện chạy trong dây. Mình chỉ thấy kết quả: đèn sáng, động cơ quay. |
| Sao dây có màu đỏ, màu đen? | Màu giúp Kỹ sư phân biệt dây nối với cực dương (thường đỏ) và cực âm (thường đen). Màu không làm điện khác đi. |
| Chạm vào dây có bị giật không? | Dây trong bộ học tập dùng pin nhỏ, an toàn. Nhưng dây điện trong nhà (ổ cắm) rất nguy hiểm, tuyệt đối không chạm. |
| Robot có tim không? | Không. Pin giống như thức ăn cho robot. Dây nối giống mạch máu đưa năng lượng đi khắp nơi. |
| Bộ não robot có giống não người không? | Giống ở việc nhận tin và ra lệnh. Nhưng bộ não robot chỉ làm theo chương trình người viết, không tự nghĩ ra điều mới. |
| Nút bấm sao lại là giác quan? | Vì robot dùng nút bấm để "cảm thấy" người chạm vào nó, giống da cảm thấy có người chạm. |

---

## Hiểu lầm thường gặp

| Hiểu lầm | Cách sửa |
| --- | --- |
| "Điện chỉ cần đi một chiều từ pin đến đèn là đủ." | Nhắc lại trò truyền bóng: bóng phải quay về chỗ thầy. Điện phải đi một vòng, về lại pin. |
| "Đứt dây ở cuối thì phần đầu vẫn có điện chạy." | Trong mạch đơn, đứt một chỗ là điện dừng ở cả vòng. Bóng dừng lại, cả vòng đứng yên. |
| "Đèn là Giác quan vì nó sáng." | Đèn là thứ robot dùng để báo cho người khác biết, giống miệng nói. Đó là Tay chân (đầu ra). |
| "Công tắc tạo ra điện." | Công tắc chỉ cho điện đi qua hay không. Điện đến từ pin. |
| "Lệnh dài thì làm được nhiều việc hơn." | Một lệnh chỉ nên một việc. Nhiều việc thì nhiều lệnh, xếp theo thứ tự. |

---

## Phân hóa

### Lớp 1–3

- Dùng tranh to hình người và robot; các em dán hình bộ phận đúng chỗ.
- Trò truyền bóng chơi 2 lần: lần 1 không ai buông tay, lần 2 có một em buông. So sánh.
- Chỉ dùng từ "bật", "tắt", không dùng "đóng", "mở".
- Câu hỏi kiểm tra chỉ cần chỉ tay vào hình hoặc hô to.

### Lớp 4–5

- Giới thiệu thuật ngữ đúng: **cảm biến, bộ xử lý, cơ cấu chấp hành, mạch kín, mạch hở**.
- Phân biệt **vật dẫn điện** (kim loại) và **vật cách điện** (nhựa, gỗ, cao su). Các em đoán vật nào dẫn điện: thìa inox, thước nhựa, đồng xu, tẩy.
- Giải thích vì sao trong điện học "đóng công tắc" là bật (hai tiếp điểm chạm nhau).
- Thử thách: kể 3 robot ngoài đời và chỉ ra Giác quan, Bộ não, Tay chân của mỗi robot (ví dụ robot hút bụi: cảm biến va chạm, bo mạch, bánh xe và chổi quay).

---

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Cảm biến (Giác quan) | Mắt, tai của robot | Linh kiện đổi thông tin môi trường thành tín hiệu điện |
| Bo mạch (Bộ não) | Bộ não ra lệnh | Mạch điện tử có vi điều khiển chạy chương trình |
| Cơ cấu chấp hành (Tay chân) | Tay chân làm việc | Linh kiện đổi tín hiệu điện thành chuyển động, ánh sáng, âm thanh |
| Dây nối (Con đường điện) | Đường cho điện đi | Dây dẫn lõi kim loại, vỏ cách điện |
| Công tắc (Người gác cổng) | Cho điện đi hay chặn lại | Linh kiện đóng hoặc ngắt mạch điện |
| Mạch kín | Con đường liền một vòng | Mạch có đường dẫn liên tục để dòng điện chạy qua |
| Mạch hở | Con đường bị đứt | Mạch bị ngắt, không có dòng điện |

---

## Ghi nhớ cuối bài

1. Robot có Giác quan, Bộ não và Tay chân.
2. Giác quan để biết, Bộ não để nghĩ, Tay chân để làm.
3. Điện đi trên Con đường điện, phải liền một vòng.
4. Công tắc là Người gác cổng: bật cho đi, tắt thì chặn.
5. Một lệnh chỉ là một việc.
