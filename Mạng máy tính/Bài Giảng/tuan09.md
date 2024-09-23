Tầng transport
    - Phương thức TCP
        -   Gởi gói tin gồm 2 lỗi:
            - Lỗi bit
            - Lỗi mất gói
        Dù mất gói hay lỗi gói đều báo bên gửi gửi lại
        Truyền dữ liệu tin cậy sẽ giải quyết được 2 lỗi này
        Cách giải quyết
            - Lỗi bit: dùng các kĩ thuật kiểm lỗi( ví dụ như checksum )
                - Trước khi gởi gói tin sẽ gắn vào đó một thông tin kiểm lỗi
                - Khi nhận được bên nhận sẽ chạy thuật toán kiểm lỗi để phát hiện gói tin có bị hư hay không
            - Lỗi mất gói:
                - Gởi gói tin sẽ bật đồng hồ và tính thời gian phản hồi, nếu bận nhận nhận được sẽ gửi lại gói tin, nếu bên gửi nhận được gói tin phản hồi thì biết bên gửi đã gửi đúng đích
                - Nếu quá thời gian chờ mà không nhận được gói tin phản hồi thì giả dụ rằng gói tin bị mất và gửi lại gói tin khác

Để truyền dữ liệu tin cậy thì có 2 loại:
    - Loại dùng đường truyền tin cậy
        - Tức là đảm bảo đường truyền nhờ vào chất lượng đường truyền, đảm bảo gói tin không bị mất và không bị hư ( trường hợp này ngoài thực tế dường như là không có)
        - Truyền trên đường truyền không tin cậy ( có thể mất, có thể hư) - nghi thức truyền dữ liệu tin cậy được sử dụng

- RDT ( Reliable Data Transfer ) 3.0 là ý tưởng thuật toán của truyền dữ liệu tin cậy, có 1 điểm hạn chế, để khác phục hạn chế thì ng ta đưa ra phương pháp pipeline
    - Phương pháp pipeline có 2 phương pháp cụ thể
        - Go-back-N
        - Gởi lại gói chọn

- Khi bên nhận nhận được sẽ gửi lại gói tin phản hồi gọi là ACK
- Bên gửi:
    - Định nghĩa trường hợp mất gói
    - Chờ nhận tín hiệu
    - Hết thời gian chờ thì sẽ gửi lại gói tin đó

- RDT ( Reliable Data Transfer ):
    - Điểm hạn chế: gởi 1 gói tin phải chờ nhận ACK mới gửi gói tiếp theo
Nguyên lý pipeline:
    - Cho gửi nhiều gói mà chưa cần nhận ACK
    - Bên gửi dùng bộ nhớ đệm Buffer đẻ gói nào bị mất thì vào buffer đó lấy gửi lại
    - Bên nhận dùng buffer để lưu lại gói tin mà chưa đúng số thứ tự

- Giải quyết mất gói:
    - Go back n
    - Selective Repeat

Nghi thức pipeline

TCP: cung cấp các hàm và thủ tục cho tần application sử dụng
    - Kiểm soát luồng
    - Kiểm soát tắc nghẽn