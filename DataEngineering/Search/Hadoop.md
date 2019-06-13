

## Hadoop Ecosystem

1. HDFS: HDFS or Hadoop File System is the file system in which data is stored. Here, the stored data may be structured or unstructured like relational database tables or log files respectively.
- MapReduce: MapReduce is basically a programming model that is designed to process the big data. MapReduce runs on large clusters of commodity hardware.
- Spark: Spark is a large-scale data processing engine. It can process any amount of data in memory so is getting popular among big data experts
- Pig: Pig is a data flow language. The Pig that is a functional language can process even huge datasets. It can access the data directly from HDFS and process it in the MapReduce clusters.
- Hive: It is nothing but just SQL on Hadoop. Hive is a distributed data warehouse on HDFS. SQL professionals need not learn anything to use Hive. Hive queries are basically translated to MapReduce for processing.
- Sqoop: Sqoop provides a way to transfer the data from relational databases to HDFS
- Flume: Flume can also transfer data but is used to transfer unstructured data to HDFS
- HBase: HBase is basically Hadoop Database and is different from HDFS. It is a column-oriented and distributed database that is built on the top of HDFS.
- Oozie: Oozie is a scheduling workflow and is used to schedule Hadoop jobs. It can start and end Pig/MapReduce or Hive jobs and schedule them as per the availability of resources.
- Hue: Hadoop User Experience, is a Browser based UI to access HDFS and M/R applications
