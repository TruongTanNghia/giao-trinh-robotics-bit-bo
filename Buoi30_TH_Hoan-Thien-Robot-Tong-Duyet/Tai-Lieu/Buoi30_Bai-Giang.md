# Bài giảng – Buổi 30: Hoàn thiện robot, thanh tra lần 2, tổng duyệt

> **Thực hành · 90 phút** · Chặng 4: Chế tạo robot của riêng em · Nhiệm vụ 15: Thanh tra Bug · Tuần 15

Đây là buổi cuối trong Xưởng chế tạo. Các đội hoàn thiện robot, được Thanh tra lần 2 bởi một đội mới, tổng duyệt phần giới thiệu như Ngày hội thật, và thử **bản đồ chung** nơi robot các đội nối tiếp nhau. Kết thúc buổi, robot phải **sẵn sàng trình diễn** và mỗi Kỹ sư biết phần việc của mình.

Bài học kỹ thuật chính của buổi: **độ tin cậy**. Robot chạy được một lần chưa đủ; ở Ngày hội nó phải chạy được nhiều lần, trước nhiều người, trong điều kiện khác phòng học. Kỹ sư chuẩn bị cho điều đó bằng thử lặp lại, danh sách kiểm tra và kế hoạch dự phòng.

## Ôn lý thuyết 5 phút

| Câu hỏi | Đáp án |
| --- | --- |
| Khung giới thiệu 4 câu là gì? | Tên – Nhiệm vụ – Cách chạy – Bác Bug |
| Mẫu câu giải thích một khối? | "Khối này bảo robot … vì …" |
| Ba bí quyết khi nói? | To – Chậm – Nhìn |
| Robot đang trình diễn bỗng không chạy thì nói gì, làm gì? | "Bác Bug vừa xuất hiện!", rồi kiểm tra Pin – Công tắc – Dây – Cổng – Chương trình |
| Robot "đạt" khi nào? | Làm đúng yêu cầu trên phiếu, nhiều lần liên tiếp |
| Khi Thanh tra, có được tự sửa robot bạn không? | Không; chỉ chỉ ra và gợi ý |

## Hướng dẫn thực hành từng bước

Nhắc an toàn: tắt công tắc khi cắm rút linh kiện và khi trang trí; đồ trang trí không che cảm biến, không quấn vào bánh xe; keo, kéo do trợ giảng giữ; thầy thay pin mới cho tất cả robot trước tổng duyệt.

### Bước 1 – Hoàn thiện robot (20 phút)

**Làm gì:**

1. Kiểm tra món nào trên phiếu bằng sáng chế còn chưa ✓. Hoàn thành món đó trước.
2. Chạy **thử độ tin cậy**: cho robot làm cả nhiệm vụ **5 lần liên tiếp**. Thư ký ghi kết quả từng lần.

| Lần | Đạt? | Nếu chưa đạt, chuyện gì xảy ra |
| --- | --- | --- |
| 1 | ☐ | |
| 2 | ☐ | |
| 3 | ☐ | |
| 4 | ☐ | |
| 5 | ☐ | |

3. Nếu đạt 4/5 trở lên: chuyển sang trang trí. Nếu dưới 4/5: tìm Bác Bug theo danh sách, sửa từng thứ một.
4. Trang trí và gắn biển tên. Luật trang trí: **không che cảm biến, không chạm bánh xe, không nặng quá**. Trang trí xong phải chạy lại 2 lần để kiểm tra trang trí không làm hỏng robot.

**Vì sao:** Robot chạy đúng 1 lần có thể do may. Ở Ngày hội, sàn khác, ánh sáng khác, người đứng xung quanh khác. Thử nhiều lần giúp phát hiện Bác Bug "lúc có lúc không".

**Đạt khi:** Robot đạt ít nhất 4/5 lần, có biển tên, trang trí xong vẫn chạy đúng.

### Bước 2 – Thanh tra lần 2 (15 phút)

**Làm gì:** Thầy ghép cặp **khác** lần 1 (ví dụ A–C, B–D). Quy trình giống buổi 28, thêm 2 mục mới vào Phiếu Thanh tra:

| Mục mới | Đội Thanh tra kiểm tra |
| --- | --- |
| Độ tin cậy | Cho robot chạy 3 lần, đếm số lần đạt |
| Sẵn sàng trình diễn | Trang trí có che cảm biến không? Biển tên có không? Robot có bị lỏng sau khi trang trí? |

Đội Thanh tra còn nghe đội bạn **tập giới thiệu 1 lần** và góp ý theo mẫu, tập trung vào: đủ 4 câu chưa, có chỉ vào khối không, có To – Chậm – Nhìn không.

**Vì sao:** Đội mới nhìn robot bằng mắt mới, phát hiện điều đội lần 1 bỏ sót. Và góp ý cho phần nói giúp các đội tự tin hơn.

