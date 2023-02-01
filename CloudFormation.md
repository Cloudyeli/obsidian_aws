## AWS CloudFormation

AWS CloudFormation is an infrastructure as code ([[IaC]]) service that allows you to easily model, provision, and manage AWS and third-party resources.

-   Infrastructure is provisioned consistently, with fewer mistakes (human error)
-   Less time and effort than configuring resources manually
-   Free to use (you're only charged for the resources provisioned)
-   A template is a [[YAML]] or [[JSON]] template used to describe the end-state of the infrastructure you are either provisioning or changing
-   CloudFormation creates a Stack based on the template
-   Can easily rollback and delete the entire stack as well

![[Pasted image 20221118121432.png]]

### Difference between CloudFormation and Elastic Beanstalk

| CloudFormation | Elastic [[Beanstalk]] |
| ------------ | -------------- |
| “Template-driven provisioning” | “Web apps made easy" |
| Deploys infrastructure using code | Deploys applications on [[EC2]] ([[PaaS]])
| Can be used to deploy almost any AWS service | Deploys web applications based on Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker
| Uses [[JSON]] or [[YAML]] template files  | Uses ZIP or WAR files (or Git)
| Similar to [[Terraform]]  | Similar to Google App Engine
