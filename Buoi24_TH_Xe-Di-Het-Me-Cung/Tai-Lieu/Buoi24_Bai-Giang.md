# Bài giảng – Buổi 24: Xe đi hết mê cung đen

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 12: Mê cung đen · Tuần 12

Mục tiêu của buổi: lắp cảm biến dò line, hiệu chỉnh trên sàn thật, lập trình xe bám vạch qua 3 mức (đoạn thẳng, đoạn cong, cả mê cung). Đây cũng là buổi **kiểm tra cuối Chặng 3**: mỗi em chỉ đúng khối điều kiện trong chương trình. Kết buổi mở Hộp Bí Ẩn số 3 và trao huy hiệu Thợ Săn Bug.

## Ôn lý thuyết 5 phút

| Câu hỏi | Đáp án |
| --- | --- |
| Giấy trắng hay đen dội lại nhiều ánh sáng? | Trắng. |
| Mắt mèo chiếu loại ánh sáng gì? | Ánh sáng hồng ngoại, mắt người không thấy. |
| Mắt mèo có biết màu đỏ, màu xanh không? | Không, chỉ biết sáng và tối. |
| Vì sao phải đo lại trước mỗi lần chạy? | Ánh sáng phòng, mặt sàn thay đổi làm cảm biến nhìn nhầm. |
| Luật bám vạch? | Thấy đen thì tiến, thấy trắng thì rẽ về phía vạch. |
| Vì sao không nên cho xe chạy nhanh? | Đến khúc cua không kịp rẽ, trượt khỏi vạch. |

## Hướng dẫn thực hành từng bước

### An toàn và chuẩn bị

- Tắt nguồn trước khi lắp cảm biến. Cầm đầu cắm, không kéo dây.
- Không đứng, không ngồi lên mê cung; giẫm làm bong băng dính.
- Mỗi đội chạy ở khu của mình, chờ lượt ở đoạn cả mê cung.
- Không chặn xe bằng tay khi bánh đang quay; muốn dừng thì nhấc xe lên.

### Bước 1 – Chiến thắng nhỏ: Mắt mèo mở mắt (10 phút)

**Làm gì:**

1. Gắn cảm biến dò line ở đầu xe, mặt nhìn xuống sàn, cách sàn đúng khoảng hướng dẫn của kit (thường vài mm đến 1–2 cm).
2. Cắm vào cổng vào theo nhãn. Bật nguồn.
3. Ghép chương trình hiện giá trị:

```text
khi bắt đầu
  lặp mãi
    hiện giá trị cảm biến dò line
```

4. Đẩy xe bằng tay qua lại trên vạch đen.

**Đạt khi:** Đèn báo trên cảm biến hoặc con số trên màn hình đổi rõ ràng giữa đen và trắng.

### Bước 2 – Hiệu chỉnh trên sàn thật (10 phút)

**Làm gì:**

1. Đặt cảm biến trên nền trắng của mê cung. Ghi số (hoặc trạng thái đèn).
2. Đặt cảm biến ngay trên vạch đen. Ghi số.
3. Nếu kit cho số: tính ngưỡng = (trắng + đen) ÷ 2. Nếu kit có núm vặn: vặn từ từ đến khi đèn báo bật trên đen, tắt trên trắng (hoặc ngược lại theo kit).

| Vị trí | Số đo |
| --- | --- |
| Trắng | ... |
| Đen | ... |
| Ngưỡng | ... |

**Vì sao:** Mê cung trong lớp có ánh sáng khác với chỗ thử ở bàn. Đo ngay trên sàn sẽ chạy thì mới chắc chắn.

**Đạt khi:** Đội có ngưỡng ghi trên phiếu, hoặc đèn báo phân biệt đúng đen/trắng.

### Bước 3 – Bám vạch qua 3 mức (35 phút)

**Làm gì:** Ghép chương trình bám vạch (xem phần giải thích). Chạy lần lượt:

| Mức | Đường | Đạt khi |
| --- | --- | --- |
| 1 | Đoạn thẳng dài 1 m | Xe đi hết đoạn, không rời vạch |
| 2 | Đoạn cong | Xe qua khúc cua, không rời vạch |
| 3 | Cả mê cung | Xe đi từ cửa vào tới cửa ra |

Quy tắc của đội:

- Trước mỗi lần chạy: đo lại cảm biến nếu đổi chỗ.
- Mỗi lần trượt: Thư ký ghi "trượt ở đâu, vì sao" vào sổ đội.
- Mỗi lần chỉ sửa **một** thứ: tốc độ, hướng rẽ, hoặc ngưỡng.

