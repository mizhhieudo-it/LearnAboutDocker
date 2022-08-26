# Docker - Working with container

Trong phần này , Chúng ta sẽ khám chúng ta sẽ có thể làm gì với container

## Docker top

Với yêu cầu này , chúng ta có thể thấy thấy `top process ` (các tiến trình đang chạy) bên trong một container

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

Yêu cầu trên sẽ cung cấp CPU và Memory được sử dụng container `9f215ed0b0d3`

### Đầu ra

Khi chúng tôi chạy ví dụ trên , nó chạy sẽ cung cấp kết quả
![enter image description here](https://www.tutorialspoint.com/docker/images/docker_stats.jpg)

## Docker attach

Yêu cầu này sẽ sử dụng để đính kèm cho phép nhập input và hiển thị output đói với container đang chạy

### Cú pháp

    docker attach ContainerID

### Tùy chọn

`Container` - Đây là Container ID để khi mà bạn cần đề đính kèm

### Ví dụ

    sudo docker attach 07b0b6f434fe

yêu cầu trên sẽ đính kèm tới Docker `07b0b6f434fe`

### Đầu ra

Khi chúng tôi chạy yêu cầu , nó sẽ cung cấp kết quả sau

![enter image description here](https://www.tutorialspoint.com/docker/images/docker_attach.jpg)
Khi Bạn có đính kèm tới docker container , bạn chạy ví yêu cầu trên để nhìn thấy tiến trình đã sử dụng in cái Docker container đó

## Docker pause

Yêu cầu này là sử dụng để dừng tiến trình đang chạy để dừng tiến trình container

### Cú pháp

    docker pause ContainerID

### Tùy chọn

ContainerId - Sử dụng ContainerID khi mà bạn cần dừng tiến trình container

#### Ví dụ :

    Sudo docker pause 07b0b6f434fe

Ví dụ trên sẽ dừng tiếng trình đang chạy trong container `07b0b6f434fe`

#### Đầu ra :

Khi chúng sử dụng triến trình trên , nó sẽ xuất ra cho chúng ra kết quả
![enter image description here](https://www.tutorialspoint.com/docker/images/docker_pause.jpg)

## Docker unpause

Yêu cầu dùng đề bỏ tạm dừng tiến trình trong a container đang chạy

### Cú pháp

    docker unpause ContainerID

### Tùy chọn

`ContainerId` - được sử dụng để bỏ tạm dừng tiến trình trong container

### Trả về giá trị

Trả về ContainerId của container đang chạy

### Ví dụ

    sudo docker unpause 07b0b6f434fe

yêu cầu ví dụ trên sẽ bỏ tạm dừng tiếng trình của container có id là `07b0b6f434fe`

### Đầu ra

Chạy ví dụ trên chúng ra sẽ nhận được kết quả
![enter image description here](https://www.tutorialspoint.com/docker/images/docker_unpause.jpg)

## Docker Kill

Yêu cầu này được sử dụng để dừng một tiến trình đang chạy container

### Cú pháp

    docker kill containerID

### Tùy chọn

`ContainerID` - Đây là ContainerID được sử dụng kill process trong container

### Trả về giá trị

Trả về giá trị `ContainerId` mà nó đang chạy

### Đầu ra

Khi chúng ta chạy command này , nó sẽ xuất ra cho chúng ta kết quả

![enter image description here](https://www.tutorialspoint.com/docker/images/docker_kill.jpg)

## Docker - Container Lifecycle

Hình minh họa sau sẽ cố gắng giải quyết vòng đời của một Docker container

![enter image description here](https://www.tutorialspoint.com/docker/images/container_lifecycle.jpg)

- Bắt đầu , docker container sẽ tạo state khi Doker `run` yêu cầu để sử dụng
- Sau đó `Docker container` chạy các `state` khi Docker `run` được sử dụng
- Docker yêu cầu `kill` được sử dụng khi kết thúc docker Container
- Docker yêu cầu `pause` được sử dụng là dừng lại Docker container
- Docker `stop` được sử dụng để dừng để Docker containẻ
- Docker `run` yêu cầu sử dụng để đẩy một container từ trạng thái dừng sang trạng thái `running`
