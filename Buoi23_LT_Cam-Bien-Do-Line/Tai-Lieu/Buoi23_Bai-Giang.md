# Bài giảng – Buổi 23: Cảm biến dò line

> **Lý thuyết · 60 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 12: Mê cung đen · Tuần 12

Buổi này giới thiệu giác quan thứ hai của robot: **cảm biến dò line**, nhìn xuống sàn để phân biệt đen và trắng. Các em sẽ dùng câu Nếu – Thì với hai trường hợp để xe bám theo vạch đen (nấc 5 nâng cao).

## Kiến thức nền cho giáo viên

### Ánh sáng, phản xạ và hấp thụ

- Khi ánh sáng chiếu vào một bề mặt, một phần bị **phản xạ** (dội lại), một phần bị **hấp thụ** (nuốt vào).
- Bề mặt **trắng, sáng** phản xạ nhiều ánh sáng.
- Bề mặt **đen, tối** hấp thụ nhiều, phản xạ ít.
- Đó là lý do áo đen phơi nắng nóng hơn áo trắng: áo đen hấp thụ nhiều năng lượng hơn.

### Cảm biến dò line hồng ngoại hoạt động thế nào

Phần lớn cảm biến dò line trong kit giáo dục có một cặp linh kiện nhìn xuống sàn:

1. **Đèn phát hồng ngoại:** phát ánh sáng hồng ngoại. Mắt người không thấy ánh sáng này (giống ánh sáng trong điều khiển tivi).
2. **Bộ thu (cảm quang):** đo lượng ánh sáng phản xạ quay về.

| Bề mặt dưới cảm biến | Ánh sáng phản xạ về | Cảm biến báo |
| --- | --- | --- |
| Trắng | Nhiều | Giá trị "sáng" (hoặc 0 / 1 tùy kit) |
| Đen | Ít | Giá trị "tối" |

Tùy kit, cảm biến cho ra:

- **Giá trị số liên tục** (ví dụ 0–100 hoặc 0–1023): cần chọn **ngưỡng** để phân biệt đen và trắng.
- **Giá trị đúng/sai** (thấy đen / không thấy đen): kit đã có ngưỡng sẵn, thường chỉnh bằng một núm vặn nhỏ trên cảm biến. Nhiều cảm biến có một đèn báo nhỏ sáng/tắt theo màu sàn.

Cách đọc chính xác xem tài liệu bộ kit của trường.

### Ngưỡng và hiệu chỉnh

Nếu cảm biến cho số liên tục:

```text
ngưỡng ≈ (số đo trên nền trắng + số đo trên vạch đen) ÷ 2
```

Ví dụ trắng = 80, đen = 20 → ngưỡng = 50. Số lớn hơn 50 là trắng, nhỏ hơn 50 là đen.

**Hiệu chỉnh** là đo lại trắng và đen ngay trên sàn sẽ chạy, rồi đặt lại ngưỡng. Phải hiệu chỉnh vì:

- Ánh sáng phòng (nắng, đèn) cũng chiếu vào bộ thu và làm số thay đổi.
- Mặt sàn khác nhau (gạch bóng, thảm, giấy) phản xạ khác nhau.
- Độ cao cảm biến so với sàn thay đổi số đo. Thường cảm biến cần cách sàn khoảng vài mm đến 1–2 cm (theo kit).

### Thuật toán bám line với 1 cảm biến: đi theo mép vạch

Với một cảm biến, xe không thể biết vạch nằm bên trái hay bên phải. Cách phổ biến là **bám mép**: xe đi theo đường ranh giới giữa đen và trắng, ví dụ mép phải của vạch.

```text
lặp mãi
  nếu cảm biến thấy đen thì
    lượn sang phải (ra phía trắng)
  không thì
    lượn sang trái (vào phía đen)
```