**Vì sao:** Đi từ dễ đến khó giúp tìm Bác Bug dễ hơn. Nếu xe trượt ở đoạn thẳng thì lỗi do cảm biến hoặc chương trình; nếu chỉ trượt ở khúc cua thì thường do tốc độ.

> **Thầy:** "Đội nào qua được mức 1 mới lên mức 2. Không vội. Kỹ sư giỏi đi từng bậc."

### Bước 4 – Kiểm tra cuối Chặng 3 (10 phút, làm song song)

Thầy đi từng đội. Mỗi em được hỏi riêng:

1. "Chỉ cho thầy khối điều kiện trong chương trình."
2. "Khi cảm biến thấy trắng, xe làm khối nào?"

Đạt: chỉ đúng khối Nếu – Thì và nói được nhánh nào chạy khi nào.

### Bước 5 – Báo cáo căn cứ, Hộp Bí Ẩn và dọn dẹp (20 phút)

- Mỗi đội cho xe chạy biểu diễn mức cao nhất đã đạt.
- Đọc 2 con Bug ghi trong sổ đội và cách đã sửa.
- Mở Hộp Bí Ẩn số 3. Trao huy hiệu Thợ Săn Bug cho em/đội bắt và sửa nhiều Bug nhất.
- Tô vùng sáng thứ 12 trên Bản đồ Hành trình.
- Tắt nguồn, tháo cảm biến, cất vào hộp.

## Giải thích chương trình từng khối

Chương trình mẫu bám mép phải của vạch, 1 cảm biến (tên khối thay theo phần mềm của trường):

```text
khi bắt đầu
  lặp mãi
    nếu cảm biến thấy đen thì
      tiến chậm
    không thì
      rẽ về phía vạch
```

| Dòng | Ý nghĩa |
| --- | --- |
| `khi bắt đầu` | Bấm Chạy thì bắt đầu. Đặt xe sao cho cảm biến nằm trên mép vạch. |
| `lặp mãi` | Kiểm tra Mắt mèo liên tục, rất nhiều lần mỗi giây. |
| `nếu cảm biến thấy đen thì` | Hỏi: dưới chân có phải vạch đen không? |
| `tiến chậm` | Đúng – còn trên vạch – đi tiếp, chậm để kịp phản ứng ở khúc cua. |
| `không thì` | Sai – dưới chân là trắng – xe đang lệch ra ngoài. |
| `rẽ về phía vạch` | Xoay nhẹ về phía vạch đen để tìm lại đường. Nếu bám mép phải của vạch thì vạch nằm bên trái, nên rẽ trái. |

Phiên bản lượn đều (xe đi zigzag mượt hơn), dành cho đội đã qua mức 1:

```text
khi bắt đầu
  lặp mãi
    nếu cảm biến thấy đen thì
      lượn sang phải   ← bánh trái quay nhanh, bánh phải chậm
    không thì
      lượn sang trái   ← bánh phải quay nhanh, bánh trái chậm
```

Xe luôn lắc qua lại quanh mép vạch: chạm đen lách ra, chạm trắng lách vào. Vì luôn có bánh quay tới trước nên xe không đứng lại.

### Chương trình 2 cảm biến (lớp 4–5, thử thách)

```text
khi bắt đầu
  lặp mãi
    nếu trái thấy trắng và phải thấy trắng thì
      tiến chậm
    nếu trái thấy đen thì
      rẽ trái
    nếu phải thấy đen thì
      rẽ phải
```

Vạch nằm giữa hai cảm biến. Cảm biến nào chạm đen tức là vạch đang lệch về phía đó, xe rẽ về phía đó.

### Các biến thể của Bác Bug để so sánh

**Bug 1 – Rẽ sai phía:**

```text
    không thì
      rẽ ra xa vạch
```

Thấy trắng mà lại rẽ ra xa: xe rời vạch ngay lần đầu và chạy mất. Sửa: xác định vạch ở bên nào của cảm biến, rẽ về phía đó.

**Bug 2 – Tiến nhanh:**

```text
    nếu cảm biến thấy đen thì
      tiến nhanh
```

Đoạn thẳng có thể vẫn qua, nhưng tới khúc cua xe trượt khỏi vạch vì không kịp rẽ. Sửa: giảm tốc độ.

**Bug 3 – Tiến có số giây:**

