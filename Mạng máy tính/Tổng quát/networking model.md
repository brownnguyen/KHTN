Dưới đây là hai mô hình mạng chính và một số mô hình bổ sung:

1. Mô hình OSI (Open Systems Interconnection)
Mô hình OSI là một mô hình lý thuyết bao gồm bảy lớp, mỗi lớp đảm nhiệm một chức năng cụ thể trong việc truyền dữ liệu qua mạng. Mục đích của mô hình OSI là cung cấp một cách tiếp cận chuẩn hóa để giao tiếp giữa các hệ thống mạng khác nhau. Các lớp của mô hình OSI từ thấp đến cao là:

Lớp Vật lý (Physical Layer): Xác định cách truyền dữ liệu dưới dạng bit qua các phương tiện truyền dẫn (cáp, sóng radio, v.v.).
Lớp Liên kết Dữ liệu (Data Link Layer): Đảm bảo truyền dữ liệu chính xác qua một liên kết vật lý, bao gồm việc phát hiện và sửa lỗi.
Lớp Mạng (Network Layer): Quản lý việc định tuyến dữ liệu từ nguồn đến đích qua các mạng và xử lý địa chỉ IP.
Lớp Giao vận (Transport Layer): Đảm bảo việc truyền dữ liệu giữa các thiết bị đầu cuối với khả năng kiểm soát lỗi và kiểm soát luồng.
Lớp Phiên (Session Layer): Quản lý và điều phối các phiên giao tiếp giữa các ứng dụng.
Lớp Trình bày (Presentation Layer): Đảm bảo dữ liệu được định dạng đúng và có thể đọc được giữa các hệ thống khác nhau.
Lớp Ứng dụng (Application Layer): Cung cấp các dịch vụ mạng trực tiếp cho các ứng dụng người dùng (e.g., email, web browsing).
2. Mô hình TCP/IP (Transmission Control Protocol/Internet Protocol)
Mô hình TCP/IP là mô hình mạng thực tế được sử dụng rộng rãi trong Internet và các mạng LAN. Nó gồm bốn lớp, mỗi lớp tương ứng với một hoặc nhiều lớp của mô hình OSI:

Lớp Liên kết (Link Layer): Bao gồm các chức năng của lớp vật lý và lớp liên kết dữ liệu trong mô hình OSI. Đảm bảo kết nối mạng cục bộ và truyền dữ liệu qua mạng cục bộ.
Lớp Mạng (Internet Layer): Tương ứng với lớp mạng trong mô hình OSI, xử lý việc định tuyến và địa chỉ IP.
Lớp Giao vận (Transport Layer): Tương ứng với lớp giao vận trong mô hình OSI, xử lý việc truyền dữ liệu và kiểm soát lỗi với các giao thức như TCP (Transmission Control Protocol) và UDP (User Datagram Protocol).
Lớp Ứng dụng (Application Layer): Tương ứng với lớp ứng dụng, lớp phiên, và lớp trình bày trong mô hình OSI. Cung cấp các dịch vụ ứng dụng mạng như HTTP, FTP, SMTP, v.v.
3. Mô hình Mạng Tầng (Layered Network Model)
Mô hình mạng tầng là một cách tiếp cận khác trong việc tổ chức các chức năng mạng, có thể bao gồm các lớp khác nhau tùy theo nhu cầu và ứng dụng cụ thể. Mô hình này tương tự như mô hình OSI nhưng có thể không phân chia thành bảy lớp cụ thể, thay vào đó, nhóm các chức năng mạng vào các lớp chung hơn.

So sánh giữa các mô hình:
Mô hình OSI: Cung cấp một cái nhìn lý thuyết chi tiết và chuẩn hóa về cách mạng hoạt động, giúp hiểu rõ từng lớp và chức năng của nó. Tuy nhiên, nó không được sử dụng trực tiếp trong các mạng thực tế.

Mô hình TCP/IP: Được sử dụng rộng rãi trong thực tế và Internet, nó cung cấp một cách tiếp cận thực tế hơn và đơn giản hơn so với mô hình OSI.

Mô hình Mạng Tầng: Có thể linh hoạt và được điều chỉnh để phù hợp với các nhu cầu và ứng dụng cụ thể, không nhất thiết phải tuân theo các lớp chính xác của OSI hoặc TCP/IP.

Tóm lại:
Mô hình mạng cung cấp các khung lý thuyết để thiết kế và quản lý mạng máy tính, giúp tiêu chuẩn hóa và đảm bảo sự tương thích giữa các hệ thống khác nhau. Mô hình OSI và TCP/IP là hai mô hình phổ biến, mỗi mô hình có cách tiếp cận và ứng dụng riêng, giúp hiểu rõ hơn về cách thức hoạt động của mạng.