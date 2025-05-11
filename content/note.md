# **SQL vs NoSQL Database (Comparison Table)**

| **Feature**              | **SQL Database** (Relational)                                                 | **NoSQL Database** (Non-Relational)                                                            |
| ------------------------ | ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **Data Model**           | **Structured data** in **tables** (rows + columns)                            | **Flexible** models: document, key-value, column, graph                                        |
| **Schema**               | **Fixed schema** (predefined, strict structure)                               | **Dynamic schema** (can change anytime, no fixed structure)                                    |
| **Examples**             | MySQL, PostgreSQL, Oracle, MS SQL Server                                      | MongoDB (Document), Redis (Key-Value), Cassandra (Column), Neo4j (Graph)                       |
| **Query Language**       | **SQL** (Structured Query Language)                                           | **Varies** — Mongo Query, CQL (Cassandra), custom APIs                                         |
| **Scalability**          | **Vertical scaling** (scale-up → bigger machine)                              | **Horizontal scaling** (scale-out → add more servers)                                          |
| **Transactions**         | **ACID compliant** (Atomicity, Consistency, Isolation, Durability — reliable) | **BASE** (Basically Available, Soft state, Eventual consistency — more flexible)               |
| **Best Suited For**      | **Structured** & **consistent** data (banking, ERP, CRM)                      | **Unstructured**, **semi-structured**, large, fast-changing data (social media, IoT, Big Data) |
| **Joins Support**        | **Supports joins** (multiple tables relations)                                | Generally **does not support joins** (except some graph DBs)                                   |
| **Data Integrity**       | **High integrity** (foreign keys, constraints)                                | Less strict, focuses on **speed & flexibility**                                                |
| **Performance**          | Best for **complex queries & transactions**                                   | Best for **fast reads/writes**, massive data, distributed systems                              |
| **Examples of Use-case** | Banking system, Inventory, HR system                                          | Chat apps, Content management, Recommendation systems, IoT                                     |


# Pig 
- run over the hadoop
- part of hadoop 
- used for data processing
- used for large complex data transformation , data analysis , data processing 
- uses its own lang pig latin
- good for batch processing 
- used for strucutred and unstructered data
- supports user defined function for complex task
- used to create data pipeline
- two way to exectire pig 
	- local mode
	- map reduce mode 
- with the help of grunt we can run pig

![[Pasted image 20250511010921.png]]

# Hive
- run over the hadoop
- used to query large data
- uses it own lang HiveQL
- used to hide complex hadoop complexity and give simple interface to user
- 