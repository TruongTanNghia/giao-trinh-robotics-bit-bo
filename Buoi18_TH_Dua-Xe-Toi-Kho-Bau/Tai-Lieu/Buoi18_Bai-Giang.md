# Bài giảng – Buổi 18: Đưa xe tới kho báu

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 9: Bản đồ kho báu · Tuần 9

Mục tiêu của buổi: mỗi đội ghép 1–5 khối để xe tự đi từ ô xuất phát tới kho báu, có còi và đèn báo hiệu khi tới nơi. Trước mỗi lần bấm Chạy, đội phải ghi dự đoán. Kỹ năng trọng tâm: **chọn con số bằng cách thử và đo**.

## Ôn lý thuyết 5 phút

| Câu hỏi | Đáp án |
| --- | --- |
| Khối "khi bắt đầu" có vai trò gì? | Đầu tàu: các khối gắn bên dưới mới chạy. |
| Bộ não đọc khối thế nào? | Từ trên xuống, lần lượt từng khối. |
| "Tiến 2 giây" và "tiến 2 bước" khác nhau ở đâu? | Một cái tính thời gian, một cái tính quãng đường. |
| Pin yếu thì "tiến 2 giây" đi xa hơn hay ngắn hơn? | Ngắn hơn. |
| Còi kêu nhờ gì? | Miếng kim loại bên trong rung. |
| Luật "giờ hót"? | Còi kêu tối đa 10 giây mỗi lượt. |

## Hướng dẫn thực hành từng bước

### An toàn và chia vai

- Mỗi đội 3 vai, đổi bằng đồng hồ cát mỗi 10 phút: **Kỹ sư lập trình** (cầm chuột), **Kỹ sư cơ khí** (đặt xe, kiểm tra dây), **Thư ký** (ghi dự đoán và kết quả).
- Xe chỉ chạy trên thảm, không chạy trên bàn (tránh rơi).
- Không giữ bánh xe khi động cơ quay. Muốn dừng gấp: nhấc xe lên khỏi sàn hoặc bấm Dừng.
- Còi kêu tối đa 10 giây.

### Bước 1 – Chiến thắng nhỏ (10 phút)

**Làm gì:** Kết nối máy tính với xe. Ghép 2 khối dưới "khi bắt đầu": "bật đèn" và "phát tiếng bíp". Bấm Chạy.

**Vì sao:** Kiểm tra mọi thứ đã thông: máy tính – bo mạch – đèn – còi. Nếu bước này lỗi, sửa trước khi đi tiếp.

**Đạt khi:** Đèn sáng và còi kêu.

### Bước 2 – Đo "1 ô mất bao nhiêu giây" (15 phút)

**Làm gì:**

1. Đặt xe ở vạch đầu một hàng ô. Chương trình: "tiến 1 giây". Chạy, đếm xe đi được mấy ô.
2. Thử "tiến 2 giây". Đếm lại.
3. Thử khối rẽ: "rẽ phải 0,5 giây". Xem xe quay được bao nhiêu (một góc vuông, ít hơn hay nhiều hơn).
4. Chỉnh số rẽ cho đến khi xe quay đúng một góc vuông. Ghi lại con số.

**Vì sao:** Đây là bước "hiệu chỉnh". Mỗi xe một khác, mỗi mặt sàn một khác. Kỹ sư thật luôn đo trước rồi mới tính.

**Đạt khi:** Thư ký ghi được 2 con số: "tiến 1 ô = ... giây" và "rẽ góc vuông = ... giây".

> **Thầy:** "Số này là bí mật riêng của xe đội em. Đội bên cạnh có thể có số khác. Không ai sai cả."

### Bước 3 – Từ kế hoạch giấy sang khối trên máy (25 phút)

**Làm gì:**

1. Lấy kế hoạch giấy ở buổi 17. Sửa con số theo kết quả đo ở bước 2.
2. Ghép khối theo kế hoạch.
3. **Trước khi bấm Chạy**, Thư ký ghi vào phiếu: "Em đoán xe dừng ở ô ...".
4. Chạy. Ghi ô xe dừng thật.
5. Nếu sai, cả đội tìm khối gây sai, sửa **một chỗ duy nhất**, rồi chạy lại.

**Vì sao:** Đoán trước giúp các em nghĩ trước khi làm. Sửa một chỗ mỗi lần giúp biết chính xác chỗ nào có tác dụng.

**Đạt khi:** Xe dừng ở ô kho báu (lệch nửa ô vẫn tính đạt), đèn sáng, còi kêu.

### Bước 4 – Thử thách sao vàng: vòng qua vật cản (10 phút, đội xong sớm)

**Làm gì:** Thầy đặt một vật cản trên đường thẳng tới kho báu. Đội vẽ đường vòng mới, viết chương trình và chạy.

**Đạt khi:** Xe tới kho báu mà không chạm vật cản.

### Bước 5 – Báo cáo căn cứ và dọn dẹp (15 phút)

- Mỗi đội chiếu chương trình lên, đọc từng khối và chỉ đường đi trên thảm.
- Kể một con Bác Bug đã bắt.
- Tắt nguồn, cất xe, gom dây.

## Giải thích chương trình từng khối

Chương trình mẫu (con số là ví dụ; mỗi đội dùng con số đã đo; tên khối thay theo phần mềm của trường):

```text
khi bắt đầu
  tiến 2 giây
  rẽ phải 0,5 giây
  tiến 1 giây
  bật đèn
  phát tiếng bíp
```

