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
7. Lightsail


### Storage
1. Simple Storage Service (S3)
  - Object store, files are stored in buckets (root folder)
2. Elastic Block Storage (EBS)
  - Network drive for better and high IOPS, connected to EC2 instance as local storage. We can add more EBS to an EC2 instance
3. Glacier
  - Archival or cold storage for backup services. Cheaper storage on Tapes
4. Snowball
  - Offline data transfer to and from local to AWS infra in the form of offline harddisks, physically transferred
  - For large data transfer
5. Storage Gateway
  - Means of data snapshot from hosted database to S3 for DR purposes
6. Cloudfront
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
5. Redshift
  - Data warehouse services for data analysis

### Security, Identity & Compliance
1. IAM

### Messaging
1. Simple Email Service (SES)

### Migration
1. Snowball

### Network & Content Delivery
1. Route 53

### Management Tools
1. Cloud Watch
