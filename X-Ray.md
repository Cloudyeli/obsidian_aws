## AWS X-Ray

AWS X-Ray is a service that **helps developers analyze and debug distributed applications**. Customers use X-Ray to monitor application traces, including the performance of calls to other downstream components or services, in either cloud-hosted applications or from their own machines during development.

![[Pasted image 20221118175036.png]]

AWS X-Ray provides a complete view of requests as they travel through your application and filters visual data across payloads, functions, traces, services, APIs, and more with no-code and low-code motions.

*   AWS X-Ray helps developers analyze and debug production, distributed applications, such as those built using a [[microservice]]s architecture.
*    Need to integrate the X-Ray [[SDK]] with your application and install the X-Ray agent
* AWS X-Ray supports applications running on:
	-   Amazon [[EC2]]
	-   Amazon [[ECS]]  
	-   AWS [[Lambda]]   
	-   AWS Elastic [[Beanstalk]]

![Diagram illustrating how AWS X-Ray collects, records, and maps traces to help users analyze issues.](https://d1.awsstatic.com/Product-Page-Diagram_AWS-X-Ray.6fd8b61bc76bd93741fc209c2afc194b494bff9a.png)

-   With X-Ray, you can understand how your application and its underlying services are performing to identify and troubleshoot the root cause of performance issues and errors.
-   X-Ray provides an end-to-end view of requests as they travel through your application and shows a map of your application’s underlying components.
-   You can use X-Ray to analyze both applications in development and in production, from simple three-[[tier]] applications to complex microservices applications consisting of thousands of service.
