# Docker - Building Files

Chúng ta đã tạo Docker file ở phần trước . Bây giờ hãy xây dựng docker file . Docker file có thể xây dụng với với lệnh sau

    docker build

hãy bắt đầu tìm hiểu nhiều hơn về nó

## Docker build

Đây là phương thức cho phé sử dụng user để xây dựng docker image của riêng chúng ta

### cú pháp

    docker build -t ImageName:TagName dir

### tùy chọn

- -t là đề cập tới tag của image
- ImageName - Đây là tên mà bạn muốn đặt cho docker image
- TagName(version) - Đây là tag mà bạn muốn đặt cho image của bạn
- Dir - Thư mục nơi chứa docker file hiện nay

### Giá trị trả về

không

### Ví dụ :

sudo docker build -t myimage:0.1.

ở đây , `myimage` là tên chúng ta đặt cho image và 0.1 là số thẻ mà chúng ta muốn đặt cho image

docker file đang hoạt động ở thư mục hiện tại , chúng ta sử dụng "." tại kết thúc của dang lệnh để biểu thị file đang ở trong thư mục hiện .

### Giá trị trả về

Từ kết quả trả về , bạn sẽ nhìn thấy rằng Ubuntu image sẽ được tải xuống từ docker hub , bởi vì đó là image không có sẵn tại máy

![description](https://www.tutorialspoint.com/docker/images/no_image.jpg)

Mặc định khi build hoàn thành , tất cả lệnh cần thiết sẽ có run trong trên image

![description](https://www.tutorialspoint.com/docker/images/commands_run_over_image.jpg)

bạn sẽ nhìn thấy thông báo hoàn thành và id của new image . Khi bạn chạy Docker images command . Sau đó bạn sẽ có thể nhìn thấy cái image mới

![](https://www.tutorialspoint.com/docker/images/built_message_id.jpg)

hiện tại bạn có thể xây dựng một containers mới từ Image
