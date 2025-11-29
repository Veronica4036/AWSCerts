# Cloud Practitioner Cheat Sheet


### Shared Responsibility
<img width="787" height="221" alt="image" src="https://github.com/user-attachments/assets/a326aad7-f4b2-4c9c-bedb-d94e4c17f2e9" />

[+] https://aws.amazon.com/compliance/shared-responsibility-model/


### Compare AWS Support Plans:
https://aws.amazon.com/premiumsupport/plans/



### 6 Advantages of Cloud Computing

<img width="784" height="337" alt="image" src="https://github.com/user-attachments/assets/018a9ad0-2ec0-4db3-a33f-7b45abd7425c" />


### 6 Pillars of the AWS Well-Architected Framework
<img width="1600" height="812" alt="image" src="https://github.com/user-attachments/assets/603dd895-f3a7-446c-8cd8-7743026039c8" />

[+] https://docs.aws.amazon.com/wellarchitected/latest/framework/sustainability.html



### 6R’s

<img width="786" height="257" alt="image" src="https://github.com/user-attachments/assets/33d48d6e-bfba-42c5-8f4b-443e97f7005b" />


### AWS Cloud Adoption Framework

Technology - Migrate and modernize legacy infrastructure, applications, and data and analytics platforms.
Process - Digitize, automate, and optimize your business operations. 
Organization - Reimagine how your business and technology teams create customer value and meet your strategic intent.
Product - Reimagine your business model by creating new value propositions and revenue models. 



### Trusted Advisor: 

<img width="783" height="344" alt="image" src="https://github.com/user-attachments/assets/4a4c35d1-4d0d-46f1-828f-50c99eb6e722" />







## Not too big concepts:

* AWS Identity and Access Management (AWS IAM), Amazon CloudFront, Amazon Route 53 and AWS Web Application Firewall (AWS WAF) are some of the ***global services.***
* ***AWS Shield Advanced provides expanded DDoS attack protection for*** web applications running on the following resources: Amazon Elastic Compute Cloud, Elastic Load Balancing (ELB), Amazon CloudFront, Amazon Route 53, AWS Global Accelerator. [WAF]
* ***AWS services has encryption enabled by default?*** CloudTrail logs, S3 Glacier, Storage Gateway
* ***AWS Compute Optimizer provides recommendations*** for several AWS services, including Amazon EC2 instances, EC2 Auto Scaling groups, Amazon EBS volumes, AWS Lambda functions, Amazon ECS services on AWS Fargate, and Amazon Aurora and RDS DB instances.
* There are ***4 different budget types*** you can create under AWS Budgets - Cost budget, Usage budget, Reservation budget and Savings Plans budget.
* ***Reserved Instance (RI) pricing is available for*** Amazon EC2 and Amazon RDS, and also for other services like Amazon ElastiCache, Redshift, and OpenSearch Service.
* You can deploy AWS WAF on Amazon CloudFront as part of your CDN solution, the Application Load Balancer that fronts your web servers or origin servers running on EC2, Amazon API Gateway for your REST APIs, or AWS AppSync for your GraphQL APIs.
* Savings Plan - Compute Savings Plans, EC2 Instance Savings Plans






### Dedicated Host VS Dedicated Instance:

<img width="798" height="628" alt="image" src="https://github.com/user-attachments/assets/cfe20d16-5eb3-40f4-869d-b0b9c582320b" />


[+] https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html



### Credits are applied in the following order:

1. Soonest expiring
2. Least number of applicable products
3. Oldest credit

[+] https://www.amazonaws.cn/en/support/faqs/





### EBS VS EFS cost :

* Amazon Elastic File System (Amazon EFS) - Infrequent Access storage class is cost-optimized for files accessed less frequently. Data stored on the Amazon Elastic File System (Amazon EFS) - Infrequent Access storage class costs less than Standard and you will pay a fee each time you read from or write to a file.
* Amazon EBS Snapshots are a point in time copy of your block data. For the first snapshot of a volume, Amazon EBS saves a full copy of your data to Amazon S3. Amazon EBS Snapshots are stored incrementally, which means you are billed only for the changed blocks stored.


AWS Pricing Calculator compares the cost of your applications in an on-premises or traditional hosting environment to AWS: server, storage, network, and IT labor. Therefore, you need to include every element relevant to these points of comparison.

