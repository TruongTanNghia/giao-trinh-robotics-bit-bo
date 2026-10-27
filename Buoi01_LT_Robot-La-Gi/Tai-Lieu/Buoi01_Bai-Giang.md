# Bài giảng – Buổi 1: Robot là gì?

> **Lý thuyết · 60 phút** · Chặng 1: Đánh thức Bít-Bô · Nhiệm vụ 1: Hộp bí ẩn kêu "bíp bíp" · Tuần 1

Buổi đầu tiên của khóa học. Mục tiêu lớn nhất không phải là nhớ định nghĩa, mà là để các em rời lớp với hai ý: robot là máy biết **nhận lệnh rồi tự làm**, và robot **chỉ làm đúng điều ta bảo**. Từ ý thứ hai sinh ra nấc lập trình đầu tiên: **lệnh phải rõ ràng**.

---

## Kiến thức nền cho giáo viên

### 1. Robot là gì theo cách nhìn kỹ thuật

Trong kỹ thuật, robot thường được mô tả là một cỗ máy thực hiện vòng lặp **Cảm nhận – Suy nghĩ – Hành động** (tiếng Anh: *sense – think – act*):

| Phần | Vai trò | Ví dụ linh kiện | Biệt danh trong khóa học |
| --- | --- | --- | --- |
| Cảm nhận | Thu thông tin từ môi trường | Cảm biến khoảng cách, cảm biến ánh sáng, nút bấm | Giác quan |
| Suy nghĩ | Xử lý thông tin, chạy chương trình, ra quyết định | Bo mạch có vi điều khiển | Bộ não |
| Hành động | Tác động lại môi trường | Động cơ, đèn, còi | Tay chân |

Một cỗ máy có đủ ba phần này và **được lập trình** để tự làm việc thì có thể gọi là robot. Thầy không cần đưa định nghĩa này cho học sinh lớp 1, nhưng cần nắm để phân loại đúng khi các em hỏi.

### 2. Robot khác máy tự động và đồ chơi thế nào

- **Đồ chơi lên dây cót, xe chạy pin không có bo mạch:** chỉ làm một việc cố định, không nhận lệnh mới, không cảm nhận môi trường. Không phải robot.
- **Máy tự động đơn giản** (máy giặt đời cũ, quạt hẹn giờ): làm theo trình tự cài sẵn, có thể có một ít cảm biến. Ranh giới với robot không tuyệt đối; nhiều tài liệu gọi chúng là "máy tự động".
- **Robot hút bụi, xe tự lái, cánh tay robot trong nhà máy:** có cảm biến, có bộ xử lý chạy chương trình, có cơ cấu chuyển động, và có thể được lập trình lại. Đây là robot.

Khi học sinh hỏi "Cái quạt có phải robot không?", câu trả lời trung thực là: *quạt bình thường thì không, vì nó không tự cảm nhận và không tự quyết định; quạt thông minh tự bật khi nóng thì đã giống robot hơn.* Nên khen câu hỏi này vì nó buộc cả lớp phải suy nghĩ về tiêu chí.

### 3. Vì sao robot "chỉ làm đúng điều ta bảo"

Máy tính và bo mạch không hiểu ý định, chỉ thực hiện **lệnh**. Một lệnh muốn máy làm được phải **rõ ràng và không mơ hồ**:

- Có hành động cụ thể: tiến, lùi, rẽ trái, rẽ phải, dừng.
- Có lượng cụ thể khi cần: 3 bước, 2 giây, 90 độ.
- Không phụ thuộc vào cách hiểu: "đi một chút", "đi ra kia", "nhanh lên" đều mơ hồ.

Đây là ý tưởng nền của **thuật toán**: một dãy bước rõ ràng, theo thứ tự, mà người hay máy làm theo đều cho cùng một kết quả. Trong khóa học, đây là **nấc 0 của bậc thang lập trình: Lệnh rõ ràng**.

