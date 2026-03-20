# Bài 5: Thiết kế kiến trúc phần mềm

## 5.1 Kiến trúc phần mềm là gì?

Kiến trúc phần mềm là bản thiết kế tổng thể của một hệ thống, giúp chúng ta hiểu rõ các bộ phận cấu thành, cách chúng kết nối và các quy tắc chi phối toàn bộ cấu trúc.

**_Kiến trúc phần mềm mô tả ba yếu tố chính của một hệ thống:_**

\- Cấu trúc (structure): Hệ thống được chia thành các thành phần (components) hoặc mô-đun nhỏ hơn (ví dụ: mô-đun quản lý người dùng, mô-đun xử lý thanh toán)

\- Tương tác (interaction): Các thành phần kết nối và trao đổi dữ liệu với nhau bằng cách nào (ví dụ: dùng API)

\- Yếu tố chất lượng (quality attributes / NFR-Non-Functional Requirements): Đây là các yêu cầu phi chức năng mà kiến trúc phải có. Ví dụ: tốc độ, bảo mật, khả năng mở rộng, độ tin cậy

Vai trò quan trọng của Kiến trúc phần mềm:

\- Tính ổn định: Đảm bảo hệ thống vững chắc, không bị sụp đổ khi lượng người dùng tăng lên

\- Tính dễ hiểu: Giúp các lập trình viên “mới” hoặc các nhóm khác nhau dễ dàng nắm bắt được cách hệ thống hoạt động, từ đó đẩy nhanh quá trình phát triển, nâng cấp và sửa lỗi

\- Tính mở rộng: Cho phép thêm tính năng hoặc tăng khả năng chịu tải một cách dễ dàng mà không cần phải phát triển lại toàn bộ hệ thống

## 5.2 Một số mô hình Kiến trúc phần mềm phổ biến

| Mô hình | Mô tả tóm tắt |
| --- | --- |
| Kiến trúc nguyên khối (monolithic) | Toàn bộ hệ thống được xây dựng như một đơn vị duy nhất, tất cả các chức năng đều nằm chung một khối mã và chia sẻ một cơ sở dữ liệu. (Giống như một căn nhà nhỏ, mọi thứ đều nằm chung một không gian) |
| Kiến trúc N-tầng (N-tiers) | Phân chia hệ thống thành các lớp (tầng) riêng biệt (thường là 3 tầng: Giao diện người dùng, Logic nghiệp vụ, Truy cập dữ liệu). Mỗi tầng chỉ giao tiếp với tầng cạnh nó. (Giống như một tòa nhà có các tầng chức năng rõ ràng) |
| Kiến trúc vi dịch vụ (Microservices)(kiến trúc phân tán) | Hệ thống được chia thành nhiều dịch vụ nhỏ độc lập (microservices), mỗi dịch vụ chạy tiến trình riêng, có thể có cơ sở dữ liệu riêng, và giao tiếp với nhau qua mạng (thường là API). (Giống như một khu phức hợp với nhiều tòa nhà chuyên biệt, kết nối bằng hệ thống đường xá riêng) |

## 5.3 Kiến trúc nguyên khối

Kiến trúc nguyên khối là mô hình truyền thống, trong đó toàn bộ ứng dụng được xây dựng và triển khai dưới dạng một khối duy nhất. Tất cả các thành phần của ứng dụng như giao diện người dùng, logic nghiệp vụ và truy cập dữ liệu đều được tích hợp chặt chẽ trong cùng một ứng dụng.

**Ưu điểm:**

\- Quá trình phát triển, triển khai đơn giản: Do tất cả nằm trong một khối duy nhất, việc phát triển, thử nghiệm và triển khai sẽ đơn giản hơn.

\- Hiệu suất cao: Do không có giao tiếp liên bộ phận, ứng dụng thường có hiệu suất cao hơn.

**Nhược điểm:**

\- Khó bảo trì và mở rộng: Khi ứng dụng phát triển lớn hơn, việc bảo trì và thêm tính năng mới trở nên phức tạp

