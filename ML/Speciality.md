## Pointers to remember

### Kinesis Services
- Kinesis Data Stream: create **real-time** machine learning applications data streams, need capacity planning, real-time applications (extra - Storage,Replay, Flink can only read from here)
- Kinesis Data Firehose: **near-real time** data ingestion to S3, Redshift, ElasticSearch, Splunk
- Kinesis Data Analytics: real-time ETL / ML algorithms on streams
- Kinesis Video Stream: real-time video stream to create ML applications
- Flink: Managed service for [Apache Flink®](https://flink.apache.org/) [Apache Kafka Vs. Apache Flink]

Here's a quick summary of all the services we've mentioned:
- Glue Data Catalog & Crawlers: Metadata repositories for schemas and datasets in your account
- Glue ETL: ETL Jobs as Spark programs, run on a serverless Spark Cluster
- DynamoDB: NoSQL store
- Redshift: Data Warehousing for OLAP, SQL language
- Redshift Spectrum: Redshift on data in S3 (without the need to load it first in Redshift)
- RDS / Aurora: Relational Data Store for OLTP, SQL language
- ElasticSearch: index for your data, search capability, clickstream analytics
- ElastiCache: data cache technology
- Data Pipelines: Orchestration of ETL jobs between RDS, DynamoDB, S3. Runs on EC2 instances
- Batch: batch jobs run as Docker containers - not just for data, manages EC2 instances for you
- DMS: Database Migration Service, 1-to-1 CDC replication, no ETL
- Step Functions: Orchestration of workflows, audit, retry mechanisms
- EMR: Managed Hadoop Clusters
- Quicksight: Visualization Tool
- DeepLens: camera by Amazon
- Athena: Serverless Query of your data

