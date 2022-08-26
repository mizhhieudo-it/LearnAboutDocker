# Docker Hub :triangular_flag_on_post:

## 1 . Docker hub là gì ?

`Docker hub` là đăng kí dịch vụ trên máy chú cho phép bạn có thể tải xuống các `Docker images` và bản thân docker hub được xây dựng bởi một cộng đồng . Bạn cũng có thể xây dựng các `images` của bạn vào `Docker Hub` . Trong bài viết này chúng ta sẽ tìm hiểu làm sao để tải xuống và sử dụng `Jenkins Docker` image từ Docker hub

Trang chủ của Docker hub là https://www.docker.com/community-edition#/add_ons

### Bước 1 : Đầu tiên bạn cần làm là đăng kí tài khoản Docker hub

![officesite](https://www.tutorialspoint.com/docker/images/docker_hub_singup.jpg)

### Bước 2 : Khi bạn đã đã đăng kí thành công , bạn sẽ đăng nhập vào Docker Hub

![Logged-into-Docker0hub](https://www.tutorialspoint.com/docker/images/logged_into_docker_hub.jpg)

### Bước 3 : Tiếp theo hãy bắt đầu duyệt qua và tìm kiếm `Jenkins image`

![ResultAfterFindJenkins](https://www.tutorialspoint.com/docker/images/jenkins_image.jpg)

### Bước 4 : Nếu bạn cuộn chuột xuống trên cái page tương tự như hình dưới . Bạn có thể nhìn thấy `Docker pull` command . Điều này sẽ sử dụng để tải xuống `Jenkins images` trên local Ubuntu server

![Pull-images](https://www.tutorialspoint.com/docker/images/pull_command.jpg)

### Bước 5 : Bây gờ , hãy tới Ubuntu server và chạy theo command

      sudo docker pull jenkins

chúng ta sẽ được kết quả như sau

![Result-oull-jenkins](https://www.tutorialspoint.com/docker/images/ubuntu_server.jpg)
Để chạy jenkins , bạn cần phải chạy theo yêu yêu cầu

    sudo docker run -p 8080:8080 -p 50000:50000 jenkins

Lưu ý theo dõi các điểm về ví dụ trên sudo

- Chúng ta sẽ sử dụng `Sudo command` để chấp nhận nó chạy với quyền truy cập root
- Ở đây , Jenkins là tên của `images` , chúng ta muốn để tải xuống từ docker hub và cài đặt trên máy Ubuntu của chúng ta
- `p` được sử dụng để map cổng port của Docker images với cổng port của main Ubuntu Server của chúng ta , tuy nhiên chúng ta có thể truy cập `container` tương ứng

![Description-images-docker](https://www.tutorialspoint.com/docker/images/sudo_command.jpg)

chúng ta sẽ có JEnkins cài đặt thành công chạy với một container trên máy ubuntu .
