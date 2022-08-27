# Public Repository

Công khai `Repository` có thể sử dụng để lưu chữ `images Docker` , cái mà có thể sử bởi mọi nguời . Với ví dụ là `images` đang tồn tại sẵn ở trong Docker Hub . Phần lớn của hình ảnh such as Centos , Ubuntu và Jenkins là tất cả đều được công khai có sẵn . Chúng ta cũng có thể tạo images có sẵn của chúng ta bởi public nó để công khai repository trên docker hub

Với ví dụ này , chúng ta sẽ sử dụng `myimage` repository xây dựng trên trên Docker file . Chương này , chúng ta cùng xây dựng dựa trên phần "Xây dựng Docker file" và tải images lên dokcer hub . Hãy bắt đầu kiểm tra lại image trên Docker host đê thấy cách mà chúng ta đẩy Docker Registry

![](https://www.tutorialspoint.com/docker/images/my_image.jpg)

Ở đây , chúng ta có myimage:0.1 , cái mà đã tạo ở chương " Xây dựng docker file " . Hãy bắt đầu sử dụng để công khai Repository này lên

Các bước ví dụ sau giải thích làm sao bạn có thể upload đươc images để công khai public Repository .

**Bước 1** Đăng nhập vào Docker hub và tạo Repository của bạn . Điều là là Repository . Nơi mà images được lưu trữ . Tiến tới https://hub.docker.com/ và đăng nhập với chứng chỉ của bạn

![description](https://www.tutorialspoint.com/docker/images/docker_hub.jpg)

** Bước 2 ** - Nhấn vào btn " Create Repository " trên ví dụ màn hình và tạo một repository với tên là **demorep** . Đảm bảo rằng chế độ hiển của repository là public

![](https://www.tutorialspoint.com/docker/images/demorep.jpg)

Sau khi repository được tạo . Tạo một lưu của lệnh pull , cái mà được đính kèm repository

![](https://www.tutorialspoint.com/docker/images/repository.jpg)

Với lệnh pull , cái mà sẽ sử dụng ở repository sau đây
docker pull domo demousr/demorep

**Bước 3** Bây giwof quay chở lại Docker host . Ở đây chusngta cần gắn thẻ myimage tới repo vừa được tạo trên docker hub . Chúng ta có thể làm điều này thong qua docker tag command

Chúng ta sẽ học điều này ở tà command trong chương sau

**Bước4** Vấn đề đăng nhập docker để login vào docker hub từ dòng lệnh . docker login command sẽ nhắc nhở bạn với usrname và password cho Docker hub

![](https://www.tutorialspoint.com/docker/images/docker_login_command.jpg)

** Bước 5 ** Sau khi được được gán thẻ images , bây giờ chúng ta có thể đẩy images lên docker hub repositoy . Chúng ta có thể thông qua DOcker push . CHúng ta sẽ tìm hiểu kỹ hơn trong phần tiếp theo

## Docker tag

Phương thức này cho phép bạn gán thẻ image liên quan tới repostory

### Cú pháp

    docker tag imageID Repositoryname

### Tùy chọn

- imageID : là ImageId cần đề gán vào repo
- repository name : là reponame gán cho image

### giá trị trả về

không

### Ví dụ

    sudo docker tag ab0c1d3744dd demousr/demorep:1.0

### Đầu ra

Một ví dụ đơn sản sẽ trả ra kết quả như bên duới đây

![](https://www.tutorialspoint.com/docker/images/docker_tag.jpg)

## Docker push

Phương thức này cho phép đẩy một image lên docker hub

### Cú pháp

- Repositoryname - đây là kho lưu trữ name , cái mà cần để đẩy lên docker hub

### giá trị tả về

trả về id của repo sau khi được đẩy lên Docker hub

### Ví dụ

    sudo docker push demousr/demorep:1.0

### Kế quả trả về

![](https://www.tutorialspoint.com/docker/images/docker_push.jpg)

nếu bạn trả lại trang docker hub và quay lại repository của bạn , bạn sẽ mình thấy tà name trong repository

![](https://www.tutorialspoint.com/docker/images/tag_name_in_repository.jpg)

Bây giờ hãy bắt đầu tải về repo và chúng ta tải xuống xuống Docker image từ docker host . Và đây là kết quả

![](https://www.tutorialspoint.com/docker/images/docker_pull_command.jpg)

