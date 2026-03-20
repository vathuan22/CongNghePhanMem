# Bài 4: Lấy và phân tích yêu cầu

## 4.1 Yêu cầu là gì

Trong phát triển phần mềm, yêu cầu (requirements) là những mô tả về các **điều kiện, khả năng, và tính năng** mà một hệ thống phần mềm phải có để đáp ứng nhu cầu của người dùng hoặc các bên liên quan. Nói một cách đơn giản, yêu cầu là cầu nối giữa mong muốn của khách hàng và sản phẩm cuối cùng.

Yêu cầu là nền tảng cho toàn bộ quá trình phát triển phần mềm. Nếu không có các yêu cầu rõ ràng và chính xác, dự án sẽ gặp rủi ro lớn vì nhóm phát triển có thể xây dựng một sản phẩm không đáp ứng được mục đích ban đầu, dẫn đến lãng phí thời gian và nguồn lực.

## 4.2 Các loại yêu cầu

Trong phát triển phần mềm, chúng ta quan tâm tới 3 loại yêu cầu sau:

\- Yêu cầu người dùng (user requirements).

\- Yêu cầu nghiệp vụ (domain requirements).

\- Phi yêu cầu (non-requirements).

Chúng ta cùng tìm hiểu chi tiết hơn về mỗi loại yêu cầu:

**\[1\] Yêu cầu người dùng**

**Yêu cầu người dùng** (user requirement) là những nhu cầu, mong đợi, và kỳ vọng của người dùng cuối về một sản phẩm, hệ thống, hoặc dịch vụ. Nó mô tả những gì người dùng mong đợi hệ thống thực hiện để giải quyết vấn đề của họ.

Yêu cầu người dùng chia thành 2 loại: chức năng (tính năng của hệ thống) và phi chức năng (tốc độ, hiệu suất, tin cậy).

Yêu cầu được viết bằng ngôn ngữ tự nhiên, dễ hiểu, không mang tính kỹ thuật. Yêu cầu người dùng thường được thu thập thông qua phỏng vấn, khảo sát, và các buổi họp với khách hàng hoặc người dùng cuối.

