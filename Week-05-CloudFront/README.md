# Week 5 - Amazon CloudFront

## Overview

Amazon CloudFront is a Content Delivery Network (CDN) service that securely delivers data, videos, applications, and APIs to users worldwide with low latency and high transfer speeds. It caches content at AWS Edge Locations to improve performance and reduce the load on the origin server.

CloudFront works seamlessly with AWS services such as Amazon S3, EC2, Elastic Load Balancer, and API Gateway.

---

## Key Features

- Global Content Delivery Network (CDN)
- Low latency and high performance
- Global Edge Locations
- HTTPS support with SSL/TLS
- Integration with Amazon S3 and EC2
- Cache Invalidation
- Improved security with AWS Shield and AWS WAF

---

## Common Use Cases

- Static website hosting
- Video streaming
- API acceleration
- Software distribution
- Content caching
- Media delivery

---

## Hands-on Labs

### Lab 1: Create a CloudFront Distribution

#### Steps Performed

1. Opened the AWS Management Console.
2. Navigated to **Amazon CloudFront**.
3. Clicked **Create Distribution**.
4. Selected the Amazon S3 bucket as the origin.
5. Accepted the default settings.
6. Created the distribution.
7. Waited for the distribution status to change to **Deployed**.

---

### Lab 2: Access the Website

#### Steps Performed

1. Copied the CloudFront Distribution Domain Name.
2. Opened the URL in a web browser.
3. Verified that the website was accessible through CloudFront.

---

### Lab 3: Cache Invalidation

#### Steps Performed

1. Updated the **index.html** file.
2. Uploaded the updated file to the Amazon S3 bucket.
3. Accessed the CloudFront URL and observed the cached content.
4. Navigated to **Invalidations**.
5. Created an invalidation using:

```
/*
```

6. Waited for the invalidation to complete.
7. Refreshed the CloudFront URL and verified the updated content.

---

## Outcome

Successfully:

- Created an Amazon CloudFront distribution.
- Connected an Amazon S3 bucket as the origin.
- Accessed the website using the CloudFront URL.
- Performed cache invalidation.
- Verified that the updated website content was delivered.

---

## Skills Gained

- Understanding Content Delivery Networks (CDNs).
- Configuring CloudFront distributions.
- Integrating CloudFront with Amazon S3.
- Managing cached content using invalidations.
- Improving website performance and availability.

---

## AWS Services Used

- Amazon CloudFront
- Amazon S3

---

## Key Takeaways

- Amazon CloudFront is a global Content Delivery Network (CDN).
- CloudFront caches content at Edge Locations to reduce latency.
- Amazon S3 can be used as an origin for CloudFront distributions.
- Cache invalidation ensures users receive the latest content after updates.
- CloudFront improves application performance, scalability, and user experience.
