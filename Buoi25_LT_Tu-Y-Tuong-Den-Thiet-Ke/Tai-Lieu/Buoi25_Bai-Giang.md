# Bài giảng – Buổi 25: Từ ý tưởng đến thiết kế

> **Lý thuyết · 60 phút** · Chặng 4: Chế tạo robot của riêng em · Nhiệm vụ 13: Hội đồng phát minh · Tuần 13

Buổi này mở đầu chặng cuối. Các Kỹ sư không học thêm nhiều thứ mới. Các em học cách **ghép những gì đã biết** thành một robot của riêng đội. Có ba ý lớn: ôn lại toàn bộ hệ thống robot, làm quen nút bấm (linh kiện cuối cùng), và học cách chia một việc lớn thành nhiều việc nhỏ. Lớp 4–5 học thêm khái niệm biến.

## Kiến thức nền cho giáo viên

### 1. Mô hình ba khối của mọi robot

Mọi robot trong khóa đều theo một sơ đồ:

```text
ĐẦU VÀO (cảm biến)  →  XỬ LÝ (bo mạch + chương trình)  →  ĐẦU RA (cơ cấu chấp hành)
   nút bấm               bộ não quyết định                    động cơ, đèn LED, còi
   cảm biến siêu âm
   cảm biến dò line
```

- **Cảm biến** đo một thứ gì đó của thế giới bên ngoài và đổi nó thành tín hiệu điện cho bo mạch đọc.
- **Bộ xử lý** (bo mạch) chạy chương trình. Chương trình so sánh tín hiệu với điều kiện rồi quyết định.
- **Cơ cấu chấp hành** biến lệnh điện thành hành động: quay (động cơ), sáng (LED), kêu (còi).

Phần nguồn (pin, dây, công tắc) và phần cơ khí (khung, bánh xe, trục, bánh răng) là "nền móng" giúp ba khối trên hoạt động.

### 2. Mười hai linh kiện của khóa

| Nhóm | Linh kiện | Biệt danh |
| --- | --- | --- |
| Nguồn và đường điện | Pin, dây nối, công tắc | Bình sữa năng lượng, Con đường điện, Người gác cổng |
| Đầu ra | Đèn LED, còi, động cơ | Đom đóm, Chú chim hót, Cơ bắp |
| Cơ khí | Bánh xe – trục – khung, bánh răng – đòn bẩy | Đôi chân, Anh em răng cưa – Bập bênh |
| Xử lý | Bo mạch | Bộ não |
| Đầu vào | Cảm biến siêu âm, cảm biến dò line, nút bấm | Dơi, Mắt mèo, Chuông cửa |

### 3. Nút bấm là một cảm biến

Nút bấm là cảm biến đơn giản nhất. Nó chỉ có **hai trạng thái**: đang bấm hoặc đang nhả. Kỹ thuật gọi đây là **đầu vào số** (digital input): giá trị chỉ là 0 hoặc 1, không có ở giữa. So sánh với cảm biến siêu âm: nó cho ra một con số khoảng cách có thể là 5, 12, 30… gọi là giá trị liên tục.

Trong phần mềm lập trình khối, nút bấm thường dùng theo hai cách:

1. **Sự kiện**: khối dạng "khi nút được bấm". Chương trình đứng chờ, đến khi có người bấm thì chạy các khối bên dưới. Giống chuông cửa: không ai bấm thì không kêu.
2. **Điều kiện**: khối "nút đang được bấm?" đặt trong Nếu – Thì, dùng trong vòng lặp để kiểm tra liên tục.

**Dội phím** (bounce): khi bấm, hai lá kim loại bên trong chạm vào nhau rồi nảy lên vài lần trong vài phần nghìn giây. Bo mạch đọc rất nhanh nên có thể tưởng là bị bấm 2–3 lần. Với trẻ, ta giải thích bằng hình ảnh "nút bấm bị nấc cụt". Cách xử lý ở mức khóa học: sau khi nhận một lần bấm, cho chương trình **chờ một chút** (khoảng 0,2–0,5 giây), và dặn các em "bấm một lần, chờ robot nghe". Tên khối chờ cụ thể tùy phần mềm của trường.

### 4. Phân rã bài toán (nấc 7)

Phân rã là chia một vấn đề lớn thành các phần nhỏ, mỗi phần đủ đơn giản để làm và thử riêng. Đây là kỹ năng cốt lõi của tư duy máy tính. Ở khóa này ta gọi mỗi phần là một **"món nhỏ"**, còn cả chương trình là **"bữa ăn"**.

