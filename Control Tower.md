## AWS Control Tower

AWS Control Tower **enables end users on your distributed teams to provision new AWS accounts quickly, by means of configurable account templates in Account Factory**. Meanwhile, your central cloud administrators can monitor that all accounts are aligned with established, company-wide compliance policies.

-   Simplifies the process of creating multi-account environments
-   Sets up governance, compliance, and security guardrails for you

### Integrates with other services and features to setup the environment for you including:

*   [[AWS Organizations]]
*   [[SCP]]s
*   [[OU]]s
*   AWS [[Config]]
*   AWS [[CloudTrail]]
*   AWS [[S3]]
*   AWS [[SNS]]
*   AWS [[CloudFormation]]
*   AWS [[Service Catalog]]
*   AWS Single Sign-On ([[SSO]])/ AWS [[IAM Identity Center]]

## Configuration: Creating a [[Landing Zone]]

-   Control Tower creates a well-architected, multi-account baseline, based on best practices
-   This is known as a [[landing zone]]
*   Directory source can be **[[SSO]]**, **[[SAML]] 2.0 IdP**, or **Microsoft [[AD]]**

When we create our configuration in control tower, it's known as a [[landing zone]], and that's a number of accounts and configurations that are applied:

##### - Root
*   Management Account
##### - Security OU
*   Audit Account
*   Log Archive Account - Logs are saved in a [[S3]] Bucket
##### - Sandbox OU
*   Dev/Test Account
##### - Production OU
*   Production Account
*   **Preventive [[Guardrails]]** disallow [[API]] actions using [[SCP]]s

##### Guardrails are used for governance and compliance:

-   **Preventive [[guardrails]]** are based on [[SCP]]s and **disallow** [[API]] actions
*   **Detective [[guardrails]]** are implemented using AWS [[Config]] rules and [[Lambda]] functions and monitor and govern compliance

The root user in the management account can perform actions that guardrails would disallow
Control Tower creates a series of **preventive guardrails**. These are essentially service control policies ([[SCP]]), that will disallow certain [[API]] actions. Now you can think of this as similar to [[managed policy\|managed policies]] with [[IAM]]. Essentially Control Tower is creating a series of managed SCPs for you, that are preconfigured a certain way for a certain purpose. Control tower also creates what are called **detective guardrails**. These are used for governance and compliance and they are based on AWS [[Lambda]] functions and AWS [[Config]] rules.

==**Note: The root user in the management account can perform actions that guardrails would disallow**==

### Examples of guardrails 

AWS Control Tower can configure for you include:

-   Disallowing public write access to Amazon Simple Storage Service (Amazon [[S3]]) buckets
-   Disallowing access as a [[root]] user without multi- factor authentication ([[MFA]])
-   Enabling encryption for Amazon [[EBS volume]]s attached to Amazon [[EC2]] instances

![[Pasted image 20230204143830.png]]


![[Pasted image 20230204090600.png]]