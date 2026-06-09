# BTL_Phattrienungdungdidong
# MÔN HỌC: PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG - TEE0419 BÀI TẬP LỚN:

1. Viết phần mềm trên công cụ Mit App inventor
   (tập trung vào quy trình tạo ra phần mềm)
   app có 3 screen:
   + about về bản thân+nút gọi sang 2 screen còn lại
   + giải 1 bài toán đơn giản
   + sử dụng webview: hiển thị 1 trang web có sẵn, hỗ trợ giao diện điện thoại
   mô tả: thanh công cụ có gì? kéo thả + thay đổi thuộc tính: làm ntn, để làm gì?
          block: mô tả bản chất việc kéo thả block ntn?
                 ưu điểm gì so với viết code? nhược điểm?
                 copy paste block ? (backpack)
2. Viết app sử dụng Android Studio
   + Android manifest.xml  => mô tả gì? app cần quyền để do-st: khai báo ntn? để làm gì?
   + vòng đời của 1 ứng dụng android.
     code tự sinh sau khi tạo 1 project: có sẵn hàm onCreate: tại sao???
   + Code: java language. 
     app cần check xem có quyền để do-st? : code ntn? ý nghĩa?
     giao diện: (res/layout) mô tả bằng file XML + UI Design review
        + thuộc tính text, hoặc các thuộc tính khác: giá trị hardcode => lưu vào nới khác, tham chiếu tới nó:
          cú pháp của việc tham chiếu là gì?
          ưu điểm của việc tham chiếu này?
          OS hỗ trợ auto việc lấy giá trị tham chiếu theo LOCATION, LANGUAGE, THEME
          việc hỗ trợ auto này giúp app làm được điều gì?	
        + đối tượng chứa: gộp các đối tượng con lại: cùng 1 quy luật sắp xếp để hiển thị 
          các đối tượng con nằm kề nhau theo chiều dọc | hoặc ngang, gravity
     code tương tác với layout: vd hiển thị text
          mong muốn text hiển thị phù hợp với thiết lập LOCATION, LANGUAGE, THEME của người dùng
          thì làm ntn? (tránh hardcode)
     event (sự kiện) người dùng tác động vào app: CLICK vào button, click vào text,...
          với 1 sự kiện nào đó, muốn chạy 1 đoạn code để do-st
          thì LAYTOUT cần làm gì?
              CODE viết như nào (2 cách)
---------------------------
     trong app có các thư mục đặc biệt: Assets
     khi sử dụng Window Explorer để copy các files + folder vào trong Assets
     thì khi compiler: mọi file này đều đi theo app, nằm trong app
     trong app có thể truy cập được đến các file này
     cú pháp truy cập vào là gì?
     lợi ích của việc app có sẵn các files (offline cũng có)?
     ứng dụng: app hướng dẫn việc X

==> tạo app1 sử dụng cơ chế Dữ liệu chuẩn bị trước trong Assets
         format dữ liệu: tuỳ ý, nội dung tuỳ ý
         công cụ để hiển thị dữ liệu: tuỳ ý
         có cần phải tiền xử lý trước khi hiển thị ko: tuỳ ý.
         SV TỰ ĐẶT RA VẤN ĐỀ => TỰ GIẢI QUYẾT VẤN ĐỀ
         MÔ TẢ ĐƯỢC DỮ LIỆU CÓ ĐẶC THÙ GÌ
                    DÙNG THUẬT TOÁN NÀO ĐỂ XỬ LÝ DỮ LIỆU (NẾU CẦN)
                    DÙNG ĐỐI TƯỢNG NÀO ĐỂ HIỂN THỊ DỮ LIỆU.
                    (ĐỘ SÁNG TẠO LÀ KO GIỚI HẠN)
