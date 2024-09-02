---
title : "Thử nghiệm"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 3.2. </b> "
---
#### Thử nghiệm
Trong tab Chung, bạn có thể xem tên miền của bản phân phối. Khi bạn truy cập miền này, yêu cầu của bạn sẽ được chuyển đến vị trí biên gần nhất. Và nếu nội dung không có trong bộ đệm cạnh hoặc bộ đệm khu vực, thì nội dung đó sẽ được chuyển tiếp đến origin, trường hợp này là bộ chứa S3 của chúng ta.
- Sao chép url + test.html
![Testing](/ws1-aws-cloudfront/images/3.connect/3.2-copy-url.png) 
- Thử mở link: `https://d2s62os8tlfgfh.cloudfront.net/test.html`

{{% notice info %}}
Phản hồi được lưu trữ ở vị trí biên để phục vụ các yêu cầu khác.
{{% /notice %}}
![Testing](/ws1-aws-cloudfront/images/3.connect/3.2-browser.png) 

#### Cập nhật HTML
1. Bây giờ hãy cập nhật trang HTML trong nhóm S3. Chúng ta sẽ cập nhật phiên bản html thử nghiệm lên 2. Lưu tệp cục bộ rồi tải lên vùng lưu trữ S3 của bạn.
- Cập nhật đối tượng HTML lên nhóm S3 (phiên bản 3 -> phiên bản 2)
![Testing](/ws1-aws-cloudfront/images/3.connect/3.2-update-file.png)

2. Bây giờ, nếu bạn mở trang bằng URL bộ chứa S3 trong tab trình duyệt khác, nó sẽ hiển thị phiên bản thứ hai của trang. Điều này là do nội dung được lấy trực tiếp từ S3
- Tải lại test.html lên nhóm **ws1-cloudfront**
- Mở test.html bằng URL S3 Object:
![Testing](/ws1-aws-cloudfront/images/3.connect/3.2-open-test-s3.png)
![Testing](/ws1-aws-cloudfront/images/3.connect/3.2-testing-s3-v2.png)

3. Mặt khác, nếu bạn làm mới trang CloudFront trong trình duyệt mà chúng ta đã mở trước đó, nó sẽ hiển thị nội dung được lưu trong bộ nhớ đệm, đây là phiên bản 3. Nội dung được sử dụng lại từ bộ nhớ đệm hết hạn cho trang và hình ảnh này.
{{% notice info %}}
Theo mặc định, CloudFront lưu trữ các đối tượng S3 trong **24 giờ**
{{% /notice %}}
- Mở test.html bằng CloudFront
{{% notice warning %}}
nó hiển thị nội dung được lưu trong bộ nhớ cache (nội dung không được cập nhật)
{{% /notice %}}
![Testing](/ws1-aws-cloudfront/images/3.connect/3.2-not-updated-v2.png)


### Lưu ý:
Trong phòng thí nghiệm này, chúng ta đã thiết lập bộ chứa S3 làm origin và chúng ta đã định cấu hình bản  CloudFront Distribution.

Có hai vấn đề mà chúng ta đã xác định với thiết lập này.

+ Nhóm S3 ở chế độ công khai.
+ Nội dung được lưu trữ trong **24 giờ**.

Hãy xem việc kiểm soát thời lượng bộ nhớ đệm trong bài thực hành tiếp theo!