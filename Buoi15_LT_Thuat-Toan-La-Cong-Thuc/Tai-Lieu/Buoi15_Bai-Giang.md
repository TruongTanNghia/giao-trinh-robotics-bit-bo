# Bài giảng – Buổi 15: Thuật toán là công thức

> **Lý thuyết · 60 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 8: Thầy-robot ngốc nghếch · Tuần 8

Buổi này mở đầu Chặng 3. Ở Chặng 2, chiếc xe đã chạy được nhờ pin và công tắc, nhưng nó chỉ biết "chạy" hoặc "đứng". Từ hôm nay, các Kỹ sư bắt đầu dạy robot làm việc theo các bước. Hai ý lớn của buổi: **thuật toán** là chuỗi bước rõ ràng, đúng thứ tự; **bo mạch** là bộ não sẽ đọc và làm theo các bước đó.

## Kiến thức nền cho giáo viên

### Thuật toán là gì

Thuật toán là một dãy các bước để giải một việc. Một thuật toán tốt có ba tính chất mà thầy cần giữ trong đầu khi giảng:

| Tính chất | Nghĩa | Ví dụ khi làm bánh mì |
| --- | --- | --- |
| Rõ ràng | Mỗi bước chỉ có một cách hiểu | "Phết bơ lên mặt trên lát bánh" thay vì "phết bơ" |
| Có thứ tự | Các bước làm lần lượt, đổi thứ tự thì kết quả đổi | Mở hộp bơ trước rồi mới lấy bơ |
| Hữu hạn | Có điểm kết thúc | Bước cuối: "Úp lát bánh thứ hai lên. Xong." |

Ngoài ra, thuật toán có **đầu vào** (nguyên liệu: bánh, bơ) và **đầu ra** (kết quả: chiếc bánh mì kẹp). Với trẻ tiểu học, thầy chỉ cần nhấn ba chữ: **rõ ràng – đúng thứ tự – có lúc xong**.

### Thuật toán khác chương trình thế nào

- **Thuật toán** là ý tưởng các bước, viết bằng lời, bằng hình, bằng thẻ.
- **Chương trình** là thuật toán được viết bằng "ngôn ngữ" mà máy hiểu. Với lớp mình, ngôn ngữ đó là các khối lệnh kéo thả.
- Một thuật toán có thể viết thành nhiều chương trình khác nhau, giống một công thức nấu ăn có thể viết bằng tiếng Việt hay tiếng Anh.

### Gỡ lỗi (săn Bug)

Lỗi trong thuật toán hoặc chương trình gọi là **bug**. Việc tìm và sửa lỗi gọi là **gỡ lỗi** (debug). Ba loại lỗi hay gặp nhất ở trẻ:

1. **Thiếu bước:** quên "mở hộp bơ" nên không lấy được bơ.
2. **Sai thứ tự:** "úp lát bánh" trước khi "phết bơ".
3. **Mơ hồ:** "phết bơ" mà không nói phết lên đâu.

Cách gỡ lỗi chuẩn: chạy từng bước một, dừng ở bước đầu tiên cho kết quả sai, sửa bước đó, chạy lại từ đầu.

### Bo mạch điều khiển

Bo mạch điều khiển có một con chip gọi là **vi điều khiển**. Nó làm việc theo vòng ba bước:

```text
Đọc đầu vào  →  Xử lý theo chương trình  →  Điều khiển đầu ra
(cảm biến, nút)   (làm theo từng lệnh)        (động cơ, đèn, còi)
```

- **Cổng vào (input):** nơi cắm cảm biến, nút bấm. Bo mạch "nghe" và "nhìn" qua đây.
- **Cổng ra (output):** nơi cắm động cơ, đèn, còi. Bo mạch "ra lệnh" qua đây.
- **Nạp chương trình:** chép chương trình từ máy tính xuống bo mạch qua cáp hoặc không dây. Bo mạch nhớ chương trình và chạy được khi đã rút cáp.
- Bo mạch không tự nghĩ ra việc. Nó chỉ làm đúng những gì chương trình viết. Đây chính là bài học "thầy-robot ngốc nghếch".

Tên cổng, màu cổng và cách nạp khác nhau tùy bộ kit. Thầy xem tài liệu bộ kit của trường trước buổi học và đánh dấu màu cổng cho các em.

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Robot làm đúng từng chữ

**Định nghĩa cho trẻ:** Robot không đoán ý mình. Mình nói gì, robot làm đúng chữ đó.

**Ví dụ đời sống:** Khi mẹ bảo "lấy cho mẹ cái ly", em biết lấy ly nào, cầm thế nào. Robot thì không biết. Nếu không nói rõ, robot có thể lấy cái ly bẩn, hoặc cầm ngược.

