# Bài giảng – Buổi 29: Giới thiệu robot của đội

> **Lý thuyết · 60 phút** · Chặng 4: Chế tạo robot của riêng em · Nhiệm vụ 15: Thanh tra Bug · Tuần 15

Làm ra robot mới là một nửa công việc. Nửa còn lại là **giải thích được** robot làm gì và vì sao nó làm như vậy. Buổi này dạy kỹ năng thuyết trình kỹ thuật: nói theo khung 4 câu, giải thích chương trình từng khối một, chia phần nói trong đội, và cách góp ý cho phần nói của đội bạn. Đây là chuẩn bị trực tiếp cho Ngày hội.

## Kiến thức nền cho giáo viên

### 1. Thuyết trình kỹ thuật khác kể chuyện thế nào

Thuyết trình kỹ thuật có mục tiêu giúp người nghe **hiểu cách sản phẩm hoạt động**. Nó cần ba thứ:

- **Cấu trúc cố định**: người nghe biết sắp nghe gì, người nói không bị quên.
- **Chỉ vào vật thật**: chỉ vào robot, chỉ vào từng khối lệnh trên màn hình. Lời nói kèm cử chỉ dễ hiểu hơn nhiều.
- **Nói nguyên nhân**: không chỉ "robot dừng", mà "robot dừng vì Dơi thấy hộp gần hơn 15 xăng-ti-mét".

### 2. Khung giới thiệu 4 câu

| Câu | Nội dung | Ví dụ |
| --- | --- | --- |
| 1. Tên | Robot tên gì | "Robot của đội Sao Xanh tên là Tí Thuốc." |
| 2. Nhiệm vụ | Robot giúp ai, làm việc gì | "Tí Thuốc chở hộp thuốc từ kho đến trạm y tế." |
| 3. Cách chạy | Chương trình chạy thế nào, chỉ từng khối | "Đầu tiên y tá bấm nút. Robot kêu bíp. Rồi Mắt mèo nhìn vạch đen để đi đúng đường. Nếu Dơi thấy vật cản gần thì robot dừng." |
| 4. Bác Bug | Đội đã bắt con Bug nào, sửa thế nào | "Lúc đầu robot không dừng trước vật. Đội phát hiện khối kiểm tra Dơi nằm sau, nên đưa nó lên trước." |

Câu 4 rất quan trọng về mặt giáo dục: nó biến lỗi thành **thành tích**. Trẻ học rằng kể về lỗi đã sửa là điều đáng tự hào.

### 3. Giải thích chương trình từng khối

Kỹ thuật "đọc to chương trình" (trong nghề gọi là duyệt mã): đi từ khối trên cùng xuống, mỗi khối nói một câu theo mẫu **"Khối này bảo robot … vì …"**. Với khối điều kiện, nói cả hai nhánh: "Nếu … thì robot …, còn không thì robot …". Với vòng lặp, nói "Robot làm đi làm lại việc này mãi".

Người nghe là phụ huynh, không biết lập trình. Vì vậy dùng **biệt danh nhân vật** (Dơi, Mắt mèo) kèm tên thật lần đầu.

### 4. Kỹ năng nói trước đám đông cho trẻ

Ba điều đơn giản, dạy bằng làm mẫu:

- **To – Chậm – Nhìn**: nói đủ to cho bạn ở cuối lớp nghe; nói chậm; nhìn người nghe chứ không nhìn sàn.
- **Đứng cạnh robot**, không đứng chắn trước robot.
- **Chuyền lượt rõ ràng**: nói xong thì quay sang bạn và nói "Bạn … sẽ kể tiếp".

Với trẻ nhút nhát: cho phương án **"robot kể thay em"**. Em bấm nút, robot nháy đèn và kêu còi theo từng bước, em chỉ cần chỉ tay và nói một từ. Hoặc em giữ vai Người cầm bảng, giơ bảng có ghi từng câu. Mục tiêu là em nào cũng tham gia, không ép nói dài.

### 5. Góp ý cho phần trình bày

Vẫn dùng mẫu "Một điều hay – Một điều nên thử", nhưng tập trung vào cách nói: có đủ 4 câu không, có chỉ vào khối không, có đủ to không.

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Vì sao kỹ sư phải giới thiệu robot

**Định nghĩa cho trẻ:** Kỹ sư làm ra robot xong phải kể cho người khác hiểu robot làm gì. Nếu không ai hiểu, robot hay đến mấy cũng không ai biết cách dùng.

**Ví dụ đời sống:** Người bán hàng giới thiệu đồ chơi mới. Hướng dẫn sử dụng nồi cơm điện. Cô giáo giải thích bài toán từng bước.

