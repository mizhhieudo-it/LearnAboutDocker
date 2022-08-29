# Docker Registry

bạn có thể sẽ cần có riêng repository private . Bạn có thể không muốn lưu trữ trên docker hub . Cho điều này , đây là một repository conatiner có vùng chứa từ docker . Hãy bắt đầu theo dỗi xem chúng ta có thể dowload và sử dụng container với registry

**Bước 1** Sử dụng docker run để dowload private registry . Bạn có thể hoàn thành bàn cách sử dụng dòng lệnh

    sudo docker run -d -p 5000:5000 --name registry registry:2

Một vài điểm cần lưu ý trong ví dụ trên

- `registry` là thùng chứa quản lý bởi docker , cái mà có thể sử dụng để lưu trử private repositories

- Cổng port tiếp xúc là 5000 . Kể từ đây với lệnh `-p` , chúng ta sec mapping cổng port 5000 với cổng port trong local hót của chúng ta

- `-d` là tùy chọn chạy ở detached mode . đây là lệnh giúp container có thể chạy trong nền

![](https://www.tutorialspoint.com/docker/images/detached_mode.jpg)

**Bước 2** hãy bắt đầu sử dụng `docker ps` để nhìn thấy rawfmg registry container thực sự đang chạy

![](https://www.tutorialspoint.com/docker/images/docker_ps.jpg)

chúng ta cần xác thực rằng registry container đang chạy dưới nền

**Bước 3** - Bây giờ hãy gắn thẻ một image đang tồn tại ,để có thể làm điều này chúng ta có thể push nó tới local repository của chúng ta . Trong ví dụ này chúng ta , khi chúng ta có centos image có sẵn ở địa máy . Chúng ta sẽ tiến tới gắn thẻ nó vào một tà name của centos

    sudo docker tag 67591570dd29 localhost:5000/centos

một điều cần lưu ý trong ví dụ dưới đây

-`67591570dd29` ánh xạ với IDimage cho centos image

- `localhost:5000` cổng port của private repository

![](https://www.tutorialspoint.com/docker/images/private_repository.jpg)

**Bước 4** Bây giờ hãy sử dụng docker push để đẩy repository vào private repository của chúng ta

    sudo docker push localhost:5000/centos

Ở đây , chúng ta đẩy centos image tới private repository lưu trử ở cổng localhost:5000

![](https://www.tutorialspoint.com/docker/images/localhost.jpg)

**Bước 5** Bây giờ hãy bắt đầu xóa local images , chúng ta có cho centos sử dụng với docker rmi commands .Chúng ta có thể downoad để cầu centos image từ private repostory của chúng ta

    sudo docker rmi centos:latest
    sudo docker rmi 67591570dd29

![](https://www.tutorialspoint.com/docker/images/docker_rmi_commands.jpg)

**Bước6** bây giwof chúng ta không có centos images trên máy ảo , bây giwof chúng ta có thểsử dụng docker pull để pull centos image từ private repostory

    sudo docker pull localhost:5000/centos

Bây giờ chúng ta sẽ pull centos image để lưu trử localhost:5000

![](https://www.tutorialspoint.com/docker/images/pulling_centos_image.jpg)

nếu bạn cần nhìn image trong hệ thống , bạn có thể thấy images centos cũng vậy
