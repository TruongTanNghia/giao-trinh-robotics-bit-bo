# Bài giảng – Buổi 17: Lập trình bằng khối màu

> **Lý thuyết · 60 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 9: Bản đồ kho báu · Tuần 9

Đây là buổi đầu tiên các Kỹ sư tự nhìn thấy "ngôn ngữ của Bộ não" trên máy tính. Ba ý lớn: **giao diện lập trình khối**, **lệnh có con số đi kèm (số giây, số bước)**, và nhân vật mới **Chú chim hót – còi buzzer**.

## Kiến thức nền cho giáo viên

### Lập trình khối

Lập trình khối là cách viết chương trình bằng cách kéo và ghép các khối hình như mảnh ghép. Mỗi khối là một lệnh. Các khối chỉ khớp khi ghép đúng kiểu, nên trẻ không mắc lỗi chính tả và tập trung vào ý tưởng.

Hầu hết phần mềm lập trình khối có 4 vùng:

| Vùng | Chức năng |
| --- | --- |
| Kho khối (bảng bên trái) | Các khối được nhóm theo màu: chuyển động, đèn, âm thanh, chờ/điều khiển, cảm biến |
| Vùng ghép khối (ở giữa) | Nơi kéo khối vào và ghép thành chương trình |
| Nút Chạy / Dừng | Chạy chương trình (hoặc nạp xuống bo mạch) và dừng lại |
| Nút kết nối | Kết nối máy tính với bo mạch qua cáp hoặc không dây |

Tên khối, màu khối và vị trí nút khác nhau theo phần mềm. Thầy chụp màn hình phần mềm của trường, in và dán lên bảng trước buổi học.

### Sự kiện và lệnh tuần tự

- **Sự kiện** là khối mở đầu, ví dụ "khi bắt đầu", "khi bấm nút". Chương trình chỉ chạy các khối gắn bên dưới sự kiện.
- **Lệnh tuần tự**: các khối gắn dưới sự kiện chạy lần lượt từ trên xuống, mỗi lần một khối. Bộ não không nhảy cóc.

### Tham số và đơn vị

Nhiều khối có ô để điền số. Con số đó gọi là **tham số**. Cùng một khối "tiến", con số khác nhau cho kết quả khác nhau. Điều quan trọng là **đơn vị**:

| Khối | Đơn vị | Xe đi bao xa phụ thuộc vào |
| --- | --- | --- |
| tiến 2 giây | Thời gian | Tốc độ xe, độ trơn của sàn, pin mạnh hay yếu |
| tiến 2 bước / 2 ô / 2 vòng | Quãng đường | Ít phụ thuộc vào tốc độ hơn |

Với xe dùng động cơ thường, điều khiển theo **giây** là phổ biến nhất. Cùng "tiến 2 giây", pin yếu thì xe đi ngắn hơn. Đây là một nguồn Bác Bug quen thuộc: hôm qua chạy đúng, hôm nay thiếu ô vì pin yếu.

### Còi buzzer

Còi buzzer có một tấm kim loại mỏng rung rất nhanh khi có điện. Tấm này đẩy không khí, tạo sóng âm, tai ta nghe thành tiếng.

- **Tần số** là số lần rung mỗi giây, đơn vị héc (Hz).
- Rung càng nhanh (tần số cao) thì tiếng càng cao (trong, chói). Rung chậm (tần số thấp) thì tiếng trầm.
- Một số bo mạch cho chọn nốt nhạc (Đô, Rê, Mi...). Thực chất mỗi nốt là một tần số.
- Tai người nghe được khoảng 20 Hz đến 20.000 Hz. Còi trong kit thường kêu vài trăm đến vài nghìn Hz.

## Lý thuyết giảng cho học sinh

### Khái niệm 1: Khối lệnh là mảnh ghép

**Định nghĩa cho trẻ:** Mỗi khối là một lệnh. Ghép các khối lại thành chương trình. Bộ não đọc từ trên xuống.

**Ví dụ đời sống:** Ghép tàu hỏa đồ chơi. Đầu tàu kéo các toa. Toa nào không nối vào đầu tàu thì đứng yên.

**Ẩn dụ nhân vật:** Khối "khi bắt đầu" là đầu tàu. Các khối lệnh là toa tàu. Bác Bug thích tháo một toa ra khỏi đoàn.

