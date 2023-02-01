## AWS EventBridge

Amazon EventBridge is a [[serverless]] [[event-driven]] [[event bus]] service, that you can use to connect your applications with data from a variety of sources. EventBridge delivers a stream of real-time data from your applications, software as a service ([[SaaS]]) applications, and AWS services to targets such as AWS Lambda functions, [[HTTP]] invocation endpoints using [[API]] destinations, or event buses in other AWS accounts.

![[Pasted image 20221117102755.png]]

| EventBridge | [[SQS]] |
| ------------ | ---- |
| Processed one at a time | Events processed in batches |
| Can match multiple rules and be sent to  multiple targets | Events no longer available after successful processing |

*   Serverless event bus  
*   Used for building event-driven architectures  
*   Ingests data and routes it to target AWS services

==EventBridge used to be known as CloudWatch Events