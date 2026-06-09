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

# 2. Viết app sử dụng Android Studio
# 2. Xây dựng ứng dụng bằng Android Studio

## 2.1 AndroidManifest.xml

### AndroidManifest.xml là gì?

`AndroidManifest.xml` là file cấu hình quan trọng của ứng dụng Android. File này giúp hệ điều hành biết ứng dụng có những thành phần gì và được phép làm gì.

AndroidManifest.xml dùng để:

* Khai báo Activity
* Khai báo quyền của ứng dụng
* Cấu hình ứng dụng
* Thiết lập các thành phần của app

Ví dụ:

```xml
<manifest>

    <application>

        <activity
            android:name=".MainActivity"/>

    </application>

</manifest>
```

---

### Khai báo quyền cho ứng dụng

Nếu ứng dụng muốn sử dụng Internet, Camera hoặc GPS thì phải khai báo quyền trong `AndroidManifest.xml`.

Ví dụ quyền Internet:

```xml
<uses-permission android:name="android.permission.INTERNET"/>
```

Ví dụ quyền Camera:

```xml
<uses-permission android:name="android.permission.CAMERA"/>
```

### Mục đích của việc khai báo quyền

Việc khai báo quyền giúp:

* Hệ điều hành kiểm soát truy cập
* Bảo vệ dữ liệu người dùng
* Tránh ứng dụng sử dụng trái phép tài nguyên thiết bị

Ví dụ:

Nếu ứng dụng sử dụng WebView hoặc gọi API thì cần quyền Internet.

---

## 2.2 Vòng đời của ứng dụng Android

Trong Android, mỗi Activity đều hoạt động theo vòng đời (Lifecycle).

Các hàm quan trọng gồm:

### onCreate()

Được gọi khi Activity vừa được tạo.

Chức năng:

* Khởi tạo giao diện
* Khởi tạo dữ liệu
* Ánh xạ View

Ví dụ:

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
}
```

### onStart()

Được gọi khi Activity bắt đầu hiển thị.

### onResume()

Được gọi khi người dùng bắt đầu tương tác với ứng dụng.

### onPause()

Được gọi khi ứng dụng tạm dừng.

Ví dụ:

* Có cuộc gọi đến
* Chuyển sang app khác

### onStop()

Được gọi khi Activity không còn hiển thị.

### onDestroy()

Được gọi trước khi Activity bị huỷ.

### Tại sao Android Studio tự sinh hàm onCreate()?

Sau khi tạo project, Android Studio tự sinh hàm `onCreate()` vì đây là nơi khởi tạo ban đầu của Activity.

Hàm này dùng để:

* Hiển thị giao diện bằng `setContentView()`
* Viết code xử lý ban đầu
* Khởi tạo component

Nếu không có `onCreate()`, ứng dụng sẽ không hiển thị giao diện.

---

## 2.3 Kiểm tra quyền trong Java

Ngoài việc khai báo trong `AndroidManifest.xml`, nhiều quyền cần được kiểm tra khi ứng dụng chạy.

Ví dụ kiểm tra quyền Camera:

```java
if (ContextCompat.checkSelfPermission(this,
        Manifest.permission.CAMERA)
        != PackageManager.PERMISSION_GRANTED) {

    ActivityCompat.requestPermissions(
            this,
            new String[]{
                    Manifest.permission.CAMERA
            },
            1
    );
}
```

### Ý nghĩa của đoạn code

`checkSelfPermission()`

* Kiểm tra ứng dụng đã được cấp quyền hay chưa.

`requestPermissions()`

* Hiển thị hộp thoại xin quyền từ người dùng.

Việc kiểm tra quyền giúp tránh lỗi khi truy cập Camera hoặc bộ nhớ.

---

## 2.4 Giao diện Android bằng XML

Trong Android Studio, giao diện được mô tả bằng file XML nằm trong:

```text
res/layout
```

Ví dụ:

```text
activity_main.xml
```

XML giúp tách riêng giao diện khỏi code Java.

Ví dụ một TextView:

```xml
<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Xin chào"/>
```

Android Studio còn hỗ trợ giao diện kéo thả (UI Design Review) để xem trước bố cục ứng dụng.

---

## 2.5 Tránh Hardcode dữ liệu

### Hardcode là gì?

Hardcode là việc ghi trực tiếp giá trị vào XML.

Ví dụ không nên dùng:

```xml
android:text="Hello"
```

### Cách đúng: lưu vào strings.xml

Android cho phép lưu text trong:

```text
res/values/strings.xml
```

Ví dụ:

```xml
<resources>

    <string name="hello">
        Hello
    </string>