Kết quả: xe đi **zigzag** dọc theo mép vạch: thấy đen thì lách ra, thấy trắng thì lách vào. Mỗi lượn chỉ là một chút, nên nhìn từ xa xe vẫn đi theo vạch. Khóa học dùng phiên bản đơn giản cho trẻ: "thấy đen thì tiến chậm, thấy trắng thì rẽ về phía vạch" – về bản chất cũng là lách qua lại quanh mép.

"Lượn" thường được làm bằng cách cho một bánh quay nhanh hơn bánh kia, hoặc cho một bánh đứng yên.

### Thuật toán bám line với 2 cảm biến (lớp 4–5)

Hai cảm biến đặt hai bên vạch, vạch nằm giữa:

| Trái | Phải | Nghĩa | Xe làm |
| --- | --- | --- | --- |
| Trắng | Trắng | Vạch nằm giữa | Đi thẳng |
| Đen | Trắng | Vạch lệch sang trái | Rẽ trái |
| Trắng | Đen | Vạch lệch sang phải | Rẽ phải |
| Đen | Đen | Ngã tư hoặc vạch ngang | Dừng hoặc làm việc đặc biệt |

Hai cảm biến cho xe biết vạch lệch về bên nào, nên đi mượt hơn, ít zigzag hơn.

### Vì sao xe nhanh quá thì trượt khỏi vạch

Bộ não kiểm tra cảm biến rất nhiều lần mỗi giây, nhưng xe vẫn cần thời gian để đổi hướng. Nếu xe chạy nhanh:

- Giữa hai lần kiểm tra, xe đã đi quá xa.
- Đến khúc cua, khi cảm biến kịp thấy "trắng", xe đã vượt ra khỏi vạch và không tìm lại được.
- Đà của xe làm nó trượt tiếp sau lệnh rẽ.

Cách sửa: giảm tốc độ, nhất là ở khúc cua; làm vạch rộng hơn; cua bớt gắt.

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Đen nuốt ánh sáng, trắng trả ánh sáng

**Định nghĩa cho trẻ:** Chiếu đèn vào giấy trắng, ánh sáng dội lại nhiều. Chiếu vào giấy đen, ánh sáng bị nuốt gần hết.

**Ví dụ đời sống:** Đi nắng mặc áo đen thấy nóng hơn áo trắng, vì áo đen nuốt nhiều ánh nắng. Trong phòng tối, tờ giấy trắng vẫn dễ thấy hơn tờ giấy đen.

**Lời giảng mẫu:**

> **Thầy:** "Thầy tắt bớt đèn. Thầy soi đèn pin vào tờ giấy trắng. Các em nhìn trần nhà: có vệt sáng dội lên. Giờ soi vào tờ giấy đen. Vệt sáng mờ hẳn. Giấy đen đã nuốt ánh sáng."

**Câu hỏi kiểm tra:**

1. Giấy nào dội lại nhiều ánh sáng hơn? → Giấy trắng.
2. Vì sao áo đen mặc nắng nóng hơn? → Áo đen nuốt nhiều ánh sáng hơn.

### Khái niệm 2: Mắt mèo – cảm biến dò line

**Định nghĩa cho trẻ:** Cảm biến dò line chiếu một thứ ánh sáng mà mắt mình không thấy xuống sàn, rồi đo xem ánh sáng dội lại nhiều hay ít. Nhiều là trắng, ít là đen.

**Ví dụ đời sống:** Điều khiển tivi cũng phát ánh sáng mà mình không thấy. Đó là ánh sáng hồng ngoại.

**Ẩn dụ nhân vật:** Mắt mèo. Mèo nhìn rất giỏi trong bóng tối và phân biệt sáng tối rất nhanh. Mắt mèo của robot nhìn xuống chân.

**Lời giảng mẫu:**

> **Thầy:** "Đây là Mắt mèo. Nó có hai con mắt nhỏ nhìn xuống sàn. Một mắt chiếu ánh sáng hồng ngoại, mắt kia đo xem ánh sáng dội về nhiều hay ít. Dưới chân là vạch đen thì ít ánh sáng về. Là sàn trắng thì nhiều ánh sáng về. Mắt mèo không biết màu đỏ, màu xanh. Nó chỉ biết sáng và tối."

