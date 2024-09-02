---
title : "Improve Security with OAC"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

With the current set up, the S3 bucket is **public**. So, anybody can directly come and view the content. In this lab, we will:

- Remove anonymous access and allow only request from CloudFront.
- Grant CloudFront distribution permission to read the S3 origin

{{% notice note %}}
Delete Bucket policy from the S3 bucket and block public access.
{{% /notice %}}

### Content:
   - [Enable block public access](5.1-enableblockpublic/)
   - [Grant CloudFront distribution permission to read the S3 origin](5.2-grantpermissionread/)
