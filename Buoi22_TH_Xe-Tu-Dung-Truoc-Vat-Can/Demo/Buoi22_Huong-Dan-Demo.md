# Hướng dẫn demo – Buổi 22: Xe tự dừng trước vật cản

> **Thực hành · 90 phút** · Chặng 3: Bắt Bác Bug, dạy robot suy nghĩ · Nhiệm vụ 11: Robot biết "nhìn thấy" · Tuần 11


## Màn mở đầu

Lắp đôi tai dơi cho xe cứu hộ!

## Cách dựng demo

1. Cho hiện số khoảng cách trên màn hình máy tính hoặc màn LED của bo mạch.

## Đồ dùng

- [ ] Mỗi đội: cảm biến siêu âm, xe có bo mạch, máy tính
- [ ] Hộp giấy phẳng làm vật cản, thước đo

## Chương trình demo

```text
khi bắt đầu
  lặp mãi
    nếu khoảng cách < 15 cm thì
      dừng
      lùi 0,5 giây      (lớp 4–5)
      rẽ trái 0,5 giây  (lớp 4–5)
    không thì
      tiến
```

## Kiểm tra trước giờ học

- [ ] Pin đầy, có pin dự phòng
- [ ] Chạy thử demo ít nhất 1 lần trong đúng phòng học
- [ ] Chuẩn bị Plan B không cần máy
