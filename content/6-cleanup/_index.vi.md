+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### Xóa S3 bucket

Đi tới [bảng điều khiển quản lý dịch vụ S3](https://s3.console.aws.amazon.com/s3/home)
   + Nhấp vào S3 bucket mà chúng ta đã tạo cho phòng thí nghiệm này. (Ví dụ: ws1-cloudfront)
   + Bấm vào **Empty**.
   + Nhập `permanently delete`, sau đó nhấn **Empty**. để tiến hành xóa đối tượng trong nhóm.
   + Bấm **Exit**.

   + Sau khi xóa hết các đối tượng trong nhóm nhấn **Delete**
![Clean](/ws1-aws-cloudfront/images/6.clean/6-delete-s3-console.png)

   + Nhập tên của S3 bucket, sau đó nhấp vào **Delete bucket** để tiến hành xóa S3 bucket.
![Clean](/ws1-aws-cloudfront/images/6.clean/6.delete-bucket.png)


#### Xóa CloudFront
Đi tới [bảng điều khiển quản lý dịch vụ Amazon CloudFront](https://console.aws.amazon.com/cloudfront/v4/home)
   + Nhấp vào **Distributions** mà chúng ta đã tạo cho phòng thí nghiệm này. (Ví dụ: E2YGKQ4RKCO9LA)
   + Bấm vào **Disable**.
   + Pop-up sẽ hiện ra, bạn nhấn **Disable** để tiến hành tắt.
![Clean](/ws1-aws-cloudfront/images/6.clean/6-cdn-disable.console.png)
   
   + Bấm vào **Distributions**.
   + Bấm vào tab **Behavior**.
   + Bấm vào **Delete**.
![Clean](/ws1-aws-cloudfront/images/6.clean/6-cdn-delete-behavior.png)

   + Bấm vào tab **Policies**.
   + Bấm vào **Custom policies**.
   + Bấm vào **Delete**.
![Clean](/ws1-aws-cloudfront/images/6.clean/6-cnd-delete-cache.png)

   + Bấm vào tab **Origin access**
   + Chọn origin của bạn.
   + Bấm **Delete**.
![Clean](/ws1-aws-cloudfront/images/6.clean/6.cdn-delete-origin.png)

   + Cuối cùng quay lại **Distributions**
   + Chọn distribution của bạn
   + Bấm **Delete**.
![Clean](/ws1-aws-cloudfront/images/6.clean/6-cdn-delete-distribution.png)

Cảm ơn đã xem!!!