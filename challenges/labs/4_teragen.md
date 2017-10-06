```
##The full teragen command and output

	time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.block.size=33554432 -Dmapred.map.tasks=12 -Dmapreduce.map.memory.mb=512 65536000 tgen
	17/10/06 09:19:17 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-5-32.us-west-2.compute.internal/172.31.5.32:8032
	17/10/06 09:19:18 INFO terasort.TeraSort: Generating 65536000 using 12
	17/10/06 09:19:18 INFO mapreduce.JobSubmitter: number of splits:12
	17/10/06 09:19:18 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
	17/10/06 09:19:18 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
	17/10/06 09:19:18 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507294723703_0002
	17/10/06 09:19:18 INFO impl.YarnClientImpl: Submitted application application_1507294723703_0002
	17/10/06 09:19:18 INFO mapreduce.Job: The url to track the job: http://ip-172-31-5-32.us-west-2.compute.internal:8088/proxy/application_1507294723703_0002/
	17/10/06 09:19:18 INFO mapreduce.Job: Running job: job_1507294723703_0002
	17/10/06 09:19:23 INFO mapreduce.Job: Job job_1507294723703_0002 running in uber mode : false
	17/10/06 09:19:23 INFO mapreduce.Job:  map 0% reduce 0%
	17/10/06 09:19:36 INFO mapreduce.Job:  map 13% reduce 0%
	17/10/06 09:19:37 INFO mapreduce.Job:  map 18% reduce 0%
	17/10/06 09:19:39 INFO mapreduce.Job:  map 26% reduce 0%
	17/10/06 09:19:40 INFO mapreduce.Job:  map 29% reduce 0%
	17/10/06 09:19:42 INFO mapreduce.Job:  map 35% reduce 0%
	17/10/06 09:19:43 INFO mapreduce.Job:  map 37% reduce 0%
	17/10/06 09:19:45 INFO mapreduce.Job:  map 42% reduce 0%
	17/10/06 09:19:46 INFO mapreduce.Job:  map 46% reduce 0%
	17/10/06 09:19:48 INFO mapreduce.Job:  map 52% reduce 0%
	17/10/06 09:19:49 INFO mapreduce.Job:  map 54% reduce 0%
	17/10/06 09:19:51 INFO mapreduce.Job:  map 57% reduce 0%
	17/10/06 09:19:52 INFO mapreduce.Job:  map 58% reduce 0%
	17/10/06 09:19:54 INFO mapreduce.Job:  map 61% reduce 0%
	17/10/06 09:19:55 INFO mapreduce.Job:  map 62% reduce 0%
	17/10/06 09:19:57 INFO mapreduce.Job:  map 64% reduce 0%
	17/10/06 09:19:58 INFO mapreduce.Job:  map 66% reduce 0%
	17/10/06 09:20:00 INFO mapreduce.Job:  map 68% reduce 0%
	17/10/06 09:20:01 INFO mapreduce.Job:  map 69% reduce 0%
	17/10/06 09:20:03 INFO mapreduce.Job:  map 70% reduce 0%
	17/10/06 09:20:04 INFO mapreduce.Job:  map 72% reduce 0%
	17/10/06 09:20:05 INFO mapreduce.Job:  map 73% reduce 0%
	17/10/06 09:20:10 INFO mapreduce.Job:  map 76% reduce 0%
	17/10/06 09:20:11 INFO mapreduce.Job:  map 77% reduce 0%
	17/10/06 09:20:13 INFO mapreduce.Job:  map 79% reduce 0%
	17/10/06 09:20:20 INFO mapreduce.Job:  map 81% reduce 0%
	17/10/06 09:20:21 INFO mapreduce.Job:  map 82% reduce 0%
	17/10/06 09:20:22 INFO mapreduce.Job:  map 87% reduce 0%
	17/10/06 09:20:24 INFO mapreduce.Job:  map 88% reduce 0%
	17/10/06 09:20:25 INFO mapreduce.Job:  map 91% reduce 0%
	17/10/06 09:20:26 INFO mapreduce.Job:  map 92% reduce 0%
	17/10/06 09:20:28 INFO mapreduce.Job:  map 95% reduce 0%
	17/10/06 09:20:29 INFO mapreduce.Job:  map 96% reduce 0%
	17/10/06 09:20:30 INFO mapreduce.Job:  map 97% reduce 0%
	17/10/06 09:20:31 INFO mapreduce.Job:  map 100% reduce 0%
	17/10/06 09:20:33 INFO mapreduce.Job: Job job_1507294723703_0002 completed successfully
	17/10/06 09:20:33 INFO mapreduce.Job: Counters: 31
		File System Counters
			FILE: Number of bytes read=0
			FILE: Number of bytes written=1484410
			FILE: Number of read operations=0
			FILE: Number of large read operations=0
			FILE: Number of write operations=0
			HDFS: Number of bytes read=1025
			HDFS: Number of bytes written=6553600000
			HDFS: Number of read operations=48
			HDFS: Number of large read operations=0
			HDFS: Number of write operations=24
		Job Counters 
			Launched map tasks=12
			Other local map tasks=12
			Total time spent by all maps in occupied slots (ms)=755482
			Total time spent by all reduces in occupied slots (ms)=0
			Total time spent by all map tasks (ms)=755482
			Total vcore-seconds taken by all map tasks=755482
			Total megabyte-seconds taken by all map tasks=773613568
		Map-Reduce Framework
			Map input records=65536000
			Map output records=65536000
			Input split bytes=1025
			Spilled Records=0
			Failed Shuffles=0
			Merged Map outputs=0
			GC time elapsed (ms)=2386
			CPU time spent (ms)=144240
			Physical memory (bytes) snapshot=2442653696
			Virtual memory (bytes) snapshot=13840896000
			Total committed heap usage (bytes)=4454350848
		org.apache.hadoop.examples.terasort.TeraGen$Counters
			CHECKSUM=140750829423462787
		File Input Format Counters 
			Bytes Read=0
		File Output Format Counters 
			Bytes Written=6553600000

##The result of the time command
	real	1m18.070s
	user	0m4.871s
	sys	0m0.273s

##The command and output of hdfs dfs -ls /user/saturn/tgen
	[saturn@ip-172-31-15-216 ~]$ hdfs dfs -ls /user/saturn/tgen
	Found 13 items
	-rw-r--r--   3 saturn supergroup          0 2017-10-06 09:20 /user/saturn/tgen/_SUCCESS
	-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 09:20 /user/saturn/tgen/part-m-00000
	-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:20 /user/saturn/tgen/part-m-00001
	-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:20 /user/saturn/tgen/part-m-00002
	-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 09:20 /user/saturn/tgen/part-m-00003
	-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:20 /user/saturn/tgen/part-m-00004
	-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:20 /user/saturn/tgen/part-m-00005
	-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 09:20 /user/saturn/tgen/part-m-00006
	-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:20 /user/saturn/tgen/part-m-00007
	-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:20 /user/saturn/tgen/part-m-00008
	-rw-r--r--   3 saturn supergroup  546133400 2017-10-06 09:20 /user/saturn/tgen/part-m-00009
	-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:20 /user/saturn/tgen/part-m-00010
	-rw-r--r--   3 saturn supergroup  546133300 2017-10-06 09:20 /user/saturn/tgen/part-m-00011


##The command and output of hadoop fsck -blocks /user/saturn
	[saturn@ip-172-31-15-216 ~]$ hdfs fsck /user/saturn -blocks
	Connecting to namenode via http://ip-172-31-15-216.us-west-2.compute.internal:50070
	FSCK started by saturn (auth:SIMPLE) from /172.31.15.216 for path /user/saturn at Fri Oct 06 09:28:51 EDT 2017
	.............Status: HEALTHY
	 Total size:	6553600000 B
	 Total dirs:	3
	 Total files:	13
	 Total symlinks:		0
	 Total blocks (validated):	204 (avg. block size 32125490 B)
	 Minimally replicated blocks:	204 (100.0 %)
	 Over-replicated blocks:	0 (0.0 %)
	 Under-replicated blocks:	0 (0.0 %)
	 Mis-replicated blocks:		0 (0.0 %)
	 Default replication factor:	3
	 Average block replication:	3.0
	 Corrupt blocks:		0
	 Missing replicas:		0 (0.0 %)
	 Number of data-nodes:		4
	 Number of racks:		1
	FSCK ended at Fri Oct 06 09:28:51 EDT 2017 in 12 milliseconds


	The filesystem under path '/user/saturn' is HEALTHY

```
