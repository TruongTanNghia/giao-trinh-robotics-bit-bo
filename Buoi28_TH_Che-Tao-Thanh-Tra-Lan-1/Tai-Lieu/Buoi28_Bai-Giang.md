# Bài giảng – Buổi 28: Chế tạo và thanh tra lần 1

> **Thực hành · 90 phút** · Chặng 4: Chế tạo robot của riêng em · Nhiệm vụ 14: Xưởng chế tạo · Tuần 14

Xưởng chế tạo mở cửa. Nửa đầu buổi, các đội chế tạo và thử theo phiếu bằng sáng chế. Giữa buổi, hai đội đổi chỗ làm **Thanh tra Bug** cho nhau. Nửa sau, các đội sửa theo góp ý. Mục tiêu: robot chạy được **phần lớn các món nhỏ** trong thiết kế.

Đây là buổi các em áp dụng trọn vẹn quy trình kỹ sư của buổi 27: chế tạo – thử – được kiểm tra chéo – cải tiến.

## Ôn lý thuyết 5 phút

| Câu hỏi | Đáp án |
| --- | --- |
| Kể 4 bước của vòng quy trình kỹ sư. | Thiết kế – Chế tạo – Thử – Sửa (lớp 4–5: thêm Xác định vấn đề, Ý tưởng) |
| Thứ tự kiểm tra khi robot không chạy? | Pin – Công tắc – Dây – Cổng cắm – Chương trình |
| Mỗi lần sửa bao nhiêu thứ? | Một thứ, rồi chạy thử ngay |
| Mẫu câu góp ý? | Một điều hay – Một điều nên thử |
| Nhận góp ý thì nói gì? | Cảm ơn, đội mình sẽ thử |
| Robot "đạt" khi nào? | Khi làm đúng yêu cầu ghi trên phiếu, nhiều lần liên tiếp (ví dụ 3 lần) |

## Hướng dẫn thực hành từng bước

Nhắc an toàn: tắt công tắc trước khi cắm hoặc rút linh kiện; không giữ bánh xe khi động cơ chạy; kẹt thì tắt ngay; dụng cụ đặt gọn trong khay; thầy thay pin.

Phát cho mỗi đội: bộ kit, phiếu bằng sáng chế của đội, 2 Phiếu Thanh tra Bug, sổ đội. Đội chia vai Cơ khí – Lập trình – Thư ký, đổi vai mỗi khi đồng hồ cát chảy hết.

### Bước 1 – Đặt mục tiêu buổi (5 phút)

**Làm gì:** Mỗi đội đọc lại "việc phải làm xong" đã viết cuối buổi 27. Thư ký ghi lên góc bàn: "Hôm nay đội sẽ làm xong món số ___ và món số ___".

**Vì sao:** Mục tiêu rõ giúp đội không làm lan man. Chỉ chọn 1–2 món, vừa sức trong 30 phút.

### Bước 2 – Chế tạo và thử (30 phút)

**Làm gì:** Với mỗi món nhỏ, đi đúng 5 bước:

1. **Lắp** phần cứng cho món đó, so với bản vẽ.
2. **Ghép** khối chỉ cho món đó.
3. **Dự đoán**: Thư ký ghi "em nghĩ robot sẽ…".
4. **Chạy** và quan sát.
5. **Ghi** vào nhật ký: đạt hay chưa, gặp Bug nào.

Món đạt 3 lần liên tiếp thì đánh dấu ✓ và sang món tiếp. Khi đã có 2 món đạt, ghép chúng lại và thử cả hai cùng lúc.

Ví dụ ghép món 1 và món 2 của robot Chở thuốc:

```text
khi nút được bấm
  phát tiếng bíp
  lặp mãi
    nếu cảm biến thấy đen thì
      tiến chậm
    không thì
      rẽ về phía vạch
```

**Vì sao:** Thử từng món rồi mới ghép giúp khoanh vùng lỗi. Nếu món 1 và món 2 đều đạt riêng mà ghép lại hỏng, lỗi chắc chắn nằm ở **chỗ nối**.

**Đạt khi:** Ít nhất 2 món đạt riêng; nếu kịp, đã ghép thử 2 món.

### Bước 3 – Thanh tra Bug (15 phút)

Thầy ghép cặp đội (A–B, C–D). Thầy rung chuông: "Thanh tra đến!"

**Làm gì:**

1. Mỗi đội để lại robot, phiếu bằng sáng chế và một **Hướng dẫn viên** ở bàn mình. Các bạn còn lại sang bàn đội kia.
2. Hướng dẫn viên giới thiệu 30 giây: robot tên gì, làm gì, món nào đã xong.
3. Đội Thanh tra kiểm tra theo phiếu, **đúng thứ tự**, đánh dấu từng mục:

| Mục | Đội Thanh tra làm | Ghi |
| --- | --- | --- |
| Pin | Nhìn đèn nguồn, xem cực | ☐ ổn ☐ cần xem |
| Công tắc | Xem vị trí | ☐ ổn ☐ cần xem |
| Dây | Lắc nhẹ từng dây | ☐ ổn ☐ cần xem |
| Cổng cắm | So với bản vẽ | ☐ ổn ☐ cần xem |
| Chương trình | Nhờ Hướng dẫn viên chạy, đọc to từng khối | ☐ ổn ☐ cần xem |
| So với yêu cầu | Robot có làm đúng câu "đạt khi" trên phiếu không? | ☐ đạt ☐ chưa |

4. Viết một câu "Một điều hay" và một câu "Một điều nên thử".
5. Đội Thanh tra **không tự tay sửa** robot của bạn. Chỉ chỉ ra và gợi ý.

**Vì sao:** Mắt người ngoài thấy lỗi người làm đã quen mắt bỏ qua. Không tự sửa để đội chủ robot được tự bắt Bác Bug.

**Đạt khi:** Phiếu thanh tra đủ 6 mục và có 2 câu góp ý cụ thể.

### Bước 4 – Quay về sửa theo góp ý (20 phút)

**Làm gì:**

1. Đội về bàn, Hướng dẫn viên đọc phiếu Thanh tra cho cả đội. Cả đội nói: "Cảm ơn, đội mình sẽ thử."
2. Chọn **một** góp ý quan trọng nhất để thử trước.
3. Sửa một thứ – chạy thử – ghi nhật ký. Rồi đến góp ý tiếp theo.
4. Còn thời gian thì tiếp tục món nhỏ chưa xong.

**Vì sao:** Đây là bước "Cải tiến" của vòng quy trình. Sửa từng góp ý một để biết góp ý nào có tác dụng.

**Đạt khi:** Ít nhất một góp ý đã được thử và ghi kết quả.

### Bước 5 – Báo cáo, dọn dẹp (15 phút)

- 10 phút: mỗi đội báo cáo căn cứ (câu hỏi ở cuối bài).
- 5 phút: tắt công tắc, cất linh kiện vào khay theo ngăn, ghi Bug đã bắt vào sổ đội, tô Bản đồ Hành trình.

## Giải thích chương trình từng khối

Giải thích chương trình ghép món 1 + món 2 ở bước 2:

| Khối | Robot hiểu là | Bác Bug có thể trốn ở đây |
| --- | --- | --- |
| khi nút được bấm | Chờ y tá bấm Chuông cửa mới bắt đầu | Nút cắm sai cổng; bấm giữ lâu làm chạy lại |
| phát tiếng bíp | Báo "tôi đã nhận nhiệm vụ" | Quên khối này thì không biết robot đã nghe chưa |
| lặp mãi | Làm đi làm lại phần bên trong, không ngừng | Khối điều kiện đặt ra ngoài vòng lặp nên chỉ kiểm tra một lần |
| nếu cảm biến thấy đen thì | Hỏi Mắt mèo: "dưới chân có phải vạch đen không?" | Ánh sáng đổi; chưa đo lại cảm biến |
| tiến chậm | Đang ở trên vạch thì đi thẳng, chậm để không vượt khỏi vạch | Tốc độ cao quá làm xe văng khỏi vạch |
| không thì rẽ về phía vạch | Lệch khỏi vạch thì rẽ lại | Rẽ sai hướng làm xe quay vòng |

