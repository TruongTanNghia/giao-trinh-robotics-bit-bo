# Bài giảng – Buổi 27: Quy trình kỹ sư và Thanh tra Bug

> **Lý thuyết · 60 phút** · Chặng 4: Chế tạo robot của riêng em · Nhiệm vụ 14: Xưởng chế tạo · Tuần 14

Các đội đã có bản thiết kế và món nhỏ đầu tiên. Buổi này dạy **cách làm việc** của kỹ sư thật: đi theo một vòng quy trình, kiểm tra có hệ thống bằng danh sách, và góp ý cho đội bạn một cách lịch sự. Buổi thực hành sau, các đội sẽ làm **Thanh tra Bug** cho nhau.

## Kiến thức nền cho giáo viên

### 1. Quy trình thiết kế kỹ thuật

Quy trình thiết kế kỹ thuật (engineering design process) là chuỗi bước kỹ sư lặp đi lặp lại để giải một vấn đề. Phiên bản dùng trong khóa có 6 bước, nối thành vòng tròn:

```text
1. Xác định vấn đề  →  2. Nghĩ ý tưởng  →  3. Thiết kế
        ↑                                      ↓
6. Cải tiến  ←  5. Thử  ←  4. Chế tạo
```

| Bước | Câu hỏi kỹ sư tự hỏi | Đội đã làm ở buổi |
| --- | --- | --- |
| Xác định vấn đề | Ai cần giúp? Cần giải quyết chuyện gì? Yêu cầu và ràng buộc là gì? | 25 |
| Nghĩ ý tưởng | Có những cách nào? Chọn cách nào? | 25 |
| Thiết kế | Vẽ ra, liệt kê linh kiện, chia món nhỏ | 26 |
| Chế tạo | Lắp và lập trình từng món | 26, 28 |
| Thử | Robot có đạt yêu cầu không? | 28, 30 |
| Cải tiến | Sửa chỗ chưa đạt, rồi thử lại | 28, 30 |

Điểm mấu chốt: đây là **vòng lặp**, không phải đường thẳng. Thử thấy chưa đạt thì quay về chế tạo hoặc thậm chí thiết kế lại. Lặp nhiều vòng là dấu hiệu làm việc đúng, không phải dấu hiệu thất bại. Ở lớp 1–3, có thể rút gọn thành 4 bước: Thiết kế – Chế tạo – Thử – Sửa.

**Yêu cầu** là điều robot phải làm được (ví dụ "chở hộp thuốc từ A đến B"). **Ràng buộc** là giới hạn phải tuân theo (ví dụ "chỉ dùng linh kiện trong kit", "làm xong trong 3 buổi").

### 2. Kiểm thử có hệ thống

Kiểm thử có hệ thống nghĩa là kiểm tra **theo thứ tự cố định**, không đoán mò. Khóa học đã dạy thứ tự này từ buổi 6 và mở rộng dần:

```text
Pin → Công tắc → Dây → Cổng cắm → Chương trình
(từ phần cứng, gần nguồn điện nhất, đến phần mềm)
```

Lý do đi từ phần cứng: lỗi phần cứng dễ thấy, kiểm tra nhanh, và nếu phần cứng hỏng thì chương trình đúng cũng không chạy.

Hai kỹ thuật kiểm thử phù hợp với trẻ:

- **Thử từng món riêng** (kiểm thử đơn vị): tạm bỏ các món khác, chỉ chạy một món.
- **Đổi một thứ mỗi lần**: mỗi lần sửa chỉ thay một chỗ, rồi chạy lại. Nếu đổi ba thứ cùng lúc, robot chạy được cũng không biết nhờ thứ nào.

### 3. Danh sách kiểm tra (checklist)

Danh sách kiểm tra giúp không bỏ sót bước, kể cả khi đang vội hay hồi hộp. Phi công, bác sĩ phẫu thuật đều dùng checklist. Phiếu Thanh tra Bug của khóa:

| Mục | Kiểm tra | Cách kiểm tra |
| --- | --- | --- |
| Pin | Pin còn đầy, lắp đúng cực | Nhìn đèn nguồn; "đỏ gặp đỏ, xanh gặp xanh" |
| Công tắc | Đang bật | Nhìn vị trí công tắc |
| Dây | Không lỏng, không đứt | Lắc nhẹ từng dây |
| Cổng cắm | Cắm đúng cổng, cắm chặt | So với bản vẽ, cầm đầu cắm ấn nhẹ |
| Chương trình | Đủ khối, đúng thứ tự, đúng con số | Đọc to từng khối |

### 4. Kiểm tra chéo và góp ý xây dựng

**Kiểm tra chéo** (peer review): một người khác kiểm tra sản phẩm của mình. Người làm ra sản phẩm thường "quen mắt" nên không thấy lỗi. Người ngoài nhìn mới sẽ thấy.

**Góp ý xây dựng** cần ba điều: cụ thể (nói rõ chỗ nào), tôn trọng (nói về robot, không chê người), và có hướng sửa. Khóa dùng mẫu câu **"Một điều hay – Một điều nên thử"**. Câu khen phải cụ thể ("bánh xe rất chặt") chứ không chung chung ("đẹp quá"). Câu góp ý bắt đầu bằng "Đội thử…" thay vì "Đội sai rồi".

Người nhận góp ý được dạy câu đáp: **"Cảm ơn, đội mình sẽ thử."** Đội có quyền quyết định có làm theo hay không.

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Vòng quy trình kỹ sư

**Định nghĩa cho trẻ:** Kỹ sư làm việc theo một vòng tròn: Thiết kế – Chế tạo – Thử – Sửa, rồi lại Thử. Đi hết vòng mà robot chưa đạt thì đi thêm vòng nữa.

**Ví dụ đời sống:** Gấp máy bay giấy (buổi 13): gấp, phóng, thấy bay chúi xuống, sửa cánh, phóng lại. Tập đi xe đạp cũng vậy: thử, ngã, chỉnh tư thế, thử lại.

**Lời giảng mẫu:**

> **Thầy:** "Các Kỹ sư nghĩ người làm ra máy bay thật có làm một lần là bay được không? … Không. Họ làm, thử, sửa hàng trăm lần. Mỗi vòng, máy bay tốt hơn một chút."
>
> **Thầy:** "Đội mình đang ở đâu trên vòng tròn này? Đội Chở thuốc đã thiết kế xong, đang chế tạo. Lát nữa sẽ đến bước Thử. Nếu thử chưa đạt thì sao? … Đúng, quay về Sửa. Quay về không phải là thua. Quay về là đang làm đúng cách kỹ sư."

**Câu hỏi kiểm tra:**

1. Sau bước Thử, nếu robot chưa đạt thì làm gì? → Sửa, rồi thử lại.
2. Bước nào phải làm trước bước Chế tạo? → Thiết kế.
3. Đi vòng thứ ba có phải là đội kém không? → Không, đó là cách kỹ sư làm việc; mỗi vòng robot tốt hơn.

### Khái niệm 2: Yêu cầu và ràng buộc

**Định nghĩa cho trẻ:** Yêu cầu là việc robot **phải làm được**. Ràng buộc là **luật** mà đội phải theo khi làm robot.

**Ví dụ đời sống:** Mẹ nhờ em "mua một ổ bánh mì" (yêu cầu), "chỉ được tiêu 10 nghìn và về trước 7 giờ" (ràng buộc).

**Lời giảng mẫu:**

> **Thầy:** "Yêu cầu của robot Chở thuốc: đưa hộp thuốc đến trạm y tế và còi kêu khi tới. Ràng buộc: chỉ dùng linh kiện trong hộp kit, robot vừa một ô thảm, làm xong trong ba buổi."
>
> **Thầy:** "Một yêu cầu tốt phải kiểm tra được. 'Robot chạy hay' không kiểm tra được. 'Robot dừng trước hộp, không chạm hộp' thì kiểm tra được: chạm hay không chạm, ai nhìn cũng biết."

**Câu hỏi kiểm tra:**

