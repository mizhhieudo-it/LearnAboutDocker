# Docker File

trong những chương trướ , chúng ta có những cái nhìn về nhiều các images file như là Centos , cài mà được tải xuống từ Docker hub từ cái mà bạn có thể tạo nên các conatiner . Với ví dụ này là lại lại từ ví dụ trên

![description](https://www.tutorialspoint.com/docker/images/docker_file.jpg)

Nếu chúng ta sử dụng lệnh Docker images , chúng ta có thể thấy các tồn tại của images trong hệ thống của chúng ta . Từ các ví dụ chụp màn hình , chúng ta có thấy rằng có 2 images là centos và nsenter .

Nhưng Docker cũng giữ bạn khả năng để tạo cho chúng ta images riêng , và nó có thể hoàn thành với sự giúp đỡ của docker file . Một Docker file là đơn giản của những đoạn text với hướng dẫn làm sao để tạo những images của riêng mình

**Bước 1** Các bước dưới đây gọi là docker file và chỉnh sửa sử dụng `vim` . Làm ơn lưu lại điều này với tên của file phải có "Dockerfile" với "D" viết hoa .

![Description](https://www.tutorialspoint.com/docker/images/edit_vim.jpg)

**Bước 2** Xây dựng một File Docker sử dụng hướng dẫn sau

```
#This is a sample Image
FROM ubuntu
MAINTAINER demousr@gmail.com

RUN apt-get update
RUN apt-get install –y nginx
CMD [“echo”,”Image created”]
```

Các điểm cần để lưu ý về file trên

- Với dòng đầu tiên "#This is a sample Image" là một comment . Bạn có thể thêm comment với docker file với sự trợ giúp của lệnh `#`

- Với dòng tiếp theo sử bắt đầu bằng key word FROM . nó nói docker , bạn muốn xây dựng images của mình từ image có sẵn nào . trong ví dụ trên , chúng ta đang tạo images của chúng ta từ image ubuntu

- Phần tiếp theo là người tạo , ai là người duy trì cái hình ảnh này . ở đây bạn chỉ ra `MAINTAINER` keyword và chỉ ra đề cập để emailID

- lệnh **RUN** là sử dụng lại hướng dẫn của image , Trong ví dụ này , trước tiên chúng ta cập nhật hệ thống Ubuntu của mình và sau đó cài đặt máy chủ nginx trên image ubuntu của mình

- lệnh cuối cùng được sử dụng để trả về một message

![description](https://www.tutorialspoint.com/docker/images/build_the_image.jpg)
