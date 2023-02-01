## AWS CloudTrail 

AWS CloudTrail is an AWS service that helps you enable operational and risk auditing, governance, and compliance of your AWS account. Actions taken by a user, role, or an AWS service are recorded as events in CloudTrail. Events include actions taken in the AWS Management Console, AWS Command Line Interface ([[CLI]]), and AWS [[SDK]]s and [[API]]s.
AWS CloudTrail monitors and records account activity across your AWS infrastructure, giving you control over storage, analysis, and remediation actions.

-   CloudTrail logs [[API]] activity for auditing
-   By default, management events are logged and retained for 90 days
-   A CloudTrail Trail logs any events to [[S3]] for indefinite retention
-   Trail can be within [[Region]] or all Regions
-   [[CloudWatch Events]] can be triggered based on [[API]] calls in [[CloudTrail]] 
-   Events can be streamed to [[CloudWatch Logs]]

[![](https://d1.awsstatic.com/product-marketing/CloudTrail/product-page-diagram_AWS-CloudTrail_HIW.feb63815c1869399371b4b9cc1ae00e78ed9e67f.png)](https://aws.amazon.com/cloudtrail/#)

## CloudTrail vs. [[CloudWatch]]

| **Parameters**                      | AWS [[CloudWatch]]                                                                                                                                                                                                     | AWS [[CloudTrail]]                                                                                                                                                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Definition**                      | CloudWatch is a monitoring service for AWS resources and applications.                                                                                                                                             | CloudTrail is a web service that records [[API]] activity in your AWS account.                                                                                                                                             |
| **Monitoring Tool**                 | CloudWatch monitors applications and infrastructure performance in the AWS environment.                                                                                                                            | CloudTrail monitors actions in the AWS environment.                                                                                                                                                                    |
| **Usage**                           | With CloudWatch, we can: Collect and track metrics; Collect and monitor log files; Set alarms and visualize                                                                                                             | CloudTrail answers these questions: Who made a request? Which services were used? What actions were performed? What were the parameters for those actions? What were the response elements returned by the AWS service? |
| **Logs or Event delivery Rate**     | CloudWatch delivers metrics data in 5-minute or 1-minute periods for essential monitoring and detailed monitoring, respectively. By default, log data will be sent by the CloudWatch Logs agent every five seconds. | CloudTrail delivers an event within 15 minutes of the [[API]] call.                                                                                                                                                        |
| **Example**                         | Suppose you have a web app running in your AWS environment; AWS CloudWatch can monitor bandwidth utilization, performance, and the traffic parameters of your app.                                                 | If your [[EC2]] instance’s security is compromised by an attacker, you can identify the culprit with the help of historical [[CloudTrail]] data Logs.                                                                          |
| **Integration with Other Services** | [[EC2]] instances, [[auto scaling]], load balancers ([[ELB]]), AWS [[SNS]], AWS [[SQS]], AWS [[RDS]], AWS [[S3]], AWS [[DynamoDB]], AWS [[CloudTrail]], other AWS resources.                                                                                      | AWS [[CloudWatch]], AWS [[Opensearch Service]], AWS [[Lambda]], third-party monitoring platforms, AWS [[SNS]], AWS, [[SQS]], etc.                                                                                                          |

