# Bài giảng – Buổi 6: Thám tử mạch điện

> **Thực hành · 90 phút** · Chặng 1: Đánh thức Bít-Bô · Nhiệm vụ 3: Bí ẩn bóng đèn không sáng · Tuần 3

Buổi cuối của Chặng 1. Lần đầu các em **tự lắp mạch từ các linh kiện rời**: hộp pin – công tắc – đèn LED – dây nối. Sau đó các em trở thành thám tử, điều tra 3 mạch bị Bác Bug phá, và làm bài kiểm tra cuối chặng: sửa một mạch lỗi trong 3 phút. Đây là buổi đặt nền cho kỹ năng gỡ lỗi (debug) dùng suốt khóa học.

**Mục tiêu buổi học**
- Tự lắp mạch pin – công tắc – LED cho đèn sáng.
- Tìm lỗi theo thứ tự: pin – công tắc – dây – LED.
- Dự đoán trước khi đổi chiều LED, rồi kiểm tra.
- Qua bài kiểm tra cuối Chặng 1.

**Chuẩn bị**
- Mỗi đội: hộp pin 2 viên AA (3 V, đã lắp pin, có công tắc riêng hoặc công tắc rời), mô-đun LED có điện trở hoặc LED rời kèm điện trở 100–220 Ω, 3–4 dây nối.
- 3 mạch lỗi đánh số, mỗi đội một bộ hoặc đặt thành 3 "trạm":
  - **Mạch 1:** một dây tháo hờ.
  - **Mạch 2:** công tắc tắt.
  - **Mạch 3:** pin lắp ngược một viên.
- Phiếu thám tử và hình dán (pin, công tắc, dây).
- Nhãn chiều lắp dán lên LED (chấm đỏ ở chân dài).
- 4–5 mạch lỗi khác nhau cho bài kiểm tra cuối chặng.
- Đồng hồ cát hoặc đồng hồ bấm giờ 3 phút.

---

## Ôn lý thuyết 5 phút

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Đèn chỉ sáng khi mạch thế nào? | Mạch kín: điện đi liền một vòng. |
| Chân dài của LED là chân gì? | Chân dương (+). Dài thì Dương. |
| Luật lắp pin là gì? | Đỏ gặp đỏ, xanh gặp xanh: cộng gặp cộng. |
| Tìm Bác Bug theo thứ tự nào? | Pin – Công tắc – Dây. |
| Có được nối thẳng hai đầu pin không? Vì sao? | Không, vì dây và pin sẽ nóng, có thể bỏng. |
| Thấy pin hoặc dây nóng thì làm gì? | Tắt công tắc, báo thầy ngay. |

> **Thầy:** "Hôm nay các em không còn là Kỹ sư tập sự nữa. Các em là Thám tử. Bác Bug đã phá 3 mạch. Muốn bắt nó, trước hết thám tử phải biết một mạch **đúng** trông thế nào."

---

## Hướng dẫn thực hành từng bước

### Bước 1: Chiến thắng nhỏ – lắp mạch đèn sáng (15')

**Làm gì:** Mỗi đội lắp mạch theo hình hướng dẫn trên bảng:

```text
Hộp pin (+) ──dây đỏ──> Công tắc ──dây──> LED chân dài (+)
                                            LED chân ngắn (−)
Hộp pin (−) <──dây đen──────────────────────┘
```

1. **Tắt công tắc** trước khi lắp.
2. Nối dây đỏ từ cực dương hộp pin tới một chân công tắc.
3. Nối dây từ chân còn lại của công tắc tới chân dài (+) của LED (hoặc cổng "+" của mô-đun LED).
4. Nối dây đen từ chân ngắn (−) của LED về cực âm hộp pin.
5. Lần ngón tay theo con đường điện: có liền một vòng không?
6. Bật công tắc.

**Vì sao:** Lắp từ đầu giúp các em thấy mỗi linh kiện nằm ở đâu trên vòng điện. Lần ngón tay là cách kiểm tra mạch kín trước khi bật.

**Đạt khi:** Đèn sáng khi bật, tắt khi tắt.

**An toàn:** Không để đầu dây đỏ và đầu dây đen của hộp pin chạm nhau. Nếu đèn không sáng, **tắt công tắc trước** rồi mới kiểm tra.

> **Thầy:** "Đội nào đèn sáng, giơ tay hô 'Mạch kín!'. Đội nào chưa sáng, đừng lo, các em vừa gặp Bác Bug đầu tiên. Thám tử bắt đầu làm việc."

### Bước 2: Điều tra 3 mạch lỗi (30')

**Làm gì:** Mỗi đội lần lượt đến 3 trạm (hoặc nhận lần lượt 3 mạch). Ở mỗi mạch, thám tử làm theo **Quy trình Thám tử**:

| Bước | Câu hỏi | Cách kiểm tra |
| --- | --- | --- |
| 1. Pin | Pin có lắp đúng chiều không? | Nhìn dấu + của pin và dấu + trên hộp. **Không tháo pin.** Báo thầy nếu thấy ngược. |
| 2. Công tắc | Công tắc đã bật chưa? | Nhìn và gạt thử. |
| 3. Dây | Có dây nào lỏng, tuột không? | Lần ngón tay theo vòng; lắc nhẹ từng đầu dây. |
| 4. LED | LED đúng chiều chưa? | Chân dài (chấm đỏ) có nối về phía cực dương không? |

Sau khi tìm ra lỗi, đội dán hình vào Phiếu thám tử, rồi **sửa** (riêng lỗi pin: báo thầy để thầy lắp lại).

**Đáp án cho giáo viên:**

| Mạch | Lỗi | Dấu hiệu | Cách sửa |
| --- | --- | --- | --- |
| 1 | Dây tháo hờ | Dây nhìn như đang cắm nhưng lắc thì tuột, hoặc đèn chớp | Cắm chặt dây |
| 2 | Công tắc tắt | Mọi thứ đúng, chỉ có công tắc ở vị trí tắt | Bật công tắc |
| 3 | Pin lắp ngược một viên | Một viên pin có núm quay sai chiều | Thầy lắp lại pin đúng chiều |

> **Lưu ý khoa học về Mạch 3:** Trong hộp pin 2 viên nối tiếp, nếu một viên bị ngược, điện áp của hai viên **triệt tiêu nhau** gần về 0 V, nên đèn không sáng. Nếu cả hai viên cùng ngược, cực của hộp pin bị đảo; LED cũng không sáng vì bị lắp "ngược" so với nguồn.

**Vì sao làm theo thứ tự:** Kiểm tra cái dễ trước, cái khó sau. Pin và công tắc nhìn là biết, dây phải lắc từng chỗ. Kỹ sư thật cũng làm như vậy để không mất thời gian.

**Đạt khi:** Đội tìm đúng cả 3 lỗi và ghi vào phiếu.

### Bước 3: Đổi chiều LED – đoán trước rồi thử (10')

**Làm gì:**
1. Mạch của đội đang sáng. **Tắt công tắc.**
2. Mỗi em ghi dự đoán vào phiếu: "Đổi chiều LED thì đèn ☐ sáng ☐ tắt."
3. Đổi hai dây ở hai chân LED (hoặc xoay mô-đun LED nếu kit cho phép).
4. Bật công tắc. Quan sát.
5. Đổi lại cho đúng chiều, đèn sáng trở lại.

**Kết quả đúng:** LED **không sáng** khi lắp ngược, vì LED chỉ cho điện đi một chiều.

**Vì sao:** Đây là lần đầu các em **đoán rồi kiểm chứng** một tính chất khoa học. Đoán sai cũng được khen: "Đoán sai mà dám thử là Kỹ sư Gan Dạ."

**Đạt khi:** Em ghi được dự đoán và kết quả thật, nói được: "LED chỉ sáng khi lắp đúng chiều."

