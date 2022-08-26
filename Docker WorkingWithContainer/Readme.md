# Docker - Working with container

Trong phần này , Chúng ta sẽ khám chúng ta sẽ có thể làm gì với container

## Docker top

Với yêu cầu này , chúng ta có thể thấy thấy `top process ` bên trong một container

### Cú pháp :

    docker top ContainerID

### Tùy chọn :

ContainerID - Đây là ContainerID với cái mà bạn muốn nhìn thấy ` the top process`

### Trả về giá trị

Đầu ra sẽ hiển thị top-level tiến trình bên trong một container

Example
sudo docker top 9f215ed0b0d3

Yêu cầu sẽ hiển thị `top-level` tiến trình bên trong a một container

### Đầu ra

Khi bạn chạy ví dụ bên trên , nó sẽ xuất ra cho bạn kết quả sau
![enter image description here](https://www.tutorialspoint.com/docker/images/docker_top.jpg)

## Docker Stop

Yêu cầu này sử dụng để dừng một container đang chạy

### Cú pháp

    docker stop ContainerID

### Tùy chọn

`ContainerID` - Đây là Container ID , cái mà cần để dùng container đang chạy

### Giá trị trả về

Đầu ra sẽ cung cấp ID của container đã dừng

### Example

    sudo docker stop 9f215ed0b0d3

yêu cầu trên sẽ dừng docker conatiner`9f215ed0b0d3`

### Đầu ra

Khi chạy ví dụ trên , nó sẽ cung cấp kết quả sau

![enter image description here](https://www.tutorialspoint.com/docker/images/docker_stop.jpg)

## docker rm

Yêu cầu này được được sử dụng để xóa một container

### Cú pháp

    docker rm ContainerID

### Tùy chọn

`ContainerID` - Đây là ContainerId , cái mà cần để gỡ bỏ container

### Ví dụ

    sudo docker rm 9f215ed0b0d3

yêu cầu này trên sẽ gỡ bỏ cái docker container `9f215ed0b0d3`

### Đầu ra

Khi chúng tôi chạy yêu cầu trên , nó sẽ xuất ra kết quả sau :

![enter image description here](https://www.tutorialspoint.com/docker/images/docker_rm.jpg)

## docker stats

Yêu cầu này đươc sử dụng để cung cấp các số liệu khi chạy container

### Cú pháp

    docker stats ConatainerId

### Tùy chọn

`ContainerId` - Đây là containerID dùng để lấy ra container cung cấp số liệu

### Trả về giá trị

Đầu ra sẽ trả về CPU và Memory được sử dụng của container

### Ví dụ

    sudo docker stats 9f215ed0b0d3
