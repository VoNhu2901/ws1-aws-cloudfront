---
title : "Configure cache"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

{{% notice note %}}
Configure how long the content is cached at the browser
{{% /notice %}}

#### Create a Cache Policy

1. Go to [Amazon CloudFront service management console](https://console.aws.amazon.com/cloudfront/v4/home)
  + Click on **Policies**.
  + Click on **Create cache policy**.
![CDN](/images/4.s3/4.1-policy-console.png)

2. At the **Create cache policy** page. Fill the information in the form
  + At the **Name** field, enter `custom-cache`
  + At the **Minimum TTL**, **Maximum TTL**, **Default TTL** enter `2`, `30`, `20`
  + Leave everything as default
  + Click "Create" button 
![CDN](/images/4.s3/4.1-create-policy.png)

#### Create Behavior
1. Back to [Amazon CloudFront service management console](https://console.aws.amazon.com/cloudfront/v4/home).
  + Click on **Distribution**.
  + Click on the **Behavior** tab.
  + Click on **Create behavior**. 
![CDN](/images/4.s3/4.1-behavior-console.png)
 
2. At the **Create behavior** page. Fill the information in the form
  + Click on **Path pattern** enter `*.html`
  + Click on **Origin and origin groups** select ***S3 bucket*** and **Cache key and origin requests** select ***custom-cache***
  + Leave everything as default
  + Click on "Create behavior" button 
![CDN](/images/4.s3/4.1-fill-form.png)
![CDN](/images/4.s3/4.1-create-success.png)

{{% notice info %}}
After 20 seconds, CloudFront will display new content (by default of AWS 24 hours -> change to 20 seconds)
{{% /notice %}}
![CDN](/images/4.s3/4.1-cache-20s.png)