**Lời giảng mẫu:**

> **Thầy:** "Các Kỹ sư nhìn này. Đây là đầu tàu: khi bắt đầu. Thầy nối toa 'bật đèn' vào. Bấm Chạy. Đèn sáng! Giờ thầy kéo toa ra xa, không nối vào đầu tàu. Bấm Chạy. Không có gì xảy ra. Toa không nối thì không chạy."

**Câu hỏi kiểm tra:**

1. Khối nào là đầu tàu? → Khối "khi bắt đầu".
2. Bộ não đọc khối theo chiều nào? → Từ trên xuống.
3. Khối nằm riêng, không nối vào đầu tàu thì sao? → Không chạy.

### Khái niệm 2: Mỗi màu là một nhóm việc

**Định nghĩa cho trẻ:** Khối được chia màu. Mỗi màu làm một loại việc: di chuyển, đèn, âm thanh, chờ.

**Ví dụ đời sống:** Hộp bút màu: bút đỏ để tô hoa, bút xanh lá để tô cây. Kho khối cũng chia ngăn theo màu để dễ tìm.

**Ẩn dụ nhân vật:** Mỗi ngăn màu là một "phòng" trong Căn cứ: phòng Động cơ, phòng Đèn, phòng Âm thanh.

**Lời giảng mẫu:**

> **Thầy:** "Muốn xe chạy, các em vào phòng màu ... (theo phần mềm) tìm khối di chuyển. Muốn còi kêu, vào phòng Âm thanh. Đừng lục khắp nơi, nhớ màu là tìm nhanh."

**Câu hỏi kiểm tra:**

1. Muốn bật đèn, tìm khối ở nhóm nào? → Nhóm Đèn (theo màu của phần mềm).
2. Vì sao chia khối theo màu? → Để tìm nhanh, mỗi màu một loại việc.

### Khái niệm 3: Con số trong lệnh – số giây và số bước

**Định nghĩa cho trẻ:** Nhiều khối có ô số. Con số cho robot biết làm bao lâu hoặc bao xa. Phải nhìn kỹ đơn vị: giây hay bước.

**Ví dụ đời sống:** "Chạy 3 bước" và "chạy 3 giây" khác nhau. Chạy 3 giây thì bạn chạy nhanh đi xa hơn bạn chạy chậm. Chạy 3 bước thì ai cũng đi 3 bước.

**Ẩn dụ nhân vật:** Bác Bug thích đổi số thật to. "Tiến 20 giây" là xe đâm vào tường.

**Lời giảng mẫu:**

> **Thầy:** "Con số là lời dặn thêm cho Bộ não. 'Tiến' thôi thì Bộ não không biết tiến bao lâu. 'Tiến 2 giây' thì rõ ràng. Nhưng các em nhớ: cùng 2 giây, pin yếu thì xe đi ngắn hơn. Kỹ sư giỏi luôn thử trước rồi mới chọn số."

**Câu hỏi kiểm tra:**

1. "Tiến 3 bước" và "tiến 3 giây", cái nào luôn đi cùng một quãng? → Tiến 3 bước.
2. Pin yếu thì "tiến 2 giây" đi xa hơn hay ngắn hơn? → Ngắn hơn.
3. Muốn xe đi xa gấp đôi, đổi số thế nào? → Tăng số lên gấp đôi (rồi thử lại để chắc chắn).

### Khái niệm 4: Chú chim hót – còi buzzer

**Định nghĩa cho trẻ:** Còi có một miếng kim loại nhỏ rung thật nhanh. Rung tạo ra tiếng. Rung càng nhanh, tiếng càng cao.

**Ví dụ đời sống:** Dây đàn guitar căng: gảy lên dây rung và kêu. Dây nhỏ rung nhanh kêu cao, dây to rung chậm kêu trầm. Đặt tay lên cổ khi hát, em thấy cổ rung.

**Ẩn dụ nhân vật:** Chú chim hót, giống chuông cửa nhà em. Chú chim hót rất to, nên có luật "giờ hót": mỗi lượt chỉ 10 giây.

**Lời giảng mẫu:**

