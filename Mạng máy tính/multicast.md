Đặc điểm của Multicast:
Giao tiếp một-đến-nhiều:

Dữ liệu được gửi từ một nguồn đến một nhóm các thiết bị nhận cụ thể.
Sử dụng địa chỉ multicast:

Gói tin multicast sử dụng địa chỉ IP multicast đặc biệt để xác định nhóm các thiết bị nhận.
Hiệu quả về băng thông:

Giảm số lượng gói tin cần thiết bằng cách gửi một gói tin duy nhất đến nhiều người nhận, giúp tiết kiệm băng thông mạng.
Ưu điểm của Multicast:
Tiết kiệm băng thông: Chỉ cần một luồng dữ liệu duy nhất để phục vụ nhiều người nhận, thay vì nhiều luồng dữ liệu riêng lẻ.
Tối ưu hóa hiệu suất mạng: Giảm tải cho mạng và các thiết bị nguồn bằng cách hạn chế số lượng gói tin phải xử lý.
Thích hợp cho các ứng dụng phát sóng: Rất hiệu quả cho các ứng dụng như hội nghị video, phát sóng video trực tiếp, và các dịch vụ truyền thông khác mà nhiều người nhận cần cùng một nội dung.
Nhược điểm của Multicast:
Phức tạp trong quản lý và cấu hình: Yêu cầu cấu hình phức tạp trên các thiết bị mạng để hỗ trợ multicast.
Hạn chế hỗ trợ trong mạng Internet công cộng: Multicast chủ yếu được hỗ trợ trong mạng cục bộ (LAN) và mạng diện rộng (WAN) có quản lý chặt chẽ. Hỗ trợ multicast qua Internet công cộng còn hạn chế.
Cần sự hỗ trợ từ các thiết bị mạng: Các thiết bị mạng như router và switch cần phải hỗ trợ và được cấu hình để xử lý multicast.
Ứng dụng của Multicast:
Phát sóng video và âm thanh trực tiếp: Các dịch vụ phát sóng trực tiếp (live streaming) sử dụng multicast để gửi luồng video/âm thanh đến nhiều người xem.
Hội nghị truyền hình: Các cuộc họp video với nhiều người tham gia từ các địa điểm khác nhau.
Hệ thống phân phối nội dung: Truyền tải các bản cập nhật phần mềm, dữ liệu định kỳ hoặc thông tin tài chính đến nhiều người nhận trong mạng.
Giao thức định tuyến: Các giao thức định tuyến như OSPF (Open Shortest Path First) sử dụng multicast để truyền tải thông tin định tuyến đến tất cả các router trong mạng.
So sánh với các phương thức khác:
Unicast:

Gửi dữ liệu từ một nguồn đến một đích duy nhất. Thích hợp cho các giao tiếp một-đến-một.
Broadcast:

Gửi dữ liệu từ một nguồn đến tất cả các thiết bị trong mạng con. Thích hợp cho các thông báo cần thiết đến toàn bộ mạng con.
Ví dụ về Multicast:
Giao thức IGMP (Internet Group Management Protocol): IGMP được sử dụng để quản lý các thành viên của nhóm multicast trong mạng IP, cho phép các thiết bị tham gia hoặc rời khỏi nhóm multicast.
Phát sóng trực tiếp một sự kiện: Khi một sự kiện thể thao hoặc buổi hòa nhạc được phát trực tiếp qua mạng, multicast có thể được sử dụng để truyền tải luồng video đến nhiều người xem một cách hiệu quả.
Tóm lại, multicast là một phương thức truyền thông hiệu quả trong mạng máy tính, cho phép gửi dữ liệu từ một nguồn đến nhiều đích cụ thể, tiết kiệm băng thông và tối ưu hóa hiệu suất mạng.


Broadcast:

Giao tiếp một-đến-tất cả.
Dữ liệu được gửi từ một nguồn đến tất cả các thiết bị trong mạng con.
Mỗi thiết bị trong mạng đều nhận được gói tin broadcast, bất kể thiết bị đó có cần thông tin đó hay không.

Multicast:

Giao tiếp một-đến-nhiều.
Dữ liệu được gửi từ một nguồn đến một nhóm các thiết bị nhận cụ thể.
Chỉ các thiết bị thuộc nhóm multicast mới nhận được gói tin multicast.