**Câu hỏi kiểm tra:**

1. Mắt mèo nhìn lên hay nhìn xuống? → Nhìn xuống sàn.
2. Mắt mèo phân biệt được màu đỏ và xanh không? → Không, chỉ biết sáng và tối.
3. Ánh sáng nó chiếu ra có nhìn thấy không? → Không, đó là ánh sáng hồng ngoại.

### Khái niệm 3: Ánh sáng phòng làm Mắt mèo nhìn nhầm

**Định nghĩa cho trẻ:** Nắng chiếu vào hoặc đèn phòng thay đổi làm Mắt mèo nhìn sai. Vì vậy trước mỗi lần chạy phải đo lại.

**Ví dụ đời sống:** Đang đọc sách trong phòng, ra nắng chói, em phải nheo mắt một lúc mới nhìn rõ.

**Ẩn dụ nhân vật:** Bác Bug trốn trong tia nắng. Hôm qua chạy tốt, hôm nay nắng chiếu vào, xe chạy lung tung.

**Lời giảng mẫu:**

> **Thầy:** "Mắt mèo quen với ánh sáng ở chỗ này. Mang sang chỗ có nắng, nó bị lóa. Kỹ sư giỏi luôn đặt Mắt mèo lên chỗ trắng, chỗ đen để đo lại trước khi chạy. Việc đó gọi là hiệu chỉnh."

**Câu hỏi kiểm tra:**

1. Vì sao phải đo lại trước mỗi lần chạy? → Ánh sáng và mặt sàn có thể khác, làm Mắt mèo nhìn nhầm.
2. Hiệu chỉnh là gì? → Đo lại chỗ trắng và chỗ đen rồi đặt lại mốc.

### Khái niệm 4: Luật bám vạch – hai trường hợp Nếu – Thì

**Định nghĩa cho trẻ:** Xe đi theo vạch bằng hai luật: Nếu thấy đen thì đi tiếp. Nếu thấy trắng thì rẽ về phía vạch.

**Ví dụ đời sống:** Đi trên vỉa hè có gạch hoa văn, em cố đặt chân trên một đường gạch. Chân lệch ra ngoài thì em bước lại vào.

**Lời giảng mẫu:**

> **Thầy:** "Robot không thấy cả mê cung. Nó chỉ thấy một chấm nhỏ dưới chân. Nên nó dùng hai luật đơn giản: còn thấy đen là còn trên đường, đi tiếp. Thấy trắng là lạc rồi, rẽ lại về phía vạch. Làm lại thật nhanh, thật nhiều lần, xe sẽ đi theo vạch."

**Câu hỏi kiểm tra:**

1. Thấy đen thì làm gì? → Đi tiếp (tiến chậm).
2. Thấy trắng thì làm gì? → Rẽ về phía vạch.
3. Vì sao xe đi ngoằn ngoèo một chút? → Vì nó liên tục lách ra lách vào quanh mép vạch.

### Khái niệm 5: Đi chậm để không lạc

**Định nghĩa cho trẻ:** Xe chạy nhanh quá thì đến khúc cua không kịp rẽ, trượt ra khỏi vạch.

**Ví dụ đời sống:** Chạy nhanh trên sân rồi rẽ gấp, em dễ trượt chân. Đi chậm thì rẽ dễ.

**Lời giảng mẫu:**

> **Thầy:** "Đua tốc độ ở mê cung là thua. Xe chạy chậm mà không lạc mới là xe giỏi."

**Câu hỏi kiểm tra:**

1. Vì sao xe chạy nhanh hay lạc ở khúc cua? → Không kịp rẽ, bị trượt ra ngoài vạch.

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

Mê cung băng dính đen đã dán trên sàn. Thầy đọc thư từ Bít-Bô:

> **Thầy:** "Bít-Bô bị lạc trong mê cung đen. Chỉ robot biết nhìn đường mới cứu được. Nhưng tai dơi của chúng ta chỉ nghe được tường. Mê cung này không có tường, chỉ có vạch trên sàn. Làm sao đây?"

### 5' – Đoán trước, cược Xu

> **Thầy:** "Tai dơi có đi theo vạch đen được không? Có hay không? Đặt 2 Xu."

(Đáp án: không, vì vạch không có độ cao, không tạo tiếng vọng.)

### 15' – Trò chơi không cần máy

1. **Soi đèn pin (4 phút):** Tắt bớt đèn. Soi đèn pin vào giấy trắng và giấy đen, quan sát vệt sáng dội lên tường/trần. Cả lớp nói "nhiều" hoặc "ít".
2. **Người dò line (8 phút):** Mỗi em cầm ống giấy (lõi giấy vệ sinh) áp sát mắt, chỉ được nhìn xuống chân qua ống. Đi theo vạch đen trên sàn. Bạn đi sau nhắc nhẹ nếu lệch. Hỏi: "Khi lệch ra trắng, em làm gì?"
3. **Rút luật (3 phút):** Cả lớp nói luật: "Thấy đen thì đi tiếp. Thấy trắng thì quay về phía vạch." Thầy viết lên bảng.

Trả Xu cho đội đoán "không".

### 20' – Khám phá và giải thích

**7 phút: Gặp Mắt mèo.** Chuyền tay cảm biến dò line. Nhìn – Sờ – Đoán: "Có mấy mắt nhỏ? Mắt nhìn hướng nào?" Thầy cắm cảm biến xe mẫu, đưa qua lại trên vạch đen; cả lớp nhìn đèn báo hoặc con số thay đổi.

**5 phút: Bác Bug trong tia nắng.** Thầy đo số trên nền trắng ở chỗ bóng râm, rồi đem ra chỗ có nắng hoặc soi đèn pin vào cảm biến. Số thay đổi. Giải thích hiệu chỉnh.

**8 phút: Viết luật lên thẻ.** Mỗi đội viết luật bám vạch bằng thẻ Nếu – Thì:

```text
lặp mãi
  nếu cảm biến thấy đen thì
    tiến chậm
  không thì
    rẽ về phía vạch
```

Thầy vẽ trên bảng đường zigzag của xe dọc mép vạch và giải thích vì sao xe đi ngoằn ngoèo. Hỏi: "Nếu xe chạy rất nhanh đến khúc cua thì sao?"

### 10' – Đố nhanh, nhận Thẻ bài

Làm Phiếu bài tập buổi 23. Đố miệng:

- "Giấy đen hay trắng dội nhiều ánh sáng hơn?" → Trắng.
- "Mắt mèo nhìn thấy màu đỏ không?" → Không.
- "Vì sao phải đo lại trước khi chạy?" → Ánh sáng thay đổi.

Trao Thẻ bài "Mắt mèo".

### 5' – Cliffhanger

> **Thầy:** "Con Bug to nhất đang chờ ở cuối mê cung. Buổi sau, xe nào đi hết mê cung sẽ đánh thức vùng sáng thứ 12 của Bít-Bô, và Hộp Bí Ẩn số 3 sẽ được mở."

## Học sinh hay hỏi gì và trả lời thế nào

