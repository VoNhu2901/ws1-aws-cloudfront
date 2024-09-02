---
title : "Thiết lập một CloudFront Distribution"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1. </b> "
---

1. Truy cập vào [giao diện quản trị của dịch vụ Amazon CloudFront](https://console.aws.amazon.com/cloudfront/v4/home).
  + Bấm vào **Distribution**.
  + Bấm vào **Create distribution**.

![Distribution](/ws1-aws-cloudfront/images/3.connect/3.1-distribution-console.png)

2. Tại trang **Create distribution**
  + Bấm vào **Origin domain** để chọn **S3 bucket**.
  + Để mặc định mọi thứ.
  + Bấm vào **Create distribution**. Một bản distribution sẽ được tạo ra sau đó.
![Distribution](/ws1-aws-cloudfront/images/3.connect/3.1-select-origin.png)

Đã tạo thành công!!!
![Distribution](/ws1-aws-cloudfront/images/3.connect/3.1-created-distribution.png)
{{% notice info %}}
Sẽ mất khoảng 5 đến 10 phút để quá trình phân phối chuyển từ trạng thái đang tiến hành sang trạng thái đã triển khai.
{{% /notice %}}
