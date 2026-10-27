# Bài giảng – Buổi 20: Xe chạy hình vuông, đèn nhạc theo vòng lặp

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 10: Phép thuật "Lặp" · Tuần 10

Mục tiêu của buổi: dùng khối lặp để (1) cho đèn nháy nhiều lần, (2) cho xe chạy đúng hình vuông, (3) soạn một điệu nhảy đèn và còi có điệp khúc. Cuối buổi trao giải "Kỹ sư lười thông minh" cho chương trình ngắn nhất mà vẫn đúng.

## Ôn lý thuyết 5 phút

| Câu hỏi | Đáp án |
| --- | --- |
| Vòng lặp dùng để làm gì? | Làm lại một nhóm lệnh nhiều lần mà không phải viết lại. |
| Lệnh bên trong hộp Lặp gọi là gì? | Thân vòng lặp. |
| Hình vuông cần lặp mấy lần [tiến, rẽ]? | 4 lần. |
| Lệnh nằm dưới hộp "lặp 4 lần" chạy mấy lần? | 1 lần, sau khi lặp xong. |
| Lệnh nằm dưới hộp "lặp mãi" có chạy không? | Không. |
| Muốn dừng "lặp mãi" thì làm gì? | Bấm Dừng hoặc tắt nguồn. |

## Hướng dẫn thực hành từng bước

### An toàn và chia vai

- Vai: Kỹ sư lập trình, Kỹ sư cơ khí, Thư ký. Đổi vai bằng đồng hồ cát mỗi 10 phút.
- Xe chạy trong khu hình vuông dán sàn. Không để xe chạy ra lối đi.
- Chương trình có "lặp mãi" phải biết trước cách dừng: bấm Dừng hoặc nhấc xe lên và tắt công tắc.
- Luật "giờ hót": còi tối đa 10 giây mỗi lượt.

### Bước 1 – Chiến thắng nhỏ: đèn nháy 5 lần (10 phút)

**Làm gì:** Ghép chương trình:

```text
khi bắt đầu
  lặp 5 lần
    bật đèn
    chờ 0,5 giây
    tắt đèn
    chờ 0,5 giây
```

Bấm Chạy, cả đội đếm số lần nháy.

**Vì sao:** Đèn nháy là ví dụ dễ thấy nhất của vòng lặp. Nhờ khối "chờ", mắt người mới kịp thấy đèn sáng và tắt.

**Đạt khi:** Đèn nháy đúng 5 lần rồi tắt hẳn.

> **Thầy:** "Bỏ hai khối 'chờ' ra thử xem. Đèn còn nháy không? Bộ não chạy nhanh quá, mắt mình không kịp thấy."

### Bước 2 – Xe đi hình vuông bằng 8 lệnh (10 phút)

**Làm gì:** Viết chương trình hình vuông **không dùng vòng lặp**: tiến – rẽ – tiến – rẽ – tiến – rẽ – tiến – rẽ. Dùng con số "rẽ góc vuông" đã đo ở buổi 18. Chạy thử.

**Vì sao:** So sánh để thấy giá trị của vòng lặp. Đếm số khối: 9 khối (cả khối "khi bắt đầu").

**Đạt khi:** Xe đi gần đúng hình vuông và về gần vạch xuất phát.

### Bước 3 – Viết lại bằng vòng lặp và chỉnh góc (25 phút)

**Làm gì:**

1. Xóa chương trình 8 lệnh. Ghép chương trình mới bằng "lặp 4 lần".
2. Chạy thử. Quan sát: xe có về đúng chỗ cũ không? Góc có vuông không?
3. Nếu góc thiếu hoặc thừa, **chỉ sửa một con số** trong khối rẽ. Chạy lại.
4. Thư ký ghi bảng thử:

| Lần thử | Số giây rẽ | Xe về cách vạch xuất phát |
| --- | --- | --- |
| 1 | 0,5 | ... cm |
| 2 | ... | ... cm |

