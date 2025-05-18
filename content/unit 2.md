historey of hadoop 
- **2003–2004** → Google published papers on **Google File System (GFS)** and **MapReduce**, which inspired Hadoop
- **2005** → **Doug Cutting and Mike Cafarella** started Hadoop project as part of **Apache Nutch**
- **2006** → Hadoop became a **separate project**; early versions of **HDFS + MapReduce** were developed
- **2008** → Hadoop entered **Apache Incubator** and later became a **top-level Apache project**
- **2008–2012** → **Hadoop 1.x** series released
    - Core components: **HDFS + MapReduce**
    - Ecosystem tools added: **Hive**, **Pig**, **HBase**
- **2013** → **Hadoop 2.x** released
    - Introduction of **YARN (Yet Another Resource Negotiator)** for better resource management
- **2015–Present** → Modern Hadoop ecosystem includes:
    - **HDFS**, **MapReduce**, **YARN**, **Hive**, **Pig**, **HBase**, **Spark**, **Zookeeper**, **Oozie**, etc.
---

history of hadoop
- 2005 -> started under paper (google file system + map reduce simplified data processing on large clusters)
- 2006 -> hdfs + mapreduce
- 2008 -> developed to apache incubator
- 2008 - 13 -> hadoop 1.x versions released . hive + pig + Hbase
- 2013 - > hadoop 2.x version realeased . yarn 
- 2015 - present -> hdfs , mapreduce, hive,pig , yarn ,  Hbase , spark

**hdfs**
- distributed storage
- block based storage
- fault tolerace
- scalable
- replication upto 3 
- write once read many model
- high throughput (large scale processing)
- master slave architecture
- data integrity using checksum
- data locality

**challenges of hdfs**
- not suitable for small files
- write once read many limitation
- single point of failure of namenode
- large meta data files because of small files

**hdfs archecture**
- namenode
- datanode

**common format in hadoop**
- text file
- sequence file
- avro
- parquet
- orc

anaylising data with hadoop

**map reduce**
- a programming model
- haaev two main function 
	- map function
	- reduce function
- working process
	- input split
	- mapping phase
	- shuffling
	- reducing phase
	- final output
- map reduce application
	- mapper class
	- reducer class
	- driver class
- map reduce for hadoop
	- map phase 
		- input data to key val pair , and processes each pair to produce output (intermediate data)
		- this map func is applied paralllely , across nodes for  effecinecy
	- reduce phase
		 - map out put is filltered or aggregated and final output is generated
		 - reduce func aggregate result and show it as result 


map reduce component 


benefit of map reduce
- parallel processing
- fault tolerance
- scalability

job scheduling 
- fifo
- fair
- capacity


hadoop scaling out 
- adding more machine to cluster to increase performance

hadoop streaming
- hadoop utility , to connect mapreduce framework to non java programs 
- can write own programs using py
- custom map func
- custom reduce func

hadoop pipe
- c++ api to connect hadoop to c++ programming lang 
- can write program using c++
- for perforce critical enironment 

more about map reduce
- map reduce (programming model + processing framework)
- used for parallel processing
- data is broken down 
- than prcessed in different machine
mapper
reducer
input output
shuffle and sort
 

