STMP:

- Mai server gửi và nhận thư bằng phương thức SMTP
    - Mail client: gửi thư cho máy chủ mail server bằng SMTP
    - Người dùng nhận thư bằng nghi thức POP3 và IMAP
        - POP3: post office protocol: người dùng lấy mail bằng nghi thức pop3, các lá thư ở mail server sẽ được download về máy của người dùng, và các mail đó sẽ bị xoá ở mail server, khi người dùng ra lệnh lấy thư ở một máy mới, họ sẽ không còn thấy các lá thư đã gửi ở mail server nữa, và họ sẽ nhận được các lá thư mới
        - IMAP: các thư của người dùng ở mail server sẽ được đồng bộ với máy của họ

- Thư từ bên gửi đến bên nhận có thể đi qua nhiều mail server trung gian mới đến mail server đích


User agent gửi mail lên mail server bằng nghi thức SMTP bằng port 25
    - Trong mail server có nhiều thành phần
    - Thành phần chính là MTA, user agent sẽ gửi lên MTA của mail server
        - Kiểm tra thông tin người gửi username/ password, kiểm tra thông tin người nhận
        - Hỏi DNS server MX record ra dịa chỉ IP ( tìm địa chỉ IP của mail server của người nhận)
        - Kiểm tra thông tin email người gửi, xem có thật không, có đúng không, kiểm tra bảo mật và spam

Thuật ngữ:
    - MUA: Mail user agent: phần mềm mail client, cung cấp khả năng kết nối đến mail server
    - MSA: Mail submission agent: nằm trong máy chủ mail server, nhận thư từ user agent và gửi đến MTA
    - MTA: Mail transport agent: module trong máy mail server, đảm nhận vại trò liên lạc với các MTA trên các máy chủ mail khác để gửi nhận thư điện tử
    - MDA: Mail delivery agent: đảm nhận việc nhận thư từ MTA và lưu vào hộp thư tương ứng của người dùng

    - Các giao thức: 
        - SMTP: Simple mail transfer protocol: dùng để gửi thư từ ứng dụng người đùng đến mail server của phía gửi và liên  lạc giữa các mail server
        - POP3: Post office protocol version 3: dùng dể liên lạc với mail servẻ để truy xuất các email nhận được. Nó tải xuống tất cả email trên hộp thư về máy cục bộ, mail servẻ không có trách nhiệm lưu trữ hay quản lý email sau đó
        - IMAP: internet message access protocol: dùng để liên lạc với mail server để truy xuất các email nhận được. Duy trì kết nối giữa ứng dụng mail người dùng và mail server để truy xuất các thư theo nhu cầu thay vì t ải xuống toàn bộ thư như POP3


Quy trình gửi nhận thư cơ bản:
    - 1 - Người gửi sử dụng một ứng dụng gửi thư (MUA) ví dụ như web gmail.com để gửi email đến địa chỉ người nhận
    - 2 - MUA sử dụng giao thức SMTP để gửi thư dến MTA của máy chủ mail phía gửi
    - 3 - 4 - Máy chủ phía gửi truy vấn DNS để tìm ra địa chỉ máy chủ phía nhận từ tên miền ví dụ như viettchgroup.vn
    - 5 - Bằng địa chỉ có được sau truy vấn, máy chủ phía gửi gửi thư đến máy chủ phái nhận bằng giao thức SMTP
    - 6 - Người nhận sử dung giao thức IMAP hoặc POP3 để truy xuất thư từ phía máy chủ phái nhận. Hiện nay, máy chủ phái nhận thường thực hiện các truy vấn DNS ngược cũng như các thao tác khác để kiếm chứng email không phải spam trước khi nhận email

Các rủi ro bảo mật với email
    - Chiếm quyền và truy cập trái phép
    - DOS denial of services: tấn công Dos là làm quá tải máy chủ bằng nhiều cách kahcs nhau khiến chúng không thể phục vụ người dùng thật sự
    - Spoofing: giả mạo địa chỉ bên gửi
    - Man in the middle: loại này thường nhắm vào đường truyền công cộng với mức bảo mật thấp hoặc không có bảo mật. Chặn các gói tin trên đường truyền để thu thập thông tin
    - Spam mail: thư rác thư quảng cáo
    - Malware
    - Social engineering: loại tấn công phối hợp nhiều phương pháp để tấn công, thu thập đầy đủ thông tin của người đó để tấn công



-----------------------------------------------------------------------------------
Tầng transport

    - Cung cấp các dịch vụ truyền nhận dữ liệu cho tầng application sử dụng
    - 2 nghi thức: UDP ( truyền dữ liệu không tin cậy ), TCP ( truyền dữ liệu tin cậy )
    - Hỗ trợ:
        - Truyền dữ liệu tin cậy
            - Điều khiển luồng ( tránh làm tràn ngập dữ liệu ở bên nhận )
            - Điều khiển tắc nghẽn
            - Thiết lập và duy trì kết nối
        - Truyền dữ liệu không tin cậy
            - Nỗ lực gửi dữ liệu hiệu quả nhất
    - Không hỗ trợ:
        - Đảm bảo thời gian trễ
        - Đảm bảo băng thông

    - Dồn kênh ( Multiplexing )
        - Thực hiện tại bên gửi
        - Thu thập dữ liệu từ các socket
        - Dán nhãn dữ liệu với 1 header

    - Phân kênh
        - Thực hiện tại bên nhận
        - Phân phối các segment nhận được cho socket tương ứng
        - Khi đóng gói dữ liệu ở tầng transportm header sẽ thêm vào:
            - Source port
            - Destination port
    
    - UDP: Usẻ datagram protocol
        - Dịch vụ nỗ lực để truyền nhanh
        - Gói tin có thể:
            - Mất
            - Không đúng thứ tự

        Không kết nối: 
            - Không có handshaking giữa bên gửi và nhận ( không cần tạo kết nối)
            - Mỗi gói tin UDP đuọc xử lý độc lập
            - Không có trạng thái kết nối

- checksum: kĩ thuật để kiểm lỗi

UDP thường sử dụng cho các ứng dụng multimedia
    Một số ứng dụng sử dụng UDP
        - DNS
        - SNMP
        - TFTP