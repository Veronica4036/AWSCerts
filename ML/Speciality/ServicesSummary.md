### Kinesis Services
- Kinesis Data Stream: create **real-time** machine learning applications data streams, need capacity planning, real-time applications (extra - Storage,Replay, Flink can only read from here)
- Kinesis Data Firehose: **near-real time** data ingestion to S3, Redshift, ElasticSearch, Splunk
- Kinesis Data Analytics: real-time ETL / ML algorithms on streams
- Kinesis Video Stream: real-time video stream to create ML applications
- Flink: Managed service for [Apache Flink®](https://flink.apache.org/) [Apache Kafka Vs. Apache Flink]

### Here's a quick summary of all the services we've mentioned:
Here's the classification of these services into Serverless and Non-Serverless:

#### SERVERLESS SERVICES:
- Athena: Serverless Query of your data
- Glue Data Catalog & Crawlers: Metadata repositories for schemas and datasets in your account
- Glue ETL: ETL Jobs as Spark programs, run on a serverless Spark Cluster
- Batch: batch jobs run as Docker containers - not just for data, manages EC2 instances for you
- Step Functions: Orchestration of workflows, audit, retry mechanisms
- Quicksight: Visualization Tool   
- RDS / Aurora: Relational Data Store for OLTP, SQL language  
- DynamoDB: NoSQL store

#### NON-SERVERLESS SERVICES (Require Infrastructure Management):
- Redshift: Data Warehousing for OLAP, SQL language
- Redshift Spectrum: Redshift on data in S3 (without the need to load it first in Redshift)
- RDS / Aurora: Relational Data Store for OLTP, SQL language
- DynamoDB: NoSQL store
- ElasticSearch: index for your data, search capability, clickstream analytics
- ElastiCache: data cache technology
- Data Pipelines: Orchestration of ETL jobs between RDS, DynamoDB, S3. Runs on EC2 instances
- DMS: Database Migration Service, 1-to-1 CDC replication, no ETL
- EMR: Managed Hadoop Clusters

### ML
- DeepLens: camera by Amazon 
- Only the Ground Truth answer produces the positive or negative labels we need
- Semantic Segmentation: a computer vision system **that can classify every pixel** in an image. It uses MXNet and the ResNet architecture to do this.


































### What training input does it expect?

What training input does it expect?

XGBoost: (open source)
- So, it takes CSV or libsvm input.
- AWS recently extended it to accept recordIO-protobuf and Parquet as well.

Seq2Seq: 
- RecordIO-Protobuf
- Tokens must be integers (this is unusual, since most algorithms want floating point data.)

DeepAR: 
- JSON lines format: Gzip or Parquet
- Each record must contain:
  - Start: the starting time stamp
  - Target: the time series values
  - Ex: {"start": "2009-11-01 00:00:00", "target": [4.3, "NaN", 5.1, ...], "cat": [0, 1], "dynamic_feat": [[1.1, 1.2, 0.5, ...]]}

BlazingText: 
- For supervised mode (text classification):
  - One sentence per line
  - First “word” in the sentence is the string __label__ followed by the label
- Also, “augmented manifest text format”
- Word2vec just wants a text file with one training sentence per line.

Object2Vec: 
- Data must be tokenized into integers
- Training data consists of pairs of tokens and/or sequences of tokens

IP Insights: 
- User names, account ID’s can be fed in directly; no need to pre-process
- Training channel, optional validation (computes AUC score)
- CSV only
- Entity, IP

#### recordIO-protobuf or CSV

LDA: 
- Train channel, optional test channel
- Pipe mode only supported with recordIO


##### File or pipe mode on either

KNN: 
- Train channel contains your data
- Test channel emits accuracy or MSE
 training
  - First column is label

K-Means: 
- Train channel, optional test
  - Train ShardedByS3Key, test FullyReplicated

Linear Learner: 
- RecordIO-wrapped protobuf: Float32 data only!
- CSV

PCA




