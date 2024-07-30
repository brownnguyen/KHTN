
Giảm lưu lượng broadcast trong mạng, cải thiện hiệu suất tổng thể của mạng.
Tăng cường bảo mật:

Cho phép phân đoạn mạng thành các phần nhỏ hơn, giúp kiểm soát và hạn chế truy cập giữa các subnet.
Các khái niệm cơ bản trong Subnetting:
Địa chỉ mạng (Network Address):

Là địa chỉ đại diện cho toàn bộ mạng hoặc subnet. Địa chỉ này có tất cả các bit của phần host bằng 0.
Địa chỉ broadcast (Broadcast Address):

Là địa chỉ được sử dụng để gửi dữ liệu đến tất cả các thiết bị trong mạng hoặc subnet. Địa chỉ này có tất cả các bit của phần host bằng 1.
Địa chỉ host (Host Address):

Là các địa chỉ IP có thể gán cho các thiết bị trong mạng hoặc subnet. Nó nằm giữa địa chỉ mạng và địa chỉ broadcast.
Subnet Mask:

Là một chuỗi các bit được sử dụng để phân biệt phần mạng và phần host của địa chỉ IP. Ví dụ: Subnet mask 255.255.255.0 (hoặc /24 trong ký hiệu CIDR) cho biết 24 bit đầu tiên là phần mạng và 8 bit cuối là phần host.
Ví dụ về Subnetting:
Giả sử bạn có một mạng với địa chỉ IP 192.168.1.0/24 và bạn muốn chia thành 4 subnet.

Xác định số subnet và số bit cần mượn:

Bạn cần chia mạng thành 4 subnet, tức là 2^2 = 4. Bạn cần mượn 2 bit từ phần host để tạo subnet.
Tính toán Subnet Mask mới:

Ban đầu: 255.255.255.0 hoặc /24
Mượn 2 bit từ phần host: 255.255.255.192 hoặc /26
Chia mạng thành các subnet:

Subnet 1: 192.168.1.0/26
Subnet 2: 192.168.1.64/26
Subnet 3: 192.168.1.128/26
Subnet 4: 192.168.1.192/26
Xác định địa chỉ mạng và địa chỉ broadcast cho mỗi subnet:

Subnet 1:
Địa chỉ mạng: 192.168.1.0
Địa chỉ broadcast: 192.168.1.63
Subnet 2:
Địa chỉ mạng: 192.168.1.64
Địa chỉ broadcast: 192.168.1.127
Subnet 3:
Địa chỉ mạng: 192.168.1.128
Địa chỉ broadcast: 192.168.1.191
Subnet 4:
Địa chỉ mạng: 192.168.1.192
Địa chỉ broadcast: 192.168.1.255
Địa chỉ host khả dụng:

Mỗi subnet có thể cung cấp 2^6 - 2 = 62 địa chỉ host khả dụng (2^6 là số bit của phần host, trừ 2 địa chỉ mạng và broadcast).
Tóm lại:
Kỹ thuật chia địa chỉ đường mạng con (Subnetting) là một phương pháp quan trọng để quản lý và tối ưu hóa mạng máy tính. Bằng cách chia một mạng lớn thành các subnet nhỏ hơn, bạn có thể cải thiện hiệu suất, quản lý mạng dễ dàng hơn và tăng cường bảo mật.