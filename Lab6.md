
# Thiết Kế Chi Tiết Các Lớp Cho Hệ Thống Payroll System

Dựa trên kết quả thiết kế hệ thống con từ bài Lab 6, dưới đây là thiết kế chi tiết các lớp trong hệ thống Payroll System.

## Phân Hệ Giao Diện Người Dùng (UI Subsystem)
### Lớp: `LoginPage`
- **Thuộc tính:**
  - `email`: String
  - `password`: String
- **Phương thức:**
  - `displayError()`: Hiển thị thông báo lỗi khi thông tin đăng nhập không hợp lệ.

### Lớp: `LoginController`
- **Thuộc tính:** 
  - `authService`: AuthService (để thực hiện xác thực người dùng)
- **Phương thức:**
  - `login(email: String, password: String)`: Xử lý yêu cầu đăng nhập từ người dùng.

---

## Phân Hệ Xác Thực (Authentication Subsystem)
### Lớp: `AuthService`
- **Phương thức:**
  - `validateUser(email: String, password: String)`: Kiểm tra tính hợp lệ của thông tin đăng nhập.

### Lớp: `Validator`
- **Phương thức:**
  - `checkFormat(email: String, password: String)`: Kiểm tra định dạng của email và độ dài mật khẩu.

---

## Phân Hệ Cơ Sở Dữ Liệu (Database Subsystem)
### Lớp: `UserRepository`
- **Phương thức:**
  - `findUser(email: String)`: Truy xuất thông tin người dùng từ cơ sở dữ liệu dựa trên email.

### Lớp: `Database`
- **Phương thức:**
  - `connect()`: Kết nối đến cơ sở dữ liệu.

---

## UML Class Diagram

![Diagram](https://www.planttext.com/api/plantuml/png/d99BJiCm48RtFiKiYqGka4LLn6F50b6L_TGUKWl74utTe0fniYvw9Av075BY9Xl4qlFu_fb__7KyhK94YVlQAUqm17Zaoledh0W-5401LADr9QoZM5_raQOhUsSnMH30sD0uFDoBi2okIcZP6lMfSkWj-oZi7Cc0ndtShKbQgwc4c_7H0rrgMLoeNy-aPq8PfHS1QD5PWv4sWUGFk2sp8_GZyUMddsNWwHtfjmUM6kD_S6cCPseus0vv69YlrflvV5rx2ewzTnXnY-6ycMRlISVSxV5uHR6SkgwcLqWrkUsvUIdtk_eiSxc5cYoLAiwpgXLvq_skRm000F__0m00)

## Trạng Thái Của Lớp LoginController
Biểu đồ trạng thái mô tả các trạng thái chính của lớp `LoginController`:

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bUqLgo2hgwTWcTAJYeNY03pmX9pCbCIIpBpqXMi54ABKuiKYakJSZDBYXMIYr9JKlDACXDpYhcGL84qEPQMP82aaXDBKbE0-c3I-Nb0tSd9gSN5QQKvw9fSYuhoYr0LfoLcvgIcS3cavgK0NGW0003__mC0)

---

## Ghi Chú
- Các lớp và phương thức được thiết kế nhằm phục vụ các chức năng chính đã phân tích trong các hệ thống con.
- Trạng thái và luồng hoạt động của hệ thống đã được mô tả chi tiết thông qua biểu đồ UML.


