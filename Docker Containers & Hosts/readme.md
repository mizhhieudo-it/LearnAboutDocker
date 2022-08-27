# Docker - Container and Hosts

Một tư duy tốt về `Docker engine` là thiết kế để làm việc trên nhiều hệ điều hành . Chúng ta đã nhìn thấy cài đặt trên windows và nhìn thấy tất cả yêu cầu Docker trên Linux system . Bây giờ hãy bất đầu nhìn các lệnh khác nhau trên Windows OS .

## Docker Images

Hãy bắt đầu chạy lệnh Docker `images` trên windows host
![enter image description here](https://www.tutorialspoint.com/docker/images/docker_images.jpg)
Từ đây , chúng ta có thể nhìn thấy rằng chúng ta có 2 images - ubuntu và hello-word

## Chạy một Container

Bây giờ hãy bắt đầu chạy một container in Windows Docker host

![enter image description here](https://www.tutorialspoint.com/docker/images/running_container.jpg)

    	docker run it ubuntu/bin/bash

## Liệt kê tất cả containers

Hãy bắt đầu tất cả danh sách containers trên Windows host

    docker ps

![enter image description here](https://www.tutorialspoint.com/docker/images/listing_containers.jpg)

## Dừng một Container

    Docker stop `IDCONTAINER`

![enter image description here](https://www.tutorialspoint.com/docker/images/stopping_a_container.jpg)

Các commnd trong Windows sẽ tương tự trên linux
