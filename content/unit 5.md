# Pig
- part of hadoop
- used for data processing
- uses its own tool called pig latin  == high level scripting language
- uses pig engine on which pig latin runs
- data transformation + processing + ananylsis
- can be used for unstrucutured + semi strucutured + struccutured data
- best for batch processing
- provide user defined functions for complexity
- can be used to create data pipe line

execution mode
- local mode
	- local machine
	- small dataset
	- io in local file sys
- map reduce mode
	- uses hadoop cluster
	- large data set
	- uses hdfs for  io
grunt 
- interactive shell to run pig 
- can run pig latin commands
- good for debugging


Hbase
- column based nosql db
- can handle any type of data
- for real time processing 
- for random read and write 

hive
- distributed ware house system

sqoop
- brings data from rdms to hdfs
- or hdfs to rdms
- can be used any rdms
- cammands written in sqoop internally converted into map reduce task in hdfs

flume
- collect data from various sources to hdfs
- works real time or batch mode
- 