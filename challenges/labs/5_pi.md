´´´
##Run the Hadoop pi program as user haley

	[haley@ip-172-31-15-216 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 10 100
	Number of Maps  = 10
	Samples per Map = 100
	Wrote input for Map #0
	Wrote input for Map #1
	Wrote input for Map #2
	Wrote input for Map #3
	Wrote input for Map #4
	Wrote input for Map #5
	Wrote input for Map #6
	Wrote input for Map #7
	Wrote input for Map #8
	Wrote input for Map #9
	Starting Job
	17/10/06 10:48:31 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-5-32.us-west-2.compute.internal/172.31.5.32:8032
	17/10/06 10:48:31 INFO hdfs.DFSClient: Created token for haley: HDFS_DELEGATION_TOKEN owner=haley@AGNOSTIC.COM, renewer=yarn, realUser=, issueDate=1507301311867, maxDate=1507906111867, sequenceNumber=1, masterKeyId=2 on 172.31.15.216:8020
	17/10/06 10:48:31 INFO security.TokenCache: Got dt for hdfs://ip-172-31-15-216.us-west-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.15.216:8020, Ident: (token for haley: HDFS_DELEGATION_TOKEN owner=haley@AGNOSTIC.COM, renewer=yarn, realUser=, issueDate=1507301311867, maxDate=1507906111867, sequenceNumber=1, masterKeyId=2)
	17/10/06 10:48:32 INFO input.FileInputFormat: Total input paths to process : 10
	17/10/06 10:48:32 INFO mapreduce.JobSubmitter: number of splits:10
	17/10/06 10:48:32 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507299452919_0001
	17/10/06 10:48:32 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.15.216:8020, Ident: (token for haley: HDFS_DELEGATION_TOKEN owner=haley@AGNOSTIC.COM, renewer=yarn, realUser=, issueDate=1507301311867, maxDate=1507906111867, sequenceNumber=1, masterKeyId=2)
	17/10/06 10:48:33 INFO impl.YarnClientImpl: Submitted application application_1507299452919_0001
	17/10/06 10:48:33 INFO mapreduce.Job: The url to track the job: http://ip-172-31-5-32.us-west-2.compute.internal:8088/proxy/application_1507299452919_0001/
	17/10/06 10:48:33 INFO mapreduce.Job: Running job: job_1507299452919_0001
	17/10/06 10:48:41 INFO mapreduce.Job: Job job_1507299452919_0001 running in uber mode : false
	17/10/06 10:48:41 INFO mapreduce.Job:  map 0% reduce 0%
	17/10/06 10:48:46 INFO mapreduce.Job:  map 10% reduce 0%
	17/10/06 10:48:52 INFO mapreduce.Job:  map 50% reduce 0%
	17/10/06 10:48:54 INFO mapreduce.Job:  map 100% reduce 0%
	17/10/06 10:48:59 INFO mapreduce.Job:  map 100% reduce 100%
	17/10/06 10:48:59 INFO mapreduce.Job: Job job_1507299452919_0001 completed successfully
	17/10/06 10:48:59 INFO mapreduce.Job: Counters: 50
		File System Counters
			FILE: Number of bytes read=84
			FILE: Number of bytes written=1376892
			FILE: Number of read operations=0
			FILE: Number of large read operations=0
			FILE: Number of write operations=0
			HDFS: Number of bytes read=2980
			HDFS: Number of bytes written=215
			HDFS: Number of read operations=43
			HDFS: Number of large read operations=0
			HDFS: Number of write operations=3
		Job Counters 
			Launched map tasks=10
			Launched reduce tasks=1
			Data-local map tasks=9
			Rack-local map tasks=1
			Total time spent by all maps in occupied slots (ms)=90708
			Total time spent by all reduces in occupied slots (ms)=3183
			Total time spent by all map tasks (ms)=90708
			Total time spent by all reduce tasks (ms)=3183
			Total vcore-seconds taken by all map tasks=90708
			Total vcore-seconds taken by all reduce tasks=3183
			Total megabyte-seconds taken by all map tasks=92884992
			Total megabyte-seconds taken by all reduce tasks=3259392
		Map-Reduce Framework
			Map input records=10
			Map output records=20
			Map output bytes=180
			Map output materialized bytes=340
			Input split bytes=1800
			Combine input records=0
			Combine output records=0
			Reduce input groups=2
			Reduce shuffle bytes=340
			Reduce input records=20
			Reduce output records=0
			Spilled Records=40
			Shuffled Maps =10
			Failed Shuffles=0
			Merged Map outputs=10
			GC time elapsed (ms)=334
			CPU time spent (ms)=7630
			Physical memory (bytes) snapshot=5171302400
			Virtual memory (bytes) snapshot=17562193920
			Total committed heap usage (bytes)=5138546688
		Shuffle Errors
			BAD_ID=0
			CONNECTION=0
			IO_ERROR=0
			WRONG_LENGTH=0
			WRONG_MAP=0
			WRONG_REDUCE=0
		File Input Format Counters 
			Bytes Read=1180
		File Output Format Counters 
			Bytes Written=97
	Job Finished in 27.851 seconds
	Estimated value of Pi is 3.14800000000000000000

	real	0m30.708s
	user	0m5.073s
	sys	0m0.261s

´´´
