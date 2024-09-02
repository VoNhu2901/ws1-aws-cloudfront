---
title : "Invalidate in CloudFront"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

{{% notice note %}}
Invalidate the content in CloudFront to force the removal of objects
{{% /notice %}}

1. Back to [Amazon CloudFront service management console](https://console.aws.amazon.com/cloudfront/v4/home).

2. Select your distribution and go to **Invalidations** tab. Create an invalidation request.
![CDN](/images/4.s3/4.1-invalidation-console.png)

3. At the **Create invalidation** page:
- Paste:
```foo
/test.html
/cf-test-image.png
```
- Click on "Create invalidation" button
![CDN](/images/4.s3/4.1-create-invalidation.png)

Now let’s update the HTML page in the S3 bucket. We are going to update the test html version to 4. Save the file locally and then upload to your S3 bucket.
- Update file test.html from 2 to 4.
![CDN](/images/4.s3/4.1-update-file-v4.png)
- Reupload file to S3.
![CDN](/images/4.s3/4.1-reupload-file-s3.png)
- Open test.html from S3 URL, the content should be version 4.
![CDN](/images/4.s3/4.1-invalidation-success-s3.png)
- And the content in return from CloudFront should be version 4 as well.
![CDN](/images/4.s3/4.1-invalidation-success-cdn.png)

{{% notice info %}}
To summarize, content updates are now reflected immediately on S3 and the CDN every 20 seconds, rather than every 24 hours.
{{% /notice %}}