</resources>
```

### Cách tham chiếu

Cú pháp:

```text
@string/tên_biến
```

Ví dụ:

```xml
android:text="@string/hello"
```

### Ưu điểm

* Dễ chỉnh sửa
* Không bị lặp dữ liệu
* Hỗ trợ đa ngôn ngữ
* Dễ bảo trì ứng dụng

---

## 2.6 LOCATION, LANGUAGE, THEME

Android hỗ trợ tự động lấy dữ liệu theo:

* Location
* Language
* Theme

Ví dụ:

Tiếng Việt:

```text
values-vi
```

Tiếng Anh:

```text
values-en
```

Android sẽ tự động chọn ngôn ngữ phù hợp với điện thoại của người dùng.

### Lợi ích

Nhờ cơ chế này, ứng dụng có thể:

* Tự đổi ngôn ngữ
* Hỗ trợ nhiều quốc gia
* Hỗ trợ Dark Mode và Light Mode
* Tăng trải nghiệm người dùng

---

## 2.7 Đối tượng chứa (Layout Container)

Layout Container dùng để nhóm các component lại với nhau.

### LinearLayout

Sắp xếp theo chiều dọc:

```xml
android:orientation="vertical"
```

Sắp xếp theo chiều ngang:

```xml
android:orientation="horizontal"
```

Ví dụ:

```xml
<LinearLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

</LinearLayout>
```

### Gravity

Dùng để căn chỉnh vị trí hiển thị.

Ví dụ:

```xml
android:gravity="center"
```

Một số giá trị thường dùng:

* center
* left
* right

---

## 2.8 Code tương tác với Layout

Ví dụ hiển thị text lên màn hình.

### Bước 1: Ánh xạ View

```java
TextView txt;

txt = findViewById(R.id.txtKetQua);
```

### Bước 2: Hiển thị text

Không nên hardcode:

```java
txt.setText("Hello");
```

Nên dùng:

```java
txt.setText(getString(R.string.hello));
```

### Lợi ích

* Tự đổi ngôn ngữ
* Hỗ trợ Theme
* Dễ sửa đổi nội dung

---

## 2.9 Event trong Android

Event là hành động của người dùng tác động vào ứng dụng.

Ví dụ:

* Click Button
* Click TextView
* Chạm màn hình

Khi xảy ra event, chương trình sẽ thực hiện một đoạn code tương ứng.

### Cách 1: Dùng XML

Trong Layout:

```xml
<Button
    android:onClick="xuLyNhanNut"/>
```

Trong Java:

```java
public void xuLyNhanNut(View view){

    Toast.makeText(
            this,
            "Đã nhấn nút",
            Toast.LENGTH_SHORT
    ).show();

}
```

### Cách 2: Dùng Listener trong Java

Ánh xạ Button:

```java
Button btn;

btn = findViewById(R.id.btnTinh);
```

Bắt sự kiện click:

```java
btn.setOnClickListener(
        new View.OnClickListener() {

    @Override
    public void onClick(View v) {

        Toast.makeText(
                MainActivity.this,
                "Đã click",
                Toast.LENGTH_SHORT
        ).show();

    }
});
```

### So sánh

**Cách XML**

Ưu điểm:

* Viết nhanh
* Dễ làm với app nhỏ

Nhược điểm:

* Khó quản lý app lớn

**Cách Listener Java**

Ưu điểm:

* Linh hoạt
* Dễ mở rộng

Nhược điểm:

* Code dài hơn

Trong thực tế, `setOnClickListener()` thường được sử dụng nhiều hơn.


