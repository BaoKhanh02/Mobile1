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

# Trả lời câu hỏi

## 1. Giới thiệu

MIT App Inventor là môi trường lập trình trực quan (Visual Programming) cho phép xây dựng ứng dụng Android bằng phương pháp kéo thả (Drag & Drop) mà không cần viết nhiều mã nguồn.

Trong bài thực hành, ứng dụng gồm 3 màn hình (Screen):

* Screen1: Giới thiệu bản thân (About).
* Screen2: Giải bài toán đơn giản.
* Screen3: Hiển thị Website bằng WebViewer.

---

# 2. Quy trình tạo phần mềm trên MIT App Inventor

Quy trình phát triển ứng dụng gồm các bước:

### Bước 1: Tạo Project

* Truy cập MIT App Inventor.
* Chọn Create New Project.
* Đặt tên Project.

Ví dụ:

```text
MyMobileApp
```

---

### Bước 2: Thiết kế giao diện (Designer)

Tại màn hình Designer:

* Kéo thả các thành phần giao diện.
* Sắp xếp bố cục.
* Thay đổi thuộc tính.

Ví dụ:

* Label
* Button
* TextBox
* Image
* WebViewer
* HorizontalArrangement
* VerticalArrangement

---

### Bước 3: Lập trình xử lý (Blocks)

Chuyển sang tab Blocks:

* Kéo các khối lệnh.
* Ghép các khối lại thành chương trình hoàn chỉnh.
* Xử lý sự kiện.
* Thực hiện tính toán.
* Chuyển màn hình.

---

### Bước 4: Chạy thử

Có thể chạy bằng:

* AI Companion
* Emulator
* Xuất file APK

---

## 3. Mô tả ứng dụng 3 Screen

### Screen1 – About

Chức năng:

* Hiển thị họ tên.
* Hiển thị MSSV.
* Hiển thị ảnh cá nhân.
* Có 2 nút chuyển màn hình.

Thành phần sử dụng:

* Label
* Image
* Button

Nút 1:

```text
Chuyển sang Screen2
```

Nút 2:

```text
Chuyển sang Screen3
```

---

### Screen2 – Giải bài toán đơn giản

Ví dụ:

Giải phương trình bậc hai:

```text
ax² + bx + c = 0
```

Thành phần:

* TextBox nhập a
* TextBox nhập b
* TextBox nhập c
* Button Giải
* Label hiển thị kết quả

Chức năng:

* Nhận dữ liệu người dùng.
* Tính toán.
* Hiển thị nghiệm.

---

### Screen3 – WebViewer

Thành phần:

* WebViewer

Chức năng:

* Hiển thị website có sẵn.
* Tương thích giao diện điện thoại.

Ví dụ:

```text
https://k58kmt.tdh.io.vn
```

Người dùng có thể tương tác trực tiếp với website trong ứng dụng.

---

# 4. Thanh công cụ của MIT App Inventor

Giao diện Designer gồm các khu vực chính:

### Palette

Chứa các thành phần có thể kéo thả:

* User Interface
* Layout
* Media
* Drawing and Animation
* Sensors
* Social
* Storage
* Connectivity

Mục đích:

* Chọn thành phần cần đưa vào ứng dụng.

---

### Viewer

Khu vực mô phỏng giao diện điện thoại.

Mục đích:

* Xem trước giao diện.
* Sắp xếp vị trí các đối tượng.

---

### Components

Danh sách các thành phần đã sử dụng.

Ví dụ:

```text
Screen1
Button1
Label1
Image1
```

Mục đích:

* Quản lý các đối tượng trên màn hình.

---

### Properties

Hiển thị thuộc tính của thành phần đang chọn.

Ví dụ:

* Text
* Width
* Height
* FontSize
* BackgroundColor
* Visible

Mục đích:

* Thay đổi cách hiển thị và hoạt động của đối tượng.

---

# 5. Kéo thả và thay đổi thuộc tính

Ví dụ tạo Button:

### Bước 1

Kéo Button từ Palette sang Viewer.

### Bước 2

Chọn Button.

### Bước 3

Tại Properties thay đổi:

```text
Text = Giải phương trình
Width = Fill Parent
FontSize = 18
```

Mục đích:

* Tùy chỉnh giao diện.
* Cải thiện trải nghiệm người dùng.
* Giúp ứng dụng trực quan hơn.

---

# 6. Blocks là gì?

Blocks là các khối lệnh trực quan đại diện cho mã nguồn lập trình.

Ví dụ:

```text
when Button1.Click
```

tương đương:

```java
button.setOnClickListener(...)
```

trong Java.

Mỗi block thực chất là:

* Lệnh điều kiện.
* Lệnh gán giá trị.
* Hàm xử lý.
* Sự kiện.
* Biến.
* Toán tử.

được biểu diễn bằng hình ảnh trực quan.

---

# 7. Bản chất của việc kéo thả Block

Khi ghép các block:

```text
when Button1.Click
    set Label1.Text to "Xin chào"
```

thực chất là:

* Tạo luồng xử lý chương trình.
* Xây dựng thuật toán.
* Sinh mã nguồn phía sau.

Nghĩa là người dùng không viết code trực tiếp mà lập trình thông qua các khối chức năng.

---

# 8. Ưu điểm của Block Programming

### Dễ học

Người mới bắt đầu có thể lập trình nhanh.

### Trực quan

Dễ nhìn thấy luồng xử lý.

### Ít lỗi cú pháp

Không cần nhớ:

```java
;
{}
()
```

như các ngôn ngữ lập trình truyền thống.

### Tăng tốc phát triển

Xây dựng ứng dụng đơn giản rất nhanh.

### Phù hợp giáo dục

Hỗ trợ học thuật toán và tư duy lập trình.

---

# 9. Nhược điểm của Block Programming

### Khó mở rộng

Dự án lớn sẽ có rất nhiều block.

### Tốn không gian

Block chiếm diện tích màn hình lớn.

### Khó quản lý

Thuật toán phức tạp trở nên rối.

### Hạn chế tính năng

Không linh hoạt bằng Java hoặc Kotlin.

### Hiệu quả thấp với dự án lớn

Khó phát triển các hệ thống chuyên nghiệp.

---

# 10. Copy và Paste Block bằng Backpack

MIT App Inventor hỗ trợ công cụ:

```text
Backpack
```

ở cuối màn hình Blocks.

### Cách sử dụng

Bước 1:

Kéo block vào Backpack.

Bước 2:

Mở Screen khác hoặc Project khác.

Bước 3:

Lấy block từ Backpack ra.

---

## Mục đích của Backpack

* Sao chép block.
* Tái sử dụng thuật toán.
* Tiết kiệm thời gian lập trình.
* Chia sẻ logic giữa nhiều màn hình.

Ví dụ:

Một khối xử lý tính toán ở Screen2 có thể được lưu vào Backpack và sử dụng lại ở Screen khác mà không cần tạo lại từ đầu.

---

