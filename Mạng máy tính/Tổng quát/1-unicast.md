

Đặc điểm của Unicast:
Giao tiếp một-đến-một:

Dữ liệu được gửi từ một máy phát đến một máy nhận duy nhất.
Hiệu quả cho giao tiếp cá nhân:

Thích hợp cho các ứng dụng yêu cầu giao tiếp trực tiếp giữa hai thiết bị, như truyền file, email, và các cuộc gọi thoại/video.
Địa chỉ đích duy nhất:

Gói tin unicast chứa địa chỉ IP của máy đích cụ thể.
Sử dụng trong nhiều giao thức mạng:

Hầu hết các giao thức truyền thông mạng, như TCP và UDP, đều hỗ trợ unicast.
Ưu điểm của Unicast:
Đơn giản: Dễ hiểu và triển khai.
Bảo mật: Chỉ có hai thiết bị tham gia vào giao tiếp, giúp hạn chế nguy cơ bảo mật.
Quản lý băng thông: Mỗi gói tin chỉ đi từ nguồn đến đích, không tiêu tốn băng thông của các thiết bị khác.
Nhược điểm của Unicast:
Không hiệu quả trong nhiều trường hợp: Đối với các ứng dụng cần gửi dữ liệu đến nhiều người nhận (ví dụ: phát sóng video trực tiếp), unicast có thể không hiệu quả vì cần phải gửi nhiều bản sao của cùng một dữ liệu.
Không tối ưu hóa mạng: Khi gửi dữ liệu đến nhiều đích, unicast có thể làm tăng tải trên mạng do số lượng gói tin truyền đi tăng lên.
So sánh với các phương thức khác:
Multicast:

Gửi dữ liệu từ một nguồn đến một nhóm các đích. Thích hợp cho các ứng dụng như hội nghị truyền hình hoặc phát sóng video, nơi mà cùng một dữ liệu cần được gửi đến nhiều người nhận.
Broadcast:

Gửi dữ liệu từ một nguồn đến tất cả các thiết bị trong một mạng con. Thường được sử dụng trong các mạng nhỏ hoặc trong các trường hợp yêu cầu phát sóng thông báo đến tất cả các thiết bị.
Ứng dụng của Unicast:
Truyền file: Gửi dữ liệu từ một máy tính đến một máy tính khác.
Email: Mỗi email được gửi từ một máy chủ email đến một người nhận cụ thể.
Dịch vụ web: Các yêu cầu HTTP từ trình duyệt web đến máy chủ web thường sử dụng unicast.
Tóm lại, unicast là một phương thức truyền thông quan trọng trong mạng máy tính, hỗ trợ giao tiếp hiệu quả giữa hai thiết bị.