\- Khả năng chịu lỗi kém: Một lỗi nhỏ có thể làm gián đoạn toàn bộ hệ thống

## 5.4 Kiến trúc N-tầng

Mô hình N-tầng (N-tiers) phân chia ứng dụng thành các tầng độc lập, chạy trên các máy chủ hoặc dịch vụ khác nhau. Sự phân tách này đạt được thông qua việc giới hạn sự giao tiếp: mỗi tầng chỉ được phép giao tiếp với tầng liền kề nó.

Mô hình N-tầng phổ biến nhất là Kiến trúc 3-tầng (3-tier architecture).

**Kiến trúc 3-tầng**

Kiến trúc 3-tầng là một mô hình kiến trúc phần mềm phổ biến. Nó được thiết kế để phân chia ứng dụng thành ba đơn vị logic và vật lý riêng biệt, giúp tăng tính linh hoạt, khả năng mở rộng, và bảo mật.

Kiến trúc 3-tầng được hình thành bằng cách tách ba chức năng chính của ứng dụng thành các tầng (tier) độc lập, thường chạy trên các máy chủ vật lý hoặc logic khác nhau.

Ba tầng đó là:

\- Trình bày (presentation)

\- Logic nghiệp vụ (business logic)

\- Dữ liệu (data)

**Ưu điểm:**

\- Khả năng tái sử dụng: Logic nghiệp vụ nằm ở tầng giữa, độc lập với tầng trình bày. Vì vậy, một logic nghiệp vụ có thể được sử dụng bởi nhiều giao diện khác nhau. Ví dụ: một API xử lý thanh toán có thể được gọi từ cả ứng dụng web và ứng dụng di động

\- Khả năng mở rộng: Đây là ưu điểm lớn nhất so với kiến trúc nguyên khối. Bạn có thể mở rộng độc lập theo từng tầng. Ví dụ: thêm máy chủ cho tầng Logic nghiệp vụ khi có nhiều yêu cầu API hơn, mà không cần thêm máy chủ cho tầng Dữ liệu

\- Có tính bảo mật cao: Tầng Dữ liệu được cô lập, chỉ giao tiếp với tầng Logic nghiệp vụ, mà không giao tiếp với người dùng cuối. Điều này giúp bảo vệ cơ sở dữ liệu khỏi các truy cập trái phép từ bên ngoài

\- Dễ phát triển và bảo trì: Vì mỗi tầng có trách nhiệm rõ ràng, các lập trình viên có thể tập trung vào một tầng cụ thể mà không làm ảnh hưởng đến các tầng khác. Đội Frontend có thể làm việc song song với đội Backend, chỉ cần tuân thủ giao diện API

**Nhược điểm:**

\- Phức tạp: Việc thiết lập và quản lý kiến trúc phân tán nhiều tầng phức tạp hơn so với kiến trúc nguyên khối

\- Độ trễ: Việc truyền dữ liệu qua nhiều tầng (qua mạng) có thể làm tăng độ trễ (latency) so với việc gọi hàm cục bộ

\- Chi phí: Việc duy trì nhiều máy chủ/dịch vụ vật lý hoặc máy ảo cho mỗi tầng sẽ tốn kém hơn

## 5.5 Kiến trúc vi dịch vụ

Kiến trúc vi dịch vụ (microservices) là một phương pháp thiết kế phần mềm, trong đó một ứng dụng lớn được chia thành một tập hợp các dịch vụ nhỏ, độc lập. Nó là một kiến trúc phần mềm phân tán.

Một số đặc điểm:

\- Tính độc lập: Mỗi dịch vụ (service) chạy trong tiến trình (process) riêng biệt của nó

\- Chức năng chuyên biệt: Mỗi dịch vụ tập trung vào việc thực hiện một chức năng nghiệp vụ cụ thể (ví dụ: dịch vụ quản lý người dùng, dịch vụ xử lý thanh toán, dịch vụ kho hàng)

\- Giao tiếp: Các dịch vụ giao tiếp với nhau qua mạng bằng các giao thức nhẹ, phổ biến nhất là RESTful API hoặc message broker (hàng đợi tin nhắn)

