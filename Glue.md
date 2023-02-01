## AWS Glue

AWS Glue is a [[serverless]] data integration service that **makes it easier to discover, prepare, move, and integrate data from multiple sources for analytics, machine learning ([[ML]]), and application development**. AWS Glue can run your extract, transform, and load ([[ETL]]) jobs as new data arrives.

-   You can create and run an ETL job with a few clicks in the AWS Management Console.
-   You simply point AWS Glue to your data stored on AWS, and AWS Glue discovers your data and stores the associated [[metadata]] (e.g. table definition and schema) in the AWS Glue Data Catalog.
-   Once cataloged, your data is immediately searchable, queryable, and available for [[ETL]].
-   AWS Glue generates the code to execute your data transformations and data loading processes.
-   Fully managed extract, transform and load ([[ETL]]) service
-   Used for preparing data for analytics
-   AWS Glue runs the [[ETL]] jobs on a fully managed, scale-out Apache Spark environment
-   Works with data lakes (e.g. data on [[S3]]), data warehouses (including [[RedShift]]), and data stores (including [[RDS]] or [[EC2]] [[database]]s)

## [[Event-driven]] [[ETL]]

AWS Glue can run your extract, transform, and load ([[ETL]]) jobs as new data arrives. For example, you can configure AWS Glue to initiate your ETL jobs to run as soon as new data becomes available in Amazon Simple Storage Service ([[S3]]).  

![Diagram showing how AWS Glue can run your ETL jobs as new data arrives.](https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Event-Driven-ETL-Pipelines%20(4).3f3f393bfdb3deefdf183c1cfd39741f99eed6c6.png)

## AWS Glue Data Catalogue

You can use the Data Catalog to quickly discover and search multiple AWS datasets without moving the data. Once the data is cataloged, it is immediately available for search and query using Amazon [[Athena]], Amazon [[EMR]], and Amazon [[Redshift]] Spectrum.  

![Diagram showing the Data Catalog discovering and searching datasets without moving the data.](https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Unified-View%20(3).cbbd4734e6a79cc3d2569064d0010605a0a307ae.png)

### No-code [[ETL]] jobs

AWS Glue Studio makes it easier to visually create, run, and monitor AWS Glue [[ETL]] jobs. You can build ETL jobs that move and transform data using a drag-and-drop editor, and AWS Glue automatically generates the code.  

![Diagram showing how users can compose ETL jobs that move and transform data using a drag-and-drop editor.](https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Elixir%20(2).522ef785088de982530b9fdde4c8be146562fa0f.png)

### Self-service data preparation with AWS [[Glue Data Brew]]

With AWS [[Glue DataBrew]], you can explore and experiment with data directly from your data lake, data warehouses, and [[database]]s, including Amazon [[S3]], Amazon [[Redshift]], AWS [[Lake Formation]], Amazon [[Aurora]], and Amazon Relational Database Service ([[RDS]]). You can choose from over 250 prebuilt transformations in DataBrew to automate data preparation tasks such as filtering anomalies, standardizing formats, and correcting invalid values.  

![Diagram showing how DataBrew automates data preparation tasks for users.](https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Self-Service-Visual-Data%20(2).0e1a87155040f71dcc92464a283f1adddd39cf85.png)