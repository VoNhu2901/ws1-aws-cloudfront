---
title : "Cải thiện bảo mật với OAC"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

Với thiết lập hiện tại, S3 bucket là **công khai**. Vì vậy, bất cứ ai cũng có thể trực tiếp đến xem nội dung. Trong phòng thử nghiệm này, chúng ta sẽ:

- Xóa quyền truy cập ẩn danh và chỉ cho phép yêu cầu từ CloudFront.
- Cấp quyền CloudFront Distribution để đọc S3 origin

{{% notice note %}}
Xóa Bucket policy khỏi nhóm S3 và chặn quyền truy cập công khai.
{{% /notice %}}

### Nội dung:
   - [Cho phép chặn quyền truy cập công khai](5.1-enableblockpublic/)
   - [Cấp quyền CloudFront Distribution để đọc S3 origin](5.2-grantpermissionread/)