Ba nguyên tắc khi phân rã:

- Mỗi món nhỏ làm **một việc** có thể kiểm tra được (ví dụ: "xe đi theo vạch" chứ không phải "xe làm mọi thứ").
- Các món nối với nhau theo **thứ tự** (chuỗi lệnh) hoặc theo **điều kiện** (Nếu – Thì).
- **Thử từng món** trước khi ghép. Nếu ghép cả rồi mới thử, khi lỗi sẽ không biết lỗi nằm ở món nào.

### 5. Biến (nấc 6, lớp 4–5)

Biến là một **ô nhớ có tên**, bên trong chứa một giá trị (ở khóa này chỉ dùng số). Bốn thao tác cơ bản:

| Thao tác | Ví dụ khối (mô tả) | Ý nghĩa |
| --- | --- | --- |
| Tạo biến | tạo biến "điểm" | Dán nhãn tên lên một chiếc hộp |
| Đặt giá trị ban đầu | đặt điểm = 0 | Đổ hết đồ trong hộp ra, bắt đầu từ 0 |
| Thay đổi | đổi điểm thêm 1 | Bỏ thêm 1 viên bi vào hộp |
| Đọc và hiển thị | hiện điểm | Mở hộp ra đếm cho mọi người xem |

Lỗi kinh điển: **quên đặt lại về 0** khi bắt đầu, nên điểm của lần chơi trước còn sót lại.

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Robot nào cũng có Giác quan – Bộ não – Tay chân

**Định nghĩa cho trẻ:** Robot nào cũng cần ba phần. Giác quan để biết chuyện gì đang xảy ra. Bộ não để quyết định làm gì. Tay chân để làm việc đó.

**Ví dụ đời sống:** Khi em thấy quả bóng bay tới (mắt – giác quan), não em nghĩ "phải bắt" (bộ não), rồi tay em đưa ra bắt (tay chân). Cửa tự động ở siêu thị: cảm biến thấy người đến, bộ não ra lệnh, động cơ mở cửa.

**Lời giảng mẫu:**

> **Thầy:** "Các Kỹ sư đã đánh thức gần hết Bít-Bô. Giờ Chỉ huy đố nhé: con Dơi là giác quan, bộ não hay tay chân?"
>
> **Thầy:** "Đúng, Dơi là giác quan vì nó giúp robot 'nghe' khoảng cách. Còn Cơ bắp? Đúng, tay chân. Robot nào thiếu một trong ba phần cũng không làm việc được. Không có giác quan thì robot như bị bịt mắt. Không có bộ não thì robot không biết quyết định. Không có tay chân thì robot biết hết mà không làm gì được."

**Câu hỏi kiểm tra:**

1. Đèn LED thuộc phần nào? → Tay chân (đầu ra), vì nó làm việc "sáng lên".
2. Cảm biến dò line thuộc phần nào? → Giác quan, vì nó "nhìn" vạch đen trắng.
3. Nếu robot có động cơ và bo mạch nhưng không có cảm biến thì sao? → Robot vẫn chạy được theo lệnh có sẵn, nhưng không biết xung quanh có gì, ví dụ không tự dừng trước tường.

### Khái niệm 2: Nút bấm – Chuông cửa của robot

**Định nghĩa cho trẻ:** Nút bấm là giác quan đơn giản nhất. Nó chỉ biết hai điều: "đang bị bấm" hoặc "không bị bấm". Giống chuông cửa: có người bấm thì kêu, không ai bấm thì im.

**Ví dụ đời sống:** Nút thang máy, nút bật quạt, nút gọi y tá ở bệnh viện, nút qua đường cho người đi bộ.

**Lời giảng mẫu:**

> **Thầy:** "Dơi cho robot biết xa hay gần, có thể là 5 xăng-ti-mét, 20 xăng-ti-mét. Còn Chuông cửa chỉ có hai câu trả lời: có hoặc không. Bật hoặc tắt. Một hoặc không."
>
> **Thầy:** "Khi viết chương trình, ta có khối 'khi nút được bấm'. Robot sẽ đứng chờ rất kiên nhẫn. Không ai bấm thì robot đứng yên. Có người bấm thì robot bắt đầu làm việc."
>
> **Thầy:** "Nhưng Chuông cửa có một tật: đôi khi bị nấc cụt. Em bấm một lần mà robot tưởng em bấm ba lần. Vì vậy luật của chúng ta là: bấm một lần, chờ robot nghe."

