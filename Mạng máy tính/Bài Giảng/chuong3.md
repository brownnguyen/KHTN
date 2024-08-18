TCP/IP

    - Khái niệm địa chỉ IP
        - Các máy tính nối vào mạng thông qua card mạng thì phải được định danh bằng một địa chỉ IP
        - Những địa chỉ này duy nhất không được trùng trong 1 hệ thống mạng

        - Gồm 2 loại:
            - Địa chỉ vật lý, vd: địa chỉ MAC (Media Access Control), do nhà sản xuất card mạng ghi cứng con số đó lên ROM của card mạng đó, không thể thay đổi được ( 6 bite )
            - Địa chỉ logic, vd: địa chỉ IP ( Internet Protocol), do nhà quản lý mạng cấp, có thể thay đổi được ( 4 bite)

    Packet sử dụng địa chỉ ip
    Frame ở tầng datalink sử dụng địa chỉ vật lý

        Địa chỉ IP v4 có 4 bytes ( 32 bits )
    4 bite thập phân : 172.29.1.10
    4 bite nhị phân: 10101100 00011101 00000001 00001010

    32 bits địa chỉ IP chia làm 2 phần
        - network ID ( NetID) gióng như tên đườngß
        - host Id: giống nhà
        - Trong cùng 1 network thì netID giống nhau, chỉ khác hostID

        - Subnet mask dùng dể xác định bit nào là net bit nào là host
        - Bit nào trong subnet mask = 1 là net, bit nào = 0 là host

        vd: 172.29.5.128/255.255.192.0
        hoặc 172.29.5.128/18
 
        Host IP : 1010 1100 | 0001 1101 | 0000 0101 | 1000 0000
     Subnet mask: 1111 1111 | 1111 1111 | 1100 0000 | 0000 0000
     => 18 bit (số 1) là networkID, còn lại 14 bit (số 0 ) là hostID

    - Địa chỉ đường mạng (Net Addr)
        - Các bit thuộc netID giữ nguyên
        - Các bit thuộc hostID bật về 0
    (Broadcast) là kiểu gởi gói tin đến tất cả các máy trong mạng
    - Địa chỉ broadcast
        - Các bit thuộc NetID giữ nguyên
        - Các bit thuộc HostID: bật lên 1
    
    - Khi cho 1 địa chỉ IP, biết cách xác định địa chỉ IP đó có địa chỉ đường mạng là bao nhiêu và địa chỉ broadcast đường mạng là bao nhiêu

    Vd: 192.168.1.2/24

         HostIP: 1100 0000 | 1010 1000 | 0000 0001 | 0000 0010
    Subnet mask: 1111 1111 | 1111 1111 | 1111 1111 | 0000 0000 ( 24 tương đương 3 byte đầu  = 1, byte còn lại = 0)
       Net Addr: 1100 0000 | 1010 1000 | 0000 0001 | 0000 0000
      Broadcast: 1100 0000 | 1010 1000 | 0000 0001 | 1111 1111

    Vd: 172.29.35.1/19

        HostIP: 1010 1100 | 0001 1101 | 0010 0011 | 0000 0001
   Subnet mask: 1111 1111 | 1111 1111 | 1110 0000 | 0000 0000 ( 19 netId, 13 host ID)
      Net Addr: 1010 1100 | 0001 1101 | 0010 0000 | 0000 0000 172.29.32.0
     Broadcast: 1010 1100 | 0001 1101 | 0011 1111 | 1111 1111 172.29.63.255


Hai node có cùng địa chỉ đường mạng thì thuộc cùng 1 đường mạng
Só địa chỉ host hợp lệ trong cùng 1 đường mạng 2^m - 1 ( m là số bít trong phần HostID)


    - Địa chỉ IP là 32 bit ( không gian địa chỉ là 2^32 )
        - Được chia ra làm 5 lớp địa chỉ
            - Chỉ sử dụng lớp A B C, còn D E không dùng tới
                Cách phân biệt:
                    - Nhìn vào bits đầu tiên
                        - Class A range: 1-126 ( 1 byte là net, 3 byte còn lại là host ) (subnet mask / 8)
                        - Class B range: 128 - 191 ( 2 byte là net, 2 byte còn lại là host ) (subnet mask / 16)
                        - Class C range: 192 - 223 ( 3 byte là net, 1 bytew còn lại là host) (subnet mask / 24)
                        - Class D range: 224 - 239
                        - Class E range: 240 - 255

    Ví dụ kết bài:
    IP: 172.29.7.10
            - Lớp: B ( là Class B dòng 63 )
            1010 1100 | 0000 1101 | 0000 0110 | 0000 1010
       - Net Addr: 1010 1100 | 0001 1101 | 0000 0000 | 0000 0000 =  172.29.0.0
       - Số host trong cùng network: ( dòng 58, 59) 2^16-2
       - Các địa chỉ của host: từ 172.29.0.1 - 172.255.254
       Địa chỉ broadcast: 1010 1100 | 0001 1101 | 1111 1111 | 1111 1111 = 172.29.255.255