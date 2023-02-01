Kinesis Client Library is a Java library that helps read records from a Kinesis Stream with distributed applications sharing the read workload.

The KCL is different from the Kinesis Data Streams API that is available in the AWS SDKs.

-   The Kinesis Data Streams API helps you manage many aspects of Kinesis Data Streams (including creating streams, resharding, and putting and getting records).
-   The KCL provides a layer of abstraction specifically for processing data in a consumer role.

![Amazon Kinesis Client Library](https://digitalcloud.training/wp-content/uploads/2022/01/amazon-kinesis-client-library.jpeg)

The KCL acts as an intermediary between your record processing logic and Kinesis Data Streams.

When you start a KCL application, it calls the KCL to instantiate a worker. The KCL performs the following tasks:

-   Connects to the stream.
-   Enumerates the shards.
-   Coordinates shard associations with other workers (if any).
-   Instantiates a record processor for every shard it manages.
-   Pulls data records from the stream.
-   Pushes the records to the corresponding record processor.
-   Checkpoints processed records.
-   Balances shard-worker associations when the worker instance count changes.
-   Balances shard-worker associations when shards are split or merged.

The KCL ensures that for every shard there is a record processor.

*   Manages the number of record processors relative to the number of shards & consumers.
*   If you have only one consumer, the KCL will create all the record processors on a single consumer.
*   Each shard is processed by exactly one KCL worker and has exactly one corresponding record processor, so you never need multiple instances to process one shard.

However, one worker can process any number of shards, so it’s fine if the number of shards exceeds the number of instances.

![Amazon Kinesis Client Library Record Processors](https://digitalcloud.training/wp-content/uploads/2022/01/amazon-kinesis-client-library-record-processors.jpeg)

If you have two consumers it will load balance and create half the processors on one instance and half on another.

Scaling out consumers:

-   With KCL, generally you should ensure that the number of instances does not exceed the number of shards (except for failure or standby purposes).
-   Each shard can be read by only one KCL instance.
-   You never need multiple instances to handle the processing of one shard.

However, one worker can process multiple shards.

Example:

-   4 shards = max 4 KCL instances.
-   6 shards = max 6 KCL instances.

Progress is checkpointed into DynamoDB (IAM access required).

KCL can run on [[EC2]], Elastic [[Beanstalk]], and on-premises servers.

Records are read in order at the shard level.