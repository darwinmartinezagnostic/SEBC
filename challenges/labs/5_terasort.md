´´´

	[saturn@ip-172-31-15-216 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort \
	> -Dmapreduce.job.maps=4 \
	> -Dmapreduce.job.reduces=12 \
	> -Dmapreduce.map.memory.mb=1024 \
	> -Dmapreduce.map.java.opts.max.heap=819 \
	> -Dmapreduce.reduce.memory.mb=1024 \
	> -Dmapreduce.reduce.java.opts.max.heap=819 \
	> tgen  \
	> tsort



	17/10/06 12:12:07 INFO terasort.TeraSort: starting
	17/10/06 12:12:09 INFO hdfs.DFSClient: Created token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AGNOSTIC.COM, renewer=yarn, realUser=, issueDate=1507306329572, maxDate=1507911129572, sequenceNumber=8, masterKeyId=4 on 172.31.15.216:8020
	17/10/06 12:12:09 INFO security.TokenCache: Got dt for hdfs://ip-172-31-15-216.us-west-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.15.216:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AGNOSTIC.COM, renewer=yarn, realUser=, issueDate=1507306329572, maxDate=1507911129572, sequenceNumber=8, masterKeyId=4)
	17/10/06 12:12:09 INFO input.FileInputFormat: Total input paths to process : 12
	Spent 345ms computing base-splits.
	Spent 7ms computing TeraScheduler splits.
	Computing input splits took 353ms
	Sampling 10 splits of 204
	Making 12 from 100000 sampled records
	Computing parititions took 844ms
	Spent 1199ms computing partitions.
	17/10/06 12:12:10 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-5-32.us-west-2.compute.internal/172.31.5.32:8032
	17/10/06 12:12:11 INFO mapreduce.JobSubmitter: number of splits:204
	17/10/06 12:12:11 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507302994609_0006
	17/10/06 12:12:11 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.15.216:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@AGNOSTIC.COM, renewer=yarn, realUser=, issueDate=1507306329572, maxDate=1507911129572, sequenceNumber=8, masterKeyId=4)
	17/10/06 12:12:12 INFO impl.YarnClientImpl: Submitted application application_1507302994609_0006
	17/10/06 12:12:12 INFO mapreduce.Job: The url to track the job: http://ip-172-31-5-32.us-west-2.compute.internal:8088/proxy/application_1507302994609_0006/
	17/10/06 12:12:12 INFO mapreduce.Job: Running job: job_1507302994609_0006
	17/10/06 12:12:26 INFO mapreduce.Job: Job job_1507302994609_0006 running in uber mode : false
	17/10/06 12:12:26 INFO mapreduce.Job:  map 0% reduce 0%
	17/10/06 12:12:42 INFO mapreduce.Job:  map 1% reduce 0%
	17/10/06 12:12:51 INFO mapreduce.Job:  map 2% reduce 0%
	17/10/06 12:12:52 INFO mapreduce.Job:  map 5% reduce 0%
	17/10/06 12:13:00 INFO mapreduce.Job:  map 6% reduce 0%
	17/10/06 12:13:01 INFO mapreduce.Job:  map 7% reduce 0%
	17/10/06 12:13:02 INFO mapreduce.Job:  map 8% reduce 0%
	17/10/06 12:13:06 INFO mapreduce.Job:  map 9% reduce 0%
	17/10/06 12:13:08 INFO mapreduce.Job:  map 12% reduce 0%
	17/10/06 12:13:12 INFO mapreduce.Job:  map 13% reduce 0%
	17/10/06 12:13:17 INFO mapreduce.Job:  map 14% reduce 0%
	17/10/06 12:13:18 INFO mapreduce.Job:  map 16% reduce 0%
	17/10/06 12:13:19 INFO mapreduce.Job:  map 22% reduce 0%
	17/10/06 12:13:24 INFO mapreduce.Job:  map 25% reduce 0%
	17/10/06 12:13:29 INFO mapreduce.Job:  map 26% reduce 0%
	17/10/06 12:13:30 INFO mapreduce.Job:  map 27% reduce 0%
	17/10/06 12:13:37 INFO mapreduce.Job:  map 28% reduce 0%
	17/10/06 12:13:38 INFO mapreduce.Job:  map 30% reduce 0%
	17/10/06 12:13:39 INFO mapreduce.Job:  map 35% reduce 0%
	17/10/06 12:13:40 INFO mapreduce.Job:  map 38% reduce 0%
	17/10/06 12:13:43 INFO mapreduce.Job:  map 39% reduce 0%
	17/10/06 12:13:49 INFO mapreduce.Job:  map 40% reduce 0%
	17/10/06 12:13:50 INFO mapreduce.Job:  map 41% reduce 0%
	17/10/06 12:13:55 INFO mapreduce.Job:  map 44% reduce 0%
	17/10/06 12:13:56 INFO mapreduce.Job:  map 45% reduce 0%
	17/10/06 12:13:57 INFO mapreduce.Job:  map 49% reduce 0%
	17/10/06 12:13:58 INFO mapreduce.Job:  map 51% reduce 0%
	17/10/06 12:13:59 INFO mapreduce.Job:  map 52% reduce 0%
	17/10/06 12:14:01 INFO mapreduce.Job:  map 53% reduce 0%
	17/10/06 12:14:07 INFO mapreduce.Job:  map 54% reduce 0%
	17/10/06 12:14:11 INFO mapreduce.Job:  map 57% reduce 0%
	17/10/06 12:14:13 INFO mapreduce.Job:  map 58% reduce 0%
	17/10/06 12:14:15 INFO mapreduce.Job:  map 62% reduce 0%
	17/10/06 12:14:17 INFO mapreduce.Job:  map 64% reduce 0%
	17/10/06 12:14:18 INFO mapreduce.Job:  map 66% reduce 0%
	17/10/06 12:14:20 INFO mapreduce.Job:  map 67% reduce 0%
	17/10/06 12:14:27 INFO mapreduce.Job:  map 71% reduce 0%
	17/10/06 12:14:32 INFO mapreduce.Job:  map 72% reduce 0%
	17/10/06 12:14:34 INFO mapreduce.Job:  map 75% reduce 0%
	17/10/06 12:14:35 INFO mapreduce.Job:  map 76% reduce 0%
	17/10/06 12:14:37 INFO mapreduce.Job:  map 79% reduce 0%
	17/10/06 12:14:38 INFO mapreduce.Job:  map 80% reduce 0%
	17/10/06 12:14:43 INFO mapreduce.Job:  map 83% reduce 0%
	17/10/06 12:14:44 INFO mapreduce.Job:  map 84% reduce 0%
	17/10/06 12:14:45 INFO mapreduce.Job:  map 85% reduce 0%
	17/10/06 12:14:53 INFO mapreduce.Job:  map 88% reduce 0%
	17/10/06 12:14:54 INFO mapreduce.Job:  map 89% reduce 0%
	17/10/06 12:14:54 INFO mapreduce.Job: Task Id : attempt_1507302994609_0006_r_000000_0, Status : FAILED
	Error: org.apache.hadoop.mapreduce.task.reduce.Shuffle$ShuffleError: error in shuffle in fetcher#4
		at org.apache.hadoop.mapreduce.task.reduce.Shuffle.run(Shuffle.java:134)
		at org.apache.hadoop.mapred.ReduceTask.run(ReduceTask.java:376)
		at org.apache.hadoop.mapred.YarnChild$2.run(YarnChild.java:164)
		at java.security.AccessController.doPrivileged(Native Method)
		at javax.security.auth.Subject.doAs(Subject.java:415)
		at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1920)
		at org.apache.hadoop.mapred.YarnChild.main(YarnChild.java:158)
	Caused by: java.io.IOException: Exceeded MAX_FAILED_UNIQUE_FETCHES; bailing-out.
		at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.checkReducerHealth(ShuffleSchedulerImpl.java:392)
		at org.apache.hadoop.mapreduce.task.reduce.ShuffleSchedulerImpl.copyFailed(ShuffleSchedulerImpl.java:307)
		at org.apache.hadoop.mapreduce.task.reduce.Fetcher.copyFromHost(Fetcher.java:366)
		at org.apache.hadoop.mapreduce.task.reduce.Fetcher.run(Fetcher.java:198)

	real	2m51.601s
	user	0m9.384s
	sys	0m0.413s
´´´