**Vì sao:** Ở chương trình 8 lệnh, muốn chỉnh góc phải sửa 4 chỗ. Ở chương trình vòng lặp, chỉ sửa 1 chỗ. Đây là ích lợi lớn của vòng lặp: **dễ sửa**.

**Đạt khi:** Xe đi hình vuông và về cách vạch xuất phát không quá một bàn tay.

### Bước 4 – Giải Kỹ sư lười thông minh (10 phút)

**Làm gì:** Mỗi đội đếm số khối trong chương trình hình vuông đúng của mình. Thầy kiểm tra xe chạy đúng rồi ghi số khối lên bảng. Đội ít khối nhất mà vẫn đúng nhận giải.

> **Thầy:** "Lười kiểu này là lười thông minh. Ít khối thì ít chỗ cho Bác Bug trốn."

### Bước 5 – Điệu nhảy đèn và còi (15 phút)

**Làm gì:** Mỗi đội soạn một điệu nhảy có điệp khúc. Gợi ý cấu trúc:

```text
khi bắt đầu
  lặp 3 lần          ← điệp khúc
    bật đèn
    phát nốt cao
    tắt đèn
    phát nốt trầm
  rẽ phải 1 giây     ← xe xoay một vòng kết thúc
```

**Vì sao:** Các em sáng tạo với vòng lặp, không chỉ dùng nó để đi hình.

**Đạt khi:** Điệu nhảy có ít nhất một vòng lặp, dài không quá 10 giây (luật "giờ hót").

### Bước 6 – Báo cáo căn cứ và dọn dẹp (15 phút)

- Mỗi đội biểu diễn điệu nhảy.
- Báo cáo: số giây rẽ đúng của xe, số khối của chương trình hình vuông, một con Bác Bug đã bắt.
- Tắt nguồn, cất xe.

## Giải thích chương trình từng khối

Chương trình mẫu hình vuông (tên khối thay theo phần mềm của trường):

```text
khi bắt đầu
  lặp 4 lần
    tiến 1 giây
    rẽ phải 0,5 giây
  phát tiếng bíp
```

| Dòng | Ý nghĩa |
| --- | --- |
| `khi bắt đầu` | Đầu tàu. Bấm Chạy thì chương trình bắt đầu. |
| `lặp 4 lần` | Mở hộp Lặp. Bộ não sẽ chạy thân vòng lặp 4 lần. |
| `tiến 1 giây` | Thân vòng lặp, lệnh 1: đi thẳng, tạo một cạnh của hình vuông. Đổi số này thì cạnh dài hay ngắn. |
| `rẽ phải 0,5 giây` | Thân vòng lặp, lệnh 2: xoay sang phải một góc vuông. Đổi số này thì góc to hay nhỏ. |
| `phát tiếng bíp` | Nằm ngoài hộp. Chạy 1 lần khi xe đi xong hình vuông: báo "xong rồi". |

Bộ não chạy theo thứ tự: tiến, rẽ (lần 1) → tiến, rẽ (lần 2) → tiến, rẽ (lần 3) → tiến, rẽ (lần 4) → bíp → hết.

### Các biến thể của Bác Bug để so sánh

**Bug 1 – Khối rơi ra ngoài vòng lặp:**

```text
khi bắt đầu
  lặp 4 lần
    tiến 1 giây
  rẽ phải 0,5 giây
```

Khối rẽ nằm ngoài hộp. Xe đi thẳng 4 giây (4 lần tiến liền nhau) rồi rẽ một lần. Kết quả: một đường thẳng dài. Sửa: kéo khối rẽ vào trong hộp, thẳng hàng với khối tiến.

**Bug 2 – Lặp mãi thay vì lặp 4 lần:**

```text
khi bắt đầu
  lặp mãi
    tiến 1 giây
    rẽ phải 0,5 giây
  phát tiếng bíp
```

Xe đi hình vuông hết vòng này đến vòng khác, không bao giờ kêu bíp. Sửa: dùng "lặp 4 lần".

