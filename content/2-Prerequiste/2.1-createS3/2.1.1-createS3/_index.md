---
title : "Create S3"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1.1 </b> "
---


#### Create S3
1. Go to [S3 service management console](https://console.aws.amazon.com/s3/home)
   + Click **Buckets**.
   + Click **Create bucket**.
![S3](/images/2.prerequisite/2.2.1-S3console.png)

2. At the **Create S3** page.
   Fill information required in “Create bucket” form
   + In the **Bucket name** field, enter `ws1-cloudfront`.
   + In the **Object Ownership** field, choose **ACLs disabled**.
   + Untick **Block all public access**.
   + Tick on warning box to confirm allow public access.
    > I acknowledge that the current settings might result in this bucket and the objects within becoming public
   + Click on **Create bucket** button to create it.
![S3](/images/2.prerequisite/2.1.1-bucketname.png)
![S3](/images/2.prerequisite/2.1.1-untickblock.png)

  
3. Create successfully
![S3](/images/2.prerequisite/2.1.1-createS3sucess.png)