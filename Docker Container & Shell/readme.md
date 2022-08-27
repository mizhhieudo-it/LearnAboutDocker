# Docker - Containers và Shell

Mặc định khi bạn chạy một container , bạn sẽ có thể sử dụng `shell command` khi đang chạy container như hình minh họa dưới đây . Đây là những gì chúng ta đã thấy trong các chương trước khi chúng ta làm việc với container

![enter image description here](https://www.tutorialspoint.com/docker/images/shell_command.jpg)

Trong hình ảnh chụp trên , bạn có thể quan sát rằng chúng ta có vấn đề với yêu cầu dưới đây

    sudo docker run -it centos /bin/bash

Chúng ta đã sử dụng dụng yêu cầu này để tạo mới container và sau đó sử dụng Ctrl + P + Q để thoát khỏi container . It đảm bảo rằng Container còn tồn tại thậm trí sau khi chúng ta thoát khỏi container

Chúng ta có thể xác thực container có còn đang chạy hay không với Docker ps . Nếu chúng ta trực tiếp thoát khỏi container , sau đó bản thân container đó sẽ bị phá hủy

Bây giờ điều này là nhiều cách để đính kèm containers và thoát khỏi chúng mà không cần phá hủy chúng . Một cách khác để đạt được chúng là sử dụng lệnh nsenter

    docker run --rm -v /usr/local/bin:/target jpetazzo/nsenter

![enter image description here](https://www.tutorialspoint.com/docker/images/nsenter_image.jpg)

Trước khi chúng ta sử dụng ví dụ `nsenter` , chúng ta cần phải lấy được ProcessID của container . bở vị điều này yêu cầu bởi `nsenter` . Chúng ta có lấy những ProcessID thông qua Docker inspect command và lọc nó thông qua `Pid`

![enter image description here](https://www.tutorialspoint.com/docker/images/inspect_command.jpg)
với thông tin in hình ảnh trên , chúng ta có lần đầu sử dụng lệnh docker ps để nhìn thấy những container đang chạy . Chúng ta nhìn thấy rằng điều này là để chạy một container với ID là ef42a4c5e663
Sau đó chúng ta sử dụng `docker inspect` để cấu hình của container và chúng ta sử dụng `grep` để lọc ra ra id của tiến trình . Từ đầu ra chúng ta có thể thấy id của tiến trình là 2978
Bây giờ chúng đã có processID , Chúng ta có tiến trình ở đằng trước và sử dụng nsenter lệnh để tính kèm vào Docker container

## Nsenter

Đây là phương thức cho phép một cách đính kèm của a một container ở ngoài vùng chứa của container

### Cú pháp

- -n là sử dụng để đề cập Uts namespace
- -m là sử dụng để đè cập đến mount namespace
- -n là sửu dụng để đề cập đến network namespace
- -p là sử dụng để để cập đến tiếp trình namespace
- -i là để tạo cho container chạy ở chế độ interractive
- -t là để sử dụng kết nối I/O streams của containers đến hệ điều hành của host
- containerId - đây là ID của container
- Command - là đề chạy trong container

### Trả về giá trị

không trả về

### Ví dụ

    sudo nsenter -m -u -n -p -i t 2979 /bin/bash

### Đầu ra

![enter image description here](https://www.tutorialspoint.com/docker/images/nsenter.jpg)
Từ đầu ra chúng ta có thể quan sát được một vài điểm

- Lời prompt đổi tới bash shell khi chúng ta sử dụng nsenter command.
- chúng ta có vấn đề với `exit` commnad . Hiện tại thông thường nếu bạn không sử dụng nsenter command , Container sẽ bị phá hủy . Nhưng bạn sẽ thông rằng khi chúng ta đang chạy nsenter command , container này vẫn còn hoạt động và chạy