**Ẩn dụ nhân vật:** Thầy-robot ngốc nghếch. Thầy rất ngoan, rất nghe lời, nhưng không hiểu "ý" mà chỉ hiểu "chữ".

**Lời giảng mẫu:**

> **Thầy:** "Các Kỹ sư thấy chưa? Thầy-robot không hư, cũng không cố tình phá. Thầy-robot chỉ làm đúng từng chữ các em nói. Muốn robot làm đúng, mình phải nói thật rõ."

**Câu hỏi kiểm tra:**

1. Vì sao thầy-robot phết bơ lên bàn? → Vì lệnh "phết bơ" không nói phết lên đâu.
2. Robot có tự đoán được ý mình không? → Không. Robot chỉ làm đúng lệnh.
3. Sửa lệnh "lấy bánh" cho rõ hơn. → Ví dụ: "Lấy một lát bánh mì trong túi, đặt lên đĩa."

### Khái niệm 2: Thuật toán là công thức

**Định nghĩa cho trẻ:** Thuật toán là danh sách các bước, làm lần lượt từ trên xuống, để xong một việc.

**Ví dụ đời sống:** Công thức nấu mì gói: đun nước sôi → bỏ mì vào → chờ 3 phút → cho gói gia vị → đổ ra bát. Nếu bỏ mì vào nồi nước lạnh rồi đổ ra bát ngay, mì sẽ sống.

**Ẩn dụ nhân vật:** Bác Bug thích nhất là thuật toán thiếu bước hoặc lộn thứ tự. Đó là nơi Bác Bug trốn.

**Lời giảng mẫu:**

> **Thầy:** "Thuật toán giống công thức nấu ăn. Mỗi bước phải rõ ràng. Các bước phải đúng thứ tự. Và phải có lúc xong. Ba điều này các Kỹ sư nhớ giúp thầy: rõ ràng, đúng thứ tự, có lúc xong."

**Câu hỏi kiểm tra:**

1. Thuật toán có mấy điều cần nhớ? → Ba: rõ ràng, đúng thứ tự, có lúc xong.
2. Đổi thứ tự "mặc áo" và "cài cúc" có được không? → Không, phải mặc áo trước rồi mới cài cúc.
3. Một thuật toán không bao giờ xong thì sao? → Robot làm mãi không dừng, việc không bao giờ hoàn thành.

### Khái niệm 3: Bug và săn Bug

**Định nghĩa cho trẻ:** Bug là chỗ sai trong các bước. Săn Bug là tìm chỗ sai và sửa nó.

**Ví dụ đời sống:** Em chỉ đường cho bạn đến lớp: "đi thẳng, rẽ phải, lên cầu thang". Nhưng thật ra phải rẽ trái. Bạn đi lạc. Lỗi nằm ở bước "rẽ phải".

**Ẩn dụ nhân vật:** Bác Bug là con sâu tinh nghịch, trốn trong các bước. Bắt được Bác Bug là được Xu.

**Lời giảng mẫu:**

> **Thầy:** "Kỹ sư giỏi không phải là người không bao giờ sai. Kỹ sư giỏi là người bắt được Bác Bug nhanh. Muốn bắt Bác Bug, mình làm thử từng bước một. Bước nào làm ra kết quả lạ, Bác Bug trốn ở đó."

**Câu hỏi kiểm tra:**

1. Có mấy kiểu Bác Bug hay gặp? → Ba: thiếu bước, sai thứ tự, nói không rõ.
2. Cách bắt Bác Bug là gì? → Làm thử từng bước, tìm bước đầu tiên bị sai, sửa rồi làm lại.
3. Sai có xấu không? → Không. Bắt được Bug là được thưởng.

### Khái niệm 4: Bộ não của robot – bo mạch

**Định nghĩa cho trẻ:** Bo mạch là bộ não của robot. Nó nhận tin từ giác quan, làm theo chương trình, rồi ra lệnh cho tay chân.

**Ví dụ đời sống:** Tay em chạm vào nồi nóng. Da (giác quan) báo cho não. Não quyết định "rút tay". Tay (tay chân) rút lại.

**Ẩn dụ nhân vật:** Nhân vật Bộ não. Bộ não có nhiều "cửa": cửa để nghe tin (cổng vào), cửa để gửi lệnh (cổng ra).

**Lời giảng mẫu:**

> **Thầy:** "Đây là Bộ não của robot. Bộ não không có mắt, không có chân. Nó cần Giác quan báo tin vào, và cần Tay chân để làm việc. Còn các bước làm thế nào, Bộ não đọc trong chương trình mà các Kỹ sư viết. Bộ não rất ngoan, giống thầy-robot lúc nãy: viết gì làm nấy."

**Câu hỏi kiểm tra:**

