---
title : "Testing"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2. </b> "
---
#### Testing
In the General tab, you can view the domain name for the distribution. When you access this domain, your request is routed to the nearest edge location. And if the content is not in the edge cache or regional cache, it is forwarded to origin which is this case is our S3 bucket.
- Copy url + test.html
![Testing](/images/3.connect/3.2-copy-url.png) 
- Try open link: `https://d2s62os8tlfgfh.cloudfront.net/test.html`

{{% notice info %}}
The response is cached at the edge location for serving other requests.
{{% /notice %}}
![Testing](/images/3.connect/3.2-browser.png) 

#### Update HTML
1. Now let’s update the HTML page in the S3 bucket. We are going to update the test html version to 2. Save the file locally and then upload to your S3 bucket.
- Update the HTML object to S3 bucket (version 3 -> version 2)
![Testing](/images/3.connect/3.2-update-file.png)

2. Now if you open the page using S3 bucket URL in a different browser tab, it renders the second version of the page. This is because the content is getting directly from S3
- Reupload test.html to **ws1-cloudfront** bucket
- Open test.html by S3 Object URL:
![Testing](/images/3.connect/3.2-open-test-s3.png)
![Testing](/images/3.connect/3.2-testing-s3-v2.png)

3. On the other hand, if you refresh the CloudFront page in the browser we opened it before, it renders the cached content, which is version 3. The content is reused from cache expires for this page and image.
{{% notice info %}}
By default, CloudFront caches S3 objects for **24 hours**
{{% /notice %}}
- Open test.html by CloudFront
{{% notice warning %}}
it renders the cached content (content was not updated)
{{% /notice %}}
![Testing](/images/3.connect/3.2-not-updated-v2.png)


### Notes:
In this lab, we set up an S3 bucket as an origin and we configured a CloudFront distribution.

There are two issues that we identified with this setup.

+ The S3 bucket is public.
+ Content is cached for **24 hours**.

Look at controlling the cache duration in next lab!