Amazon CloudFront is a content delivery network ([[CDN]]) that allows you to store (cache) your content at “[[edge location]]s” located around the world. 

*   Cache content at [[Edge Location]] for fast distribution to customers.
*   This allows customers to access content more quickly and provides security against [[DDoS]] attacks
*   CloudFront can be used for data, videos, applications, and [[API]]s
*   CloudFront reduces latency for global users
-   Integrates with many AWS services ([[S3]], [[EC2]], [[ELB]], [[Route 53]], [[Lambda]]).

### Origins and Distributions:

-   An origin is the origin of the files that the [[CDN]] will distribute.
-   Origins can be either an [[S3]] bucket, an [[EC2]] instance, an Elastic Load Balancer ([[ELB]]), or [[Route 53]] – can also be external (non-AWS).
-   To distribute content with CloudFront you need to create a distribution.

### CloudFront uses [[Edge Location]]s and Regional [[Edge Cache]]s:

[[Edge location]]s are Content Delivery Network ([[CDN]]) endpoints for CloudFront.

-   An edge location is the location where content is cached (separate to AWS [[region]]s/[[AZ]]s).
-   Requests are automatically routed to the nearest edge location.
-   Regional Edge Caches are located between origin web servers and global edge locations and have a larger cache.
-   Regional Edge caches aim to get content closer to users.

The diagram below shows where Regional Edge Caches and Edge Locations are placed in relation to end users:

![aws-cloudfront-edge-cache](https://digitalcloud.training/wp-content/uploads/2022/02/aws-cloudfront-edge-cache-1.png)

### AWS [[Global Accelerator]] vs CloudFront

| Global Accelerator | CloudFront |
| ------------------- | ------------ |
| Both use the AWS global network and [[edge location]]s | Both use the AWS global network and [[edge location]]s|
|GA improves performance for a wide range of applications over [[TCP]] and UDP| CloudFront improves performance for cacheable content and dynamic content| 
| GA proxies connections to applications in one or more AWS [[Region]]s| |
| GA provides failover between AWS [[Region]]s | |

### AWS CloudFront [[Pricing]]

* ##### Traffic distribution
data transfer and request pricing, varies across [[region]]s, and is based on the [[edge location]] from which the content is served

* ##### Requests
the number and type of requests ([[HTTP]] or [[HTTPS]]) and the geographic [[region]] in which they are made

* ##### Data transfer out
quantity of data transferred out of CloudFront edge locations;
There are additional chargeable items such as invalidation requests, field-level [[encryption]] requests, and custom [[SSL]] certificates