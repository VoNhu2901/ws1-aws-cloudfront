+++
title = "Clean up resources"
date = 2022
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

We will take the following steps to delete the resources we created in this exercise.

#### Delete S3 bucket
Go to [S3 service management console](https://s3.console.aws.amazon.com/s3/home)
   + Click on the S3 bucket we created for this lab. (Example: ws1-cloudfront)
   + Click **Empty**.
   + Enter `permanently delete`, then click **Empty** to proceed to delete the object in the bucket.
   + Click **Exit**.

   + After deleting all objects in the bucket, click **Delete**
![Clean](/ws1-aws-cloudfront/images/6.clean/6-delete-s3-console.png)

   + Enter the name of the S3 bucket, then click **Delete bucket** to proceed with deleting the S3 bucket.
![Clean](/ws1-aws-cloudfront/images/6.clean/6.delete-bucket.png)


#### Delete CloudFront
Go to [Amazon CloudFront service management console](https://console.aws.amazon.com/cloudfront/v4/home)
   + Click on the **Distributions** we created for this lab. (Example: E2YGKQ4RKCO9LA)
   + Click **Disable**.
   + Pop-up will displayed, then click **Disable** to proceed to disable it.
![Clean](/ws1-aws-cloudfront/images/6.clean/6-cdn-disable.console.png)
   
   + Click on **Distributions**.
   + Click **Behavior** tab.
   + Click **Delete**.
![Clean](/ws1-aws-cloudfront/images/6.clean/6-cdn-delete-behavior.png)

   + Click on **Policies** tab.
   + Click **Custom policies**.
   + Click **Delete**.
![Clean](/ws1-aws-cloudfront/images/6.clean/6-cnd-delete-cache.png)

   + Click on **Origin access** tab.
   + Select your origin.
   + Click **Delete**.
![Clean](/ws1-aws-cloudfront/images/6.clean/6.cdn-delete-origin.png)

   + Finally, back to **Distributions**
   + Select your distribution
   + Click **Delete**.
![Clean](/ws1-aws-cloudfront/images/6.clean/6-cdn-delete-distribution.png)

Thanks for watching!!!