# Bài giảng – Buổi 22: Xe tự dừng trước vật cản

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 11: Robot biết "nhìn thấy" · Tuần 11

Mục tiêu của buổi: lắp cảm biến siêu âm lên xe, đọc được khoảng cách, chọn ngưỡng bằng cách thử, và viết chương trình Nếu – Thì để xe tự dừng trước vật cản. Lớp 4–5 làm thêm: gặp vật thì lùi lại và rẽ.

## Ôn lý thuyết 5 phút

| Câu hỏi | Đáp án |
| --- | --- |
| Cảm biến siêu âm giống con vật nào? | Con dơi. |
| Cảm biến biết khoảng cách bằng cách nào? | Phát tiếng kêu rất cao, đo thời gian tiếng vọng quay về. |
| Tiếng vọng về nhanh nghĩa là gì? | Vật ở gần. |
| Vật nào đo tốt nhất? | Vật cứng, phẳng, đứng thẳng, quay mặt về cảm biến. |
| Nếu – Thì có mấy nhánh? Làm mấy nhánh cùng lúc? | Hai nhánh; chỉ làm một nhánh. |
| Vì sao đặt Nếu – Thì trong Lặp mãi? | Để robot kiểm tra liên tục. |

## Hướng dẫn thực hành từng bước

### An toàn

- Tắt nguồn trước khi cắm cảm biến. Cầm đầu cắm, không kéo dây.
- Gắn cảm biến chắc, mặt nhìn thẳng về phía trước, không chúc xuống sàn.
- Khi thử xe dừng, dùng hộp giấy làm vật cản, **không dùng tay hay chân bạn** làm vật cản khi xe đang chạy.
- Luôn có một bạn sẵn sàng nhấc xe lên nếu xe không dừng.

### Bước 1 – Chiến thắng nhỏ: con số biết nhảy (10 phút)

**Làm gì:**

1. Tắt nguồn, cắm cảm biến vào **cổng vào** theo nhãn màu.
2. Gắn cảm biến ở đầu xe, mặt nhìn thẳng.
3. Ghép chương trình hiện số:

```text
khi bắt đầu
  lặp mãi
    hiện khoảng cách
```

4. Bật nguồn, chạy. Đưa bàn tay từ xa lại gần cảm biến.

**Vì sao:** Các em thấy tận mắt cảm biến "nói chuyện" với Bộ não bằng con số.

**Đạt khi:** Số trên màn hình (máy tính hoặc màn LED của bo) nhỏ dần khi tay lại gần, lớn dần khi tay ra xa.

### Bước 2 – Đo ba khoảng cách (15 phút)

**Làm gì:**

1. Đặt hộp giấy phẳng trước cảm biến ở ba vị trí: **gần** (khoảng 1 gang tay), **vừa** (khoảng 1 thước kẻ 30 cm), **xa** (khoảng 1 sải tay).
2. Đọc số cảm biến báo. Dùng thước đo khoảng cách thật. Ghi cả hai vào phiếu.
3. Thử thêm: gối bông, tấm bìa đặt xiên. Ghi nhận xét.

| Vật | Khoảng cách thật (thước) | Cảm biến báo | Nhận xét |
| --- | --- | --- | --- |
| Hộp giấy – gần | ... cm | ... | |
| Hộp giấy – vừa | ... cm | ... | |
| Hộp giấy – xa | ... cm | ... | |
| Gối bông | ... cm | ... | Có đúng không? |
| Bìa xiên | ... cm | ... | Có đúng không? |

**Vì sao:** Kỹ sư phải biết cảm biến đo đúng đến đâu trước khi tin vào nó.

**Đạt khi:** Đội nói được: "Với hộp giấy, cảm biến đo gần đúng. Với gối bông/bìa xiên, cảm biến đo sai hoặc không thấy."

### Bước 3 – Viết Nếu – Thì và chọn ngưỡng (25 phút)

**Làm gì:**

1. Ghép chương trình tự dừng (xem mục giải thích bên dưới), ngưỡng ban đầu 15 cm.
2. Đặt hộp giấy cách xe 1 m. Chạy. Đo khoảng cách từ đầu xe tới hộp khi xe dừng hẳn.
3. Thử ngưỡng 5 cm, 15 cm, 30 cm. Ghi bảng:

| Ngưỡng | Xe dừng cách hộp | Có chạm hộp không? |
| --- | --- | --- |
| 5 cm | ... | |
| 15 cm | ... | |
| 30 cm | ... | |

4. Cả đội chọn ngưỡng tốt nhất và giải thích vì sao.

**Vì sao:** Xe không dừng ngay lập tức. Từ lúc Bộ não ra lệnh dừng đến lúc bánh xe ngừng hẳn, xe còn trôi một đoạn. Ngưỡng quá nhỏ thì xe chạm hộp. Ngưỡng quá lớn thì xe dừng quá xa, không tới gần được.

**Đạt khi:** Xe dừng trước hộp, không chạm, cách hộp không quá một gang tay.

> **Thầy:** "Không có con số nào đúng cho mọi xe. Kỹ sư chọn số bằng cách thử, đo và ghi lại."

### Bước 4 – Lớp 4–5: lùi và rẽ (10 phút)

**Làm gì:** Thêm khối "lùi 0,5 giây" và "rẽ trái 0,5 giây" vào nhánh "thì", sau khối dừng. Đặt vài hộp giấy rải rác. Xe tự đi lang thang và né vật.

**Đạt khi:** Xe gặp hộp thì lùi, rẽ rồi đi tiếp, không đâm.

### Bước 5 – Báo cáo căn cứ và dọn dẹp (15 phút)

- Mỗi đội báo cáo ngưỡng đã chọn và lý do.
- Kể một con Bác Bug.
- Thầy hé lộ: "Con Bug to nhất đang trốn trong mê cung đen tuần sau."
- Tắt nguồn, rút cảm biến bằng cách cầm đầu cắm, cất vào hộp.

## Giải thích chương trình từng khối

Chương trình mẫu (tên khối thay theo phần mềm của trường):

```text
khi bắt đầu
  lặp mãi
    nếu khoảng cách < 15 cm thì
      dừng
    không thì
      tiến
```

| Dòng | Ý nghĩa |
| --- | --- |
| `khi bắt đầu` | Đầu tàu: bấm Chạy thì bắt đầu. |
| `lặp mãi` | Bộ não lặp lại phần bên trong không ngừng, rất nhiều lần mỗi giây. |
| `nếu khoảng cách < 15 cm thì` | Hỏi Dơi: vật phía trước có gần hơn 15 cm không? Câu trả lời chỉ là Đúng hoặc Sai. |
| `dừng` | Nhánh Đúng: vật đã gần, dừng động cơ. |
| `không thì` | Bắt đầu nhánh Sai. |
| `tiến` | Nhánh Sai: đường còn trống, cho động cơ chạy tiến. Khối "tiến" ở đây không có số giây: xe cứ chạy cho đến lần kiểm tra sau. |

Hình dung dòng thời gian: lần 1 hỏi, xa → tiến; lần 2 hỏi, xa → tiến; ... lần thứ 100 hỏi, gần → dừng; lần 101 hỏi, vẫn gần → vẫn dừng. Nếu ai nhấc hộp đi, lần hỏi sau sẽ thấy xa → xe đi tiếp.

### Chương trình lớp 4–5

```text
khi bắt đầu
  lặp mãi
    nếu khoảng cách < 15 cm thì
      dừng
      lùi 0,5 giây
      rẽ trái 0,5 giây
    không thì
      tiến
```

Nhánh "thì" giờ có 3 khối chạy lần lượt: dừng, lùi để có chỗ quay, rẽ sang hướng mới. Sau đó vòng lặp quay lại hỏi Dơi.

### Các biến thể của Bác Bug để so sánh

**Bug 1 – Điều kiện đặt ngược:**

```text
    nếu khoảng cách > 15 cm thì
      dừng
    không thì
      tiến
```

Xe đứng yên khi đường trống, và chỉ chạy khi có vật ở gần. Nó lao vào tường! Sửa: đổi `>` thành `<`, hoặc đổi chỗ "dừng" và "tiến".

**Bug 2 – Thiếu lặp mãi:**

```text
khi bắt đầu
  nếu khoảng cách < 15 cm thì
    dừng
  không thì
    tiến
```