### Bước 4: Kiểm tra cuối Chặng 1 (15')

**Làm gì:** Mỗi em (hoặc từng cặp với lớp 1–2) nhận một mạch lỗi ngẫu nhiên do thầy chuẩn bị. Có **3 phút** để tìm và sửa lỗi.

**Các lỗi thầy chuẩn bị (mỗi mạch một lỗi):**
- Dây tuột ở cực âm.
- Công tắc tắt.
- LED lắp ngược.
- Dây lỏng ở công tắc.
- Pin lắp ngược (em chỉ cần chỉ ra, thầy sửa).

**Tiêu chí đạt:**

| Mức | Mô tả |
| --- | --- |
| Đạt | Tìm và sửa được lỗi trong 3 phút, theo đúng thứ tự kiểm tra. |
| Đạt có hỗ trợ | Tìm được sau một gợi ý của thầy ("Em kiểm tra cái gì trước?"). |
| Cần luyện thêm | Chưa tìm được; thầy làm cùng em ở buổi sau. |

**Vì sao:** Đây là mốc đánh giá đầu tiên. Không chấm điểm số, chỉ ghi nhận để thầy biết em nào cần hỗ trợ ở Chặng 2.

### Bước 5: Báo cáo căn cứ, dọn dẹp (10')

Mỗi đội kể: "Con Bác Bug khó bắt nhất hôm nay trốn ở đâu?" Tắt công tắc, tháo dây, cất linh kiện đúng hộp.

---

## Giải thích mạch điện từng đoạn

Mạch đúng của buổi hôm nay, đi theo chiều dòng điện:

| Đoạn | Điện đi từ | Đến | Vai trò | Nếu đoạn này hỏng |
| --- | --- | --- | --- | --- |
| 1 | Cực dương hộp pin | Công tắc | Đưa điện ra khỏi Bình sữa năng lượng | Mạch hở, đèn tắt |
| 2 | Công tắc | Chân dài LED | Người gác cổng cho điện qua | Công tắc tắt hoặc dây lỏng: đèn tắt |
| 3 | Bên trong LED | Từ chân dài sang chân ngắn | Đom đóm biến điện thành ánh sáng | LED ngược: đèn tắt |
| 4 | Chân ngắn LED | Cực âm hộp pin | Đưa điện về pin, khép kín vòng | Mạch hở, đèn tắt |

**Điểm nhấn:** Hỏng ở **bất kỳ đoạn nào** thì đèn cũng tắt. Vì vậy phải kiểm tra từng đoạn, theo thứ tự.

**Về điện trở:** Nếu dùng LED rời, điện trở (100–220 Ω) được mắc nối tiếp ở đoạn 2 hoặc đoạn 4. Điện trở giới hạn dòng điện để LED không cháy. Với mô-đun LED có sẵn điện trở, các em không cần lắp thêm.

---

## Bảng xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
| --- | --- | --- |
| Bật công tắc, đèn không sáng | LED lắp ngược | Tắt công tắc, đổi chiều LED: chân dài về phía cực dương. |
| Đèn không sáng, mọi dây đều chặt | Pin lắp ngược hoặc hết pin | Báo thầy kiểm tra pin. |
| Đèn chớp tắt | Dây lỏng | Lắc nhẹ từng đầu dây, cắm chặt chỗ lỏng. |
| Đèn sáng rất yếu | Pin yếu, hoặc điện trở quá lớn | Thầy thay pin; kiểm tra giá trị điện trở (dùng 100–220 Ω). |
| Đèn sáng rồi tắt hẳn, có mùi khét | LED rời không có điện trở, bị cháy | Tắt công tắc, báo thầy. Thay LED mới và **lắp thêm điện trở**. |
| Đèn sáng cả khi tắt công tắc | Dây đi vòng không qua công tắc | Lần ngón tay theo mạch, nối lại để điện bắt buộc đi qua công tắc. |
| Hộp pin hoặc dây nóng | Hai đầu dây pin chạm nhau (đoản mạch) | **Tắt ngay, báo thầy.** Thầy tách dây, để pin nguội, kiểm tra lại. |
| Đội không biết bắt đầu kiểm tra từ đâu | Chưa nhớ quy trình | Chỉ lên bảng Quy trình Thám tử: Pin – Công tắc – Dây – LED. |