------------------------
APP2 (android studio):  tạo app tương đương với Mit App inventor
  app có 3 activity
  + activity1: about: about+nút gọi sang 2 activity còn lại
  + activity2: giải toán đơn giản (tuỳ ý). mỗi khi giải xong bài toán: gọi api tại https://k58kmt.tdh.io.vn/api
    để gửi bài toán lên đó
    {app_by:mã số sv, input: {a:1,b:2,c:3,name:"hello tắc kè"},output:{ketluan:"vô nghiệm", abc:"xyz", nghiem:3.14}}
    nhận lại json: {ok:1, stt:1234}
  + activity3: 
    dùng web-view để truy cập từ 
    1 trang web https://k58kmt.tdh.io.vn?masv=mã sv của bạn
=======================
    vết để lại: mô tả quá trình làm bài tập ra file .md => upload github
    kèm hình ảnh minh hoạ quá trình làm.

    print ra giấy đóng quyển, nộp bm.

# BÀI LÀM
1. Viết phần mềm trên công cụ Mit App inventor
- Tạo Project
- Vào appinventor.mit.edu → Create Apps! → đăng nhập Google
- Click Projects → Start new project 

<img width="964" height="1024" alt="image" src="https://github.com/user-attachments/assets/e417d733-c614-433b-90e2-8a656b74dcdd" />

- Tạo Screen1 (About bản thân)
  
- Kéo Label -> Đổi nội dung -> Bên phải: Properties -> Tìm: Text -> đổi thành thông tin cá nhân ( - làm y hệt như vậy với 2 label còn lại)

- Tạo Button: Kéo: Button -> Text: giải toán ( button Web view cũng làm tương tự)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ece72356-a6cb-4951-8ef4-99e5a510320b" />

- Nút mở Screen2
- THIẾT KẾ SCREEN 2 (GIẢI PHƯƠNG TRÌNH ax+b=0)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cd306cf3-0913-4c4a-a850-020774b4f1be" />

Viết Block giải toán

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c8c1f616-1fc5-4f5c-9483-31445d685050" />

THIẾT KẾ SCREEN 3

ở phần url sẽ để https://k58kmt.tdh.io.vn?masv=K225480106102 , để test thử xem phần mit app có hoạt động không
Kéo thêm 1 dòng chữ (Label) từ cột User Interface bên trái thả vào màn hình, đặt nó nằm phía trên hoặc phía dưới cái WebViewer đó. Thay đổi chữ hiển thị của nút bấm thành: "Bài tập của Triệu Tra My".

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2305228f-5a8d-44c2-bbdc-dec446a0e056" />

- kết quả test

<img width="214" height="203" alt="image" src="https://github.com/user-attachments/assets/1330367f-182e-40d2-9574-99bdc064b5ec" />

<img width="591" height="1280" alt="image" src="https://github.com/user-attachments/assets/33f2f36f-e371-4365-bd7a-bce4dc096ea8" />

<img width="591" height="1280" alt="image" src="https://github.com/user-attachments/assets/bc559990-c372-4a24-ba44-0b990dbca8ca" />

## 1. Thanh công cụ trong MIT App Inventor

Trong quá trình xây dựng ứng dụng bằng MIT App Inventor, hệ thống cung cấp nhiều thanh công cụ hỗ trợ thiết kế giao diện và lập trình kéo thả.

### 1.1 Palette

**Palette** là nơi chứa các thành phần (component) có thể sử dụng để xây dựng ứng dụng như:

* Button (nút bấm)
* Label (văn bản)
* TextBox (ô nhập liệu)
* Image (hình ảnh)
* WebViewer (hiển thị website)
* Layout (sắp xếp giao diện)

Người dùng có thể chọn component từ Palette để đưa vào màn hình thiết kế.

### 1.2 Viewer

**Viewer** là khu vực mô phỏng giao diện điện thoại, nơi hiển thị các thành phần sau khi được kéo thả.

Mục đích:

* Thiết kế giao diện trực quan
* Quan sát bố cục ứng dụng
* Điều chỉnh vị trí các thành phần

### 1.3 Components

**Components** hiển thị danh sách các thành phần đã được thêm vào màn hình hiện tại.

Chức năng:

* Quản lý component
* Đổi tên component
* Xem cấu trúc giao diện

Ví dụ:

```text
Screen1
 ├── Label1
 ├── Button1
 └── Button2
```

