Internet domain space
- Một domain bao gồm tất cả các domain con
- Mỗi domain sẽ gồm 1 hoặc 2 máy làm dns server
- Dns server công việc chính là phân giải tên sang dịa chỉ IP và ngược lại
- Dns server miền cha sẽ quản lý dns server miền con
- Domain space:
- Domain:
- Zone:

- DNS


- HTTP
    - Nghi thức ở tầng ứng dụng
    - theo kiến trúc client server
    - có 2 kiểu message: response message, request message
    - HTTP sẽ sử dụng nghi thức TCP
    - HTTP có 2 loại:
        - Non-persistent HTTP
        - Persistent HTTP


DHCP
DNS
HTTP
SMTP

Cookies:
    - Cho web server nhận diện ra người dùng là ai mỗi khi truy cập vào web server đó
    gồm 4 components:
        - cookie header line trong response message
        - cookie header line trong request message
        - cookie file
        - lưu backend database tại website đó