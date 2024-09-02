---
title : "Cấu hình bộ đệm"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

{{% notice note %}}
Định cấu hình thời gian lưu trữ nội dung ở trình duyệt
{{% /notice %}}

#### Tạo một Cache Policy

1. Truy cập vào [giao diện quản trị dịch vụ Amazon CloudFront](https://console.aws.amazon.com/cloudfront/v4/home)
  + Bấm vào **Policies**.
  + Bấm vào **Create cache policy**.
![CDN](/ws1-aws-cloudfront/images/4.s3/4.1-policy-console.png)

2. Tại trang **Create cache policy**. Điền thông tin vào mẫu
  + Tại trường **Name** nhập `custom-cache`
  + Tại **Minimum TTL**, **Maximum TTL**, **Default TTL** nhập `2`, `30`, `20`
  + Để mọi thứ như mặc định
  + Nhấn nút "Create" 
![CDN](/ws1-aws-cloudfront/images/4.s3/4.1-create-policy.png)

#### Tạo Behavior
1. Quay lại [Bảng điều khiển quản lý dịch vụ Amazon CloudFront](https://console.aws.amazon.com/cloudfront/v4/home).
  + Bấm vào **Distribution**.
  + Bấm vào tab **Behavior**.
  + Bấm vào **Create behavior**. 
![CDN](/ws1-aws-cloudfront/images/4.s3/4.1-behavior-console.png)
 
2. Tại trang **Create behavior**. Điền thông tin vào mẫu
  + Click vào **Path pattern** nhập `*.html`.
  + Nhấp vào **Origin and origin groups** chọn ***S3 bucket*** và **Cache key and origin requests** chọn ***custom-cache***.
  + Để mọi thứ như mặc định.
  + Bấm vào nút "Create behavior". 
![CDN](/ws1-aws-cloudfront/images/4.s3/4.1-fill-form.png)
![CDN](/ws1-aws-cloudfront/images/4.s3/4.1-create-success.png)

{{% notice info %}}
Sau 20 giây, CloudFront sẽ hiển thị nội dung mới (theo mặc định của AWS là 24 giờ -> đổi thành 20 giây)
{{% /notice %}}
![CDN](/ws1-aws-cloudfront/images/4.s3/4.1-cache-20s.png)