| Dòng | Bộ não làm gì | Xe làm gì |
| --- | --- | --- |
| `khi bắt đầu` | Bắt đầu đọc chương trình khi bấm Chạy | Chưa động đậy |
| `tiến 2 giây` | Bật cả hai động cơ quay tiến, đếm 2 giây, rồi dừng động cơ | Đi thẳng khoảng 2 ô (tùy xe) |
| `rẽ phải 0,5 giây` | Cho hai bánh quay ngược nhau (hoặc một bánh quay, một bánh đứng) trong 0,5 giây | Xoay tại chỗ sang phải khoảng một góc vuông |
| `tiến 1 giây` | Bật động cơ tiến 1 giây | Đi thẳng thêm khoảng 1 ô |
| `bật đèn` | Gửi lệnh qua cổng ra tới đèn | Đèn sáng: "Tới nơi rồi!" |
| `phát tiếng bíp` | Gửi tín hiệu rung tới còi | Còi kêu |

Vì sao xe rẽ được: xe có hai bánh do hai động cơ kéo. Hai bánh cùng quay tiến thì đi thẳng. Bánh trái quay tiến, bánh phải quay lùi thì xe xoay sang phải tại chỗ. Thời gian xoay càng lâu, góc xoay càng lớn.

### Các biến thể của Bác Bug để so sánh

**Bug 1 – Số quá lớn:**

```text
khi bắt đầu
  tiến 20 giây
```

Xe đi quá xa, đâm vào tường. Có thể là gõ nhầm "2" thành "20". Sửa: đọc to từng con số trước khi bấm Chạy.

**Bug 2 – Sai hướng rẽ:**

```text
khi bắt đầu
  tiến 2 giây
  rẽ trái 0,5 giây
  tiến 1 giây
```

Xe tới ô bên trái kho báu. Mẹo: đứng sau lưng xe, nhìn theo hướng xe, tay phải là bên phải của xe.

**Bug 3 – Rẽ không đủ góc:**

```text
  rẽ phải 0,2 giây
```

Xe chỉ xoay một chút rồi đi chéo. Sửa: thử tăng dần 0,3 – 0,4 – 0,5 giây đến khi đủ góc vuông.

**Bug 4 – Quên kết nối hoặc quên bấm Chạy:** màn hình có chương trình đúng nhưng xe đứng im. Kiểm tra biểu tượng kết nối trước.

## Bảng xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
| --- | --- | --- |
| Bấm Chạy, xe đứng im | Chưa kết nối, chưa nạp, hoặc khối không gắn vào "khi bắt đầu" | Kiểm tra biểu tượng kết nối; kéo khối gắn lại vào đầu tàu |
| Xe đi quá xa | Con số giây quá lớn, hoặc đổi sang pin mới mạnh hơn | Giảm số, đo lại "1 ô = ... giây" |
| Xe đi thiếu | Pin yếu, sàn trơn, con số nhỏ | Báo thầy kiểm tra pin; tăng số giây một chút |
| Xe đi chéo khi lệnh là tiến | Bánh lỏng, một động cơ yếu hơn, bánh dính tóc/bụi | Lắc kiểm tra bánh, lau bánh; đặt xe thẳng hàng khi xuất phát |
| Xe rẽ sai bên | Nhầm trái/phải, hoặc động cơ cắm đảo | Đứng sau lưng xe để xác định; nếu cả hai rẽ đều ngược, đổi dây động cơ |
| Còi không kêu | Còi cắm sai cổng, âm lượng 0, khối âm thanh chưa gắn | Kiểm tra cổng và khối |
| Lần 1 đúng, lần 2 sai | Đặt xe xuất phát lệch, hoặc pin yếu dần | Đánh dấu vị trí và hướng xuất phát bằng băng dính |

## Thử thách mở rộng

1. **Ít khối nhất:** Ai tới kho báu với ít khối nhất? (Gợi ý cho buổi sau: vòng lặp.)
2. **Còi chiến thắng:** Ghép 3 khối nốt nhạc khác nhau thành tiếng "tới nơi" của đội.
3. **Về nhà:** Sau khi tới kho báu, xe quay đầu và trở về ô xuất phát.
4. **Lớp 4–5:** Tính trước trên giấy: nếu 1 ô = 1 giây, đường đi 3 ô – rẽ – 2 ô cần tổng bao nhiêu giây chạy thẳng? Viết chương trình đúng ngay lần đầu.

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Vì sao phải đo "1 ô mất bao nhiêu giây" trước? | Mỗi xe, mỗi sàn khác nhau; đo trước thì chọn số đúng. |
| Xe rẽ phải bằng cách nào? | Hai bánh quay khác nhau làm xe xoay sang phải. |
| Dự đoán của đội lần 1 có đúng không? Lần cuối? | Học sinh kể theo phiếu; nhấn mạnh dự đoán gần đúng dần. |
| Bác Bug của đội là loại nào? | Số quá lớn/nhỏ, rẽ sai bên, quên kết nối... |
| Vì sao mỗi lần chỉ sửa một chỗ? | Để biết chỗ nào thật sự sửa được lỗi. |

## Ghi nhớ cuối bài

1. Trước khi viết chương trình, đo xe: 1 ô mất bao nhiêu giây, rẽ góc vuông mất bao nhiêu giây.
2. Luôn ghi dự đoán trước khi bấm Chạy.
3. Mỗi lần sửa một chỗ, rồi thử lại.
4. Xe rẽ được vì hai bánh quay khác nhau.
5. Đứng sau lưng xe để phân biệt trái và phải của xe.
