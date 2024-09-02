---
title : "Grant read access"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.1.2 </b> "
---

#### Grant read access to everyone

1. Click on Bucket
  + Click on the previous **ws1-cloudfront** bucket.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-selects3.png)

2. At the **ws1-cloudfront** page
  + Choose **Permissions** tab.
  + Scroll to **Bucket policy** and choose "Edit" button.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-select-edit.png)

3. At the **Edit bucket policy** page
  - Copy Bucket ARN to paste on Generator
  - Click **Policy generator** to generate a policy.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-copy-arn.png)

1. At the **AWS Policy Generator** page
  + Fill the information in the form as below.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-generate-policy.png)
  + Choose "Generate" button then will display a pop-up with policy and copy them.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-copy-policy.png)

{{% notice note %}}
Add a more statement `arn:aws:s3:::ws1-cloudfront/*` on script as below
{{% /notice %}}

```json
{
  "Id": "Policy1725252919233",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Stmt1725252905058",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket"
      ],
      "Effect": "Allow",
      "Resource": [
        "arn:aws:s3:::ws1-cloudfront",
        "arn:aws:s3:::ws1-cloudfront/*"
      ],
      "Principal": "*"
    }
  ]
}
```

5. Back to the **Edit bucket policy** page
  + Paste that policy
  + Click **Save changes** to save information.
![S3](/ws1-aws-cloudfront/images/2.prerequisite/2.1.2-paste-policy.png)
