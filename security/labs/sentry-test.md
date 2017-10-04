
```
**Conexion con un usuario con privilegios**

	[root@ip-172-31-3-136 ~]# kinit darwinmartinezagnostic
	Password for darwinmartinezagnostic@AGNOSTIC.COM: 
	[root@ip-172-31-3-136 ~]# beeline
	Beeline version 1.1.0-cdh5.11.2 by Apache Hive
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM
	scan complete in 2ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.11.2)
	Driver: Hive JDBC (version 1.1.0-cdh5.11.2)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20171004161010_dd0fdcf3-8dbe-4156-abdf-393601a0eb2d): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20171004161010_dd0fdcf3-8dbe-4156-abdf-393601a0eb2d); Time taken: 0.06 seconds
	INFO  : Executing command(queryId=hive_20171004161010_dd0fdcf3-8dbe-4156-abdf-393601a0eb2d): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20171004161010_dd0fdcf3-8dbe-4156-abdf-393601a0eb2d); Time taken: 0.126 seconds
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
	5 rows selected (0,294 seconds)
	0: jdbc:hive2://localhost:10000/default> !q
	Closing: 0: jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM

**Conexion con un usuario sin privilegios**

	[root@ip-172-31-3-136 ~]# kinit cloudera-scm
	Password for cloudera-scm@AGNOSTIC.COM: 
	[root@ip-172-31-3-136 ~]# beeline
	Beeline version 1.1.0-cdh5.11.2 by Apache Hive
	beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM
	scan complete in 1ms
	Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-3-136.us-west-2.compute.internal@AGNOSTIC.COM
	Connected to: Apache Hive (version 1.1.0-cdh5.11.2)
	Driver: Hive JDBC (version 1.1.0-cdh5.11.2)
	Transaction isolation: TRANSACTION_REPEATABLE_READ
	0: jdbc:hive2://localhost:10000/default> show tables;
	INFO  : Compiling command(queryId=hive_20171004161313_572d740b-1182-4776-9c2d-d8d4011dce4c): show tables
	INFO  : Semantic Analysis Completed
	INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
	INFO  : Completed compiling command(queryId=hive_20171004161313_572d740b-1182-4776-9c2d-d8d4011dce4c); Time taken: 0.061 seconds
	INFO  : Executing command(queryId=hive_20171004161313_572d740b-1182-4776-9c2d-d8d4011dce4c): show tables
	INFO  : Starting task [Stage-0:DDL] in serial mode
	INFO  : Completed executing command(queryId=hive_20171004161313_572d740b-1182-4776-9c2d-d8d4011dce4c); Time taken: 0.125 seconds
	INFO  : OK
	+-----------+--+
	| tab_name  |
	+-----------+--+
	+-----------+--+
	No rows selected (0,29 seconds)
	0: jdbc:hive2://localhost:10000/default>

```