1. "Chỉ dùng linh kiện trong kit" là yêu cầu hay ràng buộc? → Ràng buộc.
2. Câu nào kiểm tra được: "robot thông minh" hay "robot đi hết vạch đen không bị lạc"? → Câu thứ hai.

### Khái niệm 3: Kiểm tra theo danh sách

**Định nghĩa cho trẻ:** Khi robot không chạy, ta không đoán mò. Ta kiểm tra theo một danh sách có thứ tự: Pin – Công tắc – Dây – Cổng cắm – Chương trình. Xong mục nào đánh dấu mục đó.

**Ví dụ đời sống:** Trước khi đi học, em kiểm tra: sách vở, bút, nước, mũ. Phi công trước khi cất cánh cũng đọc danh sách kiểm tra.

**Lời giảng mẫu:**

> **Thầy:** "Bác Bug rất thích trốn ở những chỗ ta quên nhìn. Danh sách kiểm tra là đèn pin soi từng chỗ một. Chúng ta bắt đầu từ chỗ gần Bình sữa năng lượng nhất: pin. Rồi Người gác cổng. Rồi Con đường điện. Rồi cổng cắm vào Bộ não. Cuối cùng mới đọc chương trình."
>
> **Thầy:** "Và một luật nữa: mỗi lần chỉ sửa một thứ. Sửa xong chạy thử ngay."

**Câu hỏi kiểm tra:**

1. Mục đầu tiên trong danh sách là gì? → Pin.
2. Vì sao mỗi lần chỉ sửa một thứ? → Để biết chính xác thứ nào làm robot chạy được.
3. Kiểm tra dây bằng cách nào? → Lắc nhẹ từng dây.

### Khái niệm 4: Thanh tra Bug và góp ý lịch sự

**Định nghĩa cho trẻ:** Thanh tra Bug là đội bạn sang kiểm tra robot của đội mình bằng phiếu. Mắt người khác hay thấy Bác Bug mà mình không thấy. Khi góp ý, ta nói "Một điều hay" trước, rồi "Một điều nên thử".

**Ví dụ đời sống:** Viết bài xong, nhờ bạn đọc giúp xem có sai chính tả không. Bạn thấy lỗi nhanh hơn mình vì mình đã quen câu chữ.

**Lời giảng mẫu:**

> **Thầy:** "Khi làm Thanh tra, các em nói về robot, không nói về bạn. Không nói 'Đội cậu làm sai rồi'. Hãy nói 'Một điều hay: bánh xe rất chặt. Một điều nên thử: đội thử đặt Dơi cao hơn một chút xem sao'."
>
> **Thầy:** "Khi nhận góp ý, chúng ta nói: 'Cảm ơn, đội mình sẽ thử.' Thử rồi thấy không hợp thì thôi. Đội mình là người quyết định cuối cùng."

**Câu hỏi kiểm tra:**

1. "Robot của cậu xấu quá" có phải góp ý tốt không? → Không; không cụ thể, không có hướng sửa, làm bạn buồn.
2. Nhận góp ý xong thì nói gì? → "Cảm ơn, đội mình sẽ thử."
3. Viết lại câu "Dây của các cậu lỏng" thành góp ý lịch sự. → "Một điều nên thử: đội lắc nhẹ dây cổng số 2 xem có chặt không."

### Khái niệm 5: Chương trình dài thì chia nhỏ để thử

Ôn nấc 7 từ buổi 25, áp dụng vào kiểm thử. Ví dụ robot Chở thuốc:

```text
Món 1: khi nút được bấm → phát tiếng bíp          (thử riêng: bấm nút, nghe bíp)
Món 2: lặp mãi, nếu thấy đen thì tiến, không thì rẽ (thử riêng: đặt xe trên vạch)
Món 3: nếu khoảng cách < 15 cm thì dừng            (thử riêng: đưa hộp lại gần)
Món 4: đến nơi thì còi kêu dài                     (thử riêng)
Ghép: 1 → 2 + 3 → 4                                (thử cả bữa ăn)
```