### 4. Vì sao bắt đầu bằng "thầy-robot"

Trẻ tiểu học học khái niệm trừu tượng tốt nhất khi được **trải nghiệm bằng cơ thể** trước. Khi thầy đóng vai robot và làm sai một cách vui nhộn với lệnh mơ hồ, các em tự phát hiện ra quy tắc. Đây là phương pháp "học lập trình không cần máy" (*unplugged*), được dùng rộng rãi trong giáo dục khoa học máy tính cho trẻ nhỏ.

### 5. Lưu ý với robot mẫu

- Buổi này các em **chỉ nhìn**, chưa chạm. Lý do: tạo sự tò mò và giữ an toàn cho thiết bị trong buổi đầu.
- Kiểm tra pin robot mẫu trước giờ học. Robot hết pin giữa màn mở đầu sẽ làm mất hiệu ứng.
- Chương trình chạy thử nên ngắn (10–15 giây): tiến – quay – kêu – đèn sáng.

---

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Robot là cỗ máy biết nhận lệnh rồi tự làm

**Nói cho trẻ hiểu:** Robot là một cỗ máy. Mình đưa lệnh cho nó, rồi nó tự làm mà không cần ai cầm tay.

**Ví dụ đời sống:**
- Robot hút bụi: bấm nút là nó tự chạy khắp nhà, gặp tường thì quay đầu.
- Cửa tự động ở siêu thị: thấy người đến thì tự mở.
- Xe tự lái: tự đi trên đường mà không cần người cầm vô lăng.

**Lời giảng mẫu:**

> **Thầy:** "Cái ghế có tự đi được không? Không. Cái quạt có tự biết lúc nào nóng để bật lên không? Thường là không, mình phải bấm. Còn robot hút bụi thì sao? Mình bấm một lần, nó tự đi khắp nhà, gặp tường còn biết tránh. Đó là robot: cỗ máy nhận lệnh rồi tự làm."

**Câu hỏi kiểm tra:**
1. Robot hút bụi có phải robot không? *Đáp án mong đợi: Có, vì nó tự chạy và tự tránh tường.*
2. Quả bóng có phải robot không? *Đáp án: Không, vì nó không tự làm gì, phải có người đá.*
3. Robot có cần người cầm tay mới chạy không? *Đáp án: Không, robot tự làm theo lệnh.*

### Khái niệm 2: Robot có Giác quan, Bộ não và Tay chân

Buổi này chỉ **giới thiệu sơ** để các em nhìn robot mẫu có định hướng. Buổi 3 sẽ học kỹ.

**Nói cho trẻ hiểu:** Robot giống một bạn nhỏ. Có "mắt, tai" để biết xung quanh, có "bộ não" để nghĩ, có "tay chân" để làm.

**Lời giảng mẫu:**

> **Thầy:** "Nhìn robot mẫu này. Các Kỹ sư thử đoán: chỗ nào là mắt của nó? Chỗ nào làm nó chạy được? Chỗ nào là bộ não? Hôm nay mình chỉ đoán thôi. Mấy tuần nữa các em sẽ tự lắp từng bộ phận."

**Câu hỏi kiểm tra:**
1. Robot dùng gì để chạy? *Đáp án: Bánh xe, động cơ (chấp nhận "chân", "bánh xe").*
2. Robot có bộ não không? *Đáp án: Có, ở bên trong, gọi là bo mạch.*

### Khái niệm 3: Robot chỉ làm đúng điều mình bảo

**Nói cho trẻ hiểu:** Robot rất ngoan nhưng không đoán được ý mình. Mình bảo gì, nó làm đúng y như vậy, kể cả khi mình bảo sai.

**Ví dụ đời sống:** Bảo em bé 2 tuổi "dọn phòng đi" thì em không biết dọn gì. Bảo "nhặt 3 cái gấu bông bỏ vào hộp" thì em làm được.

**Lời giảng mẫu:**

