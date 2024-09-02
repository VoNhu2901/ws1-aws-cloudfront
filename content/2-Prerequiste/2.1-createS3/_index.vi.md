---
title : "Chuẩn bị S3"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

Trong bước này, chúng ta sẽ cần tạo một S3 bucket.

#### Giới thiệu
**Amazon Simple Storage Service (S3)** là một dịch vụ lưu trữ đối tượng (object storage) của Amazon Web Services (AWS). Nó cho phép bạn lưu trữ và truy xuất bất kỳ lượng dữ liệu nào từ bất kỳ đâu trên web. Dữ liệu trong S3 được tổ chức dưới dạng các "buckets" (thùng) và các "objects" (đối tượng), trong đó một đối tượng có thể là bất kỳ loại dữ liệu nào như tệp văn bản, hình ảnh, video, hoặc các tệp sao lưu.

#### Ưu điểm của Amazon S3:
- **Khả năng mở rộng cao:** S3 được thiết kế để tự động mở rộng để xử lý bất kỳ lượng dữ liệu nào, từ vài megabyte đến hàng petabyte.

- **Độ bền và tính khả dụng cao:** Dữ liệu trong S3 được lưu trữ với độ bền cao, nhờ việc sao lưu nhiều bản sao trên nhiều khu vực địa lý khác nhau. AWS đảm bảo độ bền 99.999999999% (11 chín) và tính khả dụng lên đến 99.99%.

- **Bảo mật:** S3 cung cấp nhiều tùy chọn bảo mật như mã hóa dữ liệu trong khi lưu trữ (encryption at rest) và mã hóa khi truyền tải (encryption in transit), cùng với kiểm soát truy cập chi tiết thông qua IAM (Identity and Access Management).

- **Tích hợp với các dịch vụ AWS khác:** S3 tích hợp mạnh mẽ với các dịch vụ AWS khác như EC2, Lambda, CloudFront, và các công cụ phân tích dữ liệu như Athena, giúp dễ dàng xây dựng các ứng dụng phức tạp.

- **Tính kinh tế:** Với mô hình thanh toán theo lượng sử dụng (pay-as-you-go), S3 là một giải pháp lưu trữ có chi phí linh hoạt và hiệu quả, đặc biệt với các lớp lưu trữ khác nhau như S3 Standard, S3 Intelligent-Tiering, S3 Glacier cho các nhu cầu lưu trữ dữ liệu lạnh (cold data).

- **Dễ dàng quản lý và sử dụng:** S3 cung cấp giao diện quản lý web, SDK và API giúp dễ dàng quản lý các bucket và objects. Người dùng có thể truy cập, chỉnh sửa, và chia sẻ dữ liệu một cách linh hoạt.

- **Khả năng phục hồi dữ liệu:** S3 cung cấp các tính năng như phiên bản hoá (versioning), sao lưu và khôi phục dữ liệu, đảm bảo dữ liệu luôn được bảo vệ và có thể phục hồi nếu cần.


{{% notice info %}}
Để tìm hiểu thêm về S3, bạn có thể tham khảo trang web bên dưới mô tả
  - [Giới thiệu về Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/create-bucket-overview.html)
{{% /notice %}}

### Nội dung
  - [Tạo S3](2.1.1-createS3/)
  - [Cấp quyền truy cập đọc](2.1.2-grantread/)
  - [Tải tệp lên bucket](2.1.3-uploadfile/)