**Câu hỏi kiểm tra:**

1. Nút bấm có mấy trạng thái? → Hai: đang bấm và không bấm.
2. Kể một nút bấm ở nhà em. → Nút nồi cơm điện, nút điều khiển tivi, nút chuông cửa…
3. Vì sao không nên bấm liên tục thật nhanh? → Robot có thể đếm sai hoặc bắt đầu lại nhiều lần; bấm một lần rồi chờ.

### Khái niệm 3: Chia việc lớn thành món nhỏ (nấc 7)

**Định nghĩa cho trẻ:** Một việc lớn rất khó làm một lần. Ta chia nó thành nhiều món nhỏ. Làm xong món này mới sang món kia. Món nào cũng thử riêng trước.

**Ví dụ đời sống:** Nấu một bữa cơm gồm nhiều món: nấu cơm, rán trứng, luộc rau. Mẹ không nấu tất cả cùng lúc trong một cái nồi. Dọn phòng cũng chia: nhặt đồ chơi, xếp sách, quét nhà.

**Lời giảng mẫu:**

> **Thầy:** "Căn cứ cần một robot chở thuốc. Nghe to quá phải không? Chúng ta chia nhỏ ra. Món 1: chờ y tá bấm nút. Món 2: đi theo vạch đen. Món 3: gặp vật cản thì dừng. Món 4: đến nơi thì còi kêu báo."
>
> **Thầy:** "Mỗi món nhỏ chúng ta đều đã học rồi! Món 1 là Chuông cửa. Món 2 là Mắt mèo. Món 3 là Dơi. Món 4 là Chú chim hót. Bây giờ chỉ cần nấu từng món, nếm thử từng món, rồi bày lên mâm."

**Câu hỏi kiểm tra:**

1. Vì sao nên thử từng món riêng? → Nếu lỗi, biết ngay lỗi nằm ở món nào.
2. Chia việc "đánh răng" thành 3 món nhỏ. → Lấy kem lên bàn chải; chải răng; súc miệng.
3. Món "gặp vật cản thì dừng" dùng giác quan nào? → Cảm biến siêu âm (Dơi).

### Khái niệm 4: Biến – chiếc hộp có tên (lớp 4–5)

**Định nghĩa cho trẻ:** Biến là một chiếc hộp có dán tên. Trong hộp có một con số. Robot có thể bỏ thêm vào hộp, đổ hộp về 0, và mở hộp cho mọi người xem.

**Ví dụ đời sống:** Bảng Xu của lớp. Mỗi em có một ô ghi tên và số Xu. Làm tốt thì cộng thêm. Đầu khóa mọi ô đều là 0. Bảng điểm trận bóng đá cũng là biến.

**Lời giảng mẫu:**

> **Thầy:** "Robot canh gác muốn đếm có bao nhiêu người đi qua cổng. Nó cần một chiếc hộp tên là 'số người'. Khi bắt đầu, đổ hộp về 0. Mỗi lần nút được bấm, bỏ thêm 1 viên bi vào hộp. Muốn biết bao nhiêu người, mở hộp ra đếm."
>
> **Thầy:** "Bác Bug rất thích trốn ở chỗ này: Kỹ sư quên đổ hộp về 0. Thế là lần chơi mới vẫn còn bi của lần trước."

**Câu hỏi kiểm tra:**

1. Đầu chương trình phải làm gì với biến điểm? → Đặt điểm bằng 0.
2. Bấm nút 3 lần, mỗi lần cộng 1, điểm bằng bao nhiêu? → 3 (nếu bắt đầu từ 0).
3. Nếu quên đặt về 0 và lần trước điểm là 5, bấm thêm 2 lần thì hiện bao nhiêu? → 7.

```text
(lớp 4–5) khi bắt đầu
  đặt điểm = 0
khi nút được bấm
  đổi điểm thêm 1
  hiện điểm
```

### Khái niệm 5: Bốn vai trò cứu hộ

Các đội chọn một trong bốn vai trò. Mỗi vai trò gợi ý sẵn các món nhỏ để đội bắt đầu:

| Vai trò | Món nhỏ gợi ý | Linh kiện chính |
| --- | --- | --- |
| Chở thuốc | Chờ nút → đi theo vạch → gặp vật thì dừng → còi báo | Nút, dò line, siêu âm, còi |
| Dọn rác | Đi thẳng → gặp vật thì dừng → đẩy vật ra → quay lại | Siêu âm, động cơ, khung có cần gạt |
| Canh gác | Đứng yên → thấy người đến gần thì còi kêu và đèn nháy → đếm số lần (lớp 4–5) | Siêu âm, còi, LED, biến |
| Tìm đường | Đi theo vạch → hết vạch thì dừng → đèn báo đã tới | Dò line, LED |

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

Chiếu hoặc đọc to bức thư từ Căn cứ.

> **Thầy:** "Tin khẩn từ Căn cứ! Bít-Bô đã sáng 12 vùng. Nhưng vùng cuối cùng cần một robot đặc biệt mà Căn cứ chưa từng có. Hội đồng phát minh triệu tập các đội. Mỗi đội phải tự nghĩ ra robot của mình."

### 5' – Đoán trước, cược Xu

> **Thầy:** "Chỉ huy cầm một linh kiện mới trong tay. Nó là giác quan cuối cùng của khóa. Gợi ý: nhà em nào cũng có, khách đến là dùng. Đội nào đoán đúng, cược Xu."

Đáp án: nút bấm (Chuông cửa).

### 15' – Trò chơi không cần máy: "Đố thẻ bài"

1. Chia 4 đội. Thầy giơ biệt danh: Dơi, Mắt mèo, Cơ bắp, Đom đóm, Bộ não, Người gác cổng…
2. Đội giơ tay nhanh nhất nói tên linh kiện và nó là Giác quan, Bộ não hay Tay chân.
3. Câu thưởng: "Kể một Bác Bug hay gặp của linh kiện này."

> **Thầy:** "Mắt mèo! … Đúng, cảm biến dò line, là giác quan. Bác Bug của Mắt mèo là gì? … Đúng rồi, ánh sáng đổi làm nó nhìn sai, nên phải đo lại trước khi chạy."

Cuối trò, thầy dán 12 thẻ lên bảng thành ba cột Giác quan – Bộ não – Tay chân, để nguồn và cơ khí ở hàng dưới làm "nền móng".

### 20' – Khám phá và giải thích

- **6 phút – Gặp Chuông cửa.** Nhìn – Sờ – Đoán: các em bấm thử nút rời, nghe tiếng "tách". Giảng khái niệm 2. Làm trò "nấc cụt": một em làm robot, thầy bấm vào vai một lần, em đó đếm "1, 2, 3" để cả lớp cười và nhớ luật "bấm một lần, chờ robot nghe".
- **8 phút – Nấu cả bữa ăn.** Giảng khái niệm 3. Thầy viết "Robot chở thuốc" lên bảng, cả lớp cùng chia thành 4 món nhỏ. Mỗi món, thầy hỏi "món này dùng nhân vật nào?".
- **6 phút – Lớp 4–5: chiếc hộp có tên.** Giảng khái niệm 4 bằng một hộp thật và bi thật. Lớp 1–3: thay bằng trò "đếm Xu đội" do thầy giữ bảng.

### 10' – Đố nhanh, nhận Thẻ bài

- Phát Phiếu bài tập buổi 25.
- Giới thiệu 4 vai trò cứu hộ (bảng ở khái niệm 5). Mỗi đội thảo luận 3 phút, chọn 1 vai trò.
- Đội nào nêu đủ món nhỏ cho vai trò của mình nhận Thẻ bài "Chuông cửa".

### 5' – Cliffhanger

> **Thầy:** "Hội đồng phát minh sẽ họp buổi tới. Đội nào mang đến bản thiết kế rõ ràng nhất sẽ được đóng dấu 'Đã cấp bằng sáng chế'. Về nhà, các Kỹ sư vẽ thử robot của đội mình nhé."

## Học sinh hay hỏi gì và trả lời thế nào

**"Thầy ơi, robot của con có thể làm tất cả các việc được không?"**
Được, nhưng làm từng món một. Kỹ sư giỏi làm cho một món chạy thật tốt trước, rồi mới thêm món tiếp theo. Robot nhiều việc mà việc nào cũng hỏng thì không cứu được Bít-Bô.

**"Sao nút bấm lại là giác quan? Nó có mắt đâu?"**
Giác quan là thứ giúp robot biết chuyện gì đang xảy ra. Nút bấm giúp robot biết "có người chạm vào tôi". Giống làn da của em biết khi có ai chạm vào tay.

