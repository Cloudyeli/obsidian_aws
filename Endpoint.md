An endpoint is a [[URL]] that is the entry point for a web service.

-   For example, `https://dynamodb.us-west-2.amazonaws.com` is an entry point for the Amazon DynamoDB service.
*   Public services have public IP addresses / endpoints.
*   An endpoint is a [[URL]] that is the entry point for a web service.

## [[Region]]s and Endpoints:

-   When you work with an instance using the command line interface ([[CLI]]) or [[API]] actions, you must specify its regional endpoint.
-   To reduce data latency in your applications, most Amazon Web Services offer a regional endpoint to make your requests.

## [[VPC Endpoint]]s

##### - Interface Endpoint
##### - Gateway Endpoint

|  | Interface Endpoint | Gateway Endpoint |
| ---- | ----- | ----- |
| **What** | Elastic Network Interface with a Private IP | A gateway that is a target for a specific route
| **How** | Uses DNS entries to redirect traffic | Uses prefix lists in the route table to redirect traffic
| **Which services** | [[API Gateway]], [[CloudFormation]], [[CloudWatch]] etc. | Amazon [[S3]], [[DynamoDB]] 
| **Security** | Security Groups | VPC Endpoint Policies