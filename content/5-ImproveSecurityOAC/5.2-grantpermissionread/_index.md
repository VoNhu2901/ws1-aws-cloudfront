---
title : "Grant CloudFront distribution permission to read the S3 origin"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 5.2 </b> "
---

{{% notice note %}}
Delete Bucket policy from the S3 bucket and enable block public access.
{{% /notice %}}

1. Go to [Amazon CloudFront service management console](https://console.aws.amazon.com/cloudfront/v4/home).
  + Click on **Distribution** and click on your distribution.
  + Click on **Origins**.
  + Choose your origin.
  + Click on **Edit**.
![CDN](/images/5.fwd/5.2-origin-console.png)

2. At the **Edit origin** page
  + Select **Origin access control settings (recommended)**.
  + Click on **Create new OAC**. 
![CDN](/images/5.fwd/5.2-edit-origin.png)
  + Create Control setting, enter **Name**: `OAC-VN-S3`.
  + Click on **Create**. 
![CDN](/images/5.fwd/5.2-create-oac.png)
   + Click on **Save changes**.
  
Create successfully!!!
![CDN](/images/5.fwd/5.2-created-origin.png)


Giving CloudFront permission to access the S3 bucket. 
   + Go to CDN, click **Edit** of origin 
   + Click on “Copy policy”.
![CDN](/images/5.fwd/5.2-copy-policy.png)
   + Go to S3 bucket, paste this code to Bucket Policy in S3.
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
![S3](/images/5.fwd/5.2-paste-cdn-s3.png)
   + Click on **Save changes**
  
{{% notice info %}}
Now if we access page from the S3 Object URL, we still cannot access because we only allow access from CloudFront.
{{% /notice %}}
- Try opening link S3: `https://ws1-cloudfront.s3.amazonaws.com/test.html`
![S3](/images/5.fwd/5.2-cannot-s3.png)

{{% notice info %}}
We can access test.html from CloudFront.
{{% /notice %}}
- Try opening link CDN: `https://d2s62os8tlfgfh.cloudfront.net/test.html`
![CDN](/images/5.fwd/5.2-can-cdn.png)