> **Thầy:** "Các Kỹ sư đặt tay lên cổ, nói 'aaaa'. Thấy rung không? Tiếng nói là do rung. Chú chim hót cũng có một miếng kim loại rung bên trong. Rung nhanh thì tiếng cao như chim sẻ, rung chậm thì tiếng trầm như chim cú."

**Câu hỏi kiểm tra:**

1. Còi kêu được là nhờ cái gì? → Miếng kim loại rung.
2. Rung nhanh thì tiếng cao hay trầm? → Cao.
3. Luật "giờ hót" là gì? → Mỗi lượt còi kêu tối đa 10 giây.

## Kịch bản giảng theo khung 60 phút

### 5' – Tín hiệu từ Bít-Bô

Máy chiếu bật sẵn phần mềm, xe mẫu đã kết nối. Thầy kéo một khối "bật đèn" vào dưới "khi bắt đầu", bấm Chạy. Đèn xe sáng.

> **Thầy:** "Thầy không chạm vào xe. Thầy chỉ kéo một mảnh ghép. Vì sao đèn sáng?"

### 5' – Đoán trước, cược Xu

Thầy viết hai lệnh lên bảng: "tiến 2 giây" và "tiến 2 bước". Đặt xe trên thảm ô.

> **Thầy:** "Lệnh nào đưa xe đi xa hơn? Mỗi đội đặt 2 Xu."

Chưa chạy thử. Giữ kết quả cho bước 15' sau.

### 15' – Trò chơi không cần máy: Đếm nhịp

1. Cả lớp đứng dậy. Thầy hô: "Tiến 3 bước!" Mọi em bước 3 bước.
2. Thầy hô: "Tiến 3 giây!" và đếm to "một, hai, ba". Em nào đi nhanh sẽ đi xa hơn em đi chậm.
3. Hỏi: "Lệnh nào làm cả lớp đứng thẳng hàng?" (lệnh theo bước).
4. Chạy xe mẫu "tiến 2 giây" trên thảm ô, đếm số ô. Trả Xu cho đội đoán đúng.
5. Trò "Đầu tàu và toa": 4 em cầm thẻ khối (khi bắt đầu, tiến 1 giây, bật đèn, phát tiếng bíp), nắm vai nhau thành tàu. Em nào buông vai là "toa rời", không được làm động tác.

### 20' – Khám phá và giải thích

**8 phút: Đi tham quan giao diện.** Trên máy chiếu, thầy chỉ lần lượt 4 vùng. Gọi học sinh lên chỉ lại: "Kho khối ở đâu? Nút Chạy ở đâu?" Thầy kéo 3 khối, ghép, chạy; rồi tháo khối giữa ra, chạy lại để cả lớp thấy khác biệt.

**6 phút: Gặp Chú chim hót.** Nhìn còi buzzer thật, chuyền tay. Thầy chạy khối "phát tiếng bíp" với hai nốt thấp và cao. Cả lớp nói "trầm" hoặc "cao". Nhắc luật "giờ hót".

**6 phút: Lập kế hoạch đường đến kho báu.** Mỗi đội nhận giấy ô vẽ sẵn xuất phát và kho báu. Các em vẽ đường đi bằng mũi tên, rồi viết chuỗi 1–5 lệnh, có con số và đơn vị. Ví dụ:

```text
khi bắt đầu
  tiến 2 giây
  rẽ phải 0,5 giây
  tiến 1 giây
  phát tiếng bíp
```

> **Thầy:** "Con số này các em đang đoán. Buổi sau, xe thật sẽ cho biết các em đoán đúng chưa."

### 10' – Đố nhanh, nhận Thẻ bài

Làm Phiếu bài tập buổi 17. Đố miệng:

- "Khối đầu tàu tên gì?" → Khi bắt đầu.
- "Bộ não đọc khối theo chiều nào?" → Từ trên xuống.
- "Còi kêu nhờ gì?" → Rung.

Trao Thẻ bài "Chú chim hót".

### 5' – Cliffhanger

> **Thầy:** "Kho báu đang nằm trên thảm. Buổi sau, xe của các em sẽ tự đi tìm theo kế hoạch các em vừa viết. Liệu con số các em đoán có đúng không?"

## Học sinh hay hỏi gì và trả lời thế nào