1. Bo mạch giống bộ phận nào của người? → Bộ não.
2. Động cơ cắm vào cổng nào: cổng nghe tin hay cổng gửi lệnh? → Cổng gửi lệnh (cổng ra).
3. Bo mạch tự biết phải làm gì không? → Không. Nó làm theo chương trình mình nạp vào.

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

Thầy đeo một tấm thẻ "ROBOT" trước ngực, đứng cạnh khay bánh mì, bơ, dao nhựa, đĩa.

> **Thầy:** "Bíp. Tôi là robot làm bánh mì. Hãy ra lệnh cho tôi. Bíp."

Mời 2–3 em ra lệnh. Thầy làm đúng từng chữ, phóng đại cho vui: "lấy bánh" thì cầm cả túi bánh; "phết bơ" thì cầm dao chạm lên mặt bàn; "kẹp lại" thì kẹp hai tay vào nhau.

### 5' – Đoán trước, cược Xu

> **Thầy:** "Các đội đoán xem: cần ít nhất bao nhiêu bước để thầy-robot làm xong một chiếc bánh mì kẹp đúng cách? Mỗi đội viết một con số và đặt 2 Xu."

Ghi các con số lên bảng. Cuối phần sau sẽ đếm lại.

### 15' – Trò chơi không cần máy: Sửa lệnh cho thầy-robot

1. Cả lớp cùng đọc từng lệnh. Thầy làm đúng chữ. Lệnh nào làm ra kết quả lạ, cả lớp hô "Bác Bug!".
2. Đội phát hiện lỗi đề xuất cách sửa. Thầy ghi lệnh đã sửa lên bảng.
3. Lặp lại đến khi có chiếc bánh mì đúng. Thường cần 7–10 bước.

Ví dụ thuật toán cuối cùng trên bảng:

```text
1. Mở túi bánh.
2. Lấy 2 lát bánh, đặt lên đĩa.
3. Mở nắp hộp bơ.
4. Cầm dao bằng tay phải.
5. Lấy một ít bơ bằng đầu dao.
6. Phết bơ lên mặt trên của lát bánh thứ nhất.
7. Đặt dao xuống đĩa.
8. Úp lát bánh thứ hai lên lát thứ nhất.
9. Xong.
```

> **Thầy:** "Các Kỹ sư vừa viết một thuật toán. Thuật toán là công thức: rõ ràng, đúng thứ tự, có lúc xong."

So số bước với con số các đội đã cược. Đội gần nhất nhận Xu.

### 20' – Khám phá và giải thích

**10 phút đầu: Công thức của đội.** Mỗi đội nhận bộ thẻ hình (đánh răng hoặc mặc áo). Các em xếp thẻ thành công thức. Sau đó đổi công thức với đội bên cạnh. Đội bạn làm theo đúng từng thẻ bằng động tác giả. Nếu thiếu bước hoặc sai thứ tự, đội bạn hô "Bác Bug!" và chỉ vào thẻ có lỗi.

Thầy đi quanh và hỏi:

> **Thầy:** "Bác Bug của đội này là loại nào: thiếu bước, sai thứ tự, hay nói không rõ?"

**10 phút sau: Gặp nhân vật Bộ não.** Thầy giơ bo mạch (không cắm điện) và đi qua 3 bước Nhìn – Sờ – Đoán.

- **Nhìn:** "Các em thấy gì trên Bộ não?" (con chip, các lỗ cắm có màu, đèn nhỏ, chỗ cắm cáp).
- **Sờ:** chuyền tay nhau cầm nhẹ hai mép bo mạch. Nhắc: cầm mép, không chạm vào chân kim loại.
- **Đoán:** "Lỗ cắm này để làm gì? Theo các em, động cơ cắm ở đâu, cảm biến cắm ở đâu?"

Vẽ lên bảng sơ đồ Giác quan → Bộ não → Tay chân. Giới thiệu "cửa nghe tin" (cổng vào) và "cửa gửi lệnh" (cổng ra).

> **Thầy:** "Chương trình là công thức viết bằng ngôn ngữ của Bộ não. Tuần sau, các Kỹ sư sẽ đưa công thức vào Bộ não thật."

### 10' – Đố nhanh, nhận Thẻ bài

Làm Phiếu bài tập buổi 15. Sau đó đố miệng:

- "Ba điều của thuật toán?" → Rõ ràng, đúng thứ tự, có lúc xong.
- "Bộ não của robot tên thật là gì?" → Bo mạch điều khiển.
- "Ba loại Bác Bug?" → Thiếu bước, sai thứ tự, không rõ.

Em trả lời đúng nhận Thẻ bài "Bộ não".

### 5' – Cliffhanger

Thầy giơ 3 phong bì niêm phong có dấu hình con sâu.

