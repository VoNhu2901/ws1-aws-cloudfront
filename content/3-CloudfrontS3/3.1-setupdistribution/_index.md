---
title : "Set up a CloudFront Distribution"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1. </b> "
---

1. Go to [Amazon CloudFront service management console](https://console.aws.amazon.com/cloudfront/v4/home).
  + Click on **Distribution**.
  + Click **Create distribution**.

![Distribution](/ws1-aws-cloudfront/images/3.connect/3.1-distribution-console.png)

2. At the **Create distribution** page
  + Click on **Origin domain** to select **S3 bucket**.
  + Leave every as default.
  + Click the **Create distribution**. A distribution will be created afterward.
![Distribution](/ws1-aws-cloudfront/images/3.connect/3.1-select-origin.png)

Created successully!!!
![Distribution](/ws1-aws-cloudfront/images/3.connect/3.1-created-distribution.png)
{{% notice info %}}
It’ll take about 5 to 10 minutes for the distribution to change from in progress to deployed state.
{{% /notice %}}
