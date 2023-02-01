A region is a geographical area.

Each region consists of 2 or more Availability Zone ([[AZ]]).

Each Amazon Region is designed to be completely isolated from the other Amazon Regions.

Each AWS Region has multiple [[AZ]]s and data centers.

You can replicate data within a region and between regions using private or public Internet connections.

You retain complete control and ownership over the region in which your data is physically located, making it easy to meet regional compliance and data residency requirements.

Note that there is a [[charge for data transfer between regions]].

When you launch an EC2 instance, you must select an [[AMI]] that’s in the same region. If the AMI is in another region, you can copy the AMI to the region you’re using.

## Regions and [[Endpoint]]s:

-   When you work with an instance using the command line interface ([[CLI]]) or API actions, you must specify its regional endpoint.
-   To reduce data latency in your applications, most Amazon Web Services offer a regional endpoint to make your requests.
-   An endpoint is a URL that is the entry point for a web service.
-   For example, https://dynamodb.us-west-2.amazonaws.com is an entry point for the Amazon DynamoDB service.