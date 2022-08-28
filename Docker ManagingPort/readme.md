# Docker - Manaming port

trong docker , bản thân các vùng chứa có thể có các ứng dụng chạy trong port . KHi mà bạn chạy một container thông qua một cổng port . bạn cần map cổng port của container với cổng của port của Docker host . hãy bắt đầu xem ví dụ này để xem làm sao có để đạt được nó

Trong ví dụ này , chúng ta sẽ tiến tới dowload jenkins container từ docker hub. Sau đó chúng sẽ map cổng port của container với cổng port của docker hub .

**Step 1** Đầu tiên bạn cần làm là đăng kí tài khoản của Docker hub

![](https://www.tutorialspoint.com/docker/images/simple_sing_up.jpg)

**Step 2** Sau khi đăng kí , bạn hãy login vào docker hub

![](https://www.tutorialspoint.com/docker/images/logged_docker_hub.jpg)

**Step 3** Tiếp theo hãy bắt đầu với trình duyệt và tìm kiếm Jenkins images

![](https://www.tutorialspoint.com/docker/images/run_command.jpg)

**Step 4** Nếu bạn cuộn chuột xuống , bạn có thể thấy Docker pull command . Điều này sẽ sử dụng để dowload jenkins images trên máy chủ ubuntu cục bộ

![](https://www.tutorialspoint.com/docker/images/local_ubuntu_server.jpg)

**Step 5** Bây giờ hãy tiến tới Ubuntu server và chạy lệnh

sudo docker pull jenkins

![](https://www.tutorialspoint.com/docker/images/inspect_image.jpg)

**Bước 6** Để biết những cổng nào được tiếp xúc với container . bạn cần sử dụng Docker `inspect command` để quan sát image

Bây giờ hãy bắt đầu tìm hiểu về inspect docker này

## Docker inspect

Cái phương thức này cho phép một cách để trả về thông tin của vùng chứa hình ảnh

### Cú phá

    docker inspect Container/Image

### Tùy chọn

Thông tin của image sẽ được trả về dưới dạng JSON

## Ví dụ

    sudo docker inspect jenkins

Đầu ra của `inspect` trả về một đối tượng json . nếu chúng ta quan sát đầu ra , chúng ta sẽ có thể có thể thấy là một secction của ExposerdPost và nhìn thấy là có 2 cổng được đề cập tới . Một là cổng data port 8080 và một cổng control port là 50000

Để chạy Jenkins và map cổng port , bạn cần thay đổi Docker chạy lệnh và thêm -p tùy chọn , nó để chỉ ra cổng port mapping . Vì thê bạn cần chạy theo lệnh dưới đây

    sudo docker run -p 8080:8080 -p 50000:50000 jenkins

Bên trả của cổng port là cổng port để mapping của docker , bên phải là cổng port của

Khi bạn chạy trình duyệt và truy cập trên thanh công cụ của Docker trên port 8080 , bạn sẽ nhìn thấy kinkins chạy

![](https://www.tutorialspoint.com/docker/images/unlock_jenkins.jpg)
