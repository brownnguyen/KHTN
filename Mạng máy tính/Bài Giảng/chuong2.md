OSI:
    - Tầng application
        - Nhưng dịch vụ ứng dụng mạng end user sử dụng - theo kiến trúc client server, nói chuyện với nhau tuân theo ứng dụng protocol đó

    - Tầng presentation
        - Chuyển đổi bộ mã kí tự, nén dữ liệu, mã hoá dữ liệu

    - Tầng session
        - Quản lý phiên kết nối giữa hai ứng dụng ( cụ thể liên quan tới authentication : chứng thực user name password
         và authorization: có quyền gì, uỷ thác quyền gì)

    - Transport:
        - Giải quyết vấn đề truyền nhận dữ liệu giữa 2 ứng dụng
            - Phân đoạn dữ liệu ( Segmentation )
            - Kiểm soát, điều khiển dòng dữ liệu từ bên gửi sang bên nhận ( flow control )
            - Đảm bảo dữ liệu từ bên gửi sang bên nhận khong bị mất ( error control )
            - Có 2 kiểu truyền, tạo ra kết nối (connection : gọi điện thoại), gắn địa chỉ bên gửi và địa chỉ bên nhận ( connectionless: gửi thư )
    - Network:
        - Chịu trách nhiệm truyền nhận gói tin giữa hai network khác nhau
            - Segments đưa xuống network gọi là packet
            - Các network nối với nhau dùng router gọi là routing ( định tuyến, xác nhận con đường đi từ mạng này đến mạng kia)
            - Path determination: xác định con đường đi tốt nhất( có các protocol để làm công việc đó: OSPF, BGP, IS-IS) ( Chức  năng quan trọng)
            - Gói tin ở tầng network dùng địa chỉ logic ( IP )
    - Data link:
        - Truyền nhận gói tin giữa hai thiết bị trong một mạng ( Địa chỉ vật lý Mac address)
        - Truy cập đường truyền ( Gởi gói tin từ trong card mạng xuống đường dây cáp mạng, đọc dữ liệu từ đường dây cáp mạng đi vào)

    - Tầng vật lý:
        - Chuyển thành các bit và truyền đi vào media ( cáp )