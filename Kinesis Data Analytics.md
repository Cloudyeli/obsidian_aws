## AWS Kinesis Data Analytics
#(AWS [[Kinesis]])

[[Kinesis]] Data Analytics is the easiest way to process and analyze real-time, streaming data.

* Can use standard SQL queries to process Kinesis data streams.
* Provides real-time analysis.

Use cases:

-   Generate time-series analytics.
-   Feed real-time dashboards.
-   Create real-time alerts and notifications.

Quickly author and run powerful [[SQL]] code against streaming sources.

* Can ingest data from Kinesis Streams and [[Kinesis Data Firehose]].
* Output to [[S3]], [[RedShift]], [[OpenSearch Service]] and [[Kinesis Data Streams]].
* Sits over [[Kinesis Data Streams]] and [[Kinesis Data Firehose]].

A Kinesis Data Analytics application consists of three components:

-   **Input** – the streaming source for your application.
-   **Application code** – a series of SQL statements that process input and produce output.
-   **Output** – one or more in-application streams to hold intermediate results.

Kinesis Data Analytics supports two types of inputs: 

- ##### Streaming data sources
A streaming data source is continuously generated data that is read into your application for processing.

* ##### Reference data sources
A reference data source is static data that your application uses to enrich data coming in from streaming sources.

* Can configure destinations to persist the results.
* Supports Kinesis Streams and [[Kinesis Data Firehose]] ([[S3]], [[RedShift]], [[OpenSearch Service]]) as destinations.

[[IAM]] can be used to provide Kinesis Analytics with permissions to read records from sources and write to destinations.