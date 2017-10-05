
```
**Conexion con unusuario george**

	[root@ip-172-31-3-136 ~]# kinit george
	Password for george@AGNOSTIC.COM: 
	[root@ip-172-31-3-136 ~]# beeline
	Beeline version 1.1.0-cdh5.11.2 by Apache Hive
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM
	scan complete in 2ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.11.2)
	Driver: Hive JDBC (version 1.1.0-cdh5.11.2)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20171004163939_4f233161-d63b-4d09-8c53-61a588893197): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20171004163939_4f233161-d63b-4d09-8c53-61a588893197); Time taken: 0.061 seconds
	INFO  : Executing command(queryId=hive_20171004163939_4f233161-d63b-4d09-8c53-61a588893197): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20171004163939_4f233161-d63b-4d09-8c53-61a588893197); Time taken: 0.127 seconds
	INFO  : OK
	+-------------+--+
	|  tab_name   |
	+-------------+--+
	| customers   |
	| sample_07   |
	| sample_08   |
	| web_logs    |
	| web_logs_1  |
	+-------------+--+
	5 rows selected (0,295 seconds)
	0: jdbc:hive2://localhost:10000/default> 


**Conexion con usuario ferdinand**

	[root@ip-172-31-3-136 ~]# kinit ferdinand
	Password for ferdinand@AGNOSTIC.COM: 
	[root@ip-172-31-3-136 ~]# beeline
	Beeline version 1.1.0-cdh5.11.2 by Apache Hive
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM
	scan complete in 2ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.11.2)
	Driver: Hive JDBC (version 1.1.0-cdh5.11.2)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20171004164141_476026df-216f-4a1c-8963-aeef9e23b0d4): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20171004164141_476026df-216f-4a1c-8963-aeef9e23b0d4); Time taken: 0.061 seconds
	INFO  : Executing command(queryId=hive_20171004164141_476026df-216f-4a1c-8963-aeef9e23b0d4): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20171004164141_476026df-216f-4a1c-8963-aeef9e23b0d4); Time taken: 0.129 seconds
	INFO  : OK
	+------------+--+
	|  tab_name  |
	+------------+--+
	| sample_07  |
	+------------+--+
	1 row selected (0,3 seconds)
	0: jdbc:hive2://localhost:10000/default> 

```