\- Công nghệ đa dạng (polyglot): Các dịch vụ khác nhau có thể được xây dựng bằng các ngôn ngữ lập trình, framework và thậm chí là cơ sở dữ liệu riêng (independent database) phù hợp nhất với yêu cầu của dịch vụ đó

**Ưu điểm:**

\- Khả năng mở rộng độc lập: Có thể mở rộng từng dịch vụ riêng biệt dựa trên nhu cầu tải thực tế, giúp tối ưu hóa tài nguyên (ví dụ: chỉ cần thêm server cho dịch vụ giỏ hàng mà không cần thêm server cho dịch vụ tài khoản)

\- Linh hoạt công nghệ: Cho phép các nhóm sử dụng công nghệ (tech stack) tốt nhất cho từng dịch vụ cụ thể (polyglot programming)

\- Dễ dàng bảo trì và phát triển: Mã nguồn của mỗi dịch vụ nhỏ và dễ hiểu hơn. Các nhóm phát triển có thể làm việc, triển khai và cập nhật dịch vụ của họ độc lập với các dịch vụ khác (decoupling)

\- Khả năng chịu lỗi cao: Nếu một dịch vụ bị lỗi, các dịch vụ khác vẫn có thể tiếp tục hoạt động (fault isolation). Hệ thống không bị sập toàn bộ như trong monolithic

\- Triển khai liên tục (CI/CD): Dễ dàng áp dụng DevOps và CI/CD vì chỉ cần triển khai lại các dịch vụ nhỏ đã thay đổi, không cần triển khai toàn bộ ứng dụng lớn

**_Nhược điểm:_**

\- Phức tạp về vận hành: Việc quản lý, giám sát (monitoring) và gỡ lỗi (debugging) một hệ thống gồm hàng chục hoặc hàng trăm dịch vụ phân tán phức tạp hơn nhiều

\- Độ trễ mạng (latency): Các dịch vụ giao tiếp qua mạng (API call) thay vì gọi hàm cục bộ, dẫn đến độ trễ cao hơn so với monolithic

\- Quản lý dữ liệu phân tán: Xử lý giao dịch trải dài qua nhiều cơ sở dữ liệu (distributed transactions) rất phức tạp và cần các mẫu thiết kế như Saga

\- Chi phí cơ sở hạ tầng: Cần nhiều tài nguyên hơn cho việc chạy nhiều tiến trình, nhiều cơ sở dữ liệu và các công cụ quản lý phức tạp (kubernetes, service mesh, API gateway)

\- Kiểm thử tích hợp: Việc đảm bảo tất cả các dịch vụ phối hợp nhịp nhàng với nhau khó khăn hơn so với kiểm thử end-to-end trong monolithic

## 5.6 Bài tập

Bài 5a. Dựa trên URS ứng dụng của bạn (nhóm), hãy phân tích và thiết kế theo kiến trúc 3-tầng. Bạn có thể tự phân tích, thiết kế hoặc nhờ sự hỗ trợ của chatbot.

Phân tích URS – Hệ thống Quản lý Nhà hàng (3-Tier, mức tổng quát)

1\. Mục tiêu

Hệ thống hỗ trợ:

Quản lý món ăn theo nhóm

Quản lý bàn và hóa đơn

Hỗ trợ nhân viên thao tác bán hàng

2\. Yêu cầu chức năng chính

Món ăn: quản lý thông tin cơ bản, mỗi món thuộc 1 nhóm

Bàn: theo dõi trạng thái (trống / đang sử dụng)

Hóa đơn:

Mỗi bàn chỉ có 1 hóa đơn tại một thời điểm

Cho phép thêm / sửa / xóa món

Thanh toán để kết thúc hóa đơn

Tài khoản:

Admin: toàn quyền

Nhân viên: chỉ thao tác trên hóa đơn

3\. Logic nghiệp vụ tổng quát

Khi thêm món:

Nếu chưa có hóa đơn → tạo mới

Nếu đã có → cập nhật hóa đơn hiện tại

Trong hóa đơn:

Món trùng → tăng số lượng

Số lượng = 0 → tự động xóa

Hóa đơn:

Không tồn tại hóa đơn rỗng

Sau khi thanh toán:

Được lưu lại (lịch sử)

Không được chỉnh sửa

Trạng thái bàn:

Có hóa đơn → “đang sử dụng”

Không có hóa đơn → “trống”

Phân quyền:

Nhân viên chỉ thao tác trên hóa đơn

Admin có toàn quyền hệ thống

4\. Ánh xạ vào kiến trúc 3 tầng

4.1 Presentation Layer

Giao diện hiển thị:

Bàn, món ăn, hóa đơn

Gửi yêu cầu người dùng (thêm món, thanh toán)

Không xử lý logic

4.2 Business Logic Layer (trung tâm)

Xử lý toàn bộ nghiệp vụ:

Tạo hóa đơn tự động

Gộp món / cập nhật số lượng

Xóa món khi cần

Kiểm soát trạng thái bàn

Kiểm tra phân quyền

Đây là tầng đảm bảo hệ thống hoạt động đúng quy tắc đã định.

4.3 Data Access Layer

Lưu trữ và truy xuất dữ liệu:

Món, bàn, hóa đơn, chi tiết hóa đơn

Chỉ thực hiện CRUD

Không chứa logic nghiệp vụ

5\. Luồng xử lý điển hình

Thêm món vào bàn:

UI → BLL (kiểm tra + xử lý) → DAL (lưu dữ liệu) → trả kết quả về UI

Bài 5b. Dựa trên URS ứng dụng của bạn (nhóm), hãy phân tích và thiết kế theo kiến trúc vi dịch vụ. Bạn có thể tự phân tích, thiết kế hoặc nhờ sự hỗ trợ của chatbot.

Phân tích URS – Hệ thống Quản lý Nhà hàng (Microservices)

1\. Mục tiêu

Hệ thống hỗ trợ:

Quản lý món ăn theo nhóm

Quản lý bàn và hóa đơn

Hỗ trợ nhân viên thao tác bán hàng

2\. Yêu cầu chức năng chính

Món ăn: mỗi món thuộc 1 nhóm

Bàn: trạng thái (trống / đang sử dụng)

Hóa đơn:

1 bàn = 1 hóa đơn tại một thời điểm

Thêm / sửa / xóa món

Thanh toán → lưu lịch sử, không cho sửa

Tài khoản:

Admin: toàn quyền

Nhân viên: thao tác trên hóa đơn

3\. Logic nghiệp vụ tổng quát

Thêm món:

Chưa có hóa đơn → tạo mới

Đã có → cập nhật

Trong hóa đơn:

Món trùng → tăng số lượng

Số lượng = 0 → xóa

Hóa đơn:

Không tồn tại hóa đơn rỗng

Sau thanh toán:

Lưu lịch sử

Không chỉnh sửa

Trạng thái bàn:

Có hóa đơn → đang sử dụng

Không → trống

Phân quyền:

Nhân viên: chỉ thao tác hóa đơn

Admin: toàn quyền

4\. Thiết kế theo kiến trúc Microservices

Thay vì gom vào 3 tầng, hệ thống được chia thành các service độc lập:

4.1 Các service chính

Food Service

Quản lý món ăn và nhóm

Cung cấp danh sách món

Table Service

Quản lý bàn

Cập nhật trạng thái bàn

Invoice Service (trung tâm logic)

Tạo và quản lý hóa đơn

Xử lý:

Thêm / sửa / xóa món

Thanh toán

Đảm bảo:

1 bàn chỉ có 1 hóa đơn

Auth Service

Xác thực người dùng

Phân quyền:

Admin / Nhân viên

5\. Tương tác giữa các service

Luồng: Thêm món

UI gọi Invoice Service

Invoice Service:

Kiểm tra quyền qua Auth Service

Kiểm tra hóa đơn

Nếu cần → tạo mới

Có thể gọi:

Food Service (lấy thông tin món)

Table Service (cập nhật trạng thái bàn)

Lưu dữ liệu