```text
    nếu cảm biến thấy đen thì
      tiến 1 giây
```

Trong 1 giây đó Bộ não không nhìn xuống. Xe "bịt mắt" chạy 1 giây và lạc. Sửa: dùng "tiến chậm" không có thời gian (hoặc thời gian rất ngắn).

**Bug 4 – Thiếu lặp mãi:** xe nhìn một lần lúc bắt đầu, rồi thôi. Sửa: bọc trong lặp mãi.

**Bug 5 – Chưa hiệu chỉnh:** chương trình đúng nhưng ngưỡng sai, Mắt mèo thấy sàn trắng là "đen". Xe chạy thẳng ra ngoài hoặc quay vòng tại chỗ. Sửa: đo lại ở Bước 2.

## Bảng xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
| --- | --- | --- |
| Xe quay vòng tròn tại chỗ | Cảm biến luôn báo trắng: ngưỡng sai, cảm biến quá cao, hoặc xe đặt lệch khỏi vạch | Hiệu chỉnh lại; hạ cảm biến; đặt xe sao cho cảm biến nằm trên mép vạch |
| Xe chạy thẳng bỏ đi | Cảm biến luôn báo đen (ngưỡng sai), hoặc rẽ sai phía | Hiệu chỉnh lại; đổi hướng rẽ |
| Đoạn thẳng qua, khúc cua trượt | Tốc độ cao, khúc cua gắt | Giảm tốc; rẽ mạnh hơn trong nhánh "không thì" |
| Xe lắc quá mạnh, gần như đứng yên | Mỗi lần lượn quá gắt | Giảm độ chênh tốc độ hai bánh |
| Chỗ có nắng xe chạy lung tung | Ánh sáng mạnh chiếu vào bộ thu | Che nắng; che cảm biến bằng một miếng bìa nhỏ quanh thân; hiệu chỉnh tại chỗ |
| Đèn báo cảm biến không đổi | Cắm sai cổng, lỏng dây, cảm biến quá cao | Tắt nguồn, cắm lại; chỉnh độ cao |
| Xe dừng giữa đường | Pin yếu, bánh kẹt bụi băng dính | Báo thầy thay pin; lau bánh |
| Băng dính bóng làm đo sai | Băng dính đen bóng phản xạ ánh sáng như gương | Dùng băng dính đen mờ hoặc giấy đen |

## Thử thách mở rộng

1. **Về đích có còi:** Đặt một vạch đen ngang ở cửa ra. Khi xe tới (lớp 4–5: hai cảm biến cùng thấy đen), dừng và phát tiếng bíp.
2. **Ai ổn định nhất:** Không phải ai nhanh nhất, mà đội nào chạy 3 lần liên tiếp đều qua mê cung.
3. **Lớp 4–5 – hai cảm biến:** Viết chương trình 2 cảm biến, so sánh với 1 cảm biến: xe có ít lắc hơn không?
4. **Kết hợp Dơi và Mắt mèo:** Đặt hộp giấy chắn giữa mê cung. Xe vừa bám vạch, vừa dừng khi thấy hộp. Gợi ý: kiểm tra khoảng cách trước, rồi mới kiểm tra vạch.

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Chỉ khối điều kiện trong chương trình. | Khối "nếu cảm biến thấy đen thì ... không thì ...". |
| Khi cảm biến thấy trắng, xe làm gì? Vì sao? | Rẽ về phía vạch, vì trắng nghĩa là xe đang lệch ra ngoài. |
| Vì sao xe đi ngoằn ngoèo? | Xe liên tục lách vào đen, lách ra trắng quanh mép vạch. |
| Đội em sửa Bác Bug nào ở khúc cua? | Thường là giảm tốc hoặc tăng góc rẽ. |
| Vì sao phải hiệu chỉnh ngay trên mê cung? | Ánh sáng và mặt sàn ở đó khác chỗ thử. |

## Ghi nhớ cuối bài

1. Gắn Mắt mèo nhìn xuống, gần sàn; luôn hiệu chỉnh ngay trên đường sẽ chạy.
2. Luật bám vạch: thấy đen thì tiến chậm, thấy trắng thì rẽ về phía vạch, trong lặp mãi.
3. Xe đi zigzag quanh mép vạch là bình thường.
4. Chậm và ổn định thắng nhanh và lạc.
5. Đi từ dễ đến khó (thẳng → cong → cả mê cung), mỗi lần sửa một thứ, ghi Bug vào sổ đội.
