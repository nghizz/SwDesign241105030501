
# Thiết Kế Hệ Thống Con cho Payroll System

## 1. Phân hệ Giao diện Người Dùng (UI Subsystem)

### 1.1. Phân bổ hành vi
- **Nhận và hiển thị thông tin đăng nhập từ người dùng**: Giao diện người dùng cung cấp các trường nhập liệu để người dùng nhập thông tin như email và mật khẩu.
- **Hiển thị thông báo lỗi nếu thông tin đăng nhập không hợp lệ**: Khi thông tin nhập vào không hợp lệ, thông báo lỗi sẽ được hiển thị để người dùng điều chỉnh.

### 1.2. Tài liệu các phần tử
- **LoginPage**: Giao diện người dùng để nhập thông tin đăng nhập.
- **LoginController**: Quản lý các sự kiện và tương tác của người dùng với giao diện.

### 1.3. Sự phụ thuộc
- Phụ thuộc vào **Authentication Subsystem** để xử lý thông tin đăng nhập và trả về kết quả.

### 1.4. UML
Đề xuất UML cho phân hệ Giao diện Người Dùng:

![Diagram](https://www.planttext.com/api/plantuml/png/R91B2W8n44JtEKNXIXTpWIn458K15u9uW6Z24En9Gj9HH3oP2u_a5JGgE7vM3LNLhp_NysMKM4NEBOcWDblL6FHMDPPvdGw9JTl3KG0RKYbXxXlh5YLIDA22QPMbcJMa9POShMjUHhZdzpxgVnuLp3WpUoVnh0y7q3O5KeV-G6BdhRwh9_4vVU8THqzauci7OAV8QiMcTY5pfxK3dCReupVrVKrL3N_e4ZcP94vYP9mktxa1003__mC0)
- **Class Diagram**: Hiển thị các lớp như `LoginPage`, `LoginController`, và sự tương tác giữa chúng.

---

## 2. Phân hệ Xác thực (Authentication Subsystem)

### 2.1. Phân bổ hành vi
- **Kiểm tra tính hợp lệ của thông tin đăng nhập (email và mật khẩu)**: Xử lý logic xác thực để đảm bảo thông tin người dùng hợp lệ.
- **Gửi yêu cầu kiểm tra đến Database Subsystem**: Kiểm tra tính hợp lệ của thông tin đăng nhập trong cơ sở dữ liệu.

### 2.2. Tài liệu các phần tử
- **AuthService**: Xử lý logic xác thực đăng nhập.
- **Validator**: Kiểm tra tính hợp lệ của dữ liệu (ví dụ: định dạng email, độ dài mật khẩu).

### 2.3. Sự phụ thuộc
- Phụ thuộc vào **Database Subsystem** để truy xuất thông tin tài khoản người dùng.

### 2.4. UML
Đề xuất UML cho phân hệ Xác thực:
- **Class Diagram**: Hiển thị lớp `AuthService` và `Validator`.

![Diagram](https://www.planttext.com/api/plantuml/png/X91D2i8m48NtESNGLGLxWIwa8kw5WljfEjHWcfHCKX7foLnu9AzWunyjBfpbuxtlpSpzUYlOe_EXrQ93USI685a7Vo3ZbKIlh84oL7ncJsq25m4WDJ93z9JaUYNfgSRfKQiQFMqSrJ6FcbDgKUaSIk-KQPRGZTcJTVL7MUHGMQi9pSWOn1U_Vw6i-u5l8t2EdK6ctjsxBVrVExqdorQJ1N88J2m6KP2fuvyU0000__y30000)

---

## 3. Phân hệ Cơ sở Dữ liệu (Database Subsystem)

### 3.1. Phân bổ hành vi
- **Lưu trữ và truy xuất thông tin tài khoản người dùng**: Cơ sở dữ liệu lưu trữ các thông tin đăng nhập của người dùng (email, mật khẩu).
- **Kiểm tra tính hợp lệ của thông tin đăng nhập trong cơ sở dữ liệu**: Truy vấn và xác minh tài khoản người dùng.

### 3.2. Tài liệu các phần tử
- **UserRepository**: Xử lý các thao tác lưu trữ và truy vấn với cơ sở dữ liệu.
- **Database**: Quản lý kết nối với cơ sở dữ liệu.

### 3.3. Sự phụ thuộc
- Phụ thuộc vào **Authentication Subsystem** để xác thực thông tin đăng nhập.

### 3.4. UML
Đề xuất UML cho phân hệ Cơ sở Dữ liệu:
- **Class Diagram**: Hiển thị lớp `UserRepository` và `Database`.

![Diagram](https://www.planttext.com/api/plantuml/png/N5113e8m4Bpt5GqdFF013eOOVO0G7x2KbJH2mUwMI0mly-2J_88K1Onpc6GpipkJVJsU2J5OTdKbMb0NA546Us38WL1cBgUU6Ej0teMKgW8YUIAqARODQMviFmaUPsqAB-twGmsw2j5pB3EssfIRU5hxMWawz6FeHleeew5hT34Q1h4aBJtc3DKOWuh3rUs1DrIEyUZGzk7LyqziYkGgdk_-TO-YxHeIox4EYK4aQ0h_ZpS0003__mC0)

---

## 4. Các bước tiếp theo trong thiết kế hệ thống con

### 4.1. Kiểm tra các phân hệ
Đảm bảo rằng các hệ thống con được triển khai đúng chức năng và có thể giao tiếp với nhau như mong đợi.
Các kiểm tra có thể bao gồm việc xác minh sự tương tác giữa UI Subsystem, Authentication Subsystem, và Database Subsystem.

### 4.2. Tài liệu hóa sự phụ thuộc giữa các hệ thống con
Ghi lại rõ ràng các mối quan hệ giữa các phân hệ:
- UI Subsystem phụ thuộc vào Authentication Subsystem để xác thực thông tin đăng nhập.
- Authentication Subsystem phụ thuộc vào Database Subsystem để kiểm tra tính hợp lệ của thông tin tài khoản.

### 4.3. Lập tài liệu các phân hệ
Chi tiết hóa các lớp, phương thức, và chức năng của mỗi phân hệ trong tài liệu hệ thống con. Ví dụ:
- UI Subsystem: Lớp LoginPage và LoginController với các phương thức tương tác.
- Authentication Subsystem: Lớp AuthService và Validator.
- Database Subsystem: Lớp UserRepository và Database.

---

## 5. Các điểm kiểm tra

### 5.1. Xác thực hành vi của các phân hệ
Kiểm tra xem liệu các phân hệ có thực hiện đúng chức năng không, chẳng hạn như đăng nhập người dùng và xử lý lỗi.

### 5.2. Kiểm tra tính hợp lệ của các lớp
Đảm bảo các lớp trong mỗi phân hệ đáp ứng các yêu cầu chức năng và không có lỗi logic.

### 5.3. Đảm bảo tính liên kết
Kiểm tra các mối quan hệ giữa các phân hệ để đảm bảo chúng có thể giao tiếp và hoạt động đúng.
