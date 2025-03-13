## Pointers to remember

### Kinesis Services
- Kinesis Data Stream: create **real-time** machine learning applications data streams, need capacity planning, real-time applications (extra - Storage,Replay, Flink can only read from here)
- Kinesis Data Firehose: **near-real time** data ingestion to S3, Redshift, ElasticSearch, Splunk
- Kinesis Data Analytics: real-time ETL / ML algorithms on streams
- Kinesis Video Stream: real-time video stream to create ML applications
- Flink: Managed service for [Apache Flink®](https://flink.apache.org/) [Apache Kafka Vs. Apache Flink]

### Here's a quick summary of all the services we've mentioned:
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

## Section 3: Exploratory Data Analysis

- [The Shape of Data: Distributions: Crash Course Statistics #7](https://www.youtube.com/watch?v=bPFNxD3Yg6U)
- Normal distribution:
```
Let's understand the complete normal distribution formula:

(1/(σ√(2π))) * e^(-(x-μ)²/(2σ²))

1. It has TWO main parts:
   - (1/(σ√(2π))) : The normalizing constant
   - e^(-(x-μ)²/(2σ²)) : The exponential part that gives the bell shape

2. What each part does:
   - Normalizing constant ensures total area = 1 (100% probability)
   - Exponential part creates the bell shape
   - Together they make a perfect probability distribution

3. How parameters affect the shape:
   μ (mean):
   - Controls where the peak is
   - Shifts the curve left or right
   
   σ (standard deviation):
   - Controls the spread/width
   - Larger σ = flatter, wider curve
   - Smaller σ = taller, narrower curve

4. Key properties that result:
   - Symmetric around the mean
   - 68% of data within ±1σ
   - 95% within ±2σ
   - 99.7% within ±3σ

    For 68% (±1σ): ∫(from μ-σ to μ+σ) (1/(σ√(2π))) * e^(-(x-μ)²/(2σ²)) dx ≈ 0.6826 (68.26%)
    For 95% (±2σ): ∫(from μ-2σ to μ+2σ) (1/(σ√(2π))) * e^(-(x-μ)²/(2σ²)) dx ≈ 0.9544 (95.44%)
    For 99.7% (±3σ): ∫(from μ-3σ to μ+3σ) (1/(σ√(2π))) * e^(-(x-μ)²/(2σ²)) dx ≈ 0.9973 (99.73%)

5. Example:
   For height of adult males:
   - If μ = 5'10" (mean height)
   - σ = 3 inches (standard deviation)
   Then:
   - 68% are between 5'7" and 6'1"
   - 95% are between 5'4" and 6'4"
   - 99.7% are between 5'1" and 6'7"

The beauty of this formula is that it describes many natural phenomena and is foundational in statistics and probability theory.
```
