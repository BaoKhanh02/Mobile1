## PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG

### Thông tin sinh viên

* Họ và tên: Vũ Bảo Khánh
* MSSV: K225480106028
* Lớp: K58KTPM

---

# PHẦN A - ỨNG DỤNG MIT APP INVENTOR

## Giới thiệu

Ứng dụng được xây dựng bằng MIT App Inventor gồm 3 Screen:

1. Screen1 - Giới thiệu bản thân
2. Screen2 - Giải phương trình bậc 2
3. Screen3 - Hiển thị Website bằng WebViewer

---

# Screen1 - Giới thiệu bản thân

## Thiết kế giao diện

Các thành phần sử dụng:

* VerticalArrangement
* Label
* Image
* Button

Thông tin hiển thị:

* Họ tên sinh viên
* MSSV
* Lớp
* Ảnh cá nhân

Hai nút chức năng:

* Giải phương trình bậc 2
* Xem Website lớp

### Hình ảnh giao diện

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/567bcd67-e5f9-4c7a-99f3-90c5456bb025" />

### Hình ảnh chạy thực tế

<img width="900" height="2030" alt="z7934851155193_d4f428e570f7abd39ebb250392d090fd" src="https://github.com/user-attachments/assets/034a00a0-7952-47a2-aac6-140cc1a3f81a" />

---

## Lập trình Block

### Chuyển sang Screen2

```text
when Button_GiaiToan.Click
    open another screen "Screen2"
```

### Chuyển sang Screen3

```text
when Button_Web.Click
    open another screen "Screen3"
```

### Hình ảnh Block

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/e5bef578-0783-4175-ac5e-910f24318284" />

---

# Screen2 - Giải phương trình bậc 2

## Thiết kế giao diện

Các thành phần:

* 3 HorizontalArrangement
* 3 Label
* 3 TextBox
* 1 Button
* 1 Label kết quả

### Danh sách điều khiển

| Thành phần | Chức năng        |
| ---------- | ---------------- |
| txtA       | Nhập hệ số a     |
| txtB       | Nhập hệ số b     |
| txtC       | Nhập hệ số c     |
| btnGiai    | Thực hiện giải   |
| lblKetQua  | Hiển thị kết quả |

### Hình ảnh giao diện Designer

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/855658f7-c376-4012-8f0c-56101aad814a" />

### Hình ảnh chạy thực tế

<img width="900" height="2030" alt="z7934861936899_96cd57354e32c8faa533e9027d26fbb5" src="https://github.com/user-attachments/assets/fe10129c-a4cb-4b54-b36b-222cde929370" />

---

## Thuật toán giải phương trình

Phương trình:

[
ax^2 + bx + c = 0
]

### Trường hợp 1

Nếu:

[
a = 0
]

Thì trở thành phương trình bậc nhất:

[
bx + c = 0
]

### Trường hợp 2

Nếu:

[
a \neq 0
]

Tính:

[
\Delta = b^2 - 4ac
]

#### Nếu Δ < 0

Phương trình vô nghiệm.

#### Nếu Δ = 0

Phương trình có nghiệm kép:

[
x = \frac{-b}{2a}
]

#### Nếu Δ > 0

Phương trình có hai nghiệm phân biệt:

[
x_1 = \frac{-b+\sqrt{\Delta}}{2a}
]

[
x_2 = \frac{-b-\sqrt{\Delta}}{2a}
]

---

## Mã giả (Pseudo Code)

```text
when btnGiai.Click

    if a = 0 then

        if b = 0 then

            if c = 0 then
                vô số nghiệm
            else
                vô nghiệm

        else
            nghiệm bậc nhất

    else

        delta = b*b - 4*a*c

        if delta < 0
            vô nghiệm

        else if delta = 0
            nghiệm kép

        else
            tính x1
            tính x2
```

---

## Hình ảnh Block

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/8e8d08d7-20bc-4efc-8473-c2e3c06ce5a8" />

---

# Screen3 - Hiển thị Website bằng WebViewer

## Thiết kế giao diện

Thành phần sử dụng:

* WebViewer

Thiết lập:

```text
Width = Fill Parent
Height = Fill Parent
```

### Hình ảnh giao diện

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/d88a34f6-f614-4ac7-bf48-2977f56b54f6" />

---

## Lập trình Block

```text
when Screen3.Initialize

set WebViewer1.HomeUrl to
https://k58kmt.tdh.io.vn

call WebViewer1.GoHome
```

### Hình ảnh Block

<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/234c5dfd-3600-4562-9cd9-b155705def6c" />

---

## Hình ảnh chạy thực tế

<img width="900" height="2030" alt="z7934861942646_1403de2d4da4d7f6cf77ab5444d6e23a" src="https://github.com/user-attachments/assets/cd2611d9-2458-47f1-bd0a-9c77c0bfefe4" />

---

# Các thành phần sử dụng trong MIT App Inventor

## Designer

Designer là nơi thiết kế giao diện bằng phương pháp kéo thả.

Các thành phần chính:

* Palette
* Viewer
* Components
* Properties

## Palette

Palette chứa các nhóm điều khiển:

* User Interface
* Layout
* Media
* Drawing and Animation
* Sensors
* Connectivity

Người dùng kéo thả các đối tượng từ Palette vào Viewer.

---

## Viewer

Viewer là màn hình mô phỏng giao diện điện thoại.

Giúp quan sát vị trí hiển thị của các đối tượng.

---

## Components

Hiển thị danh sách tất cả các thành phần đã được thêm vào ứng dụng.

Ví dụ:

* Button_GiaiToan
* Button_Web
* txtA
* txtB
* txtC

---

## Properties

Cho phép thay đổi thuộc tính của đối tượng.

Ví dụ:

| Thuộc tính      | Ý nghĩa           |
| --------------- | ----------------- |
| Text            | Nội dung hiển thị |
| Width           | Chiều rộng        |
| Height          | Chiều cao         |
| FontSize        | Kích thước chữ    |
| BackgroundColor | Màu nền           |
| TextColor       | Màu chữ           |

---

# Lập trình Block

## Khái niệm

Block là hình thức lập trình trực quan.

Người dùng ghép các khối lệnh lại với nhau để tạo chương trình.


## Ưu điểm

* Dễ học
* Không cần nhớ cú pháp
* Thiết kế nhanh
* Phù hợp cho người mới bắt đầu

---

## Nhược điểm

* Khó xây dựng dự án lớn
* Khó bảo trì
* Hiệu năng thấp hơn Android Studio
* Khó quản lý khi số lượng Block nhiều

---

## Backpack

Backpack là công cụ dùng để:

* Sao chép Block
* Lưu Block tạm thời
* Chuyển Block giữa các Screen

# Kết luận

Ứng dụng đã hoàn thành các yêu cầu:

✔ Screen giới thiệu bản thân

✔ Screen giải phương trình bậc 2

✔ Screen sử dụng WebViewer

✔ Điều hướng giữa các Screen bằng Button

✔ Áp dụng lập trình trực quan bằng Block của MIT App Inventor

Qua bài tập, sinh viên hiểu được quy trình thiết kế giao diện kéo thả, thay đổi thuộc tính đối tượng và xây dựng chức năng bằng Block Programming trên nền tảng MIT App Inventor.
