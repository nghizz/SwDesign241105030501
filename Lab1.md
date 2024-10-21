## LAB01

# 1. Phân tích kiến trúc

## Đề xuất kiến trúc: Kiến trúc 3 lớp (3-tier architecture)

### Lý do lựa chọn:
Kiến trúc 3 lớp là một kiến trúc phần mềm phổ biến và linh hoạt, phù hợp cho việc phát triển các ứng dụng doanh nghiệp như Hệ thống Quản lý Bảng lương (Payroll System). Kiến trúc này chia ứng dụng thành ba lớp riêng biệt: Lớp Giao diện người dùng (Presentation Layer), Lớp Logic nghiệp vụ (Business Logic Layer) và Lớp Dữ liệu (Data Layer), giúp tách biệt các mối quan tâm, tăng tính bảo trì và mở rộng của hệ thống.

### Ý nghĩa từng thành phần trong kiến trúc:

- **Lớp Giao diện người dùng (Presentation Layer)**: Chịu trách nhiệm hiển thị giao diện người dùng và xử lý tương tác của người dùng. Trong bài toán này, lớp này sẽ bao gồm các thành phần giao diện như Windows Desktop Application để nhân viên có thể nhập thông tin thẻ giờ làm việc, đơn đặt hàng và thay đổi phương thức thanh toán.

- **Lớp Logic nghiệp vụ (Business Logic Layer)**: Chứa các quy tắc nghiệp vụ và xử lý logic của hệ thống. Trong bài toán này, lớp này sẽ bao gồm các thành phần như xử lý tính toán lương, kiểm tra giới hạn giờ làm việc, tính toán hoa hồng, quản lý thông tin nhân viên và xử lý các quy tắc nghiệp vụ khác.

- **Lớp Dữ liệu (Data Layer)**: Chịu trách nhiệm truy cập và quản lý dữ liệu từ các nguồn dữ liệu khác nhau. Trong bài toán này, lớp này sẽ bao gồm các thành phần như kết nối và truy vấn cơ sở dữ liệu Project Management Database (IBM DB2), lưu trữ và truy xuất thông tin nhân viên, thẻ giờ làm việc và đơn đặt hàng.

