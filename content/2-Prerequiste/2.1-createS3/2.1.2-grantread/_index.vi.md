---
title : "Cấp quyền truy cập đọc"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.1.2 </b> "
---

#### Cấp quyền truy cập đọc cho mọi người

1. Nhấp vào Bucket
  + Nhấp vào **ws1-cloudfront** bucket đã tạo trước đó.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-selects3.png)

2. Tại trang **ws1-cloudfront**
  + Chọn tab **Permissions**.
  + Cuộn đến **Bucket policy** và chọn nút "Edit".
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-select-edit.png)

3. Tại trang **Edit bucket policy**
  - Copy Bucket ARN để dán vào Generator
  - Nhấp vào **Policy generator** để tạo chính sách.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-copy-arn.png)

1. Tại trang **AWS Policy Generator**
  + Điền thông tin vào biểu mẫu như bên dưới.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-generate-policy.png)
  + Chọn nút "Generate" sau đó sẽ hiển thị một cửa sổ bật lên có chính sách và sao chép chúng.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-copy-policy.png)

{{% notice note %}}
Thêm một câu lệnh khác `arn:aws:s3:::ws1-cloudfront/*` trên tập lệnh như bên dưới
{{% /notice %}}

```json
{
  "Id": "Policy1725252919233",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Stmt1725252905058",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket"
      ],
      "Effect": "Allow",
      "Resource": [
        "arn:aws:s3:::ws1-cloudfront",
        "arn:aws:s3:::ws1-cloudfront/*"
      ],
      "Principal": "*"
    }
  ]
}
```

5. Quay lại trang **Edit bucket policy**
  + Dán chính sách đó
  + Bấm vào **Save changes** để lưu thông tin.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-paste-policy.png)