| Câu hỏi | Gợi ý trả lời |
| --- | --- |
| "Sao không gõ chữ như người lớn lập trình?" | Gõ chữ là bước sau. Khối màu giúp mình hiểu ý tưởng trước, không lo sai chính tả. Ý tưởng giống hệt nhau. |
| "Có bao nhiêu khối tất cả?" | Rất nhiều, nhưng hôm nay chỉ cần 4–5 khối. Mỗi tuần mình học thêm vài khối. |
| "Kéo nhầm khối thì sao?" | Kéo nó ra khỏi đoàn tàu và thả về kho khối. Không có gì hỏng cả. |
| "Còi kêu được bài hát không?" | Được, nếu ghép nhiều khối nốt nhạc liên tiếp. Đó là thử thách sao vàng. |
| "Sao cùng 2 giây mà xe đội em đi ngắn hơn?" | Có thể pin yếu, bánh lỏng, hoặc sàn trơn. Đó là một Bác Bug cần điều tra. |
| "Máy tính có điều khiển xe mãi không?" | Khi nạp xong, chương trình nằm trong Bộ não. Rút cáp xe vẫn chạy. |

## Hiểu lầm thường gặp

- **"Kéo khối vào màn hình là robot chạy."** Khối phải gắn dưới sự kiện và phải bấm Chạy (hoặc nạp).
- **"Số càng to càng tốt."** Số to quá làm xe đi quá xa, đâm vào tường.
- **"Giây và bước giống nhau."** Giây đo thời gian, bước đo quãng đường.
- **"Chương trình chạy tất cả khối cùng lúc."** Bộ não chạy lần lượt từng khối, rất nhanh nhưng vẫn theo thứ tự.
- **"Còi kêu được là do có cái loa nhỏ hát."** Tiếng đến từ miếng kim loại rung.

## Phân hóa

### Lớp 1–3

- Chỉ dùng 4 khối: khi bắt đầu, tiến … giây, bật đèn, phát tiếng bíp.
- Kế hoạch trên giấy dùng mũi tên và số, không cần viết tên khối.
- Còi: chỉ cần phân biệt "cao" và "trầm".

### Lớp 4–5

- Thêm khối rẽ trái/phải có số giây và khối chờ.
- Yêu cầu ghi rõ đơn vị trong kế hoạch.
- Còi: giới thiệu từ "tần số", đơn vị Hz, ý "rung nhiều lần mỗi giây". Thử 2 tần số khác nhau và so sánh.
- Câu hỏi suy luận: "Nếu xe đi 1 ô mất 1 giây, đi 4 ô cần mấy giây?"

## Từ khóa của buổi

| Thuật ngữ | Nghĩa cho trẻ | Nghĩa chính xác |
| --- | --- | --- |
| Lập trình khối | Viết chương trình bằng cách ghép mảnh màu | Lập trình trực quan bằng các khối lệnh kéo thả |
| Khối lệnh | Một mảnh ghép là một lệnh | Đơn vị lệnh trong môi trường lập trình khối |
| Sự kiện | Đầu tàu, tiếng còi xuất phát | Khối kích hoạt chạy chuỗi lệnh khi điều kiện xảy ra (khởi động, bấm nút) |
| Tuần tự | Làm lần lượt từ trên xuống | Các lệnh thực hiện theo đúng thứ tự viết |
| Tham số | Con số trong ô của khối | Giá trị truyền vào lệnh để điều chỉnh hoạt động |
| Đơn vị | Giây hay bước | Đại lượng đo đi kèm con số (thời gian, quãng đường) |
| Còi buzzer | Chú chim hót | Linh kiện tạo âm nhờ màng rung khi có tín hiệu điện |
| Tần số | Rung nhanh hay chậm | Số dao động mỗi giây, đơn vị Hz; quyết định độ cao của âm |

## Ghi nhớ cuối bài

1. Mỗi khối là một lệnh. Ghép dưới "khi bắt đầu" thì mới chạy.
2. Bộ não đọc khối từ trên xuống, lần lượt từng khối.
3. Con số trong khối cho biết bao lâu hoặc bao xa. Nhìn kỹ đơn vị: giây hay bước.
4. Cùng số giây, pin yếu thì xe đi ngắn hơn. Luôn thử trước khi chọn số.
5. Còi kêu nhờ rung. Rung nhanh tiếng cao, rung chậm tiếng trầm.
