Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon [[S3]] using standard [[SQL]].
Athena is [[serverless]], so there is no infrastructure to manage, and you pay only for the queries that you run.
With a few clicks in the AWS Management Console, customers can point Athena at their data stored in [[S3]] and begin using standard [[SQL]] to run ad-hoc queries and get results in seconds.

-   You can use Athena to process logs, perform ad-hoc analysis, and run interactive queries.
-   Athena scales automatically – executing queries in parallel – so results are fast, even with large datasets and complex queries.
-   Athena queries data in [[S3]] using [[SQL]]
-   Can be connected to other data sources with
    [[Lambda]]
-   Data can be in CSV, TSV, [[JSON]], Parquet and ORC formats
-   Uses a managed Data Catalog (AWS [[Glue]]) to store information and schemas about the [[database]]s and tables

![[Pasted image 20221119112327.png]]


