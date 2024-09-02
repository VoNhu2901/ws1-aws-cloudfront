---
title : "Tạo S3 "
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1.1 </b> "
---


#### Tạo S3
1. Truy cập [giao diện quản trị dịch vụ S3](https://console.aws.amazon.com/s3/home)
  + Chọn **Buckets**.
  + Chọn **Create bucket**.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.2.1-S3console.png)

2. Tại trang **Create S3**.
  Điền thông tin cần thiết vào biểu mẫu "Create bucket"
  + Trong trường **Bucket name**, nhập `ws1-cloudfront`.
  + Trong trường **Object Ownership**, chọn **ACLs disabled**.
  + Bỏ chọn **Block all public access**.
  + Đánh dấu vào ô cảnh báo để xác nhận cho phép truy cập công khai.
  > I acknowledge that the current settings might result in this bucket and the objects within becoming public
  + Nhấp vào nút **Create bucket** để tạo nó.

![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.1-bucketname.png)
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.1-untickblock.png)

  
1. Tạo thành công
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.1-createS3sucess.png)
