# Docker Images :card_file_box:

## Docker images là gì ?

Trong docker , mọi thứ sẽ được xây dụng trên `Images`. Một `Images` là sự kết hợp cảu một file hệ thống và các tham số . Hãy bắt đầu lấy một ví dụ của các lệnh sau trong docker

    Docker run hello-word

- yều cầu Docker là chỉ rõ và nói với chương trình docker trên hệ điều hành rằng có một cái gì đó cần hoàn thành
- Yêu cầu `run` là được sử dụng đề cập tới rằng chúng ta muốn tạo ra một `instance` của một image , cái mà sau khi đã gọi một `container`
- mặc định , `hello-word` đại diện `image` từ cài mà `container` tạo ra

Bây giờ hãy nhìn vào tại sao chúng ta cần sử dụng `CentOS image` có sẵn in Docker hub để chạy CentOs trên máy Ubuntu của chúng ta . Chúng ta có thẻ làm điều này bởi khi thực thi theo yêu cầu trên máy Ubuntu

    sudo docker run -it centos /bin/bash

Một số điểm lưu ý ở ví dụ trên

- Chúng ta đang sử dụng sudo command để chấp chạy với quyền `root` access
- ở đấy , `centos` là tên của images` mà chúng ta cần tải xuống từ docker hub và cài đặt trên máy Ubuntu
- - it là sử dụng để đề cập rằng chúng ta muốn chạy trên `interactive mode`
- /bin/bash là sử dụng để chạy bash shell sau khi CentOS được thiết lập và chạy

## Hiển thị `Docker iamges`

Để nhìn thấy danh sách của docker images trên hệ thống , bạn có thể đưa ra lệnh sau
docker images
Yêu cầu này sẽ sử dụng để hiện thị tất cả `images` hiện tại đã được cài đặt vào hệ thống

## Cú pháp

      docker images

## Tùy chọn

Không có

## Trả về giá trị

Đầu ra sẽ cung cấp một danh sách images on hệ thống

### Output

Khi bạn chạy ví dụ comand , nó sẽ cung cấp cho bạn result kiểu như sau

![Description-result](https://www.tutorialspoint.com/docker/images/displaying_docker_images.jpg)

Từ ví dụ trên , bạn có thể nhìn thấy rằng server có 3 images : `centos`,`newcentos` và `jenkins` . Mỗi `images` có thuộc tính sau đây :

- `Tag` : Điều này được sử dụng để gán nhãn hình ảnh một cách hợp lý .
- `Image ID` : Điều này được sử dụng để định danh một images độc nhất
- `Created` : Số lượng ngày kể từ khi `image` được tạo
- `Visual Size` : Kích thước của image

## Tải xuống `Docker images`

`Images có thể dowloads từ docker hub sử dụng the Docker run comand . Hãy bắt đầu theo dõi chi tiết làm sao chúng ta có thể làm điều đó

### Cú pháp

Cú pháp sau đây sử dụng để chạy một yêu cầu trong một `Docker Container`

    docker run image

Options
`Image` - Nó là tên của `image` , cái mà được sử dụng để chạy container

### Giá trị trả về

Đầu ra sẽ chạy yêu cầu trong `conatiner` mong muốn

### Ví dụ

    Sudo docker run centos

Với yêu cầu này sẽ tải xuống `centos images` , nếu nó chưa tồn tại và chạy OS với a container

### Đầu ra

Khi chúng ta chạy một yêu cầu trên , chúng ta sẽ nhận được một kết quả sau đây :

![Result ](https://www.tutorialspoint.com/docker/images/downloading_docker_images.jpg)

chúng ta sẽ nhìn thấy CentOS Docker images tải xuống . Bây giờ , nếu chúng ta chạy yêu docker images để thấy danh sách `image` trong hệ thống , Chúng ta sẽ thấy image centos ở đây

## Gỡ bỏ Docker Images

` Docker images` trên hệ thống có thể bị gỡ bỏ thông qua yêu cầu `docker rmi` . Hãy bắt đầu theo dõi với yêu cầu chi tiết howb

     docker rmi ImageID

yêu cầu sẽ được sử dụng để gỡ bỏ Docker images

### Cú pháp

    docker rmi ImageID

### Tùy chọn

`ImageID` - ID của image này cần được sử dụng để remove Image

### Example

     sudo docker rmi 7a86f8ffcb25

Ở đây , 7a86f8ffcb25 là `ID của newcentos Images `

### Đầu ra

Khi chúng ta chạy yêu cầu ví dụ trên , nó sẽ cung cấp kết quả sau

![Description-result-Id-image](https://www.tutorialspoint.com/docker/images/removing_docker_images.jpg)

## Docker images -q

Yêu cầu này được sử dụng để trả duy nhất ID của `Images` .

### Cú pháp

    docker images

### Tùy chọn

`q` - Nó nói rằng yêu cầu docker để trả về duy nhất Id của `Images`

### Trả về giá trị

Đầu ra sẽ hiển thị duy nhất id của images trên máy chủ docker

![Docker result](https://www.tutorialspoint.com/docker/images/docker_images_q.jpg)

## Docker inspect

Yêu cầu này sử dụng để theo dõi chi tiết của `images` or `container`

### Cú pháp

    docker inspect Repository

### Tùy chọn

`Repository` : Tên của image .

### Giá trị trả về

Giá trị trả về sẽ hiển thị chi tiết thông tin của Images

### Ví dụ :

Khi chúng ta chạy yêu cầu trên , nó sẽ cung cấp kết quả

![descriptionp- result](https://www.tutorialspoint.com/docker/images/docker_inspect.jpg)