**Lời giảng mẫu:**

> **Thầy:** "Tuần sau, bố mẹ các Kỹ sư sẽ đến Căn cứ. Bố mẹ chưa học Dơi, chưa học Mắt mèo. Nếu robot chạy mà không ai giải thích, bố mẹ chỉ thấy 'xe chạy rồi dừng'. Nếu các em giải thích, bố mẹ sẽ hiểu: 'À, con mình đã dạy robot biết nhìn đường!'"

**Câu hỏi kiểm tra:**

1. Người nghe ở Ngày hội là ai? → Bố mẹ, các bạn, thầy cô.
2. Vì sao phải dùng biệt danh kèm tên thật? → Để người chưa học cũng hiểu và nhớ.

### Khái niệm 2: Khung giới thiệu 4 câu

**Định nghĩa cho trẻ:** Bài giới thiệu có 4 câu, nói theo thứ tự: Tên – Nhiệm vụ – Cách chạy – Bác Bug.

**Ví dụ đời sống:** Giới thiệu bản thân cũng có khung: tên em, em học lớp mấy, em thích gì.

**Lời giảng mẫu:**

> **Thầy:** "Bốn ngón tay, bốn câu. Ngón 1: Tên robot. Ngón 2: Robot làm gì. Ngón 3: Robot chạy thế nào. Ngón 4: Đội đã bắt Bác Bug nào. Quên câu nào thì nhìn tay mình."
>
> **Thầy:** "Câu số 4 là câu Chỉ huy thích nhất. Kể về Bác Bug đã bắt không phải là xấu hổ. Đó là bằng chứng các em là kỹ sư thật."

**Câu hỏi kiểm tra:**

1. Câu thứ 3 nói gì? → Robot chạy thế nào, chỉ vào từng khối.
2. Vì sao nên kể về Bác Bug? → Vì đó là điều đội đã học và vượt qua; kỹ sư thật đều sửa lỗi.
3. Sắp xếp lại: "Robot dừng khi gặp vật / Robot tên Bi / Robot dọn rác / Đội sửa lỗi Dơi chĩa xuống sàn". → Tên Bi – Dọn rác – Dừng khi gặp vật – Sửa lỗi Dơi.

### Khái niệm 3: Giải thích chương trình từng khối

**Định nghĩa cho trẻ:** Khi giải thích chương trình, em chỉ vào từng khối từ trên xuống. Mỗi khối nói một câu: "Khối này bảo robot … vì …".

**Ví dụ đời sống:** Đọc công thức nấu ăn từng bước. Chỉ đường cho bạn: "Đi thẳng, đến ngã tư rẽ trái, vì nhà tớ ở bên trái".

**Lời giảng mẫu:** Thầy chiếu một chương trình mẫu và làm mẫu cách nói.

```text
khi nút được bấm
  phát tiếng bíp
  lặp mãi
    nếu khoảng cách < 15 cm thì
      dừng
    không thì
      tiến
```

> **Thầy:** "Khối đầu bảo robot chờ, vì robot chỉ được đi khi y tá bấm nút. Khối thứ hai bảo robot kêu bíp, để y tá biết robot đã nghe. Khối 'lặp mãi' bảo robot làm đi làm lại phần bên trong không ngừng, vì đường đi có thể có vật cản bất cứ lúc nào. Bên trong: nếu Dơi thấy vật gần hơn 15 xăng-ti-mét thì robot dừng, để không đâm vào vật. Còn không thì robot tiến."

**Câu hỏi kiểm tra:**

1. Mẫu câu giải thích một khối là gì? → "Khối này bảo robot … vì …".
2. Với khối Nếu – Thì, phải nói mấy trường hợp? → Hai: khi đúng và khi không đúng.
3. Vì sao chọn con số 15 xăng-ti-mét? → Đội thử nhiều lần, thấy con số đó vừa đủ để dừng mà không chạm (câu trả lời theo kết quả thử của đội).

### Khái niệm 4: To – Chậm – Nhìn

**Định nghĩa cho trẻ:** Khi nói trước mọi người: nói To, nói Chậm, Nhìn vào người nghe.

**Ví dụ đời sống:** Bạn lớp trưởng đọc thông báo; người dẫn chương trình trên tivi.

**Lời giảng mẫu:**

> **Thầy:** "Chỉ huy sẽ giới thiệu một robot hai lần. Các em xem lần nào hay hơn nhé."