**Đạt khi:** Phiếu thanh tra đủ mục, có góp ý cho cả robot và phần nói.

### Bước 3 – Tổng duyệt (25 phút)

**Làm gì:** Cả lớp ngồi thành khán giả. Từng đội lên "sân khấu" (bàn trình diễn), giới thiệu như Ngày hội thật, **đúng 2 phút**, trợ giảng bấm giờ.

Thứ tự mỗi lượt:

1. Người dẫn chương trình của lớp giới thiệu đội: "Xin mời đội … với robot …!"
2. Đội đặt robot vào vị trí xuất phát, kiểm tra nhanh pin và công tắc.
3. Đội giới thiệu 4 câu, chạy robot ở câu 3.
4. Khán giả vỗ tay. Thầy hỏi 1 câu (lớp 4–5) hoặc khen 1 điều cụ thể.

Trong tổng duyệt, thầy **cố ý tạo một tình huống** cho 1–2 đội (ví dụ tắt công tắc khi đội không để ý) để các em tập xử lý sự cố bình tĩnh trên sân khấu.

**Kịch bản lời dẫn mẫu** cho Người dẫn chương trình:

> **Dẫn chương trình:** "Kính chào các vị khách quý đến Căn cứ Bít-Bô! Hôm nay, bốn đội Kỹ sư Nhí sẽ giới thiệu những robot do chính các bạn thiết kế, chế tạo và lập trình. Xin mời đội đầu tiên!"
>
> **Dẫn chương trình (chuyển đội):** "Cảm ơn đội Sao Xanh và robot Tí Thuốc! Tiếp theo là đội … với robot …"
>
> **Dẫn chương trình (kết):** "Bây giờ, tất cả robot sẽ cùng nhau làm một nhiệm vụ cuối cùng: đánh thức Bít-Bô!"

**Vì sao:** Tổng duyệt giúp các em quen sân khấu, quen thời gian 2 phút, và biết phần mình. Gặp sự cố trong tổng duyệt tốt hơn gặp lần đầu ở Ngày hội.

**Đạt khi:** Đội nói đủ 4 câu trong khoảng 2 phút, mọi bạn đều có phần, robot chạy hoặc đội xử lý sự cố bình tĩnh.

### Bước 4 – Thử bản đồ chung (15 phút)

**Làm gì:** Trên sa bàn, mỗi đội có một **trạm**. Robot các đội nối tiếp như trò chạy tiếp sức:

```text
Trạm 1 (đội A)  →  Trạm 2 (đội B)  →  Trạm 3 (đội C)  →  Trạm 4 (đội D)  →  Vùng sáng thứ 16
robot A chạy đến cuối trạm, chạm nút hoặc chắn trước Dơi của robot B, robot B bắt đầu...
```

Cách "chuyền gậy" tùy robot:

- Robot sau dùng **nút bấm**: robot trước đẩy vào nút, hoặc một bạn bấm nút khi robot trước đến vạch đích.
- Robot sau dùng **Dơi**: robot trước dừng trước Dơi của robot sau. Robot sau lập trình "khi thấy vật gần thì bắt đầu đi".

Chạy thử cả chuỗi 2 lần. Ghi lại trạm nào hay bị "rớt gậy".

**Vì sao:** Đây là bài học về **giao tiếp giữa các hệ thống**: đầu ra của robot này là đầu vào của robot kia. Cũng là cách cả lớp cùng chung một mục tiêu, không đội nào thắng một mình.

**Đạt khi:** Cả chuỗi chạy trọn ít nhất 1 lần (có thể có bạn hỗ trợ bấm nút ở trạm khó).

### Bước 5 – Chốt kế hoạch Ngày hội, dọn dẹp (10 phút)

- Mỗi đội điền **danh sách kiểm tra trước Ngày hội** (Phiếu bài tập buổi 30).
- Cất robot vào hộp riêng có dán tên đội; tháo pin ra để pin không tụt. Thầy giữ robot đến Ngày hội.
- Thầy phát thiệp mời phụ huynh. Tô Bản đồ Hành trình.

## Giải thích chương trình từng khối

Chương trình "nhận gậy" cho robot dùng Dơi làm tín hiệu bắt đầu:

```text
khi bắt đầu
  chờ đến khi khoảng cách < 10 cm
  phát tiếng bíp
  lặp mãi
    nếu cảm biến thấy đen thì
      tiến chậm
    không thì
      rẽ về phía vạch
```

| Khối | Robot hiểu là | Lưu ý |
| --- | --- | --- |
| khi bắt đầu | Chương trình chạy ngay khi bật | Bật robot trước khi chuỗi bắt đầu |
| chờ đến khi khoảng cách < 10 cm | Đứng yên chờ robot đội trước đến sát | Con số nhỏ để không xuất phát nhầm khi có tay người lướt qua |
| phát tiếng bíp | Báo "tôi đã nhận gậy" | Khán giả nghe rõ lúc chuyền |
| lặp mãi … | Đi theo vạch đến trạm sau | Như món đi theo vạch đã học ở buổi 24 |