**"Nếu đội con chọn vai trò khác bốn vai trò này được không?"**
Được, nếu đội nói rõ được robot làm những món nhỏ nào và dùng linh kiện gì. Chỉ huy sẽ duyệt ý tưởng ở buổi sau.

**"Biến với bảng Xu khác gì nhau?"**
Bảng Xu là biến của lớp mình, do thầy ghi bằng tay. Biến trong robot là bảng Xu do robot tự ghi.

**"Bấm nút nhiều lần thì robot có hỏng không?"**
Không hỏng, nhưng robot có thể hiểu nhầm và làm lại từ đầu nhiều lần. Bấm một lần, chờ robot nghe.

## Hiểu lầm thường gặp

- **"Chương trình càng dài càng giỏi."** Thật ra chương trình tốt là chương trình chia rõ món nhỏ và mỗi món chạy đúng. Nhắc lại giải "Kỹ sư lười thông minh" ở buổi 20.
- **"Ghép hết rồi mới chạy cho nhanh."** Ghép hết rồi chạy, khi hỏng sẽ mất rất lâu để tìm Bác Bug. Thử từng món nhanh hơn.
- **"Nút bấm và công tắc là một."** Công tắc giữ nguyên trạng thái bật hoặc tắt (như công tắc đèn). Nút bấm chỉ "bật" khi đang ấn, nhả tay ra là thôi (như chuông cửa).
- **"Biến là một khối lệnh làm robot chạy."** Biến không làm robot chạy. Biến chỉ nhớ một con số cho robot dùng.
- **"Robot tự biết phải làm gì."** Robot chỉ làm đúng điều chương trình bảo, giống bài học buổi 1.

## Phân hóa

**Lớp 1–3**

- Robot của đội dùng tối đa 2 giác quan (ví dụ nút bấm + Dơi).
- Chia việc thành 3 món nhỏ, thầy gợi ý sẵn bằng thẻ hình.
- Bỏ phần biến; thay bằng việc đếm số lần bấm bằng tay trên phiếu.
- Phiếu bài tập dùng hình, khoanh và nối nhiều hơn viết.

**Lớp 4–5**

- Robot có thể dùng 2–3 giác quan và một biến.
- Tự chia việc thành 4–5 món nhỏ, ghi rõ món nào dùng Nếu – Thì, món nào dùng vòng lặp.
- Thử thách: viết trên giấy chương trình đếm số lần bấm nút và hiển thị, nhớ đặt về 0.
- Mỗi đội tự đặt **một yêu cầu** cho robot (ví dụ: "dừng cách vật ít nhất 10 cm").

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Cảm biến | Giác quan của robot | Linh kiện đo đại lượng vật lý và chuyển thành tín hiệu điện |
| Bộ xử lý / bo mạch | Bộ não | Mạch điện tử chạy chương trình, đọc đầu vào và điều khiển đầu ra |
| Cơ cấu chấp hành | Tay chân | Linh kiện biến tín hiệu điện thành chuyển động, ánh sáng, âm thanh |
| Nút bấm | Chuông cửa | Công tắc nhấn nhả, đầu vào số chỉ có hai trạng thái |
| Sự kiện | Lúc có chuyện xảy ra | Tín hiệu kích hoạt một đoạn chương trình, ví dụ "khi nút được bấm" |
| Dội phím | Nút bị nấc cụt | Tiếp điểm nảy nhiều lần khi nhấn, làm bo mạch đọc thành nhiều lần bấm |
| Phân rã | Chia việc lớn thành món nhỏ | Tách bài toán thành các bài toán con độc lập, dễ giải và dễ kiểm thử |
| Biến (lớp 4–5) | Chiếc hộp có tên chứa số | Vùng nhớ có tên lưu một giá trị có thể thay đổi khi chương trình chạy |

## Ghi nhớ cuối bài

1. Robot nào cũng có Giác quan – Bộ não – Tay chân.
2. Nút bấm là giác quan đơn giản nhất: chỉ có bấm hoặc không bấm.
3. Bấm một lần, chờ robot nghe.
4. Việc lớn thì chia thành món nhỏ, và thử từng món trước khi ghép.
5. Biến là chiếc hộp có tên; nhớ đổ hộp về 0 khi bắt đầu (lớp 4–5).
6. Đội em đã chọn vai trò cứu hộ; buổi sau sẽ vẽ thiết kế.