Thầy diễn lần "dở": nói lí nhí, nhanh, nhìn xuống sàn, đứng che robot, không chỉ vào khối. Rồi lần "hay": đứng cạnh robot, nói to rõ, chỉ từng khối, nhìn cả lớp.

> **Thầy:** "Lần hai hay hơn ở điểm nào? … Đúng: to hơn, chậm hơn, nhìn mọi người, chỉ vào robot."

**Câu hỏi kiểm tra:**

1. Ba bí quyết khi nói là gì? → To – Chậm – Nhìn.
2. Nên đứng ở đâu khi giới thiệu? → Đứng cạnh robot, không che robot.

### Khái niệm 5: Chia phần nói trong đội và "robot kể thay em"

**Định nghĩa cho trẻ:** Mỗi bạn trong đội nói ít nhất một câu. Bạn nào ngại nói có thể để robot "kể" bằng đèn và còi, còn em chỉ tay hoặc giơ bảng.

**Lời giảng mẫu:**

> **Thầy:** "Đội 4 bạn, 4 câu: mỗi bạn một câu, thật vừa! Nói xong câu của mình thì quay sang bạn: 'Bạn Minh sẽ kể tiếp'. Bạn nào hồi hộp thì làm Người bấm nút: bạn bấm, robot nháy đèn, bạn nói 'Đây là món số 1'. Vậy là bạn đã giới thiệu rồi."

**Câu hỏi kiểm tra:**

1. Nói xong phần mình thì làm gì? → Chuyền lượt cho bạn tiếp theo.
2. Bạn ngại nói có thể tham gia bằng cách nào? → Bấm nút cho robot kể thay, giơ bảng, chỉ vào robot.

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

> **Thầy:** "Thư từ Căn cứ: 'Ngày hội Giải cứu Bít-Bô sẽ có khách quý đến thăm. Khách quý chưa từng thấy robot của các Kỹ sư. Mỗi đội có đúng 2 phút để giới thiệu.' Chỉ 2 phút thôi! Phải nói gì cho đủ?"

### 5' – Đoán trước, cược Xu

Thầy diễn hai lần giới thiệu (dở và hay) như khái niệm 4.

> **Thầy:** "Đội nào tìm ra nhiều điểm khác nhau nhất giữa hai lần? Cược Xu: 2, 4 hay 6 điểm?"

Danh sách khác biệt: âm lượng, tốc độ, ánh mắt, vị trí đứng, chỉ vào khối, có nói nguyên nhân, có kể Bác Bug.

### 15' – Trò chơi không cần máy

**Trò 1 – Bốn ngón tay (7 phút).** Thầy nói tên một đồ vật quen thuộc (quạt điện, đèn đường, máy giặt). Cả lớp giơ 4 ngón tay và từng em nói một câu theo khung: Tên – Nhiệm vụ – Cách chạy – (câu 4 đổi thành "Hỏng thì sửa thế nào"). Ví dụ đèn đường: "Đây là đèn đường. Đèn giúp người đi đêm. Trời tối thì cảm biến ánh sáng bật đèn. Đèn không sáng thì kiểm tra bóng đèn."

**Trò 2 – Phóng viên và Kỹ sư (8 phút).** Một em làm phóng viên cầm micro giả, hỏi "Khối này làm gì?". Em làm kỹ sư chỉ vào một khối trên thẻ in và trả lời theo mẫu "Khối này bảo robot … vì …". Đổi vai.

### 20' – Khám phá và giải thích

- **5 phút:** Giảng khái niệm 1 và 2, dán bảng khung 4 câu lên tường.
- **7 phút:** Giảng khái niệm 3. Mỗi đội nhận ảnh in chương trình của đội mình, dùng bút đánh số từng khối và viết một câu giải thích bên cạnh (lớp 1–3 nói miệng, trợ giảng ghi).
- **8 phút:** Giảng khái niệm 4 và 5. Mỗi đội chia câu cho từng bạn, ghi tên lên phiếu. Chọn Người bấm nút, Người chỉ màn hình.

### 10' – Đố nhanh, nhận Thẻ bài

- Tập nói theo cặp đội: đội A giới thiệu 2 phút, đội B nghe và góp ý "Một điều hay – Một điều nên thử", rồi đổi lại.
- Làm Phiếu bài tập buổi 29.
- Đội giới thiệu đủ 4 câu, đúng giờ nhận Thẻ bài "Người dẫn chuyện".

### 5' – Cliffhanger

> **Thầy:** "Phụ huynh sẽ đến Căn cứ. Robot của mình đã sẵn sàng chưa? Buổi sau là buổi cuối trong Xưởng: hoàn thiện robot, Thanh tra lần 2, và tổng duyệt như Ngày hội thật."

