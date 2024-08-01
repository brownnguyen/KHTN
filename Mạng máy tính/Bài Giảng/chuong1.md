internet

protocol

network edge (access network (cable-based access), physical media) how to connect end systems to edge router

network core

performance

security

protocol layer, service model

history

802.11 b/g/n

link: physical media
bit:

physical link

guided media:

unguiđe media

twisted pair


packet-switching:

Trong mạng sử dụng công nghệ packet switching, độ trễ (latency) bao gồm bốn thành phần chính:

Thời gian xử lý (Processing Delay): ( độ trễ trong router )

Là thời gian cần thiết để router hoặc switch kiểm tra tiêu đề của gói dữ liệu và quyết định tuyến đường tiếp theo.
Thời gian xử lý có thể bao gồm việc kiểm tra lỗi, tìm địa chỉ đích, và quyết định chuyển tiếp gói.
Thời gian xếp hàng (Queuing Delay):

Là thời gian gói dữ liệu phải chờ trong hàng đợi trước khi được xử lý và gửi đi.
Thời gian xếp hàng phụ thuộc vào tải lượng mạng, nếu mạng bị tắc nghẽn, thời gian xếp hàng có thể tăng lên đáng kể.

Thời gian truyền tải (Transmission Delay):  ( độ trễ ngay card mạng , độ trễ từ máy tính ra card mạng, xuống đường dây cáp mạng, đi xuống router, gọi là transmission delay )

Là thời gian cần thiết để truyền toàn bộ gói dữ liệu qua một liên kết mạng.
Tính bằng công thức: Transmission Delay = Kích thước gói / Tốc độ truyền tải của liên kết
Ví dụ: Nếu kích thước gói là 1000 bits và tốc độ truyền tải của liên kết là 1 Mbps, thời gian truyền tải là 1 ms.
Thời gian lan truyền (Propagation Delay):

Là thời gian cần thiết để một bit của gói dữ liệu truyền từ đầu gửi đến đầu nhận qua liên kết vật lý.
Tính bằng công thức: Propagation Delay = Khoảng cách / Tốc độ lan truyền của tín hiệu
Tốc độ lan truyền phụ thuộc vào môi trường truyền tải, như cáp quang hoặc cáp đồng.
Tổng độ trễ (Total Latency)
Tổng độ trễ của một gói dữ liệu từ nguồn đến đích sẽ là tổng của tất cả các thành phần trên:

Total Latency
=
Processing Delay
+
Queuing Delay
+
Transmission Delay
+
Propagation Delay
Total Latency=Processing Delay+Queuing Delay+Transmission Delay+Propagation Delay

Mỗi thành phần này đóng góp vào độ trễ tổng thể của mạng và có thể thay đổi tùy theo điều kiện mạng và các yếu tố kỹ thuật khác.


Các độ trễ:
transmision delay
nodal processing delay
queueing delay
propagation delay



throughput

packet sniffing
IP spoofing
Denial of service DOS



lines of defense