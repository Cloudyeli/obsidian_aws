## Elastic Beanstalk

AWS Elastic Beanstalk is the fastest and simplest way to get web applications up and running on AWS.

Developers simply upload their application code, and the service automatically handles all the details such as resource provisioning, load balancing ([[ELB]]), [[Auto Scaling]], and monitoring.

Elastic Beanstalk is ideal if you have a PHP, Java, [[Python]], Ruby, Node.js, .NET, Go, or [[Docker]] web application.

Elastic Beanstalk uses core AWS services such as Amazon [[EC2]], Amazon Elastic Container Service ([[ECS]]), [[Auto Scaling]], and Elastic Load Balancing ([[ELB]]) to easily support applications that need to scale to serve millions of users.

-   Managed service for web applications on Amazon [[EC2]] instances and [[Docker]] containers
-   Deploys an environment that can include [[Auto Scaling]], Elastic Load Balancing ([[ELB]]) and databases
-   Considered a Platform as a Service ([[PaaS]]) solution
-   Allows full control of the underlying resources
-   Code is deployed using a ZIP file, WAR file or Git repository

![aws-elastic-beanstalk-application](https://digitalcloud.training/wp-content/uploads/2022/02/aws-elastic-beanstalk-application-1.png)

### Difference between CloudFormation and Elastic Beanstalk

| [[CloudFormation]] | Elastic Beanstalk |
| ------------ | -------------- |
| “Template-driven provisioning” | “Web apps made easy" |
| Deploys infrastructure using code | Deploys applications on [[EC2]] ([[PaaS]])
| Can be used to deploy almost any AWS service | Deploys web applications based on Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker
| Uses [[JSON]] or [[YAML]] template files  | Uses ZIP or WAR files (or Git)
| Similar to [[Terraform]]  | Similar to Google App Engine