> **Thầy:** "Món nào cũng phải 'nếm' riêng trước. Ghép xong mà hỏng, các em chỉ cần tìm ở chỗ nối giữa các món."

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

> **Thầy:** "Tin từ Xưởng chế tạo: Bác Bug đã trà trộn vào các xưởng! Hắn trốn rất giỏi, đội tự tìm thì khó thấy. Căn cứ quyết định lập Đội Thanh tra Bug. Nhưng muốn làm Thanh tra, phải được huấn luyện."

### 5' – Đoán trước, cược Xu

Thầy đưa robot mẫu có 3 lỗi cố ý (dây lỏng, cắm sai cổng, điều kiện đặt ngược), bật lên, robot không chạy đúng.

> **Thầy:** "Robot của Chỉ huy có mấy con Bác Bug? Đội cược Xu: 1, 2, 3 hay 4 con?"

Chưa công bố đáp án; để dành cho phần thực hành danh sách.

### 15' – Trò chơi không cần máy

**Trò 1 – Vòng quy trình bằng cơ thể (7 phút).** Dán 6 tấm thẻ bước lên sàn thành vòng tròn. Thầy kể chuyện "đội gấp máy bay", cả lớp nhảy sang ô đúng bước. Khi thầy nói "máy bay chúi xuống!", các em phải nhảy về ô Cải tiến rồi ô Thử, không được nhảy ra khỏi vòng.

**Trò 2 – Thử mỗi lần một thứ (8 phút).** Thầy đặt 3 cốc úp, một cốc có viên bi. Luật 1: được lật cả 3 cốc cùng lúc, nhưng phải nói cốc nào có bi trước khi nhìn. Luật 2: lật từng cốc. Hỏi: cách nào chắc chắn hơn? Rút ra: kiểm tra từng chỗ một thì không bỏ sót.

### 20' – Khám phá và giải thích

- **7 phút:** Giảng khái niệm 1 và 2 trên vòng tròn vừa chơi. Mỗi đội đặt nam châm tên đội vào bước mình đang ở.
- **8 phút:** Giảng khái niệm 3. Cả lớp dùng Phiếu Thanh tra Bug kiểm tra robot mẫu của thầy, từng mục theo thứ tự. Tìm ra đủ 3 Bug. Đội cược đúng nhận Xu.
- **5 phút:** Giảng khái niệm 4. Thầy và trợ giảng đóng hai cảnh: cảnh góp ý "dở" (chê bai, chung chung) và cảnh góp ý "hay". Các em chỉ ra khác biệt.

### 10' – Đố nhanh, nhận Thẻ bài

- Đóng vai theo cặp đội: đội A góp ý cho bản thiết kế của đội B bằng mẫu "Một điều hay – Một điều nên thử", rồi đổi lại.
- Làm Phiếu bài tập buổi 27.
- Đội góp ý cụ thể nhất nhận Thẻ bài "Thanh tra Bug".

### 5' – Cliffhanger

> **Thầy:** "Mỗi đội viết lên phiếu một việc phải làm xong ở buổi sau. Buổi sau, Xưởng chế tạo mở cửa. Và giữa buổi, sẽ có tiếng gõ cửa: Đội Thanh tra đến!"

## Học sinh hay hỏi gì và trả lời thế nào

**"Đội bạn tìm ra lỗi của đội con thì đội con có bị trừ điểm không?"**
Không. Cả hai đội đều được điểm: đội Thanh tra được điểm vì giúp bạn, đội được kiểm tra được điểm khi sửa xong. Bắt được Bác Bug là chuyện vui.

**"Nếu con thấy góp ý của bạn sai thì sao?"**
Em vẫn nói "Cảm ơn, đội mình sẽ thử". Thử rồi thấy không hợp, đội có quyền giữ cách cũ. Nếu chưa chắc, hỏi Chỉ huy.

**"Sao phải kiểm tra pin trước, con chắc chương trình sai mà?"**
Vì kiểm tra pin chỉ mất 5 giây. Nếu pin yếu mà em sửa chương trình cả buổi thì phí công. Kỹ sư kiểm tra chỗ dễ trước.