### 1.4 Properties

**Properties** dùng để thay đổi thuộc tính của component được chọn.

Một số thuộc tính thường dùng:

| Thuộc tính      | Chức năng         |
| --------------- | ----------------- |
| Text            | Nội dung hiển thị |
| FontSize        | Kích thước chữ    |
| BackgroundColor | Màu nền           |
| Width           | Chiều rộng        |
| Height          | Chiều cao         |
| Visible         | Hiển thị hoặc ẩn  |

Ví dụ:

```text
Button
Text = Giải phương trình
Width = Fill Parent
FontSize = 18
```

## 2. Kéo thả component và thay đổi thuộc tính

### 2.1 Cách kéo thả component

Để tạo giao diện ứng dụng, người dùng thực hiện các bước:

**Bước 1:** Chọn component trong mục **Palette**

**Bước 2:** Giữ chuột và kéo component vào **Viewer**

**Bước 3:** Thả component vào vị trí mong muốn

Ví dụ:

* Kéo `Button` để tạo nút bấm
* Kéo `TextBox` để nhập dữ liệu
* Kéo `Label` để hiển thị kết quả

### 2.2 Thay đổi thuộc tính

Sau khi kéo thả component, người dùng có thể chỉnh sửa giao diện bằng cách:

**Bước 1:** Chọn component trong Viewer hoặc Components

**Bước 2:** Sang mục **Properties**

**Bước 3:** Thay đổi thuộc tính phù hợp

Ví dụ:

```text
Button1
Text = Đi tới màn hình giải toán
BackgroundColor = Blue
Width = Fill Parent
```

### 2.3 Mục đích của việc thay đổi thuộc tính

Việc chỉnh thuộc tính giúp:

* Làm giao diện đẹp hơn
* Điều chỉnh kích thước phù hợp
* Thay đổi nội dung hiển thị
* Tăng trải nghiệm người dùng
* Giúp ứng dụng trực quan hơn trên điện thoại

## 3. Block trong MIT App Inventor

### 3.1 Bản chất của block kéo thả

MIT App Inventor sử dụng **lập trình trực quan bằng block** thay vì viết code bằng cú pháp.

Người dùng sẽ kéo các khối lệnh (block) và ghép chúng với nhau để tạo logic cho chương trình.

Ví dụ:

Khi người dùng nhấn nút:

```text
when Button1.Click
```

Thực hiện hành động:

```text
open another screen
```

Các block sẽ liên kết với nhau giống như các mảnh ghép để mô tả luồng xử lý của ứng dụng.

### 3.2 Ưu điểm của block so với viết code

MIT App Inventor có nhiều ưu điểm:

* Dễ học và dễ tiếp cận với người mới
* Không cần ghi nhớ cú pháp lập trình
* Hạn chế lỗi cú pháp
* Thiết kế ứng dụng nhanh chóng
* Có thể quan sát luồng xử lý trực quan

Đặc biệt phù hợp với:

* Sinh viên mới học lập trình
* Người mới bắt đầu phát triển ứng dụng di động

### 3.3 Nhược điểm của block

Bên cạnh ưu điểm, block cũng có hạn chế:

* Khó phát triển ứng dụng lớn
* Thiếu tính linh hoạt so với viết code
* Khó quản lý khi logic chương trình quá nhiều
* Một số chức năng nâng cao khó thực hiện
* Giao diện lập trình có thể bị rối khi số lượng block lớn

### 3.4 Sao chép block bằng Backpack

MIT App Inventor hỗ trợ tính năng **Backpack** để sao chép và tái sử dụng block.

Cách thực hiện:

**Bước 1:** Chọn block muốn sao chép

**Bước 2:** Kéo block vào biểu tượng **Backpack**

**Bước 3:** Mở Backpack và kéo block ra để sử dụng lại

Mục đích của Backpack:

* Tiết kiệm thời gian
* Không cần tạo lại block giống nhau
* Dễ tái sử dụng logic giữa các màn hình
* Giảm thao tác lặp lại khi phát triển ứng dụng