- **Biểu đồ Package:**
  ![Diagram](https://www.planttext.com/api/plantuml/png/P59BRW8n3DtFAI9MxOOZL9JI1HAeemeEu7eCfEGpjPDAeugJTT4ZzGfDWCbqX9VlsNxlEVdz_fb900xHcge5FCAUrAHc4d81WlPEhQ0ZdgYlIYaq8AAsGhnqWNW7I6SyLwEbDT1jbtVtL-G0hZ5KkW7pkZDxgaxLe3QFeXsbnIk_rtYhr_CNkjT3C1WD1AgXOszCaGr9wRZHbWfYmIMXPziQtn59mSkA9s-j5kdjvIAtyupKQxz6SnqSUrz0W5l76Nr4p9cANUySOTZupBs13Eu-8d5NitzFzFhirARRB-QbGOBduZwF5uOfiAPFocaHk1cHbzHrP3makHTkYFyb63_YTFemFdCrFdhcXr3LZ5oJFimV0000__y30000)


# 2. Cơ chế phân tích

Để giải quyết bài toán này, tôi sẽ đề xuất một số cơ chế phân tích phù hợp cùng với lý giải:

1. **Phân tích nhu cầu và yêu cầu**: Hiểu rõ mục tiêu, phạm vi và ràng buộc của bài toán là điều cực kỳ quan trọng. Cần xác định rõ các yêu cầu chức năng và phi chức năng, đối tượng sử dụng, môi trường triển khai và các yếu tố liên quan khác.

2. **Phân tích dữ liệu đầu vào và đầu ra**: Xác định rõ cấu trúc, định dạng và nguồn của dữ liệu đầu vào. Đồng thời, cần xác định cấu trúc và định dạng của dữ liệu đầu ra mong muốn. Điều này giúp xác định các bước xử lý dữ liệu cần thiết.

3. **Phân tích quy trình nghiệp vụ**: Nếu bài toán liên quan đến quy trình nghiệp vụ, cần phân tích và mô hình hóa các bước, luồng công việc và quy trình liên quan để hiểu rõ logic nghiệp vụ.

4. **Phân tích kiến trúc và thiết kế hệ thống**: Xác định kiến trúc phần mềm phù hợp với yêu cầu bài toán, bao gồm các thành phần, mô-đun, giao diện và mối quan hệ giữa chúng. Đồng thời, xác định mô hình thiết kế chi tiết cho từng thành phần.

5. **Phân tích hiệu suất và tối ưu hóa**: Nếu bài toán đòi hỏi hiệu suất cao hoặc tối ưu hóa tài nguyên, cần phân tích các yếu tố ảnh hưởng và đề xuất các giải pháp tối ưu hóa phù hợp.

6. **Phân tích rủi ro và đảm bảo chất lượng**: Xác định các rủi ro tiềm ẩn và đề xuất các biện pháp giảm thiểu rủi ro. Đồng thời, xác định các yêu cầu và quy trình đảm bảo chất lượng phù hợp.

7. **Phân tích an toàn và bảo mật**: Nếu bài toán liên quan đến xử lý dữ liệu nhạy cảm hoặc yêu cầu an toàn cao, cần phân tích các mối đe dọa an toàn và bảo mật, đề xuất các biện pháp kiểm soát và bảo vệ phù hợp.

# 3. Phân tích ca sử dụng Select Payment

## Biểu đồ lớp phân tích cho ca sử dụng Payment

## Hình ảnh UML

![Diagram](https://www.planttext.com/api/plantuml/png/f5BBIWD14BplLpGvHN43NeTb2GOFWa8E_a2pwNtWF9RfpY6eN-R1J_8N72V3iXD5q1oxkhgehkwFj_Sr2thP6rqq6fdXrepQ7OZWkG0eWL9vjrCmM8cOHKCAMFnWkmYCU31avO6aTu6tdPU10C2agP4CN_usT56y5ibFXaTJLHMCa6-neRgEygDt3J4dwXADsrjHq6g7SZMjeARTPl8Rv3xDHV6pn6xGFZrwjDoIFryjpMoF2iwdYsIviOBxWQNAKZg6ugaB7V9_IVtVZgUlMLmleFH3rqjPno9_XcyxHNxvnRqyvSvFirgzr2VjBEmV-ckok_3Mdm000F__0m00)

### Giải thích:
- **Employee**: 
  - Đại diện cho một nhân viên, có các thuộc tính như ID nhân viên, tên và phương thức thanh toán. 
  - Nhân viên có thể chọn phương thức thanh toán thông qua phương thức `selectPaymentMethod`.
  
- **PaymentMethod**: 
  - Là một **interface** định nghĩa phương thức `processPayment` để xử lý thanh toán với số tiền và thông tin nhân viên nhất định.
  
- **CashPayment và BankTransfer**: 
  - Là các lớp cụ thể triển khai interface `PaymentMethod`, tương ứng với các phương thức thanh toán bằng tiền mặt và chuyển khoản ngân hàng.
  
- **PaymentProcessor**: 
  - Quản lý các phương thức thanh toán đã đăng ký và xử lý thanh toán cho một nhân viên với số tiền nhất định.

## Biểu đồ sequence mô tả hành vi của ca sử dụng Select Payment

## Hình ảnh UML

![Diagram](https://www.planttext.com/api/plantuml/png/X95D2i8m48NtESKiAzWBk91kN0h56uHqq42I2SbaqREvw96yWe6qeZNMtVnzxpsOnttg8il0oHeX5LE0a_M6HaJXyrWhxQLZwELeqN4VI66C56hBC_AD1Y4M0MYFNzm18XfK_84q_htRYJLK5mfurP4nR4hz2UDBEIyQQIavtWnGX7-GUy3PxgLHxg6jsvV91MCoN77Dq99_VToX6_BFdW000F__0m00)

### Giải thích:
1. Nhân viên chọn phương thức thanh toán bằng cách gọi phương thức `selectPaymentMethod` trên `PaymentProcessor`.
2. `PaymentProcessor` đăng ký phương thức thanh toán bằng cách gọi phương thức `registerPaymentMethod`.
3. Nhân viên yêu cầu xử lý thanh toán bằng cách gọi phương thức `processPayment` trên `PaymentProcessor` với số tiền cần thanh toán.
4. `PaymentProcessor` chuyển tiếp yêu cầu thanh toán đến phương thức thanh toán đã đăng ký bằng cách gọi phương thức `processPayment` trên đối tượng `PaymentMethod`.
5. `PaymentMethod` xử lý thanh toán và trả về kết quả cho `PaymentProcessor`.
6. `PaymentProcessor` trả về kết quả thanh toán cho nhân viên.

# 4. Phân tích ca sử dụng Maintain Timecard

## Biểu đồ lớp phân tích cho ca sử dụng Maintain Timecard

## Hình ảnh UML

![Diagram](https://www.planttext.com/api/plantuml/png/d9DDReCm48Ntd6B4YbG1ALk4K1QDr4hDfie59k0GLyP6zX0rQdkoBdgaNg76_9GGL4NT83FpvfldiVtz-RKsX9hgKdYPG6DWKrP2dHc3DmyW1DRzFkOnS4ak9h5aCHZIN1Os063gVSbfnqkMeSu3wXOnzA65z-5r_3xKyNljc3_NqxcyHxADcs-ha_aaGefGFAXQcnWEGY4vUvZdJTUD97qEyg5Y2SUHSk6a6Ogi5ZQv6qZ1ZFajIYoOdkp1efwueQHNfRSEnvciAgrEx4hN3Q4LQVR2icjMfrdQF1eb-xEPCVvSY_PaayGMC7t0ZAMjpnCAtWpdBwSnx9KI3EKlUOklRam3-H-awLZzbGzX6ARWt_b3oMsgnePtuIcAtjFBz7357K7puaWDPHL5utPhUxtii_W1003__mC0)

### Giải thích:
- **Employee**: 
  - Đại diện cho một nhân viên, có các thuộc tính như ID nhân viên và tên. 
  - Nhân viên có thể gửi thẻ giờ làm việc bằng cách gọi phương thức `submitTimecard`.
  
- **Timecard**: 
  - Đại diện cho một thẻ giờ làm việc, có các thuộc tính như ID thẻ giờ, ID nhân viên, ngày bắt đầu, ngày kết thúc và tổng số giờ làm việc. 
  - Thẻ giờ có thể thêm mục nhập giờ làm việc và tính toán tổng số giờ làm việc.
  
- **TimecardManager**: 
  - Quản lý các thẻ giờ làm việc, bao gồm gửi, phê duyệt và từ chối thẻ giờ làm việc. 
  - Nó cũng quản lý các quy tắc kiểm tra thẻ giờ làm việc.
  
- **TimecardRule**: 
  - Là một **interface** định nghĩa phương thức `validateTimecard` để kiểm tra tính hợp lệ của thẻ giờ làm việc.
  
- **MaxHoursRule**: 
  - Là một lớp cụ thể triển khai interface `TimecardRule`, kiểm tra xem tổng số giờ làm việc trong thẻ giờ có vượt quá giới hạn tối đa hay không.

## Biểu đồ sequence mô tả hành vi của ca sử dụng Maintain Timecard

## Hình ảnh UML

![Diagram](https://www.planttext.com/api/plantuml/png/Z58xRWCX4EqvnPHhoRx0IexSM8gBD8ulC859GZGB20PBFbiA7ybN24XBVekYT33lo-VsVjqbmIXvOeLQV8Jz5DXVY5GeOwjjG2TmiXDfZEO17RvGx6BTuJ4pATKyONFtYOo0njJDtacy30Q5rl3gSqmhrJW_-HfPPowyanVa-qeTLbtlkUO8AJzDLjfua7dnbJ0plujhvH7EoBPs-aDRYR3fnSvYwzsHKcPH2baMKzXkGM8c1RyTkcV14A8_BmiTIYNYH5t_Pop8FmCYlP5UNjR1h0k4oRkIuunQtbqnQwymGfCz2afEQbSavNDz0000__y30000)
### Giải thích:
1. Nhân viên thêm mục nhập giờ làm việc vào thẻ giờ bằng cách gọi phương thức `addTimeEntry` trên đối tượng `Timecard`.
2. `Timecard` tính toán tổng số giờ làm việc bằng cách gọi phương thức `calculateTotalHours`.
3. Nhân viên gửi thẻ giờ làm việc bằng cách gọi phương thức `submitTimecard` trên `TimecardManager`.
4. `TimecardManager` kiểm tra tính hợp lệ của thẻ giờ làm việc bằng cách gọi phương thức `validateTimecard` trên các đối tượng `TimecardRule`.
5. `TimecardRule` trả về kết quả kiểm tra tính hợp lệ cho `TimecardManager`.
6. Nếu thẻ giờ làm việc hợp lệ, `TimecardManager` phê duyệt thẻ giờ bằng cách gọi phương thức `approveTimecard`. Nếu không hợp lệ, `TimecardManager` từ chối thẻ giờ bằng cách gọi phương thức `rejectTimecard` với lý do từ chối.
7. `TimecardManager` trả về trạng thái của thẻ giờ làm việc (được phê duyệt hoặc bị từ chối) cho nhân viên.

# 5. Hợp nhất kết quả phân tích

## Hình ảnh UML

![Diagram](https://www.planttext.com/api/plantuml/png/f5HBRi8m4Dtd51QhW02fsmX5LJzIAnK9LLnWI0P8wzZ8dg2YjYVheaVg5UeuJXe7g6ZPHF7Cc-StusT_VNnUQW95HSw3X8FMx3RVSBb3PAy1OoE6RdcVHYmJP6C2SeoO9fM9bGriO9UZe2dIMXhShBqq0COqSap8YuU_5VMhgcAHPpJFSan0fI6vduZLeNxm7ZZPTSZ9hh5jsOTQiStV09b-oc-54sadGfA0tyb2wOWjkGIoyY1Dorrl1QbTc3OLGxPk8QjE4k19mKrotZ25BV5UxxQ3oSGeHBM41EFOKcoKJ51h1mqXbuKWjycmwIrgpgz5VmrwxUei-LbaLo2Uvmg4Ng8wdytLp2e6gTpnUTumetp8D4syALL3KRWo6LH_TTOPYckZJK702bN7RxNM6XMVQcHhg8tHjSKzd3DitxNyPAxICSpGv45BKL_F0y8V2uv7FBO5dfL6_arfn1PISWJnmpo55slfXlaVJCspqxleiP7ALciQnNRXloR7SEFneDTG1tksikXHYHnq6TktOpn-Ypjfp-y7ybq_U3irWav2bVCBl67Q_RpqfNcTp6Fz3G00__y30000)

## Mô tả:

- **Lớp Employee**:
  - Đại diện cho một nhân viên trong hệ thống.
  - Có các thuộc tính như ID nhân viên, tên và phương thức thanh toán.
  - Có phương thức để chọn phương thức thanh toán và gửi thẻ giờ làm việc.

- **Lớp Timecard**:
  - Đại diện cho một thẻ giờ làm việc.
  - Có các thuộc tính như ID thẻ giờ, ID nhân viên, ngày bắt đầu, ngày kết thúc và tổng số giờ làm việc.
  - Có phương thức để thêm mục nhập giờ làm việc và tính toán tổng số giờ làm việc.

- **Lớp PaymentMethod**:
  - Là một **interface** định nghĩa phương thức xử lý thanh toán.
  - Có phương thức `processPayment` để xử lý thanh toán với số tiền và thông tin nhân viên.

- **Lớp CashPayment và BankTransfer**:
  - Là các lớp cụ thể triển khai interface `PaymentMethod`.
  - Tương ứng với các phương thức thanh toán bằng tiền mặt và chuyển khoản ngân hàng.

- **Lớp PaymentProcessor**:
  - Quản lý các phương thức thanh toán đã đăng ký.
  - Có phương thức để đăng ký phương thức thanh toán và xử lý thanh toán cho nhân viên với số tiền nhất định.

- **Lớp TimecardManager**:
  - Quản lý các thẻ giờ làm việc và các quy tắc kiểm tra thẻ giờ.
  - Có phương thức để gửi, phê duyệt và từ chối thẻ giờ làm việc.

- **Lớp TimecardRule**:
  - Là một **interface** định nghĩa phương thức kiểm tra tính hợp lệ của thẻ giờ làm việc.

- **Lớp MaxHoursRule**:
  - Là một lớp cụ thể triển khai interface `TimecardRule`.
  - Kiểm tra xem tổng số giờ làm việc trong thẻ giờ có vượt quá giới hạn tối đa hay không.

Trong mô hình hợp nhất này, các lớp phân tích từ cả hai ca sử dụng đã được kết hợp lại. Lớp `Employee` liên kết với cả `PaymentMethod` và `Timecard`. Các lớp `PaymentProcessor` và `TimecardManager` tương ứng với xử lý thanh toán và quản lý thẻ giờ làm việc. Các quy tắc kiểm tra được áp dụng cho thẻ giờ làm việc thông qua lớp `TimecardRule`.

Mô hình này cung cấp một cái nhìn tổng quan về các lớp và mối quan hệ giữa chúng trong hệ thống quản lý nhân viên, thanh toán và thẻ giờ làm việc. Nó có thể được sử dụng làm cơ sở cho việc thiết kế và triển khai hệ thống trong các giai đoạn tiếp theo.