Bộ não chỉ hỏi một lần lúc bắt đầu. Đường trống nên xe tiến – rồi chương trình hết. Tùy phần mềm, xe đứng luôn hoặc chạy mãi không bao giờ kiểm tra lại. Sửa: bọc trong lặp mãi.

**Bug 3 – Ngưỡng quá nhỏ:** "nếu khoảng cách < 3 cm". Xe trôi quá đà và chạm hộp. Sửa: tăng ngưỡng.

**Bug 4 – "Tiến 2 giây" trong nhánh không thì:** xe mỗi lần tiến 2 giây liền mới hỏi lại Dơi. Trong 2 giây đó xe "bịt mắt" và có thể đâm. Sửa: dùng "tiến" không có thời gian, hoặc thời gian rất ngắn.

## Bảng xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
| --- | --- | --- |
| Số khoảng cách luôn bằng 0 hoặc không đổi | Cảm biến cắm sai cổng, lỏng dây, chương trình đọc sai cổng | Tắt nguồn, cắm lại đúng cổng vào; kiểm tra cổng trong khối |
| Số nhảy lung tung | Có vật lộn xộn phía trước, cảm biến gắn lỏng rung lắc, hai đội đo sát nhau | Dọn khoảng trống trước xe; siết cảm biến; các đội cách xa nhau |
| Xe đâm vào hộp | Ngưỡng nhỏ quá; xe chạy nhanh trôi quá đà; vật mềm/xiên | Tăng ngưỡng; dùng hộp phẳng đứng thẳng |
| Xe đứng im khi đường trống | Điều kiện đặt ngược; cảm biến chúc xuống đo trúng sàn | Kiểm tra `<`/`>`; chỉnh cảm biến nhìn thẳng |
| Xe dừng rồi không đi tiếp khi bỏ hộp | Thiếu lặp mãi; nhánh không thì trống | Bọc trong lặp mãi; thêm "tiến" vào không thì |
| Xe không thấy chân bàn | Vật quá nhỏ, mảnh | Bình thường với cảm biến siêu âm; dùng vật to phẳng khi thử |
| Lớp 4–5: xe lùi rồi rẽ mãi tại chỗ | Rẽ chưa đủ, cảm biến vẫn thấy vật | Tăng thời gian rẽ hoặc lùi |

## Thử thách mở rộng

1. **Còi báo động:** Khi gặp vật, xe dừng và phát tiếng bíp.
2. **Cảm biến lùi xe ô tô:** Xe đứng yên. Vật càng gần, còi kêu càng nhanh. Gợi ý: hai điều kiện "< 30" và "< 10" với khoảng chờ khác nhau.
3. **Lớp 4–5 – Robot đi theo:** Nếu vật xa hơn 20 cm thì tiến; nếu gần hơn 10 cm thì lùi; ở giữa thì dừng. Xe sẽ "đi theo" tấm bìa trong tay bạn.
4. **Dự đoán:** Nếu cầm gối bông làm vật cản, xe sẽ dừng hay đâm? Thử và giải thích.

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Ngưỡng đội em chọn là bao nhiêu? Vì sao? | Ví dụ 15 cm: nhỏ hơn thì xe chạm hộp do trôi quá đà, lớn hơn thì dừng quá xa. |
| Vì sao xe vẫn trôi một đoạn sau lệnh dừng? | Xe đang chạy có đà, cần thời gian để bánh dừng hẳn. |
| Đổi `<` thành `>` thì xe làm gì? | Đứng im khi đường trống, lao tới khi có vật gần. |
| Vì sao cảm biến đo gối bông kém? | Vật mềm nuốt tiếng vọng. |
| Bỏ lặp mãi thì sao? | Bộ não chỉ hỏi một lần, không còn biết vật xuất hiện sau đó. |

## Ghi nhớ cuối bài

1. Cảm biến cắm vào cổng vào; luôn kiểm tra con số trước khi viết điều kiện.
2. Ngưỡng được chọn bằng cách thử, đo và ghi lại.
3. Xe cần một quãng để dừng hẳn, nên ngưỡng không được quá nhỏ.
4. Nếu – Thì phải nằm trong Lặp mãi để robot luôn để ý.
5. Điều kiện đặt ngược là Bác Bug nguy hiểm: xe lao vào chỗ cần tránh.
