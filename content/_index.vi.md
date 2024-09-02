---
title : "CloudFront"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# Làm việc với CloudFront

### Tổng quan

 Trong bài thực hành này, bạn sẽ học các kiến thức cơ bản và thực hành về CloudFront.
- Triển khai một CloudFront sử dụng S3 bucket làm Origin với thời gian TTL mặc định.
- Cấu hình thời gian lưu trữ nội dung tại edge bằng cách tạo Chính sách Cache và Hành vi tùy chỉnh.
- Cấp quyền cho CloudFront distribution để đọc Origin S3 bảo mật bằng cách sử dụng Origin Access Control (OAC).

### Nội dung

 1. [Giới thiệu](1-introduce/)
 2. [Các bước chuẩn bị](2-Prerequiste/)
 3. [CloudFront Distribution với S3 Origin](3-CloudfrontS3/)
 4. [Cấu hình và vô hiệu hóa bộ nhớ đệm CloudFront](4-Cloudfrontcache/)
 5. [Cải thiện bảo mật với OAC](5-ImproveSecurityOAC/)
 6. [Dọn dẹp tài nguyên](6-cleanup/)
