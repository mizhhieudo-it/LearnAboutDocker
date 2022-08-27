# Docker - Architeture

Hình ảnh dưới đây hiển thị một chuẩn và kiến trúc truyền thông của việc ảo hóa

![descriprion-architeture](https://www.tutorialspoint.com/docker/images/virtualization.jpg)

- `Server` là một server vật lý , nó sử được sử dụng để lưu trữ nhiều máy ảo
- `Host OS` là máy cơ sơ như là linux hoặc windows
- `Hypervisor` là một trong hai VMWare hoặc Windows Hyper V, điều này được sử để lưu chữ máy ảo
- sau đó bán sẽ cài nhiều hệ điều hành với máy ảo trên cùng `hypervisor` như hệ điều hành máy khách
- Sau đó bạn sẽ lưu trữ ứng dựng của mình trên đầu mỗi `Gusest OS`

Hình ản sau trình bày về thế hệ mới của máy chủ ảo hóa . Điều đó được kích hoạt thông qua Docker . Hãy bắt đầu có một cái nhìn với các tầng khác nhau
![architechture](https://www.tutorialspoint.com/docker/images/various_layers.jpg)

- máy chủ là Server vật lý được sử dụng để quản lý nhiều máy ảo . Vì vậy tầng này sẽ giống với tầng `server` trong đoạn mô tả trước .
- `The Host OS` được xây dựng trên hệ điều hành như là Linux hoặc windows . Tầng này cũng sẽ giống với tầng trước
- Bây giờ hãy tiến tới một thế hệ mới , cái mà được gọi là Docker engine . Điều này được sử dụng để chạy các hệ điều hành , các mà trước đây từng là máy ảo dưới dạng Doker containers
- Tất cả các ứng dụng sẽ chạy dưới dạng Docker containers
  Thuận lợi trong kiến trúc này là bạn không cần phải có thêm phần cứng cho hệ điều hành khách . Mọi thức hoạt động như vùng chứa Docker
