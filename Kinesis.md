## AWS Kinesis
* ### AWS [[Kinesis Video Streams]]
* ### AWS [[Kinesis Data Streams]]
* ### AWS [[Kinesis Data Firehose]]
* ### AWS [[Kinesis Data Analytics]]

Amazon Kinesis makes it easy to collect, process, and analyze real-time, streaming data so you can get timely insights and react quickly to new information.

* Kinesis is a collection of services for processing streams of various data.
* Data is processed in “shards” – with each shard able to ingest 1000 records per second.
* There is a default limit of 500 shards, but you can request an increase to unlimited shards.
* A record consists of a partition key, sequence number, and data blob (up to 1 MB).
* Transient data store – default retention of 24 hours but can be configured for up to 7 days.

![](https://digitalcloud.training/wp-content/uploads/2022/01/word-image-2.png)

### There are four types of Kinesis service:

* ##### [[Kinesis Video Streams]]:
Kinesis Video Streams makes it easy to securely stream video from connected devices to AWS for analytics, machine learning ([[ML]]), and other processing.

* ##### [[Kinesis Data Streams]]:
Kinesis Data Streams enables you to build custom applications that process or analyze streaming data for specialized needs.
*   Producers send data which is stored in shards for up to 7 days
*   Consumers process the data and save to another service

* ##### [[Kinesis Data Firehose]]:
Kinesis Data Firehose is the easiest way to load streaming data into data stores and analytics tools.
*   No shards, completely automated and elastically scalable
*   Saves data directly to another service such as [[S3]], Splunk, [[RedShift]], or [[OpenSearch Service]]

* ##### [[Kinesis Data Analytics]]:
Amazon Kinesis Data Analytics is the easiest way to process and analyze real-time, streaming data.
*   Provides real-time [[SQL]] processing for streaming data


![[Pasted image 20221119114314.png]]

### Benefits

* ##### Real-time
Amazon Kinesis enables you to ingest, buffer, and process streaming data in real-time, so you can derive insights in seconds or minutes instead of hours or days.  

* ##### Fully managed
Amazon Kinesis is fully managed and runs your streaming applications without requiring you to manage any infrastructure.  

* ##### Scalable
Amazon Kinesis can handle any amount of streaming data and process data from hundreds of thousands of sources with very low latencies.

### Kinesis client library ([[KCL]])

Kinesis Client Library is a Java library that helps read records from a Kinesis Stream with distributed applications sharing the read workload.

### Security

*   Control access / authorization using [[IAM policy]].
*   Encryption in flight using HTTPS endpoints.
*   Encryption at rest using [[KMS]].
*   Possible to encrypt / decrypt data on the client side.
*   VPC endpoints available for Kinesis to access within a VPC.

###  Examples of streaming data use cases include:  

*   Purchases from online stores  
*   Stock prices  
*   Game data (statistics and results as the gamer plays)
*   Social network data
*   Geospatial data (think uber.com)
*   [[IoT]] sensor data

## [[SQS]] vs [[SNS]] vs Kinesis

| [[SQS]]                                                  | [[SNS]]                                                      | [[Kinesis]]                                                      |
| ---------------------------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------ |
| \- Consumers pull data.                              | \- Push data to many subscribers.                        | \- Consumers pull data.                                      |
| \- Data is deleted after being consumed.             | \- Up to 10,000,000 subscribers.                         | \- As many consumers as you need.                            |
| \- Can have as many workers (consumers) as you need. | \- Data is not persisted (lost if not deleted).          | \- Possible to replay data.                                  |
| \- No need to provision throughput.                  | \- [[Pub-sub]].                                              | \- Meant for real-time big data, analytics, and [[ETL]]. |
| \- No ordering guarantee (except with [[FIFO queue]]s).  | \- Up to 10,000,000 topics.                              | \- Ordering at the shard level.                              |
| \- Individual message delay.                         | \- No need to provision throughput.                      | \- Data expires after X days.                                |
|                                                      | \- Integrates with [[SQS]] for fan-out architecture pattern. | \- Must provision throughput.                                |

