---
title : "Preparing S3"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

In this step, we will need to create an S3 bucket.

#### Introduce
**Amazon Simple Storage Service (S3)** is an object storage service provided by Amazon Web Services (AWS). It allows you to store and retrieve any amount of data from anywhere on the web. Data in S3 is organized into "buckets" and "objects," where an object can be any type of data like text files, images, videos, or backup files.

#### Advantages of Amazon S3:
- **High Scalability:** S3 is designed to automatically scale to handle any amount of data, from a few megabytes to petabytes.

- **High Durability and Availability:** Data in S3 is stored with high durability, as multiple copies are backed up across different geographic regions. AWS guarantees 99.999999999% (11 nines) durability and up to 99.99% availability.

- **Security:** S3 offers various security options such as encryption of data at rest and in transit, along with detailed access control through IAM (Identity and Access Management).

- **Integration with Other AWS Services:** S3 integrates seamlessly with other AWS services like EC2, Lambda, CloudFront, and analytics tools like Athena, making it easy to build complex applications.

- **Cost-Effective:** With a pay-as-you-go pricing model, S3 provides a flexible and cost-efficient storage solution, especially with different storage classes like S3 Standard, S3 Intelligent-Tiering, and S3 Glacier for cold data storage needs.

- **Ease of Management and Use:** S3 offers a web management interface, SDKs, and APIs, making it easy to manage buckets and objects. Users can access, edit, and share data flexibly.

- **Data Resilience:** S3 provides features like versioning, backups, and data recovery, ensuring that data is always protected and can be recovered when needed.


{{% notice info %}}
To learn more about S3, you can refer to the website below described
  - [About Amazon S3](https://aws.amazon.com/vi/s3/)
{{% /notice %}}

### Content
  - [Create S3](2.1.1-createS3/)
  - [Grant read access](2.1.2-grantread/)
  - [Upload file to the bucket](2.1.3-uploadfile/)