## Học sinh hay hỏi gì và trả lời thế nào

**"Nếu đang giới thiệu mà robot không chạy thì sao ạ?"**
Bình tĩnh. Nói: "Bác Bug vừa xuất hiện! Đội mình sẽ bắt nó ngay." Rồi kiểm tra theo danh sách: pin, công tắc, dây. Người xem rất thích xem kỹ sư sửa lỗi. Buổi sau đội sẽ tập tình huống này.

**"Con quên mất câu của con thì sao?"**
Nhìn tay: ngón số mấy là câu số mấy. Hoặc nhìn bảng khung 4 câu. Bạn trong đội có thể nhắc nhỏ.

**"Có cần nói hết tất cả các khối không ạ?"**
Trong 2 phút, chọn những khối quan trọng nhất: khối bắt đầu, khối cảm biến (Nếu – Thì), khối lặp. Các khối giống nhau thì nói gộp.

**"Kể chuyện robot bị lỗi thì bố mẹ có nghĩ đội con kém không?"**
Không. Kỹ sư thật luôn kể họ đã sửa những lỗi gì. Bố mẹ sẽ thấy các em biết tìm và sửa lỗi, đó là điều rất giỏi.

**"Con nói nhỏ lắm, con ngại."**
Em có thể làm Người bấm nút để robot kể thay em, hoặc giơ bảng. Nói một câu thôi cũng được. Chỉ huy sẽ đứng gần em.

## Hiểu lầm thường gặp

- **"Nói càng dài càng giỏi."** Trong 2 phút, nói đủ 4 câu, rõ ràng mới là giỏi.
- **"Chỉ cần cho robot chạy, không cần nói."** Người xem không biết robot đang dùng giác quan nào, vì sao dừng.
- **"Giải thích chương trình là đọc tên khối."** Đọc "lặp mãi, nếu, dừng" là chưa đủ; phải nói **vì sao** robot cần khối đó.
- **"Phải giấu lỗi đi."** Kể lỗi đã sửa là phần đáng tự hào nhất.
- **"Bạn nói giỏi nhất nói hết."** Mỗi bạn đều có phần; đội là một khối thống nhất.

## Phân hóa

**Lớp 1–3**

- Mỗi câu trong khung chỉ cần 1 câu ngắn.
- Câu 3 nói 2–3 khối chính bằng biệt danh nhân vật.
- Dùng thẻ hình gợi nhớ: hình cái tên, hình nhiệm vụ, hình Dơi/Mắt mèo, hình Bác Bug.
- Cho phép "robot kể thay em" rộng rãi.

**Lớp 4–5**

- Câu 3 giải thích đầy đủ các khối, nói rõ cả hai nhánh của Nếu – Thì.
- Giải thích lý do chọn con số (ví dụ 15 cm, 0,5 giây) dựa trên kết quả thử.
- Chuẩn bị trả lời 1 câu hỏi của khán giả.
- Đội nào có biến: giải thích biến dùng để đếm gì và vì sao đặt về 0.

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Thuyết trình kỹ thuật | Giới thiệu robot cho người khác hiểu | Trình bày cách sản phẩm hoạt động, có cấu trúc và minh chứng |
| Khung 4 câu | Tên – Nhiệm vụ – Cách chạy – Bác Bug | Cấu trúc cố định giúp người nói không quên và người nghe dễ theo dõi |
| Giải thích từng khối | Chỉ từng khối và nói "khối này bảo robot … vì …" | Duyệt chương trình tuần tự, nêu chức năng và lý do của từng lệnh |
| Nhánh điều kiện | Hai đường của Nếu – Thì | Hai khả năng thực thi tùy điều kiện đúng hay sai |
| Khán giả | Người nghe | Đối tượng của bài trình bày; quyết định cách dùng từ |
| Chuyền lượt | Đưa lời cho bạn tiếp theo | Chuyển tiếp giữa các người trình bày trong nhóm |

## Ghi nhớ cuối bài

1. Giới thiệu robot theo 4 câu: Tên – Nhiệm vụ – Cách chạy – Bác Bug.
2. Giải thích chương trình bằng câu "Khối này bảo robot … vì …".
3. Khối Nếu – Thì phải nói cả hai trường hợp.
4. Nói To – Chậm – Nhìn, đứng cạnh robot.
5. Mỗi bạn trong đội đều có phần; ngại nói thì để robot kể thay em.
6. Kể về Bác Bug đã bắt là điều đáng tự hào.
