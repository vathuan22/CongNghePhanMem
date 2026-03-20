# Bài 6: Thiết kế chi tiết

## 6.1. Mục tiêu của thiết kế chi tiết

\- Giảm sai sót và sự mơ hồ khi lập trình

\- Tăng khả năng bảo trì và mở rộng hệ thống

\- Ước tính chính xác hơn thời gian và nguồn lực cần thiết

## 6.2. Nội dung của thiết kế chi tiết

**\[1\] Thiết kế dữ liệu chi tiết**

Đây là bước cụ thể hóa sơ đồ thực thể quan hệ (ERD) từ giai đoạn kiến trúc thành cấu trúc lưu trữ thực tế.

\- Cơ sở dữ liệu: Xác định chính xác tên bảng, kiểu dữ liệu, độ dài trường dữ liệu, các ràng buộc (Not Null, Unique) và các khóa (Primary Key, Foreign Key)

\- Cấu trúc dữ liệu trong bộ nhớ: Thiết kế các mảng (Array), danh sách (List), hay các cấu trúc dữ liệu phức tạp để xử lý dữ liệu tạm thời trong quá trình phần mềm chạy

**\[2\] Thiết kế logic xử lý**

Mô tả cách thức hoạt động bên trong của từng chức năng. Thay vì viết mã ngay, kiến trúc sư sẽ sử dụng công cụ trung gian để mô tả logic.

\- Công cụ: Sử dụng lưu đồ (flowchart) hoặc mã giả (pseudo-code)

\- Nội dung: Xác định các bước rẽ nhánh (if-else), vòng lặp (loop) và các thuật toán đặc thù (ví dụ: cách tính thuế, cách lọc dữ liệu)

**\[3\] Thiết kế giao diện lập trình**

Đây là việc thiết kế các "hợp đồng" kết nối giữa các thành phần phần mềm (không phải giao diện người dùng).

\- Định nghĩa API/Phương thức: Xác định tên hàm, danh sách tham số đầu vào (input) và kiểu dữ liệu trả về (output)

\- Mục tiêu: Giúp các nhóm lập trình viên có thể làm việc song song. Nhóm A chỉ cần biết nhóm B cung cấp hàm calculateTotal(items) là có thể gọi để dùng, không cần quan tâm bên trong nhóm B viết gì

**\[4\] Thiết kế phân cấp lớp**

Dành cho các ngôn ngữ lập trình hướng đối tượng (OOP).

\- Cấu trúc: Xác định các thuộc tính và phương thức cho từng lớp

\- Mối quan hệ: Mô tả các mối quan hệ kế thừa (Inheritance), bao đóng (Encapsulation) và đa hình (Polymorphism) để tối ưu hóa việc tái sử dụng mã nguồn

## 6.3. Mẫu thiết kế

\- Mẫu khởi tạo (Creational): Ví dụ như _Singleton_ (đảm bảo một lớp chỉ có một đối tượng duy nhất, dùng cho kết nối Database)

\- Mẫu cấu trúc (Structural): Ví dụ như _Adapter_ (giúp các thành phần không tương thích có thể làm việc với nhau)

\- Mẫu hành vi (Behavioral): Ví dụ như _Observer_ (tự động cập nhật giao diện khi dữ liệu thay đổi)

## 6.4. Kết quả đầu ra của thiết kế chi tiết

Kết thúc giai đoạn này, bạn phải có tài liệu thiết kế chi tiết (DDD: Detailed Design Document). Đây là "kim chỉ nam" cho lập trình viên. Một tài liệu DDD tốt là khi lập trình viên chỉ cần nhìn vào đó và viết mã, gần như không phải đưa ra quyết định về mặt logic hay cấu trúc nữa.