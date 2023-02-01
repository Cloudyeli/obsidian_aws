## AWS Webaplication Firewall (WAF)

AWS WAF is a **Web Application [[Firewall]]** that lets you monitor the [[HTTP]]/[[HTTPS]] requests that are forwarded to your protected web application resources. With AWS WAF, you can create security rules that control **[[bot]]** traffic and block common attack patterns such as [[SQL injection]] or cross-site scripting ([[XSS]]).

AWS WAF can be used to protect on-premises resources if they are deployed behind an Application Load Balancer (ALB). In this scenario the on-premises website servers are added to a target group by IP address. The ALB has a WAF WebACL attached to it and distributes connections to the on-premises website.

*   AWS WAF is a web application [[firewall]]
*   Create rules that block common web exploits like [[SQL injection]] and cross site scripting
*   WAF lets you create rules to filter web traffic based on conditions that include IP addresses, [[HTTP]] headers and body, or custom [[URI]]s
*   The rules are known as [[Web ACLs]]

![[Pasted image 20221119201428.png]]

### You can protect the following resource types:

-   Amazon [[CloudFront]] distribution
-   Amazon [[API Gateway]] REST API
-   Application Load Balancer ([[ALB]])
-   AWS [[AppSync]] [[GraphQL]] [[API]]
-   Amazon [[Cognito]] user pool

## WAF vs. [[Shield]]

You can use **AWS WAF web access control lists ([[web ACLs]]) to help minimize the effects of a Distributed Denial of Service ([[DDoS]]) attack**. For additional protection against DDoS attacks, AWS also provides AWS [[Shield]] Standard and AWS [[Shield]] Advanced.


    
AWS WAF also lets you control access to your content. Based on criteria that you specify, such as the IP addresses that requests originate from or the values of query strings, the service associated with your protected resource responds to requests either with the requested content, with an [[HTTP]] 403 [[status code]] (Forbidden), or with a custom response.

Note

You can also use AWS WAF to protect your applications that are hosted in Amazon Elastic Container Service ([[ECS]]) containers. Amazon ECS is a highly scalable, fast container management service that makes it easy to run, stop, and manage [[Docker]] containers on a cluster. To use this option, you configure Amazon ECS to use an Application Load Balancer ([[ALB]]) that is enabled for AWS WAF to route and protect [[HTTP]]/[[HTTPS]] layer 7 traffic across the tasks in your service. For more information, see [Service Load Balancing](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/service-load-balancing.html) in the _Amazon Elastic Container Service Developer Guide_.