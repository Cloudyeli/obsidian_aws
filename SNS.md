## Simple Notification Service (SNS)

Amazon Simple Notification Service (SNS) is **a web service that makes it easy to set up, operate, and send notifications from the cloud**. It provides developers with a highly scalable, flexible, and cost-effective capability to publish messages from an application and immediately deliver them to subscribers or other applications. 

-   [[Pub-sub]] model
-   Amazon SNS is used for building and integrating loosely- coupled, distributed applications
-   Provides instantaneous, push-based delivery (no polling)
-   Uses simple [[API]]s and easy integration with applications
-   Offered under an inexpensive, pay-as-you-go model with no up-front costs

![[Pasted image 20221117154324.png]]

It is designed to make web-scale computing easier for developers. Amazon SNS follows the “publish-subscribe” ([[pub-sub]]) messaging paradigm, with notifications being delivered to clients using a “push” mechanism that eliminates the need to periodically check or “poll” for new information and updates. 
With simple [[API]]s requiring minimal up-front development effort, no maintenance or management overhead and pay-as-you-go pricing, Amazon SNS gives developers an easy mechanism to incorporate a powerful notification system with their applications.



## [[SQS]] vs SNS vs [[Kinesis]]

| [[SQS]]                                                  | [[SNS]]                                                      | [[Kinesis]]                                                      |
| ---------------------------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------ |
| \- Consumers pull data.                              | \- Push data to many subscribers.                        | \- Consumers pull data.                                      |
| \- Data is deleted after being consumed.             | \- Up to 10,000,000 subscribers.                         | \- As many consumers as you need.                            |
| \- Can have as many workers (consumers) as you need. | \- Data is not persisted (lost if not deleted).          | \- Possible to replay data.                                  |
| \- No need to provision throughput.                  | \- [[Pub-sub]].                                              | \- Meant for real-time big data, analytics, and [[ETL]]. |
| \- No ordering guarantee (except with [[FIFO queue]]s).  | \- Up to 10,000,000 topics.                              | \- Ordering at the shard level.                              |
| \- Individual message delay.                         | \- No need to provision throughput.                      | \- Data expires after X days.                                |
|                                                      | \- Integrates with [[SQS]] for fan-out architecture pattern. | \- Must provision throughput.                                |

## Difference between SNS and [[SES]]

The main difference between [[SES]] and SNS is that **SES is designed to manage and monitor social media accounts from the AWS cloud, while SNS is designed to manage and publish content to a group of people**.