---

## Thử thách mở rộng

### Sao vàng (cho đội xong sớm)

1. **Hai đom đóm:** Lắp thêm một LED thứ hai nối tiếp với LED đầu tiên (cùng một vòng). Quan sát: hai đèn sáng thế nào so với một đèn? (Thường sáng yếu hơn hoặc không sáng với nguồn 3 V, vì mỗi LED cần khoảng 2 V.) Tháo một LED, đèn còn lại thế nào? (Tắt, vì mạch hở.)
2. **Bác Bug ngược:** Đội tự cài một lỗi vào mạch của mình, đưa cho đội bạn bắt.
3. **Thám tử nhanh nhất:** Thi tìm lỗi trong mạch thầy cài, tính giờ.

### Lớp 4–5

- **Mạch song song:** Lắp hai mô-đun LED, mỗi LED có một đường riêng nối về pin. Tháo một LED, LED còn lại vẫn sáng. So sánh với mạch nối tiếp. Giải thích: đèn trong nhà em mắc song song, nên tắt một đèn thì đèn khác vẫn sáng.
- **Vẽ sơ đồ:** Vẽ mạch của đội bằng ký hiệu: pin, công tắc, LED (hình tam giác có vạch, kèm mũi tên chỉ ánh sáng), điện trở (hình chữ nhật nhỏ).
- **Câu hỏi suy nghĩ:** "Vì sao Kỹ sư kiểm tra pin trước, dây sau?" (Pin và công tắc kiểm tra nhanh; dây phải kiểm tra từng chỗ, tốn thời gian hơn.)

---

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Mạch 1, 2, 3 có lỗi gì? | Mạch 1: dây lỏng. Mạch 2: công tắc tắt. Mạch 3: pin ngược. |
| Thám tử kiểm tra theo thứ tự nào? | Pin – Công tắc – Dây – LED. |
| Đổi chiều LED thì đèn thế nào? Vì sao? | Không sáng, vì LED chỉ cho điện đi một chiều. |
| Đội em đoán đúng hay sai? Đoán sai có sao không? | Kể kết quả; đoán sai không sao, quan trọng là đã thử. |
| Trước khi tháo dây phải làm gì? | Tắt công tắc. |
| Con Bác Bug khó bắt nhất trốn ở đâu? | Thường là dây lỏng hoặc pin ngược; chấp nhận mọi câu có lý do. |

---

## Kết buổi

Mỗi đội tô vùng sáng thứ ba trên Bản đồ Hành trình. Thầy đọc tín hiệu mới từ Bít-Bô (phát âm thanh hoặc đọc thư):

> **Thầy:** "Tin khẩn từ Bít-Bô: 'Các Kỹ sư đã thắp sáng được đèn. Nhưng các vùng của Bít-Bô ở rất xa nhau. Đèn thì không tự đi được. Chúng tôi cần một chiếc xe cứu hộ!' Chặng 2 bắt đầu từ tuần sau: các em sẽ chế tạo xe."

Ghi nhận kết quả kiểm tra cuối Chặng 1 vào sổ theo dõi. Thưởng Xu cho mọi đội đã bắt được Bác Bug.

---

## Ghi nhớ cuối bài

1. Mạch đúng là một vòng: pin, công tắc, đèn, quay về pin.
2. Thám tử kiểm tra: pin – công tắc – dây – LED.
3. Đom đóm LED lắp ngược thì không sáng.
4. Hỏng một chỗ thì cả mạch tắt.
5. Tắt công tắc trước khi sửa mạch.
6. Đoán sai cũng tốt, miễn là dám thử.