Nếu phần mềm của trường không có khối "chờ đến khi", dùng vòng lặp kiểm tra điều kiện rồi thoát. Tên khối thay theo phần mềm của trường.

## Bảng xử lý sự cố

Bảng này dùng cho cả tổng duyệt và Ngày hội. Đội dán bảng cạnh robot.

| Hiện tượng | Nguyên nhân | Cách sửa nhanh trên sân khấu |
| --- | --- | --- |
| Robot không động đậy | Công tắc tắt hoặc pin hết | Kiểm tra công tắc; giơ tay xin thầy pin dự phòng |
| Bấm nút không chạy | Chưa nạp chương trình mới nhất hoặc cắm lỏng | Ấn chặt đầu cắm; nhờ thầy nạp lại |
| Robot không đi theo vạch ở sân khấu | Ánh sáng khác phòng học | Đo lại cảm biến trên sàn sân khấu trước lượt |
| Robot dừng giữa đường dù không có vật | Người đứng gần Dơi hoặc đồ trang trí che Dơi | Nhờ khán giả lùi lại; gỡ đồ trang trí |
| Bánh kêu, xe chạy lệch sau khi trang trí | Đồ trang trí chạm bánh, robot nặng một bên | Gỡ bớt trang trí, cân lại |
| Robot xuất phát sớm trong chuỗi bản đồ chung | Con số khoảng cách quá lớn | Giảm con số; khán giả không đứng sát trạm |
| Robot đội trước không "chuyền gậy" được | Dừng quá xa nút hoặc Dơi của đội sau | Dời trạm gần hơn; bạn trợ giúp bấm nút |
| Đội quên câu, đứng im | Hồi hộp | Nhìn 4 ngón tay; bạn bên cạnh nhắc câu đầu |
| Đội nói quá 2 phút | Giải thích quá nhiều khối | Chỉ nói khối bắt đầu, khối cảm biến, khối lặp |

Câu "cứu nguy" mọi đội đều học thuộc: **"Bác Bug vừa xuất hiện! Các Kỹ sư sẽ bắt nó ngay."** Sau đó kiểm tra theo danh sách. Nếu sau 1 phút vẫn chưa sửa được, đội **kể** robot đã chạy thế nào và mời khán giả xem lại sau phần các đội khác.

## Thử thách mở rộng

- **Sao vàng 1:** Robot đạt 5/5 lần liên tiếp.
- **Sao vàng 2:** Thêm "màn chào khán giả": khi bắt đầu, robot nháy đèn 3 lần và kêu một điệu ngắn bằng vòng lặp.
- **Sao vàng 3 (lớp 4–5):** Trong bản đồ chung, robot cuối dùng biến đếm số robot đã đến (mỗi lần có robot dừng trước Dơi thì cộng 1), đủ 4 thì còi kêu dài báo "Bít-Bô thức dậy".
- **Đội hỗ trợ:** Đội xong sớm giúp làm biển chỉ dẫn, trang trí sa bàn bản đồ chung.

## Câu hỏi báo cáo căn cứ

| Câu hỏi | Đáp án mong đợi |
| --- | --- |
| Robot đạt bao nhiêu lần trên 5 lần thử? | Con số từ bảng độ tin cậy |
| Bác Bug "lúc có lúc không" nào đội đã gặp? | Ví dụ: dây lỏng khi rung, ánh sáng đổi |
| Đội Thanh tra lần 2 góp ý gì cho phần nói? | Đọc câu "Một điều nên thử" |
| Trong tổng duyệt, đội gặp sự cố gì, xử lý thế nào? | Kể lại bước kiểm tra đã làm |
| Robot của đội nhận "gậy" và chuyền "gậy" bằng cách nào? | Nút bấm hoặc Dơi |
| Ở Ngày hội, mỗi bạn trong đội làm việc gì? | Tên từng bạn và vai trò |

## Ghi nhớ cuối bài

1. Robot tốt là robot chạy đúng nhiều lần, không chỉ một lần.
2. Trang trí xong phải chạy thử lại; đồ trang trí không được che cảm biến.
3. Tổng duyệt giống hệt Ngày hội: đủ 4 câu, khoảng 2 phút, ai cũng có phần.
4. Gặp sự cố trên sân khấu: "Bác Bug vừa xuất hiện!", rồi kiểm tra theo danh sách.
5. Trong bản đồ chung, đầu ra của robot này là đầu vào của robot kia.
6. Tháo pin, cất robot vào hộp có tên đội; Ngày hội đang chờ.
