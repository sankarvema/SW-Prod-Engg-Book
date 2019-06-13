## AWS Service Domains

### Compute
1. EC2 - Virtual Machine or Cloud Virtual Machine
2. EC2 Container Service
3. Lambda - Server-less, AWS Functions
  - Event Driven model for running background tasks
  - Cannot host applications
4. Elastic Beanstalk - Containerized Compute
  - Can be used to host and run applications
5. Elastic Load Balancer
6. Auto Scale
7. Lightsail - lightweight easy to virtual private machines. Infact, they are Ec2 t2 instances with preconfigured spec good for development
- Workspaces - Cloud desktops


### Storage
1. Simple Storage Service (S3)
  - Object store, files are stored in buckets (root folder)
- Elastic Block Storage (EBS)
  - Network drive for better and high IOPS, connected to EC2 instance as local storage. We can add more EBS to an EC2 instance
  - Used with EC2 instances
- Elastic File System (EFS)
  - managed cloud-based file storage.
- Glacier
  - Archival or cold storage for backup services. Cheaper storage on Tapes
- Snowball
  - Offline data transfer to and from local to AWS infra in the form of offline harddisks, physically transferred
  - For large data transfer
- Storage Gateway
  - Means of data snapshot from hosted database to S3 for DR purposes
  - enable on-premises apps to access cloud data
- Cloudfront
  - CDN

### Database
1. Relational DB Service (RDS)
  - Managed relation services in terms of DB engine setup, updates, refresh etc.,
  - Provides Amazon Arora, MSSQL, Oracle, MySQL, Postgres, Mariadb
2. DynamoDB
  - NoSQL, tabular model
3. Arora
  - Fork of MySQL, 5 time faster than MySQL
4. Elasticache
  - DB cache service
  - Elasticache supports Memcache and Redis.
5. Redshift
  - Data warehouse services for data analysis
- Kinesis
  - Full managed data streaming service delivering real-time streaming data to destinations such as Amazon Simple Storage Service (Amazon S3), Amazon Redshift, Amazon Elasticsearch Service (Amazon ES), and Splunk.
- Glue - a fully managed extract, transform, and load (ETL) service
- Data Pipeline - orchestration service, helps in define data-driven workflows, so that tasks can be dependent on the successful completion of previous tasks.
- Athena - interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL

### Security, Identity & Compliance
1. IAM

### Messaging
1. Simple Email Service (SES) - Email services with custom email header fields, and many MIME types.
2. Simple Notification Services (SNS) - Pub/Sub Notification, with multiple subscribers, service via a choice of transport protocols, including HTTP, Amazon SQS, and email. The body of an Amazon SNS notification is limited to 8192 characters of UTF-8 strings, and is not intended to support multimedia content.
3. Simple Queue Services (SQS) - Queue service for single receiver to poll and pull the message. Once pulled it is gone (a standard q service)

### Migration
1. Snowball
- Snowball Mobile

### Network & Content Delivery
1. Route 53

### Management Tools
1. Cloud Watch

### Other
1. Amazon VPC - Virtual Private Cloud
- ElasticSearch -
- ElasticMapReduce (EMR)
