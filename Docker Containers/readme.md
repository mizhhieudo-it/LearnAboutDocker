# Docker Container

## 1 . Docker container là gì ?

Container là một `instances` của `Docker images` có thể chạy sử dụng Docker run command . Về cơ bản , mặc định của docker là để chạy `containers` . Hãy cùng thảo luận cách làm việc của containers

## 2. Chạy một Container

Việc chạy một container được quản lý với yêu cầu `Docker run` . Để chạy một `container` trong ` interactive mode` . Đầu tiên chạy `Docker container`

    sudo docker run -it centos /bin/bash

Sau đó bấm `ctr + p` và bạn sẽ trả về OS Shell

![Description run contianer](https://www.tutorialspoint.com/docker/images/containers.jpg)

Sau đó bạn sẽ chạy trong `instance` của hệ thống CentOS on Ubuntu server

## Danh sách của containers

Chúng ta có thế liệt kê danh sách của containers trên máy chủ thông qua yêu cầu `docker ps ` . Yêu cầu này sử dụng để trả về các containers đang chạy hiện tại

    docker ps

### Cú pháp

    docker ps

### Tùy chọn

không có

### Trả về giá trị

Khi chúng ta chạy yêu cầu ví dụ trên command , nó sẽ cung cấp kết quả sau
![Result run ps docker](https://www.tutorialspoint.com/docker/images/listing_of_containers.jpg)

## Docker ps -a

Yêu cầu này sử dụng để liệt kê tất cả container có trong hệ thống

### Cú pháp :

    docker ps -a

### Tùy chọn :

`-a` nó nói với `docker ps` yêu cầu liệt kê tất cả các container có trong hệ thống

### Trả về giá trị :

Đầu ra sẽ hiển thị tất cả container

### Ví dụ :

    sudo docker ps -a

### Đầu ra

Khi chạy yêu cầu này , nó sẽ xuất ra kết quả sau

![enter image description here](https://www.tutorialspoint.com/docker/images/docker_ps_a.jpg)

## Docker history

Với yêu cầu này , bạn có thể nhìn thấy tất cả yêu cầu chạy images thông qua `container`

### Cú pháp :

    Docker history ImageID

### Tùy chọn L

`Images` - Đây là Image ID cho cái mà bạn muốn nhìn tất tất cả yêu cầu đã chạy nó

### Trả về giá trị

Đầu ra sẽ hiển thị tất cả yêu cầu đã chạy nó

    sudo docker history centos

Yêu cầu trên sẽ hiển thị các yêu cầu đã chạy `centos` images

### Đầu ra

Khi chúng ra chạy ví dụ yêu cầu trên , nó sẽ trả về về kết quả sau

![enter image description here](https://www.tutorialspoint.com/docker/images/docker_history.jpg)

# Docker Container

## 1 . Docker container là gì ?

Container là một `instances` của `Docker images` có thể chạy sử dụng Docker run command . Về cơ bản , mặc định của docker là để chạy `containers` . Hãy cùng thảo luận cách làm việc của containers

## 2. Chạy một Container

Việc chạy một container được quản lý với yêu cầu `Docker run` . Để chạy một `container` trong ` interactive mode` . Đầu tiên chạy `Docker container`

    sudo docker run -it centos /bin/bash

Sau đó bấm `ctr + p` và bạn sẽ trả về OS Shell

![Description run contianer](https://www.tutorialspoint.com/docker/images/containers.jpg)

Sau đó bạn sẽ chạy trong `instance` của hệ thống CentOS on Ubuntu server

## Danh sách của containers

Chúng ta có thế liệt kê danh sách của containers trên máy chủ thông qua yêu cầu `docker ps ` . Yêu cầu này sử dụng để trả về các containers đang chạy hiện tại

    docker ps

### Cú pháp

    docker ps

### Tùy chọn

không có

### Trả về giá trị

Khi chúng ta chạy yêu cầu ví dụ trên command , nó sẽ cung cấp kết quả sau
![Result run ps docker](https://www.tutorialspoint.com/docker/images/listing_of_containers.jpg)

## Docker ps -a

Yêu cầu này sử dụng để liệt kê tất cả container có trong hệ thống

### Cú pháp :

    docker ps -a

### Tùy chọn :

`-a` nó nói với `docker ps` yêu cầu liệt kê tất cả các container có trong hệ thống

### Trả về giá trị :

Đầu ra sẽ hiển thị tất cả container

### Ví dụ :

    sudo docker ps -a

### Đầu ra

Khi chạy yêu cầu này , nó sẽ xuất ra kết quả sau

![enter image description here](https://www.tutorialspoint.com/docker/images/docker_ps_a.jpg)

## Docker history

Với yêu cầu này , bạn có thể nhìn thấy tất cả yêu cầu chạy images thông qua `container`

### Cú pháp :

    Docker history ImageID

### Tùy chọn L

`Images` - Đây là Image ID cho cái mà bạn muốn nhìn tất tất cả yêu cầu đã chạy nó

### Trả về giá trị

Đầu ra sẽ hiển thị tất cả yêu cầu đã chạy nó

    sudo docker history centos

Yêu cầu trên sẽ hiển thị các yêu cầu đã chạy `centos` images

### Đầu ra

Khi chúng ra chạy ví dụ yêu cầu trên , nó sẽ trả về về kết quả sau

![enter image description here](https://www.tutorialspoint.com/docker/images/docker_history.jpg)
