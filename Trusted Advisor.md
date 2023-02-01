## AWS Trusted Advisor

AWS Trusted Advisor provides recommendations that help you follow AWS best practices. Trusted Advisor evaluates your account by using checks. These checks identify ways to optimize your AWS infrastructure, improve security and performance, reduce costs, and monitor service quotas. You can then follow the recommendations to optimize your services and resources.

-   Online resource that helps to reduce cost, increase performance and improve security by optimizing your AWS environment
-   Provides real time guidance to help you provision your resources following best practices
-   Advises you on **Cost Optimization**, **Performance**, **Security**, and **Fault Tolerance**

![[Pasted image 20221119143459.png]]

AWS Basic Support and AWS Developer [[Support Plan]] customers can access core security checks and checks for service quotas. AWS Business [[Support Plan]] and AWS Enterprise Support customers can access all checks, including cost optimization, security, fault tolerance, performance, and service quotas. For a complete list of checks and descriptions, see the Trusted Advisor Best Practices.

AWS Trusted Advisor Priority helps you focus on the most important recommendations to optimize your cloud deployments, improve resilience, and address security gaps. Available to AWS Enterprise Support customers, Trusted Advisor Priority provides prioritized and context-driven recommendations that come from your AWS account team as well as machine-generated checks from AWS services.

## Benefits

Checks from Trusted Advisor analyze your AWS environment and recommend actions to follow best practices.

![[Pasted image 20221119142836.png]]

### Cost optimization

Trusted Advisor can help you save cost with actionable recommendations by analyzing usage, configuration and spend. Examples include identifying idle [[RDS]] [[database]] instances, underutilized [[EBS volume]]s, unassociated Elastic addresses ([[ElP]]), and excessive timeouts in [[Lambda]] functions.  

### Performance

Trusted Advisor can help improve the performance of your services with actionable recommendations by analyzing usage and configuration. Examples include analyzing [[EBS]] throughput and latency, compute usage of [[EC2]] instances, and configurations on [[CloudFront]].  

### Security

Trusted Advisor can help improve the security of your AWS environment by suggesting foundational security best practices curated by security experts. Examples include identifying [[RDS]] [[security group]] access risk, exposed access keys, and unnecessary [[S3]] bucket permissions.  

### Fault tolerance

Trusted Advisor can help improve the reliability of your services. Examples include examining [[EC2 Auto scaling]] groups, deleted health checks on [[Route 53]], disabled [[AZ]]s, and disabled [[RDS]] backups.  

### Service quotas

Service quotas are the maximum number of resources that you can create in an AWS account.  AWS implements quotas to provide highly available and reliable service to all customers, and protects you from unintentional spend. Trusted Advisor will notify you once you reach more than 80% of a service quota. You can then follow recommendations to delete resources or request a quota increase.