Khi ghép thêm món 3 (Dơi), câu hỏi quan trọng là: **kiểm tra Dơi trước hay Mắt mèo trước?** Trả lời: kiểm tra Dơi trước. An toàn quan trọng hơn: thấy vật cản thì phải dừng, dù đang ở trên vạch.

```text
lặp mãi
  nếu khoảng cách < 15 cm thì
    dừng
  không thì
    nếu cảm biến thấy đen thì
      tiến chậm
    không thì
      rẽ về phía vạch
```

Tên khối thật thay theo phần mềm lập trình khối của trường.

## Bảng xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
| --- | --- | --- |
| Từng món chạy đúng, ghép lại thì hỏng | Lỗi ở chỗ nối: thứ tự khối sai, khối nằm ngoài vòng lặp | Đọc to chương trình; kiểm tra khối nào nằm trong "lặp mãi" |
| Xe đi theo vạch nhưng không dừng trước vật | Kiểm tra Mắt mèo trước Dơi nên lệnh dừng bị bỏ qua | Đặt điều kiện khoảng cách lên trước |
| Xe dừng ngay khi bắt đầu dù không có vật | Con số khoảng cách quá lớn hoặc Dơi chĩa xuống sàn | Giảm con số; dựng Dơi thẳng, cao hơn sàn |
| Robot chạy lúc được lúc không | Dây lỏng, rung khi chạy | Lắc nhẹ từng dây; dùng dây buộc gọn |
| Robot yếu dần, chạy chậm | Pin sắp hết | Báo thầy thay pin; kiểm tra pin đầu tiên |
| Đội Thanh tra và đội chủ cãi nhau | Góp ý chưa đúng mẫu, hoặc tự tay sửa robot bạn | Nhắc mẫu câu; Thanh tra chỉ ra, không sửa |
| Đội sửa nhiều thứ, robot vẫn hỏng, không biết vì sao | Sửa nhiều thứ cùng lúc | Quay lại phiên bản chạy được gần nhất, sửa từng thứ một |
| Linh kiện lắp vướng nhau, bánh cọ vào cảm biến | Bản vẽ chưa tính chỗ đặt | Dời linh kiện, cập nhật bản vẽ bằng bút màu khác |

## Thử thách mở rộng

- **Sao vàng 1:** Robot đạt cả món 1, 2 và 3, chạy trọn 3 lần liên tiếp.
- **Sao vàng 2:** Thêm đèn LED báo trạng thái: đèn sáng khi đang đi, đèn tắt khi dừng vì vật cản.
- **Sao vàng 3 (lớp 4–5):** Dùng biến đếm số lần robot phải dừng vì vật cản; khi đến nơi, hiện con số đó.
- **Trợ lý Thanh tra:** Đội xong sớm được thầy cử sang giúp đội đang gặp khó, nhưng chỉ được hỏi và gợi ý, không làm hộ.

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Đội đã làm xong những món nhỏ nào? | Liệt kê món có dấu ✓ |
| Đội Thanh tra khen điều gì? | Đọc câu "Một điều hay" |
| Đội Thanh tra gợi ý điều gì? Đội đã thử chưa, kết quả ra sao? | Đọc câu "Một điều nên thử" và kết quả |
| Bác Bug lớn nhất hôm nay trốn ở đâu? | Ví dụ: chỗ nối giữa hai món, dây cổng 3 lỏng |
| Khi làm Thanh tra, đội tìm được gì ở robot bạn? | Một mục "cần xem" trên phiếu |
| Buổi sau đội cần làm gì để robot sẵn sàng cho Ngày hội? | Món còn thiếu, việc trang trí, chuẩn bị giới thiệu |

## Ghi nhớ cuối bài

1. Lắp – ghép – dự đoán – chạy – ghi: làm cho từng món nhỏ.
2. Từng món đạt mà ghép lại hỏng thì Bác Bug trốn ở chỗ nối.
3. An toàn trước: kiểm tra vật cản trước khi đi theo vạch.
4. Thanh tra chỉ ra và gợi ý, không tự tay sửa robot của bạn.
5. Nhận góp ý thì cảm ơn, rồi thử từng góp ý một.
6. Giúp bạn bắt Bug cũng là một cách làm kỹ sư giỏi.
