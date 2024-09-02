---
title : "Cấp quyền CloudFront Distribution để đọc S3 origin"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 5.2 </b> "
---

{{% notice note %}}
Xóa Bucket policy khỏi nhóm S3 và bật chặn quyền truy cập công khai.
{{% /notice %}}

1. Truy cập [bảng điều khiển quản lý dịch vụ Amazon CloudFront](https://console.aws.amazon.com/cloudfront/v4/home).
  + Nhấp vào **Distribution** và nhấp vào distribution của bạn.
  + Bấm vào **Origins**.
  + Chọn origin của bạn.
  + Bấm vào **Edit**.
![CDN](/ws1-aws-cloudfront/images/5.fwd/5.2-origin-console.png)

1. Tại trang **Edit origin**
  + Chọn **Origin access control settings (recommended)**.
  + Bấm vào **Create new OAC**.
![CDN](/ws1-aws-cloudfront/images/5.fwd/5.2-edit-origin.png)
  + Tạo cài đặt Control, nhập **Name**: `OAC-VN-S3`.
  + Bấm vào **Create**. 
![CDN](/ws1-aws-cloudfront/images/5.fwd/5.2-create-oac.png)
   + Bấm vào **Save changes**.
  
Tạo thành công!!!
![CDN](/ws1-aws-cloudfront/images/5.fwd/5.2-created-origin.png)


Cấp cho CloudFront quyền truy cập vào S3 bucket. 
   + Truy cập CDN click **Edit** origin. 
   + Click vào “Chính sách sao chép”.
![CDN](/ws1-aws-cloudfront/images/5.fwd/5.2-copy-policy.png)
   + Truy cập S3 Bucket, dán đoạn code này vào Bucket Policy trong S3.
```json
{
   "Version": "2008-10-17",
        "Id": "PolicyForCloudFrontPrivateContent",
        "Statement": [
           {
              "Sid": "AllowCloudFrontServicePrincipal",
                "Effect": "Allow",
                "Principal": {
                   "Service": "cloudfront.amazonaws.com"
                },
                "Action": "s3:GetObject",
                "Resource": "arn:aws:s3:::ws1-cloudfront/*",
                "Condition": {
                   "StringEquals": {
                      "AWS:SourceArn": "arn:aws:cloudfront::905418478295:distribution/E2YGKQ4RKCO9LA"
                    }
                }
            }
        ]
      }
```
![S3](/ws1-aws-cloudfront/images/5.fwd/5.2-paste-cdn-s3.png)
   + Bấm vào **Save changes**
  
{{% notice info %}}
Bây giờ nếu chúng ta truy cập trang từ URL đối tượng S3, chúng ta vẫn không thể truy cập vì chúng ta chỉ cho phép truy cập từ CloudFront.
{{% /notice %}}
- Thử mở link S3: `https://ws1-cloudfront.s3.amazonaws.com/test.html`
![S3](/ws1-aws-cloudfront/images/5.fwd/5.2-cannot-s3.png)

{{% notice info %}}
Chúng ta có thể truy cập test.html từ CloudFront.
{{% /notice %}}
- Thử mở link CDN: `https://d2s62os8tlfgfh.cloudfront.net/test.html`
![CDN](/ws1-aws-cloudfront/images/5.fwd/5.2-can-cdn.png)