| Câu hỏi | Gợi ý trả lời |
| --- | --- |
| "Sao không dùng tai dơi đi theo vạch?" | Vạch đen nằm phẳng trên sàn, không có tiếng vọng. Tai dơi chỉ biết vật đứng chắn phía trước. |
| "Ánh sáng hồng ngoại có hại mắt không?" | Ánh sáng của cảm biến rất yếu, giống điều khiển tivi, an toàn khi dùng bình thường. Không nhìn sát vào bất kỳ đèn nào lâu. |
| "Vạch màu xanh đậm có được không?" | Có thể được, vì xanh đậm cũng tối. Nhưng đen là chắc chắn nhất. |
| "Xe có thấy cả mê cung không?" | Không. Nó chỉ thấy một chấm nhỏ dưới cảm biến. Nó đi được nhờ luật lặp lại rất nhanh. |
| "Sao xe đi lắc lắc?" | Vì nó liên tục lách vào vạch, lách ra trắng. Thêm cảm biến thứ hai thì đi mượt hơn. |
| "Xe tự lái ngoài đường có dùng cái này không?" | Xe thật dùng camera và nhiều cảm biến phức tạp hơn, nhưng ý tưởng "nhìn vạch kẻ đường rồi giữ làn" thì giống. |

## Hiểu lầm thường gặp

- **"Cảm biến dò line là camera."** Nó chỉ đo sáng/tối ở một chấm nhỏ, không chụp hình.
- **"Cảm biến biết màu."** Nó chỉ biết nhiều hay ít ánh sáng phản xạ.
- **"Đo một lần dùng mãi."** Ánh sáng và mặt sàn thay đổi, phải hiệu chỉnh lại.
- **"Xe nhanh là xe giỏi."** Trong mê cung, xe chậm và ổn định mới đi hết.
- **"Đặt cảm biến càng cao càng nhìn rõ."** Đặt quá cao thì ánh sáng tản ra, khó phân biệt đen trắng. Cần đặt gần sàn theo hướng dẫn kit.

## Phân hóa

### Lớp 1–3

- Dùng 1 cảm biến, đầu ra kiểu "thấy đen / không thấy đen".
- Luật hai câu: "Thấy đen thì đi. Thấy trắng thì rẽ."
- Không dạy công thức ngưỡng; thầy hiệu chỉnh giúp.

### Lớp 4–5

- Đọc số đo trắng/đen, tự tính ngưỡng = (trắng + đen) ÷ 2.
- Giải thích bám mép và đường zigzag.
- Giới thiệu bảng 4 trường hợp của 2 cảm biến; thử viết luật trên giấy.
- Câu hỏi suy luận: "Vì sao xe nhanh dễ trượt ở khúc cua?"

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Cảm biến dò line | Mắt mèo nhìn xuống sàn | Cảm biến quang đo cường độ ánh sáng phản xạ từ bề mặt để phân biệt vạch |
| Hồng ngoại | Ánh sáng mắt mình không thấy | Bức xạ có bước sóng dài hơn ánh sáng đỏ, mắt người không nhìn thấy |
| Phản xạ | Ánh sáng dội lại | Ánh sáng bị bề mặt hắt trở lại |
| Hấp thụ | Ánh sáng bị nuốt | Năng lượng ánh sáng bị bề mặt giữ lại |
| Ngưỡng | Mốc chia đen và trắng | Giá trị giới hạn dùng để phân loại tín hiệu |
| Hiệu chỉnh | Đo lại trước khi chạy | Điều chỉnh mốc đo theo điều kiện thực tế |
| Bám mép (line following) | Đi theo vạch | Thuật toán điều khiển xe theo ranh giới đen – trắng |
| Zigzag | Đi ngoằn ngoèo | Dao động trái – phải quanh mép vạch do điều khiển bật/tắt |

## Ghi nhớ cuối bài

1. Trắng dội lại nhiều ánh sáng, đen nuốt ánh sáng.
2. Mắt mèo chiếu ánh sáng hồng ngoại xuống sàn và đo phần dội lại để biết sáng hay tối.
3. Ánh sáng phòng thay đổi làm Mắt mèo nhìn nhầm: luôn hiệu chỉnh trước khi chạy.
4. Luật bám vạch: thấy đen thì đi tiếp, thấy trắng thì rẽ về phía vạch, lặp lại thật nhanh.
5. Xe chậm và ổn định mới đi hết mê cung; nhanh quá sẽ trượt khỏi vạch.