> **Thầy:** "Lúc nãy bạn Minh bảo thầy-robot 'đi một chút'. Thầy đi có một bước xíu, các em cười. Bạn Lan bảo 'đi tới đó', thầy hỏi 'tới đó là tới đâu?'. Vì robot không đoán được ý mình. Robot chỉ làm đúng lời mình nói."

**Câu hỏi kiểm tra:**
1. Nếu mình bảo robot "đi một chút", robot sẽ làm gì? *Đáp án: Không biết đi bao xa, có thể đi sai.*
2. Robot có tự sửa lệnh sai của mình không? *Đáp án: Không, robot làm đúng lệnh, kể cả lệnh sai.*

### Khái niệm 4: Lệnh rõ ràng (nấc 0 của bậc thang lập trình)

**Nói cho trẻ hiểu:** Lệnh rõ ràng là lệnh nói **làm gì** và **bao nhiêu**. Ai nghe cũng làm giống nhau.

| Lệnh mơ hồ | Lệnh rõ ràng |
| --- | --- |
| Đi một chút | Tiến 3 bước |
| Đi ra kia | Tiến 5 bước rồi rẽ trái |
| Quay lại đi | Quay phải 2 lần |
| Nhanh lên | Tiến 4 bước không dừng |

**Lời giảng mẫu:**

> **Thầy:** "Bí quyết của Kỹ sư là gì? Lệnh phải đếm được. 'Tiến 3 bước' thì ai cũng đi đúng 3 bước. 'Đi một chút' thì mỗi người đi một kiểu. Từ hôm nay, các em chỉ ra lệnh đếm được nhé."

**Câu hỏi kiểm tra:**
1. "Tiến 2 bước" hay "đi tới đó", lệnh nào rõ ràng? *Đáp án: Tiến 2 bước.*
2. Sửa lệnh "đi một chút" cho rõ ràng. *Đáp án: chấp nhận mọi lệnh có số, ví dụ "tiến 1 bước".*
3. Vì sao lệnh rõ ràng quan trọng với robot? *Đáp án: Vì robot không đoán được ý mình.*

---

## Kịch bản giảng theo khung 60 phút

### 0'–5': Tín hiệu từ Bít-Bô

Thầy bước vào, tay ôm chiếc hộp đang rung, phát tiếng "bíp bíp".

> **Thầy:** "Các bạn ơi, sáng nay Căn cứ nhận được chiếc hộp này. Nó cứ rung và kêu bíp bíp từ sáng tới giờ. Thầy chưa dám mở. Trong đó là gì nhỉ? Nó có sống không?"

Kể cốt truyện ngắn (dưới 1 phút):

> **Thầy:** "Xa xa có hành tinh Bít-Bô, nơi toàn robot sinh sống. Một đêm, Bác Bug, con sâu tinh nghịch, lẻn vào và làm cả hành tinh ngủ đông. Bít-Bô đang gửi tín hiệu cầu cứu. Thầy là Chỉ huy Căn cứ. Các em sẽ là Kỹ sư cứu hộ. Mỗi buổi học là một nhiệm vụ đánh thức Bít-Bô."

### 5'–10': Đoán trước, cược Xu

Phát mỗi em 3 Xu giấy. Ghi 3 lựa chọn lên bảng: *Con vật thật · Đồ chơi · Robot*. Các em đặt Xu vào lựa chọn mình đoán.

> **Thầy:** "Đoán sai cũng không sao. Kỹ sư giỏi là người dám đoán rồi kiểm tra."

**Câu chuyển ý:** "Muốn biết đáp án, mình phải mở hộp. Nhưng nhớ: chỉ nhìn, chưa chạm nhé."

### 10'–25': Trò chơi không cần máy (Hoạt động 1–2)

