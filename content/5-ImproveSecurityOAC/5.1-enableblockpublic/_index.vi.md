---
title : "Cho phép chặn quyền truy cập công khai"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 5.1 </b> "
---

{{% notice note %}}
Xóa Bucket policy khỏi nhóm S3 và bật chặn quyền truy cập công khai.
{{% /notice %}}

#### Xóa Bucket Policy
1. Truy cập vào [bảng điều khiển quản lý dịch vụ S3](https://console.aws.amazon.com/s3/home)
  + Chọn nhóm của bạn và trong tab  **Permission**
  + Chọn **Bucket Policy**
  + Bấm vào **Delete** để xóa chính sách bucket policy
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-permission-console.png)

{{% notice note %}}
Bucket Policy bây giờ sẽ trống.
{{% /notice %}}
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-deleted-policy.png)

#### Bật Block public access
Chọn Block public access và bật cài đặt Block all public access setting. 
   + Chọn **Edit**.
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-block-public-console.png)

   + Tích vào **Block all public access**.
   + Bấm vào **Save changes**.
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-edit-block.png)
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-blocked-public.png)

#### Kiểm tra trên trình duyệt
Bây giờ nếu bạn cố truy cập trang HTML, bạn sẽ gặp lỗi Truy cập bị từ chối dưới dạng truy cập ẩn danh.
- Thử mở link S3: `https://ws1-cloudfront.s3.amazonaws.com/test.html`
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-cannot-s3.png)

   Thử mở link CDN: `https://d2s62os8tlfgfh.cloudfront.net/test.html`
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-cannot-cdn.png)
