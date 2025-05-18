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
Doug and Mike 
history of hadoop
- 2005 -> started under paper (google file system + map reduce simplified data processing on large clusters)
- 2006 -> hdfs + mapreduce
- 2008 -> developed to apache incubator
- 2008 - 13 -> hadoop 1.x versions released . hive + pig + Hbase
- 2013 - > hadoop 2.x version realeased . yarn 
- 2015 - present -> hdfs , mapreduce, hive,pig , yarn ,  Hbase , spark

hadoop framwork consists of
- hadoop common
- hdfs
- map reduce
- yarn


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

 job -> task 
 **map reduce component** 

🔹1. **JobTracker (Deprecated → ResourceManager in YARN)**
- **JobTracker** Hadoop v1 me ek **master daemon** tha jo:
    - MapReduce jobs ko **accept** karta tha.
    - Input splits banata tha.
    - Tasks ko available TaskTrackers pe **assign** karta tha.
    - Task ki **progress monitor** karta tha.
- Hadoop v2 me yeh **deprecated** ho chuka hai aur iska kaam **ResourceManager (YARN)** karta hai.

🔹 2. **TaskTracker (Deprecated → NodeManager in YARN)**
- **TaskTracker** ek **slave daemon** tha jo JobTracker se tasks receive karta tha.
    - Yeh har task ko execute karta tha (Map ya Reduce).
    - Apni health aur progress JobTracker ko report karta tha.
- YARN me isko **NodeManager** ne replace kar diya hai.

 🔹 3. **InputSplit**
- InputSplit ek logical chunk hai input data ka.
- Hadoop ek large file ko multiple **InputSplits** me tod deta hai so that parallel execution ho sake.
- **Map tasks** ko yeh splits assign kiya jaata hai.
- Example: Agar file 1GB hai and block size 128MB hai, to ~8 splits banenge.

🔹 4. **RecordReader**
- **InputSplit** me data hota hai, par RecordReader us data ko read karke **(key, value)** pairs me convert karta hai Mapper ke liye.
- Example: `TextInputFormat` me key line offset hota hai aur value full line.

 🔹 5. **Mapper**
- Map function input data ko process karta hai aur intermediate **(key, value)** pairs banata hai.
- For example: "Hello world" line ko `(hello, 1), (world, 1)` me convert karega.
- Har InputSplit ke liye ek Mapper task banta hai.

 🔹 6. **Combiner (Optional)**
- Mini reducer jaisa hota hai, **Map output** par local aggregation karta hai before sending it across the network.
- Network traffic reduce karta hai.
- Example: Word count me same words ke counts ko locally combine karega.

 🔹 7. **Partitioner**
- Partitioner decide karta hai ki **kaunsa key kis Reducer** ko milega.
- Default: **HashPartitioner** – key ka hash leke modulo with number of reducers.
- Iska role hai ki **load balancing** ho across reducers.

 🔹 8. **Shuffle and Sort**
- **Shuffle** phase me Map outputs Reducers ke paas jaate hain.
- Hadoop ensures ki same key wale pairs ek hi Reducer ko milein.
- **Sort** phase me keys ko ascending order me arrange kiya jaata hai before reducing.
- Yeh phase **automatically** Hadoop handle karta hai.

 🔹 9. **Reducer**
- Reducer same key ke values ko **aggregate** karta hai.
- For example: `(hello, [1,1,1]) → (hello, 3)`
- Har key ke liye ek reduce function call hota hai.

 🔹 10. **OutputFormat**
- Reduce ke output ko **HDFS me store** karne ka kaam karta hai.
- Default: `TextOutputFormat` – key and value ko tab se separate karke likhta hai.
- Custom OutputFormats bhi bana sakte ho (e.g., DBOutputFormat for databases).


**benefit of map reduce**
- parallel processing
- fault tolerance
- scalability
- data locality

map reduce application
- log processing
- data minig
- recommendation sys
- search indexing
- financial modeling
- social media anaylitics
- 

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



failure in mapreduce
- task failure
- node failure
- job failure

map reduce types
- simple mapreduce
- multiple mapper / reducer
- mapreduce with combiner
- chain mapreduce

input format
- textinput format
- keyvalue input format
- sequence file input format
- mutiple inputs
- Nline input format 

output format 
- textoutput format
- sequencefileoutput format
- multiple outputs
- null output format
