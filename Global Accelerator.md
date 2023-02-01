## AWS Global Accelerator

AWS Global Accelerator is a networking service that **helps you improve the availability, performance, and security of your public applications**.

*   User traffic ingresses using the closest [[Edge Location]]
*   Routes connections to application endpoints ([[EC2]]/[[ELB]]) in multiple [[Region]]s
-   Improves the availability and performance of applications with local or global users
-   Uses the AWS global network to optimize the path from users to applications, improving the performance of [[TCP]] and UDP traffic 
- 
![[Pasted image 20221118120408.png]]

### AWS Global Accelerator vs [[CloudFront]]

| Global Accelerator | CloudFront |
| ------------------- | ------------ |
| Both use the AWS global network and [[edge location]]s | Both use the AWS global network and [[edge location]]s|
|GA improves performance for a wide range of applications over [[TCP]] and UDP| CloudFront improves performance for cacheable content and dynamic content| 
| GA proxies connections to applications in one or more AWS [[Region]]s| |
| GA provides failover between AWS [[Region]]s | |