Yêu cầu này thường được ghi lại trong một tài liệu gọi là [Tài liệu đặc tả yêu cầu người dùng](https://www.google.com/search?cs=0&sca_esv=518de7ca735d1bf8&q=T%C3%A0i+li%E1%BB%87u+%C4%91%E1%BA%B7c+t%E1%BA%A3+y%C3%AAu+c%E1%BA%A7u+ng%C6%B0%E1%BB%9Di+d%C3%B9ng&sa=X&ved=2ahUKEwiozcbigb6PAxVQoa8BHXM7EcEQxccNegQIBRAB&mstk=AUtExfBi2lqwSs0FaQ-OCrHrJVrN4GgUqkrszafRA_ah0AYDNiiAM8ypyyDaDZRr2UwWiyVhIuD0-IgMPowbxKMZCBgnHznj8gUJ0PFFigeiHEWmiHoi48mkLJghor3iU7l2XhndIXJYv9meuGu9Z77Dkf2QJNhwD-hZ2KWRo8jlcXtm0p8&csui=3) (User Requirement Specification - URS) để làm cơ sở cho việc thiết kế và phát triển sản phẩm.

**_Mục đích của yêu cầu người dùng_**

\- Định hướng phát triển: Giúp đội ngũ phát triển và kỹ sư hiểu rõ nhu cầu của người dùng để xây dựng sản phẩm đúng mong muốn.

\- Đảm bảo sự hài lòng: Sản phẩm cuối cùng sẽ đáp ứng các kỳ vọng của người dùng, mang lại trải nghiệm tốt và sự hài lòng.

\- Quản lý dự án: Là cơ sở để lập kế hoạch, ước tính chi phí, kiểm soát dự án và đánh giá thành công.

**_Đặc điểm của yêu cầu người dùng_**

\- Từ góc độ người dùng: Tài liệu URS được viết theo góc nhìn của người dùng cuối, không quá kỹ thuật hay phức tạp, và để người dùng có kiến thức chung về hệ thống có thể hiểu được.

\- Chức năng và phi chức năng: Bao gồm các tính năng mà hệ thống cần có (chức năng) và các yếu tố khác như hiệu suất, tốc độ, độ tin cậy (phi chức năng).

\- Làm cơ sở cho tài liệu kỹ thuật: Là nền tảng cho các tài liệu đặc tả kỹ thuật do đội ngũ phát triển tạo ra, quy định cách thức đáp ứng yêu cầu của người dùng.

**_Yêu cầu chức năng_**

Yêu cầu chức năng là các tính năng cụ thể mà một hệ thống phải thực hiện để đáp ứng nhu cầu của người dùng.

Ví dụ, yêu cầu tính năng của hệ thống Bán sách trực tuyến, gồm:

**1\. Yêu cầu liên quan đến người dùng**

Các yêu cầu này tập trung vào việc quản lý thông tin và tương tác của người dùng với hệ thống.

(FR là viết tắt của Functional Requirements: yêu cầu chức năng)

**\- Đăng ký và đăng nhập:**

**\+ FR-1.1:** Hệ thống phải cho phép người dùng mới đăng ký tài khoản bằng cách cung cấp email, tên đầy đủ và mật khẩu.

\+ **FR-1.2:** Hệ thống phải xác thực thông tin đăng nhập của người dùng đã có tài khoản.

\+ **FR-1.3:** Hệ thống phải cung cấp tính năng "Quên mật khẩu", cho phép người dùng đặt lại mật khẩu qua email.

\- **Quản lý tài khoản cá nhân:**

**\+ FR-1.4:** Người dùng phải có khả năng cập nhật thông tin cá nhân của họ, bao gồm tên, địa chỉ, số điện thoại.

\+ **FR-1.5:** Người dùng phải có thể xem lịch sử mua hàng của họ, bao gồm các đơn hàng đã đặt, trạng thái đơn hàng và chi tiết các sản phẩm đã mua.

**2\. Yêu cầu liên quan đến sản phẩm và tìm kiếm**

Những yêu cầu này mô tả cách người dùng tương tác với danh mục sản phẩm.

\- **Tìm kiếm và lọc sản phẩm:**

**\+ FR-2.1:** Hệ thống phải cho phép người dùng tìm kiếm sách theo tiêu đề, tác giả, hoặc nhà xuất bản.

\+ **FR-2.2:** Người dùng phải có khả năng lọc kết quả tìm kiếm theo nhiều tiêu chí như thể loại (tiểu thuyết, kinh tế, khoa học), giá cả, hoặc đánh giá của người dùng.

\- **Hiển thị thông tin sản phẩm:**

**\+ FR-2.3:** Hệ thống phải hiển thị một trang chi tiết cho mỗi cuốn sách, bao gồm hình ảnh bìa, mô tả, giá, tác giả, và các thông số kỹ thuật khác (số trang, năm xuất bản).

\+ **FR-2.4:** Trang chi tiết sản phẩm phải hiển thị các đánh giá và nhận xét từ những người dùng khác.

**3\. Yêu cầu liên quan đến giỏ hàng và thanh toán**

Các yêu cầu này mô tả quy trình mua hàng, từ khi thêm sản phẩm vào giỏ đến khi hoàn tất thanh toán.

\- **Quản lý giỏ hàng:**

**\+ FR-3.1:** Người dùng phải có khả năng thêm một hoặc nhiều cuốn sách vào giỏ hàng.

\+ **FR-3.2:** Người dùng có thể chỉnh sửa số lượng sách trong giỏ hàng hoặc xóa sách ra khỏi giỏ.

\+ **FR-3.3:** Giỏ hàng phải tự động cập nhật tổng giá trị đơn hàng khi có thay đổi về số lượng hoặc sản phẩm.

\- **Thanh toán và Đặt hàng:**

**\+ FR-3.4:** Hệ thống phải cho phép người dùng lựa chọn phương thức thanh toán.

\+ **FR-3.5:** Hệ thống phải gửi một email xác nhận đơn hàng tới người dùng sau khi thanh toán thành công, kèm theo chi tiết đơn hàng và mã theo dõi.

**4\. Yêu cầu liên quan đến đánh giá và nhận xét**

\- **FR-4.1:** Người dùng đã mua một cuốn sách phải có khả năng viết đánh giá và xếp hạng (ví dụ, từ 1 đến 5 sao) cho cuốn sách đó.

\- **FR-4.2:** Các đánh giá phải được hiển thị trên trang chi tiết sản phẩm và được sắp xếp theo thời gian hoặc độ hữu ích.

**_Yêu cầu phi chức năng_**

Yêu cầu phi chức năng không tập trung vào các tính năng cụ thể, mà quan tâm tới chất lượng của hệ thống, như tốc độ, bảo mật, khả năng mở rộng, độ tin cậy.

Ví dụ:

Các yêu cầu phi chức năng của hệ thống Bán sách trực tuyến:

1\. Hiệu suất (Performance)

\- **Tốc độ tải trang:** Trang chủ và trang danh sách sản phẩm phải tải hoàn toàn trong vòng dưới 3 giây, ngay cả trong giờ cao điểm.

\- **Thời gian phản hồi:** Hệ thống phải xử lý yêu cầu tìm kiếm và lọc sản phẩm trong vòng chưa đầy 2 giây.

\- **Khả năng chịu tải:** Hệ thống phải có khả năng xử lý đồng thời 5.000 người dùng mà không bị chậm hoặc ngừng hoạt động.

2\. Khả năng sử dụng (Usability)

**\- Giao diện trực quan:** Giao diện người dùng phải dễ hiểu, các nút và liên kết phải rõ ràng để người dùng có thể dễ dàng tìm kiếm, thêm sách vào giỏ hàng và thanh toán mà không cần hướng dẫn.

\- **Tương thích đa nền tảng:** Website phải hiển thị và hoạt động tốt trên các trình duyệt phổ biến như Chrome, Firefox và trên các thiết bị di động (điện thoại, máy tính bảng) với các kích thước màn hình khác nhau.

\- **Trợ giúp và hỗ trợ:** Hệ thống nên có các mục FAQ (câu hỏi thường gặp) hoặc chatbot để trả lời các câu hỏi cơ bản của người dùng.

3\. Bảo mật (Security)

\- **Bảo vệ dữ liệu người dùng:** Tất cả thông tin cá nhân của người dùng, bao gồm tên, địa chỉ, và mật khẩu, phải được mã hóa và lưu trữ an toàn.

\- **Bảo mật thanh toán:** Toàn bộ giao dịch thanh toán phải tuân thủ các tiêu chuẩn bảo mật quốc tế (ví dụ: PCI DSS) để đảm bảo thông tin thẻ tín dụng của người dùng được bảo vệ.

\- **Chống tấn công:** Hệ thống phải có cơ chế bảo vệ chống lại các cuộc tấn công mạng phổ biến như SQL Injection và XSS (Cross-Site Scripting).

4\. Độ tin cậy (Reliability)

\- **Thời gian hoạt động (Uptime):** Hệ thống phải đảm bảo thời gian hoạt động ít nhất 99.9% mỗi tháng, tức là không được ngừng hoạt động quá 44 phút.

\- **Sao lưu dữ liệu:** Dữ liệu người dùng và đơn hàng phải được sao lưu tự động hàng ngày để có thể khôi phục lại trong trường hợp xảy ra sự cố.

5\. Khả năng mở rộng (Scalability)

\- **Mở rộng kho sách:** Hệ thống phải được thiết kế để dễ dàng thêm hàng nghìn đầu sách mới mà không ảnh hưởng đến hiệu suất.

\- **Hỗ trợ tính năng mới:** Kiến trúc hệ thống phải cho phép tích hợp các tính năng bổ sung trong tương lai, chẳng hạn như hệ thống tích điểm thưởng cho khách hàng hoặc chương trình giới thiệu sản phẩm.

**\[2\] Yêu cầu nghiệp vụ**

**Yêu cầu nghiệp vụ** (domain requirements) là những quy tắc, chính sách, và nguyên tắc kinh doanh mà một hệ thống phần mềm phải tuân thủ. Chúng không phải là các chức năng cụ thể mà người dùng tương tác, mà là những ràng buộc nền tảng quyết định cách hệ thống hoạt động trong một lĩnh vực cụ thể (ví dụ: bán lẻ, tài chính, y tế).

Nói một cách đơn giản, yêu cầu nghiệp vụ trả lời câu hỏi: "Doanh nghiệp/tổ chức của tôi hoạt động như thế nào, và phần mềm này phải tuân theo những quy tắc nào?"

**_Ví dụ:_**

Trong một ứng dụng bán sách, yêu cầu nghiệp vụ có thể là:

Quản lý kho sách:

\- Hệ thống phải có khả năng thêm mới, cập nhật, và xóa thông tin sách (tên sách, tác giả, nhà xuất bản, giá, số lượng tồn kho).

\- Hệ thống cần tự động trừ số lượng sách khi có đơn hàng được đặt thành công.

\- Hệ thống phải thông báo cho người quản lý khi số lượng một đầu sách xuống dưới mức cảnh báo để nhập hàng.

Quản lý đơn hàng:

\- Khách hàng phải có khả năng tạo đơn hàng mới với nhiều đầu sách khác nhau.

\- Hệ thống cần tính toán tổng giá tiền cho đơn hàng, bao gồm cả thuế và phí vận chuyển.

\- Hệ thống phải theo dõi trạng thái của đơn hàng (đang xử lý, đã giao, đã thanh toán, đã hủy) và thông báo cho khách hàng.

Quản lý tài khoản khách hàng:

\- Khách hàng phải có khả năng đăng ký tài khoản, đăng nhập, và quản lý thông tin cá nhân (địa chỉ, số điện thoại).

\- Hệ thống cần lưu trữ lịch sử đơn hàng của từng khách hàng.

**\[3\] Phi yêu cầu**

Phi yêu cầu (non-requirement) là một khái niệm hoặc giả định được xác định trong giai đoạn phân tích dự án, nhưng không phải là một yêu cầu chức năng hay phi chức năng mà hệ thống cần phải thực hiện.

Các "phi yêu cầu" thường là những điều kiện không thể đáp ứng, nằm ngoài phạm vi của dự án, hoặc những giả định cơ bản mà nhóm phát triển cần biết để tránh hiểu lầm. Chúng đóng vai trò làm rõ ranh giới của dự án và giúp tránh lãng phí tài nguyên vào những việc không cần thiết.

**_Ví dụ về phi yêu cầu cho hệ thống Bán sách trực tuyến_**

\- Không hỗ trợ hình thức thanh toán bằng tiền mặt: Hệ thống sẽ chỉ xử lý các giao dịch thanh toán trực tuyến qua thẻ tín dụng, ví điện tử hoặc chuyển khoản ngân hàng. Việc giao hàng và thu tiền mặt không thuộc phạm vi của dự án này.

\- Không bao gồm chức năng chatbot tích hợp AI: Hệ thống này sẽ chỉ sử dụng các câu hỏi thường gặp (FAQ) và form liên hệ để hỗ trợ khách hàng, thay vì tích hợp một chatbot phức tạp.

\- Không xử lý việc vận chuyển sản phẩm: Hệ thống sẽ chỉ tạo ra đơn hàng và chuyển thông tin cho một đối tác vận chuyển bên thứ ba. Trách nhiệm theo dõi, giao hàng, và xử lý các vấn đề phát sinh trong quá trình vận chuyển sẽ do đối tác đó đảm nhận, nằm ngoài phạm vi phát triển của phần mềm.

\- Không hỗ trợ nhiều ngôn ngữ: Hệ thống sẽ chỉ được phát triển với ngôn ngữ tiếng Việt.

Những ví dụ trên giúp làm rõ những gì dự án sẽ không làm, từ đó giúp nhóm phát triển tập trung vào các yêu cầu đã được xác định, tránh việc phát sinh công việc ngoài ý muốn.

Sau khi đã có Đặc tả yêu cầu người dùng (URS), chúng ta sẽ chuyển từ Đặc tả yêu cầu người dùng thành Đặc tả yêu cầu phần mềm (SRS - Software Requirements Specification).

SRS là "bản thiết kế" chi tiết hơn URS, giúp lập trình viên biết chính xác mình cần xây dựng logic gì, cơ sở dữ liệu ra sao.

## 4.3 Kỹ thuật lấy yêu cầu

Trong quy trình phát triển phần mềm, Kỹ thuật lấy yêu cầu là bước quan trọng nhất để đảm bảo chúng ta không làm ra một thứ mà không ai cần.

Có 3 kỹ thuật để lấy yêu cầu: phỏng vấn, khảo sát và viết các câu chuyện người dùng

**\[1\] Phỏng vấn**

\- Gặp trực tiếp (hoặc nhóm nhỏ) để hỏi sâu về yêu cầu phần mềm

\- Đặt câu hỏi mở (cái gì? tại sao? như thế nào?)

\- Luôn ghi âm hoặc ghi chép có thông tin chi tiết khi làm việc với khách hàng

\[2\] Khảo sát

\- Dùng để thu thập dữ liệu từ số lượng lớn người dùng trong thời gian ngắn

\- Sử dụng Google Forms hoặc các mẫu in với các câu hỏi trắc nghiệm hoặc thang đo (1-5 sao)

\- Tập trung vào số liệu

\- Đảm bảo thời gian khảo sát không mất quá nhiều thời gian. Nếu quá dài, người dùng sẽ trả lời qua loa, làm sai lệch dữ liệu

\[3\] Câu chuyện người dùng (user story)

\- Đây là kỹ thuật cốt lõi trong Agile/Scrum để diễn đạt yêu cầu từ góc độ của người dùng cuối

\- Cấu trúc chuẩn: "Là một \[Vai trò\], tôi muốn \[Hành động\], để \[Lợi ích/Giá trị\].". Ví dụ: "Là một khách mua sách, tôi muốn lưu sách vào 'Danh sách yêu thích' để có thể tìm lại và mua sau này khi có giảm giá."

\- Mỗi user story phải đi kèm với “Tiêu chí chấp nhận”, để lập trình viên biết khi nào thì tính năng đó được coi là hoàn thành

## 4.3 Bài tập
DỰ ÁN: HỆ THỐNG BÁN SÁCH TRỰC TUYẾN

1. Giới thiệu

Tài liệu này cụ thể hóa các yêu cầu kỹ thuật cho hệ thống Bán sách trực tuyến, phục vụ cho việc thiết kế, lập trình và kiểm thử. Hệ thống tập trung vào trải nghiệm mua sắm mượt mà và bảo mật thông tin.

2. Mô tả tổng quát

Hệ thống là một ứng dụng Web cho phép khách hàng thực hiện toàn bộ quy trình từ tìm kiếm đến thanh toán trực tuyến

- Tác nhân (Actors): Khách hàng (User), Quản trị viên (Admin), Hệ thống thanh toán bên thứ 3, Đơn vị vận chuyển.

3. Yêu cầu chức năng chi tiết

3.1. Quản lý Tài khoản & Xác thực

- SRS-F01 (Đăng ký): Hệ thống cung cấp form nhập Email (định dạng hợp lệ), Tên đầy đủ, Mật khẩu (tối thiểu 8 ký tự, gồm chữ và số). Lưu trữ mật khẩu dưới dạng mã hóa (Hashing)

- SRS-F02 (Đăng nhập): Xác thực tài khoản qua Email/Password. Sử dụng Session hoặc Token để duy trì trạng thái đăng nhập

- SRS-F03 (Lịch sử đơn hàng): Truy vấn cơ sở dữ liệu để hiển thị danh sách đơn hàng theo User_ID, sắp xếp từ mới nhất đến cũ nhất

3.2. Quản lý Sản phẩm & Tìm kiếm

- SRS-F04 (Tìm kiếm): Sử dụng thuật toán tìm kiếm theo từ khóa (partial match) trên các trường: Title, Author, Publisher

- SRS-F05 (Lọc dữ liệu): Cho phép áp dụng nhiều bộ lọc cùng lúc theo Category_ID, Price_Range, và Rating_Score

- SRS-F06 (Chi tiết sản phẩm): Hiển thị dữ liệu từ bảng Books, bao gồm các trường thông số kỹ thuật và danh sách đánh giá liên kết

3.3. Giỏ hàng & Xử lý đơn hàng

- SRS-F07 (Logic giỏ hàng): Thêm sản phẩm: Nếu sản phẩm đã có, tăng Quantity.

    + Tính toán: Subtotal = Price * Quantity

    + Cập nhật Total_Price theo thời gian thực

- SRS-F08 (Thanh toán): Tích hợp API cổng thanh toán. Hệ thống nhận phản hồi từ cổng thanh toán để cập nhật trạng thái đơn hàng thành

- SRS-F09 (Thông báo): Kích hoạt mô-đun gửi Email tự động chứa mã Tracking_ID sau khi giao dịch thành công

3.4. Tương tác người dùng

- SRS-F10 (Đánh giá): Cho phép người dùng có đơn hàng trạng thái “đã giao” gửi đánh giá. Giới hạn 1 đánh giá/sản phẩm/người dùng.

4. Yêu cầu phi chức năng (Non-Functional Requirements)

Mã số

Đặc tính

Chi tiết kỹ thuật

SRS-N01

Hiệu suất

Phản hồi truy vấn Database < 1s. Tải trang (Frontend) < 3s

SRS-N02

Khả năng chịu tải

Hỗ trợ 5.000 người dùng cùng lúc

SRS-N03

Bảo mật

Giao thức HTTPS. Chống SQL Injection

SRS-N04

Tính sẵn sàng

Hoạt động 99.9%. Sao lưu dữ liệu hàng ngày.

SRS-N05

Tương thích

Tùy chỉnh giao diện theo kích thước màn hình sử dụng

5. Quy tắc nghiệp vụ

- BR-01 (Quản lý kho): Khi đơn hàng xác nhận, hệ thống thực hiện trừ kho: Stock_Quantity = Stock_Quantity - Ordered_Quantity

- BR-02 (Cảnh báo tồn kho): Nếu Stock_Quantity < Threshold (mặc định là 10), hệ thống gửi thông báo cho Admin

- BR-03 (Tính giá): Final_Amount = Subtotal + Tax + Shipping_Fee.

6. Ràng buộc & Phạm vi

- Chỉ chấp nhận thanh toán số (No COD)

- Không xử lý quá trình vận chuyển

- Ngôn ngữ: Tiếng Việt 