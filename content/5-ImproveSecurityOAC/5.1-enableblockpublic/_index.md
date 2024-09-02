---
title : "Enable block public access"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 5.1 </b> "
---

{{% notice note %}}
Delete Bucket policy from the S3 bucket and enable block public access.
{{% /notice %}}

#### Delete Bucket Policy
1. Go to [S3 service management console](https://console.aws.amazon.com/s3/home)
  + Select your bucket and in the **Permission** tab
  + Select **Bucket Policy**
  + Click **Delete** to remove the bucket policy   
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-permission-console.png)

{{% notice note %}}
The Bucket Policy should be empty now.
{{% /notice %}}
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-deleted-policy.png)

#### Enable Block public access
Select Block public access and turn on Block all public access setting. 
   + Choose **Edit**.
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-block-public-console.png)

   + Tick on **Block all public access**.
   + Click on **Save changes**.
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-edit-block.png)
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-blocked-public.png)

#### Testing on browser
Now if you try to visit the HTML page, you will get an Access Denied error as anonymous access.
- Try opening link S3: `https://ws1-cloudfront.s3.amazonaws.com/test.html`
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-cannot-s3.png)

- Try opening link CDN: `https://d2s62os8tlfgfh.cloudfront.net/test.html`
![S3](/ws1-aws-cloudfront/images/5.fwd/5.1-cannot-cdn.png)
