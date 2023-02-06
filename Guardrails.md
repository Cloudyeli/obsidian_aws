## Guardrails are used for governance and compliance:

-   **Preventive guardrails** are based on [[SCP]]s and **disallow** [[API]] actions
*   **Detective guardrails** are implemented using AWS [[Config]] rules and [[Lambda]] functions and monitor and govern compliance

The root user in the management account can perform actions that guardrails would disallow
[[Control Tower]] creates a series of **preventive guardrails**. These are essentially service control policies ([[SCP]]), that will disallow certain [[API]] actions. Now you can think of this as similar to [[managed policy\|managed policies]] with [[IAM]]. Essentially [[Control Tower]] is creating a series of managed SCPs for you, that are preconfigured a certain way for a certain purpose. 

[[Control tower]] also creates what are called **detective guardrails**. These are used for governance and compliance and they are based on AWS [[Lambda]] functions and AWS [[Config]] rules.

==**Note: The root user in the management account can perform actions that guardrails would disallow**==

### Examples of guardrails 

AWS Control Tower can configure for you include:

-   Disallowing public write access to Amazon Simple Storage Service (Amazon [[S3]]) buckets
-   Disallowing access as a [[root]] user without multi- factor authentication ([[MFA]])
-   Enabling encryption for Amazon [[EBS volume]]s attached to Amazon [[EC2]] instances