**Bug 3 – Sai số lần lặp:**

```text
  lặp 3 lần
```

Xe đi 3 cạnh, không khép kín, dừng ở góc thứ tư. Sửa: đổi thành 4.

**Bug 4 – Góc không vuông:** "rẽ phải 0,3 giây" làm xe xoay thiếu. Sau 4 lần, đường đi xoắn thành hình lệch, không về chỗ cũ. Sai số nhỏ ở mỗi góc cộng dồn qua 4 lần lặp. Sửa: tăng số giây rẽ từng chút một.

## Bảng xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
| --- | --- | --- |
| Đèn sáng liên tục, không thấy nháy | Thiếu khối "chờ" nên bật/tắt quá nhanh | Thêm "chờ 0,5 giây" sau bật và sau tắt |
| Xe đi một đường thẳng dài | Khối rẽ nằm ngoài vòng lặp | Kéo khối rẽ vào trong thân vòng lặp |
| Xe đi mãi không dừng | Dùng "lặp mãi" | Đổi sang "lặp 4 lần" |
| Hình bị xoắn, không về chỗ cũ | Góc rẽ thiếu hoặc thừa; sai số cộng dồn | Chỉnh số giây rẽ; đánh dấu và đặt xe đúng hướng khi xuất phát |
| Hình lệch, cạnh này dài cạnh kia ngắn | Bánh trượt, sàn không đều, pin yếu dần | Chạy trên mặt thảm phẳng; báo thầy thay pin |
| Lần chạy đầu đúng, lần sau sai | Pin yếu dần nên góc rẽ nhỏ đi | Đo lại số giây rẽ, ghi chú pin |
| Còi kêu quá lâu | Còi nằm trong vòng lặp nhiều lần, mỗi lần kêu lâu | Rút ngắn thời gian nốt, giảm số lần lặp |

## Thử thách mở rộng

1. **Hình vuông to:** Đổi số giây tiến từ 1 lên 2. Hình to gấp mấy lần? Có cần đổi góc rẽ không? (Không; chỉ cạnh dài hơn.)
2. **Hai vòng:** Cho xe đi hình vuông 2 vòng mà không thêm khối nào, chỉ đổi một con số. (Lặp 8 lần.)
3. **Lặp lồng nhau (lớp 4–5):** "Lặp 2 lần [lặp 4 lần [tiến, rẽ], phát tiếng bíp]". Đoán: còi kêu mấy lần? (2 lần.)
4. **Tam giác (lớp 4–5):** Lặp 3 lần với góc rẽ lớn hơn. Thử tìm số giây rẽ để xe khép thành tam giác. Gợi ý: góc tam giác đều cần xe xoay 120°, gần gấp rưỡi góc vuông.

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Chương trình hình vuông không có vòng lặp cần mấy khối? Có vòng lặp cần mấy? | Khoảng 9 khối so với 4 khối. |
| Muốn chỉnh góc, chương trình nào dễ sửa hơn? Vì sao? | Chương trình vòng lặp, vì chỉ sửa một chỗ. |
| Vì sao đèn cần khối "chờ" mới thấy nháy? | Bộ não chạy quá nhanh, mắt không kịp thấy. |
| Nếu khối rẽ nằm ngoài hộp Lặp thì xe làm gì? | Đi thẳng dài rồi rẽ một lần. |
| Số giây rẽ đúng của xe đội em là bao nhiêu? | Học sinh đọc theo bảng thử. |

## Ghi nhớ cuối bài

1. Khối nằm **bên trong** hộp Lặp mới được làm lại.
2. Vòng lặp làm chương trình ngắn hơn và dễ sửa hơn: sửa một chỗ, tác dụng cả 4 lần.
3. Sai số nhỏ trong thân vòng lặp sẽ cộng dồn qua mỗi lần lặp.
4. Đèn nháy cần khối "chờ" để mắt kịp thấy.
5. "Lặp mãi" không bao giờ tự dừng; khối bên dưới nó không bao giờ chạy.
