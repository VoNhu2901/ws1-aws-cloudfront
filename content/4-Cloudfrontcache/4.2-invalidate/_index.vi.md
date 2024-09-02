---
title : "Vô hiệu hóa trong CloudFront"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 4.2 </b> "
---

{{% notice note %}}
Vô hiệu hóa nội dung trong CloudFront để buộc xóa đối tượng
{{% /notice %}}

1. Quay lại [Bảng điều khiển quản lý dịch vụ Amazon CloudFront](https://console.aws.amazon.com/cloudfront/v4/home).

2. Chọn bản distribution của bạn và chuyển đến tab **Invalidations**. Tạo một yêu cầu vô hiệu.
![CDN](/images/4.s3/4.1-invalidation-console.png)

3. Tại trang **Create invalidation**:
- Dán:
``` foo
/test.html
/cf-test-image.png
```
- Bấm vào nút "Create invalidation"
![CDN](/images/4.s3/4.1-create-invalidation.png)

Bây giờ hãy cập nhật trang HTML trong nhóm S3. Chúng ta sẽ cập nhật phiên bản html thử nghiệm lên 4. Lưu tệp cục bộ rồi tải lên S3 bucket của bạn.
- Cập nhật file test.html từ 2 lên 4.
![CDN](/images/4.s3/4.1-update-file-v4.png)
- Tải lại tập tin lên S3.
![CDN](/images/4.s3/4.1-reupload-file-s3.png)
- Mở test.html từ URL S3, nội dung phải là phiên bản 4.
![CDN](/images/4.s3/4.1-invalidation-success-s3.png)
- Và nội dung trả về từ CloudFront cũng phải là phiên bản 4.
![CDN](/images/4.s3/4.1-invalidation-success-cdn.png)

{{% notice info %}}
Tóm lại, các cập nhật nội dung hiện được phản ánh ngay lập tức trên S3 và CDN cứ sau 20 giây, thay vì cứ sau 24 giờ.
{{% /notice %}}