**"Robot chạy được rồi, sao còn phải thử nữa?"**
Chạy được một lần có thể là may mắn. Robot đạt khi chạy đúng nhiều lần liên tiếp, ví dụ 3 lần.

**"Phải đi mấy vòng quy trình thì xong?"**
Không có số cố định. Đi đến khi robot đạt yêu cầu ghi trên phiếu bằng sáng chế, hoặc hết thời gian (đó là ràng buộc).

## Hiểu lầm thường gặp

- **"Quay lại bước Sửa là thất bại."** Ngược lại, kỹ sư giỏi đi nhiều vòng. Khen đội nào sửa nhiều lần có ghi chép.
- **"Thanh tra là đi bắt lỗi để chê."** Thanh tra là đi giúp. Mục tiêu là robot của đội bạn chạy được.
- **"Sửa nhiều thứ cùng lúc cho nhanh."** Nhanh lúc đầu nhưng chậm về sau, vì không biết thứ nào có tác dụng.
- **"Chỉ cần kiểm tra chương trình."** Phần lớn lỗi ở các buổi thực hành trước là phần cứng: dây lỏng, cắm sai cổng, pin yếu.
- **"Khen thì nói đẹp quá là đủ."** Khen tốt phải cụ thể để đội bạn biết giữ điều gì.

## Phân hóa

**Lớp 1–3**

- Dùng vòng 4 bước: Thiết kế – Chế tạo – Thử – Sửa.
- Phiếu Thanh tra bằng hình (cục pin, công tắc, sợi dây, cổng, máy tính), các em tô màu khi kiểm tra xong.
- Góp ý bằng lời; trợ giảng ghi giúp.

**Lớp 4–5**

- Dùng vòng 6 bước, phân biệt rõ yêu cầu và ràng buộc.
- Tự viết thêm 1–2 mục riêng cho Phiếu Thanh tra phù hợp robot của đội (ví dụ "Dơi đặt cao bao nhiêu").
- Ghi nhật ký thử nghiệm: lần thử – thay đổi gì – kết quả.
- Viết góp ý thành câu hoàn chỉnh trên phiếu.

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Quy trình thiết kế kỹ thuật | Vòng tròn làm việc của kỹ sư | Chuỗi bước lặp: xác định vấn đề, ý tưởng, thiết kế, chế tạo, thử, cải tiến |
| Yêu cầu | Việc robot phải làm được | Tiêu chí chức năng mà sản phẩm phải đạt, có thể kiểm tra |
| Ràng buộc | Luật phải theo khi làm robot | Giới hạn về vật liệu, kích thước, thời gian, chi phí |
| Kiểm thử | Chạy thử xem robot có đúng không | Hoạt động chạy sản phẩm để so sánh kết quả thật với kết quả mong đợi |
| Danh sách kiểm tra | Phiếu đánh dấu từng mục | Danh mục bước kiểm tra theo thứ tự cố định để không bỏ sót |
| Kiểm tra chéo | Đội bạn kiểm tra giúp | Người khác rà soát sản phẩm để phát hiện lỗi người làm bỏ sót |
| Góp ý xây dựng | Một điều hay – Một điều nên thử | Nhận xét cụ thể, tôn trọng, kèm hướng cải thiện |
| Cải tiến | Sửa cho tốt hơn | Thay đổi thiết kế dựa trên kết quả thử nghiệm |

## Ghi nhớ cuối bài

1. Kỹ sư làm theo vòng: Thiết kế – Chế tạo – Thử – Sửa, rồi thử lại.
2. Yêu cầu là việc robot phải làm; ràng buộc là luật phải theo.
3. Robot không chạy thì kiểm tra theo thứ tự: Pin – Công tắc – Dây – Cổng – Chương trình.
4. Mỗi lần chỉ sửa một thứ, rồi chạy thử ngay.
5. Góp ý bằng "Một điều hay – Một điều nên thử"; nhận góp ý bằng "Cảm ơn, đội mình sẽ thử".
6. Chương trình dài thì thử từng món trước khi ghép.
