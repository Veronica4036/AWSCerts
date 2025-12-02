# Solutions Architect Associate Cheat Sheet

## Concepts:
- Each region has many availability zones(min is 3, max is 6). Each availability zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity

## EC2 & EBS concepts: 
- Dedicated Hosts: book an entire physical server, control instance placement | Dedicated Instances: no other customers will share your hardware | EC2 Capacity Reservations: Reserve On-Demand instances capacity in a specific AZ for any
duration
-  Placement Groups(PG):: Cluster: Low latency, 10 Gbps network[all instances in single AZ] | Spread: 7I/AZ/PG | Partition(P): 7P/AZ upto 100+ Instances, instances have access to P metdata. Use cases: HDFS, HBase, Cassandra,
Kafka
- Hibernate - RAM state is written to a file in the root EBS volume[must be encrypted] (Not for >60 days)
- EBS Snapshots Features: Move a Snapshot to an ”archive tier” that is 75% cheaper(24 to 72 hours for restoring)
- EC2 Instance Store: Better I/O performance |  Good for buffer / cache / scratch data / temporary content | ephemeral

## When the answer is in Pointers:
- How to choose an AWS Region? Compliance, Proximity, Available services, Pricing
- AWS has Global Services: IAM, R53, WAF, CloudFront


## Services:

