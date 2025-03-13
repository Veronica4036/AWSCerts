### Kinesis Services
- Kinesis Data Stream: create **real-time** machine learning applications data streams, need capacity planning, real-time applications (extra - Storage,Replay, Flink can only read from here)
- Kinesis Data Firehose: **near-real time** data ingestion to S3, Redshift, ElasticSearch, Splunk
- Kinesis Data Analytics: real-time ETL / ML algorithms on streams
- Kinesis Video Stream: real-time video stream to create ML applications
- Flink: Managed service for [Apache Flink®](https://flink.apache.org/) [Apache Kafka Vs. Apache Flink]

### Here's a quick summary of all the services we've mentioned:
Here's the classification of these services into Serverless and Non-Serverless:

SERVERLESS SERVICES:
1. AWS Glue
   - Glue Data Catalog & Crawlers
   - Glue ETL (serverless Spark)

2. Amazon Athena
   - Serverless query service

3. AWS Step Functions
   - Serverless workflow orchestration

4. AWS Batch
   - Serverless container orchestration (manages EC2 instances automatically)

5. AWS QuickSight
   - Serverless visualization service

NON-SERVERLESS SERVICES (Require Infrastructure Management):
1. Amazon EMR
   - Managed Hadoop clusters
   - Requires cluster management

2. Amazon Redshift
   - Requires cluster provisioning and management
   - (Though Redshift Spectrum is serverless)

3. Amazon RDS/Aurora
   - Requires database instance management
   - (Though Aurora Serverless is available as a serverless option)

4. Amazon ElastiCache
   - Requires cache node management

5. Amazon ElasticSearch (now OpenSearch)
   - Requires cluster management

6. AWS Data Pipeline
   - Runs on EC2 instances
   - Requires infrastructure management

7. AWS DMS
   - Requires replication instance management

8. Amazon DeepLens
   - Physical hardware device

HYBRID (Can be both depending on configuration):
1. Amazon DynamoDB
   - Serverless by default
   - But requires capacity planning if using provisioned capacity mode
   - Fully serverless when using on-demand capacity mode

Note: Some services like Aurora and Redshift now offer serverless options, showing AWS's trend toward more serverless offerings.
