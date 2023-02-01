## Simple Queue Service (SQS)

Amazon Simple Queue Service (SQS) is a [[serverless]] service, that lets you send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available.

Amazon SQS is a message queue service used by distributed applications **to exchange messages through a polling model, and can be used to decouple sending and receiving components**.


| [[EventBridge]] | SQS |
| ------------ | ---- |
| Processed one at a time | Events processed in batches |
| Can match multiple rules and be sent to  multiple targets | Events no longer available after successful processing |

Amazon Simple Queue Service (SQS)

-   SQS offers a reliable, highly-scalable, hosted queue for storing messages in transit between computers
-   SQS is used for distributed/decoupled applications
-   SQS uses a message-oriented API
-   SQS uses pull based (polling) not push based

## SQS vs [[SNS]] vs [[Kinesis]]

| [[SQS]]                                                  | [[SNS]]                                                      | [[Kinesis]]                                                      |
| ---------------------------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------ |
| \- Consumers pull data.                              | \- Push data to many subscribers.                        | \- Consumers pull data.                                      |
| \- Data is deleted after being consumed.             | \- Up to 10,000,000 subscribers.                         | \- As many consumers as you need.                            |
| \- Can have as many workers (consumers) as you need. | \- Data is not persisted (lost if not deleted).          | \- Possible to replay data.                                  |
| \- No need to provision throughput.                  | \- [[Pub-sub]].                                              | \- Meant for real-time big data, analytics, and [[ETL]]. |
| \- No ordering guarantee (except with [[FIFO queue]]s).  | \- Up to 10,000,000 topics.                              | \- Ordering at the shard level.                              |
| \- Individual message delay.                         | \- No need to provision throughput.                      | \- Data expires after X days.                                |
|                                                      | \- Integrates with [[SQS]] for fan-out architecture pattern. | \- Must provision throughput.                                |