1. **Mở hộp, quan sát robot mẫu (5').** Cho robot chạy chương trình ngắn: tiến, quay, kêu, đèn sáng. Hỏi: "Nó có tự chạy không? Có ai cầm tay nó không?" Công bố đáp án: đây là robot. Ai cược đúng giữ Xu, ai cược sai vẫn được 1 Xu "dám đoán".
2. **So sánh robot với đồ chơi thường (10').** Đặt cạnh robot mẫu một xe đồ chơi đẩy tay. Cả lớp tìm khác biệt.

> **Thầy:** "Xe này mình đẩy mới chạy. Robot thì mình chỉ cần ra lệnh. Vậy robot khác đồ chơi ở chỗ nào?"
> **Đáp án mong đợi:** "Robot tự làm theo lệnh."

**Câu chuyển ý:** "Vậy robot có nghe hiểu mọi lệnh không? Thầy sẽ biến thành robot để các em thử."

### 25'–45': Khám phá và giải thích (Hoạt động 3–4)

3. **Trò "Bạn là robot" vòng 1 (12').** Thầy đội mũ giấy "ROBOT", đứng đầu lớp. Đặt một hộp "kho báu" ở cuối lớp. Các em ra lệnh tự do để đưa thầy-robot tới kho báu.
   - Lệnh "đi một chút": thầy nhích một bước rất nhỏ.
   - Lệnh "đi tới đó": thầy đứng im, nói giọng robot "KHÔNG HIỂU. TỚI ĐÓ LÀ TỚI ĐÂU?".
   - Lệnh "quay lại": thầy quay một vòng tròn rồi đứng đúng chỗ cũ.
   - Lệnh "tiến 3 bước": thầy đi đúng 3 bước, nói "ĐÃ LÀM XONG".
4. **Rút ra quy tắc (8').** Ghi lên bảng hai cột "Lệnh làm robot bối rối" và "Lệnh robot hiểu". Cả lớp xếp các lệnh vừa dùng vào hai cột. Kết luận nấc 0: **Lệnh phải rõ ràng, đếm được.**

> **Thầy:** "Robot không ngốc đâu. Robot chỉ không biết đoán. Người phải nói rõ là Kỹ sư."

**Câu chuyển ý:** "Giờ mình kiểm tra xem Kỹ sư nào đã thành thạo lệnh rõ ràng."

### 45'–55': Đố nhanh, nhận Thẻ bài (Hoạt động 5)

5. Thầy đọc từng lệnh, cả lớp giơ thẻ xanh (rõ ràng) hoặc đỏ (mơ hồ):
   - "Tiến 2 bước" → xanh
   - "Đi tới đó" → đỏ
   - "Rẽ trái" → xanh
   - "Đi nhanh nhanh" → đỏ
   - "Lùi 1 bước" → xanh

Sau đó làm Phiếu bài tập buổi 1. Phát Thẻ tên Kỹ sư cho từng em.

### 55'–60': Cliffhanger

> **Thầy:** "Hôm nay thầy-robot nghe lời các em. Nhưng robot thật trong hộp kia có nghe lệnh của chúng ta không? Buổi sau, mỗi đội sẽ thử."

Cất robot mẫu vào hộp, đóng nắp trước mặt các em.

---

## Học sinh hay hỏi gì và trả lời thế nào

| Câu hỏi | Gợi ý trả lời |
| --- | --- |
| Robot có sống không? | Không. Robot là máy. Nó không ăn, không ngủ, không lớn lên. Nó chạy nhờ điện từ pin. |
| Robot có biết buồn, biết vui không? | Robot không có cảm xúc như người. Nó có thể được lập trình để phát tiếng hoặc bật đèn giống như đang vui, nhưng thật ra chỉ là làm theo lệnh. |
| Điện thoại có phải robot không? | Điện thoại có cảm biến và bộ não, nhưng không tự di chuyển hay làm việc ngoài đời. Người ta thường gọi nó là máy tính nhỏ, không gọi là robot. Câu hỏi rất hay! |
| Robot có thông minh hơn người không? | Robot làm rất nhanh những việc được dạy, như tính toán. Nhưng robot không tự nghĩ ra việc mới. Người dạy robot mới là người thông minh. |
| Robot có làm hại người không? | Robot làm theo lệnh của người. Vì vậy Kỹ sư phải ra lệnh cẩn thận và đúng luật an toàn. |
| Sao robot của thầy không tự đi mà phải có lệnh? | Vì nó cần chương trình, giống bài hát cần lời. Các em sẽ học cách viết chương trình cho robot trong khóa này. |

---

## Hiểu lầm thường gặp

| Hiểu lầm | Cách sửa |
| --- | --- |
| "Robot phải có hình người." | Cho xem ảnh robot hút bụi, cánh tay robot, xe tự lái. Robot có nhiều hình dạng; quan trọng là nó tự làm theo lệnh. |
| "Cái gì chạy bằng pin cũng là robot." | So sánh xe đồ chơi chạy pin (chỉ chạy thẳng, không nhận lệnh) với robot mẫu (nhận lệnh, làm nhiều việc). |
| "Robot hiểu ý mình." | Nhắc lại trò thầy-robot: robot không đoán, chỉ làm đúng lời. |
| "Robot làm sai là do robot hư." | Phần lớn lỗi là do lệnh chưa rõ. Giới thiệu sơ: lỗi đó có tên là Bác Bug, và Kỹ sư sẽ bắt nó. |
| "Lệnh càng ngắn càng tốt." | Lệnh ngắn mà mơ hồ thì vẫn sai. "Tiến 3 bước" dài hơn "đi đi" nhưng rõ hơn. |

---

## Phân hóa

### Lớp 1–3

- Dùng tranh to thay cho chữ khi phân loại robot và không phải robot.
- Trò thầy-robot chơi chậm, mỗi lệnh dừng lại hỏi "Thầy-robot làm đúng chưa?".
- Chỉ dùng 3 loại lệnh: tiến, rẽ trái, rẽ phải.
- Phiếu bài tập: thầy đọc to từng câu; các em chỉ khoanh hoặc tô.

### Lớp 4–5

- Đưa thêm tiêu chí phân loại: "Có cảm nhận không? Có tự quyết định không? Có hành động không?" Các em chấm từng đồ vật theo 3 tiêu chí.
- Thử thách: viết lệnh rõ ràng để thầy-robot **cầm một quyển sách từ bàn A sang bàn B**. Thầy-robot cố ý làm sai ở mỗi chỗ mơ hồ (cầm bằng tay nào, cầm thế nào, đặt ở đâu).
- Thảo luận: "Vì sao người lập trình phải nghĩ trước mọi tình huống?"
- Giới thiệu từ **thuật toán**: dãy bước rõ ràng để làm xong một việc.

---

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Robot | Cỗ máy nhận lệnh rồi tự làm | Máy có cảm biến, bộ xử lý và cơ cấu chấp hành, được lập trình để tự thực hiện công việc |
| Lệnh | Lời bảo robot làm một việc | Một chỉ thị mà máy thực hiện được |
| Lệnh rõ ràng | Lệnh nói làm gì và bao nhiêu | Chỉ thị không mơ hồ, mọi người thực hiện đều cho cùng kết quả |
| Kỹ sư | Người làm ra và dạy robot | Người thiết kế, chế tạo và lập trình máy móc |
| Bác Bug | Con sâu làm robot chạy sai | Lỗi (bug) trong phần cứng hoặc chương trình |

---

## Ghi nhớ cuối bài

Cả lớp đọc to, thầy đọc trước, các em đọc theo:

1. Robot là cỗ máy nhận lệnh rồi tự làm.
2. Robot có Giác quan, Bộ não và Tay chân.
3. Robot chỉ làm đúng điều mình bảo.
4. Lệnh rõ ràng thì nói làm gì và bao nhiêu.
5. Kỹ sư giỏi là người ra lệnh rõ ràng.