> **Thầy:** "Bác Bug vừa gửi thư. Bác đã giấu lỗi trong 3 công thức. Buổi sau, đội nào bắt đủ 3 con sẽ được mở Hộp Bí Ẩn số 2."

## Học sinh hay hỏi gì và trả lời thế nào

| Câu hỏi | Gợi ý trả lời |
| --- | --- |
| "Sao robot ngốc vậy thầy?" | Robot không ngốc, robot chỉ không đoán ý. Nó làm đúng chữ. Người viết lệnh cần nói rõ. |
| "Robot có biết suy nghĩ không?" | Robot làm theo các bước người viết. Khi mình dạy nó "nếu thấy... thì...", nó sẽ trông như đang suy nghĩ. Mình sẽ học điều đó ở tuần 11. |
| "Bo mạch có bị điện giật không?" | Bo mạch dùng pin nhỏ, an toàn khi dùng đúng cách. Nhưng không được để nước dính vào và không được tự nối pin. |
| "Viết sai thì robot có hỏng không?" | Không. Viết sai thì robot làm sai, mình sửa lại là xong. Đó là săn Bug. |
| "Thuật toán có phải chỉ dành cho máy tính?" | Không. Công thức nấu ăn, cách đánh răng, đường đi đến trường đều là thuật toán. |
| "Có mấy cách đúng để làm bánh mì?" | Nhiều cách. Miễn là rõ ràng, đúng thứ tự và làm ra bánh mì. |

## Hiểu lầm thường gặp

- **"Robot cố tình làm sai."** Robot không có ý định. Nó chỉ làm theo lệnh. Sai là do lệnh.
- **"Thuật toán càng dài càng giỏi."** Không phải. Thuật toán tốt là đủ bước và rõ ràng. Thừa bước cũng là một kiểu lộn xộn.
- **"Thuật toán và chương trình là một."** Thuật toán là ý tưởng các bước. Chương trình là thuật toán viết cho máy hiểu.
- **"Bo mạch là cục pin."** Pin cho năng lượng. Bo mạch là bộ não làm theo chương trình.
- **"Có Bug là mình kém."** Ai cũng gặp Bug. Kỹ sư thật mỗi ngày đều săn Bug.

## Phân hóa

### Lớp 1–3

- Dùng thẻ hình, không yêu cầu viết chữ.
- Công thức 4–5 bước (đánh răng, rửa tay).
- Chỉ dạy hai loại Bug: thiếu bước và sai thứ tự.
- Bo mạch: chỉ cần nhớ "Bộ não, có cửa nghe tin và cửa gửi lệnh".

### Lớp 4–5

- Các em tự viết công thức 6–8 bước bằng chữ.
- Thêm loại Bug thứ ba: lệnh không rõ ràng. Yêu cầu các em viết lại cho rõ.
- Giới thiệu từ "đầu vào" và "đầu ra" của thuật toán: nguyên liệu và kết quả.
- Bo mạch: phân biệt cổng vào và cổng ra, nêu được ví dụ mỗi loại. Hỏi thêm: "Vì sao rút cáp rồi robot vẫn chạy?" (bo mạch đã nhớ chương trình).

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Thuật toán | Công thức các bước để làm xong một việc | Dãy hữu hạn các bước rõ ràng, có thứ tự, biến đầu vào thành kết quả |
| Chương trình | Công thức viết bằng ngôn ngữ của robot | Thuật toán được biểu diễn bằng ngôn ngữ lập trình để máy thực hiện |
| Bug | Chỗ sai trong các bước | Lỗi trong thuật toán hoặc chương trình làm kết quả sai |
| Gỡ lỗi (săn Bug) | Tìm chỗ sai và sửa | Quá trình xác định, khoanh vùng và sửa lỗi |
| Bo mạch điều khiển | Bộ não của robot | Bảng mạch có vi điều khiển, đọc tín hiệu vào, chạy chương trình, điều khiển thiết bị ra |
| Cổng vào | Cửa nghe tin | Chân/cổng nhận tín hiệu từ cảm biến, nút bấm |
| Cổng ra | Cửa gửi lệnh | Chân/cổng xuất tín hiệu điều khiển động cơ, đèn, còi |
| Nạp chương trình | Đưa công thức vào Bộ não | Chép chương trình từ máy tính xuống bộ nhớ của vi điều khiển |

## Ghi nhớ cuối bài

1. Robot làm đúng từng chữ, không đoán ý mình.
2. Thuật toán là công thức: rõ ràng, đúng thứ tự, có lúc xong.
3. Chương trình là thuật toán viết bằng ngôn ngữ của robot.
4. Bác Bug hay trốn ở chỗ thiếu bước, sai thứ tự hoặc nói không rõ.
5. Bo mạch là Bộ não: nghe tin qua cổng vào, gửi lệnh qua cổng ra, làm theo chương trình.