* Server administration is included in the IT labor costs.
* Power/Cooling are included in the server, storage, and network cost.








## Misc concepts:

* The AWS account must be able to operate as a standalone account. Only then it can be removed from AWS organizations
* There is a one-minute minimum charge for Linux based EC2 instances, so this is the correct option.
* The *platform* perspective focuses on accelerating the delivery of your cloud workloads via an enterprise-grade, scalable, hybrid cloud environment. It comprises seven capabilities shown in the following figure. Common stakeholders include CTO, technology leaders, architects, and engineers.
* No charges for traffic between EC2 and S3 in the same region
* AWS Storage Gateway service provides three different types of gateways – Tape Gateway, File Gateway, and Volume Gateway
* AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET bla bla
* **EC2 instances can access files on an Amazon Elastic File System (Amazon EFS) file system across many Availability Zones (AZ), Regions and VPCs**
* Bob receives the cost-benefit from Susan's Reserved Instances (RI) only if he launches his instances in the same Availability Zone (AZ) not same region where Susan purchased her Reserved Instances
* Universal 2nd Factor (U2F) Security Key is a device that you can plug into a USB port on your computer. 
* **Hardware Multi-Factor Authentication (AWS MFA) device** - This is a hardware device that generates a six-digit numeric code based upon a time-synchronized one-time password algorithm. 
* Global Accelerator improves performance for a wide range of applications over TCP or UDP by proxying packets at the edge to applications running in one or more AWS Regions. It static IP addresses that act as a fixed entry point to your applications (good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover.)
* S3 stores data in a flat non-hierarchical structure. You can also append up to 10 key-value pairs called Amazon S3 object tags to each object, which can be created, updated, and deleted throughout an object’s lifecycle.
* Amazon Elastic File System (Amazon EFS) provides a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources.
* AWS Partner Solutions are automated reference deployments built by Amazon Web Services (AWS) solutions architects and AWS Partners. Partner Solutions help you deploy popular technologies to AWS according to AWS best practices.
* All traffic between Availability Zones (AZ) is encrypted
* Management events - An event in AWS CloudTrail is the record of activity in an AWS account. This activity can be an action taken by a user, role, or service that is monitorable by CloudTrail. 



### Waste Services:

* AWS OpsHub is a graphical user interface you can use to manage your AWS Snowball devices, enabling you to rapidly deploy edge computing workloads and simplify data migration to the cloud.
* **AppStream 2.0** - Amazon AppStream 2.0 is a fully managed non-persistent application and desktop streaming service. 
* **AWS OpsWorks** - AWS OpsWorks is a configuration management service that provides managed instances of Chef and Puppet. 
* Amazon Elastic Transcoder lets you convert media files that you have stored in Amazon Simple Storage Service (Amazon S3) into media files in the formats required by consumer playback devices. 
* AWS Control Tower is an AWS native service providing a pre-defined set of blueprints and guardrails to help customers implement a landing zone for new AWS accounts
* Service Control Policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization
* AWS CloudTrail Insights helps AWS users identify and respond to unusual activity associated with write API calls by continuously analyzing CloudTrail management events.
* **AWS Wavelength** - AWS Wavelength is an AWS Infrastructure offering optimized for mobile edge computing applications. (5G)
* You can use AWS Resource Groups to organize your AWS resources. Resource groups make it easier to manage and automate tasks on large numbers of resources at a time
* The AWS Well-Architected Tool helps you review the state of your workloads and compares them to the latest AWS architectural best practices. The tool is based on the AWS Well-Architected Framework, developed to help cloud architects build secure, high-performing, resilient, and efficient application infrastructure.
* AWS CodeArtifact is a fully managed artifact repository service that makes it easy for organizations of any size to securely store, publish, and share software packages used in their software development process. 






### Elastic Beanstalk:

* Supports programing languages and docker
* With basic health reporting, the AWS Elastic Beanstalk service does not publish any metrics to Amazon CloudWatch
* The AWS Elastic Beanstalk health monitoring can determine that the environment's Auto Scaling group is available and has a minimum of at least one instance



Three architecture models:

* Single Instance deployment: good for dev
* LB + ASG: great for production or pre-production web applications
* ASG only: great for non-web apps in production (workers, etc..)




