```
**Create an end-user Linux account named with your GitHub handle**

	**Make sure this Linux account is added to all cluster nodes**

	[ec2-user@ip-172-31-1-176 ~]$ sudo useradd -u 2800 darwinmartinezagnostic
	[ec2-user@ip-172-31-1-176 ~]$ sudo passwd darwinmartinezagnostic
	Cambiando la contraseña del usuario darwinmartinezagnostic.
	Nueva contraseña: 
	Vuelva a escribir la nueva contraseña: 
	passwd: todos los símbolos de autenticación se actualizaron con éxito.
	[ec2-user@ip-172-31-1-176 ~]$ 

	**Create an HDFS directory under /user**
	
	[ec2-user@ip-172-31-1-176 ~]$ sudo -u hdfs hdfs dfs -mkdir -p /user/darwinmartinezagnostic/
	[ec2-user@ip-172-31-1-176 ~]$ sudo -u hdfs hdfs dfs -chown darwinmartinezagnostic /user/darwinmartinezagnostic
	[ec2-user@ip-172-31-1-176 ~]$


**Create a 10 GB file using teragen**
[ec2-user@ip-172-31-1-176 ~]$ su darwinmartinezagnostic
Contraseña: 
[darwinmartinezagnostic@ip-172-31-1-176 ec2-user]$ cd
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen \
> -Ddfs.block.size=33554432 \
> -Dmapred.map.tasks=4 \
> 107374182 \
> tgen10gb
17/10/03 09:49:32 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-3-136.us-west-2.compute.internal/172.31.3.136:8032
17/10/03 09:49:32 INFO terasort.TeraGen: Generating 107374182 using 4
17/10/03 09:49:32 INFO mapreduce.JobSubmitter: number of splits:4
17/10/03 09:49:32 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/10/03 09:49:32 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/10/03 09:49:33 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507032320246_0002
17/10/03 09:49:33 INFO impl.YarnClientImpl: Submitted application application_1507032320246_0002
17/10/03 09:49:33 INFO mapreduce.Job: The url to track the job: http://ip-172-31-3-136.us-west-2.compute.internal:8088/proxy/application_1507032320246_0002/
17/10/03 09:49:33 INFO mapreduce.Job: Running job: job_1507032320246_0002
17/10/03 09:49:39 INFO mapreduce.Job: Job job_1507032320246_0002 running in uber mode : false
17/10/03 09:49:39 INFO mapreduce.Job:  map 0% reduce 0%
17/10/03 09:49:57 INFO mapreduce.Job:  map 4% reduce 0%
17/10/03 09:49:58 INFO mapreduce.Job:  map 14% reduce 0%
17/10/03 09:50:03 INFO mapreduce.Job:  map 19% reduce 0%
17/10/03 09:50:04 INFO mapreduce.Job:  map 21% reduce 0%
17/10/03 09:50:09 INFO mapreduce.Job:  map 24% reduce 0%
17/10/03 09:50:10 INFO mapreduce.Job:  map 25% reduce 0%
17/10/03 09:50:16 INFO mapreduce.Job:  map 26% reduce 0%
17/10/03 09:50:22 INFO mapreduce.Job:  map 27% reduce 0%
17/10/03 09:50:28 INFO mapreduce.Job:  map 28% reduce 0%
17/10/03 09:50:34 INFO mapreduce.Job:  map 32% reduce 0%
17/10/03 09:50:40 INFO mapreduce.Job:  map 37% reduce 0%
17/10/03 09:50:46 INFO mapreduce.Job:  map 42% reduce 0%
17/10/03 09:50:52 INFO mapreduce.Job:  map 48% reduce 0%
17/10/03 09:50:58 INFO mapreduce.Job:  map 51% reduce 0%
17/10/03 09:51:04 INFO mapreduce.Job:  map 52% reduce 0%
17/10/03 09:51:10 INFO mapreduce.Job:  map 56% reduce 0%
17/10/03 09:51:16 INFO mapreduce.Job:  map 60% reduce 0%
17/10/03 09:51:23 INFO mapreduce.Job:  map 62% reduce 0%
17/10/03 09:51:29 INFO mapreduce.Job:  map 63% reduce 0%
17/10/03 09:51:34 INFO mapreduce.Job:  map 64% reduce 0%
17/10/03 09:51:35 INFO mapreduce.Job:  map 68% reduce 0%
17/10/03 09:51:40 INFO mapreduce.Job:  map 70% reduce 0%
17/10/03 09:51:41 INFO mapreduce.Job:  map 72% reduce 0%
17/10/03 09:51:46 INFO mapreduce.Job:  map 74% reduce 0%
17/10/03 09:51:47 INFO mapreduce.Job:  map 75% reduce 0%
17/10/03 09:51:52 INFO mapreduce.Job:  map 78% reduce 0%
17/10/03 09:51:53 INFO mapreduce.Job:  map 79% reduce 0%
17/10/03 09:51:58 INFO mapreduce.Job:  map 81% reduce 0%
17/10/03 09:52:04 INFO mapreduce.Job:  map 87% reduce 0%
17/10/03 09:52:10 INFO mapreduce.Job:  map 88% reduce 0%
17/10/03 09:52:16 INFO mapreduce.Job:  map 91% reduce 0%
17/10/03 09:52:22 INFO mapreduce.Job:  map 94% reduce 0%
17/10/03 09:52:27 INFO mapreduce.Job:  map 95% reduce 0%
17/10/03 09:52:29 INFO mapreduce.Job:  map 100% reduce 0%
17/10/03 09:52:31 INFO mapreduce.Job: Job job_1507032320246_0002 completed successfully
17/10/03 09:52:31 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=513012
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=344
		HDFS: Number of bytes written=10737418200
		HDFS: Number of read operations=16
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=8
	Job Counters 
		Launched map tasks=4
		Other local map tasks=4
		Total time spent by all maps in occupied slots (ms)=668703
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=668703
		Total vcore-milliseconds taken by all map tasks=668703
		Total megabyte-milliseconds taken by all map tasks=684751872
	Map-Reduce Framework
		Map input records=107374182
		Map output records=107374182
		Input split bytes=344
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=1265
		CPU time spent (ms)=154740
		Physical memory (bytes) snapshot=779165696
		Virtual memory (bytes) snapshot=6386089984
		Total committed heap usage (bytes)=1573388288
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=230593859918397906
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=10737418200

real	3m1.359s
user	0m5.584s
sys	0m0.264s

**Run the terasort command on this file**
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort tgen10gb tsort10gb
17/10/03 09:57:49 INFO terasort.TeraSort: starting
17/10/03 09:57:51 INFO input.FileInputFormat: Total input paths to process : 4
Spent 225ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 232ms
Sampling 10 splits of 320
Making 12 from 100000 sampled records
Computing parititions took 694ms
Spent 929ms computing partitions.
17/10/03 09:57:52 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-3-136.us-west-2.compute.internal/172.31.3.136:8032
17/10/03 09:57:52 INFO mapreduce.JobSubmitter: number of splits:320
17/10/03 09:57:52 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1507032320246_0003
17/10/03 09:57:52 INFO impl.YarnClientImpl: Submitted application application_1507032320246_0003
17/10/03 09:57:52 INFO mapreduce.Job: The url to track the job: http://ip-172-31-3-136.us-west-2.compute.internal:8088/proxy/application_1507032320246_0003/
17/10/03 09:57:52 INFO mapreduce.Job: Running job: job_1507032320246_0003
17/10/03 09:57:59 INFO mapreduce.Job: Job job_1507032320246_0003 running in uber mode : false
17/10/03 09:57:59 INFO mapreduce.Job:  map 0% reduce 0%
17/10/03 09:58:07 INFO mapreduce.Job:  map 1% reduce 0%
17/10/03 09:58:11 INFO mapreduce.Job:  map 2% reduce 0%
17/10/03 09:58:12 INFO mapreduce.Job:  map 4% reduce 0%
17/10/03 09:58:13 INFO mapreduce.Job:  map 5% reduce 0%
17/10/03 09:58:15 INFO mapreduce.Job:  map 6% reduce 0%
17/10/03 09:58:20 INFO mapreduce.Job:  map 7% reduce 0%
17/10/03 09:58:22 INFO mapreduce.Job:  map 8% reduce 0%
17/10/03 09:58:23 INFO mapreduce.Job:  map 9% reduce 0%
17/10/03 09:58:24 INFO mapreduce.Job:  map 11% reduce 0%
17/10/03 09:58:25 INFO mapreduce.Job:  map 12% reduce 0%
17/10/03 09:58:28 INFO mapreduce.Job:  map 13% reduce 0%
17/10/03 09:58:35 INFO mapreduce.Job:  map 15% reduce 0%
17/10/03 09:58:36 INFO mapreduce.Job:  map 16% reduce 0%
17/10/03 09:58:37 INFO mapreduce.Job:  map 18% reduce 0%
17/10/03 09:58:43 INFO mapreduce.Job:  map 19% reduce 0%
17/10/03 09:58:46 INFO mapreduce.Job:  map 21% reduce 0%
17/10/03 09:58:47 INFO mapreduce.Job:  map 22% reduce 0%
17/10/03 09:58:49 INFO mapreduce.Job:  map 23% reduce 0%
17/10/03 09:58:50 INFO mapreduce.Job:  map 24% reduce 0%
17/10/03 09:58:55 INFO mapreduce.Job:  map 25% reduce 0%
17/10/03 09:58:56 INFO mapreduce.Job:  map 26% reduce 0%
17/10/03 09:58:57 INFO mapreduce.Job:  map 28% reduce 0%
17/10/03 09:59:01 INFO mapreduce.Job:  map 29% reduce 0%
17/10/03 09:59:03 INFO mapreduce.Job:  map 30% reduce 0%
17/10/03 09:59:05 INFO mapreduce.Job:  map 31% reduce 0%
17/10/03 09:59:07 INFO mapreduce.Job:  map 32% reduce 0%
17/10/03 09:59:09 INFO mapreduce.Job:  map 33% reduce 0%
17/10/03 09:59:10 INFO mapreduce.Job:  map 34% reduce 0%
17/10/03 09:59:11 INFO mapreduce.Job:  map 35% reduce 0%
17/10/03 09:59:12 INFO mapreduce.Job:  map 36% reduce 0%
17/10/03 09:59:18 INFO mapreduce.Job:  map 38% reduce 0%
17/10/03 09:59:19 INFO mapreduce.Job:  map 39% reduce 0%
17/10/03 09:59:20 INFO mapreduce.Job:  map 40% reduce 0%
17/10/03 09:59:22 INFO mapreduce.Job:  map 41% reduce 0%
17/10/03 09:59:26 INFO mapreduce.Job:  map 42% reduce 0%
17/10/03 09:59:28 INFO mapreduce.Job:  map 43% reduce 0%
17/10/03 09:59:30 INFO mapreduce.Job:  map 44% reduce 0%
17/10/03 09:59:31 INFO mapreduce.Job:  map 45% reduce 0%
17/10/03 09:59:33 INFO mapreduce.Job:  map 47% reduce 0%
17/10/03 09:59:37 INFO mapreduce.Job:  map 48% reduce 0%
17/10/03 09:59:40 INFO mapreduce.Job:  map 49% reduce 0%
17/10/03 09:59:41 INFO mapreduce.Job:  map 50% reduce 0%
17/10/03 09:59:42 INFO mapreduce.Job:  map 51% reduce 0%
17/10/03 09:59:43 INFO mapreduce.Job:  map 52% reduce 0%
17/10/03 09:59:46 INFO mapreduce.Job:  map 53% reduce 0%
17/10/03 09:59:47 INFO mapreduce.Job:  map 54% reduce 0%
17/10/03 09:59:50 INFO mapreduce.Job:  map 55% reduce 0%
17/10/03 09:59:53 INFO mapreduce.Job:  map 57% reduce 0%
17/10/03 09:59:55 INFO mapreduce.Job:  map 58% reduce 0%
17/10/03 09:59:57 INFO mapreduce.Job:  map 59% reduce 0%
17/10/03 09:59:59 INFO mapreduce.Job:  map 60% reduce 0%
17/10/03 10:00:01 INFO mapreduce.Job:  map 61% reduce 0%
17/10/03 10:00:02 INFO mapreduce.Job:  map 62% reduce 0%
17/10/03 10:00:03 INFO mapreduce.Job:  map 63% reduce 0%
17/10/03 10:00:07 INFO mapreduce.Job:  map 64% reduce 0%
17/10/03 10:00:08 INFO mapreduce.Job:  map 66% reduce 0%
17/10/03 10:00:13 INFO mapreduce.Job:  map 67% reduce 0%
17/10/03 10:00:14 INFO mapreduce.Job:  map 68% reduce 0%
17/10/03 10:00:15 INFO mapreduce.Job:  map 69% reduce 0%
17/10/03 10:00:18 INFO mapreduce.Job:  map 70% reduce 0%
17/10/03 10:00:19 INFO mapreduce.Job:  map 71% reduce 0%
17/10/03 10:00:23 INFO mapreduce.Job:  map 73% reduce 0%
17/10/03 10:00:25 INFO mapreduce.Job:  map 74% reduce 0%
17/10/03 10:00:28 INFO mapreduce.Job:  map 75% reduce 0%
17/10/03 10:00:30 INFO mapreduce.Job:  map 77% reduce 0%
17/10/03 10:00:33 INFO mapreduce.Job:  map 78% reduce 0%
17/10/03 10:00:35 INFO mapreduce.Job:  map 79% reduce 0%
17/10/03 10:00:37 INFO mapreduce.Job:  map 81% reduce 0%
17/10/03 10:00:40 INFO mapreduce.Job:  map 82% reduce 0%
17/10/03 10:00:41 INFO mapreduce.Job:  map 83% reduce 0%
17/10/03 10:00:43 INFO mapreduce.Job:  map 84% reduce 0%
17/10/03 10:00:46 INFO mapreduce.Job:  map 85% reduce 0%
17/10/03 10:00:48 INFO mapreduce.Job:  map 86% reduce 0%
17/10/03 10:00:51 INFO mapreduce.Job:  map 87% reduce 0%
17/10/03 10:00:59 INFO mapreduce.Job:  map 87% reduce 5%
17/10/03 10:01:00 INFO mapreduce.Job:  map 88% reduce 9%
17/10/03 10:01:01 INFO mapreduce.Job:  map 89% reduce 16%
17/10/03 10:01:03 INFO mapreduce.Job:  map 89% reduce 21%
17/10/03 10:01:04 INFO mapreduce.Job:  map 89% reduce 24%
17/10/03 10:01:05 INFO mapreduce.Job:  map 89% reduce 26%
17/10/03 10:01:06 INFO mapreduce.Job:  map 89% reduce 27%
17/10/03 10:01:08 INFO mapreduce.Job:  map 90% reduce 27%
17/10/03 10:01:09 INFO mapreduce.Job:  map 91% reduce 27%
17/10/03 10:01:13 INFO mapreduce.Job:  map 91% reduce 28%
17/10/03 10:01:14 INFO mapreduce.Job:  map 92% reduce 28%
17/10/03 10:01:17 INFO mapreduce.Job:  map 93% reduce 28%
17/10/03 10:01:22 INFO mapreduce.Job:  map 94% reduce 28%
17/10/03 10:01:24 INFO mapreduce.Job:  map 94% reduce 29%
17/10/03 10:01:25 INFO mapreduce.Job:  map 95% reduce 29%
17/10/03 10:01:28 INFO mapreduce.Job:  map 96% reduce 29%
17/10/03 10:01:31 INFO mapreduce.Job:  map 97% reduce 29%
17/10/03 10:01:33 INFO mapreduce.Job:  map 98% reduce 29%
17/10/03 10:01:36 INFO mapreduce.Job:  map 98% reduce 30%
17/10/03 10:01:38 INFO mapreduce.Job:  map 99% reduce 30%
17/10/03 10:01:43 INFO mapreduce.Job:  map 100% reduce 30%
17/10/03 10:01:44 INFO mapreduce.Job:  map 100% reduce 31%
17/10/03 10:01:46 INFO mapreduce.Job:  map 100% reduce 35%
17/10/03 10:01:47 INFO mapreduce.Job:  map 100% reduce 38%
17/10/03 10:01:48 INFO mapreduce.Job:  map 100% reduce 47%
17/10/03 10:01:49 INFO mapreduce.Job:  map 100% reduce 61%
17/10/03 10:01:50 INFO mapreduce.Job:  map 100% reduce 64%
17/10/03 10:01:52 INFO mapreduce.Job:  map 100% reduce 66%
17/10/03 10:01:53 INFO mapreduce.Job:  map 100% reduce 71%
17/10/03 10:01:54 INFO mapreduce.Job:  map 100% reduce 74%
17/10/03 10:01:55 INFO mapreduce.Job:  map 100% reduce 80%
17/10/03 10:01:56 INFO mapreduce.Job:  map 100% reduce 81%
17/10/03 10:01:58 INFO mapreduce.Job:  map 100% reduce 83%
17/10/03 10:01:59 INFO mapreduce.Job:  map 100% reduce 86%
17/10/03 10:02:00 INFO mapreduce.Job:  map 100% reduce 88%
17/10/03 10:02:01 INFO mapreduce.Job:  map 100% reduce 90%
17/10/03 10:02:02 INFO mapreduce.Job:  map 100% reduce 91%
17/10/03 10:02:06 INFO mapreduce.Job:  map 100% reduce 92%
17/10/03 10:02:07 INFO mapreduce.Job:  map 100% reduce 93%
17/10/03 10:02:10 INFO mapreduce.Job:  map 100% reduce 95%
17/10/03 10:02:11 INFO mapreduce.Job:  map 100% reduce 96%
17/10/03 10:02:12 INFO mapreduce.Job:  map 100% reduce 97%
17/10/03 10:02:14 INFO mapreduce.Job:  map 100% reduce 99%
17/10/03 10:02:17 INFO mapreduce.Job:  map 100% reduce 100%
17/10/03 10:02:18 INFO mapreduce.Job: Job job_1507032320246_0003 completed successfully
17/10/03 10:02:18 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=4770335937
		FILE: Number of bytes written=9476404623
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10737472280
		HDFS: Number of bytes written=10737418200
		HDFS: Number of read operations=996
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=24
	Job Counters 
		Launched map tasks=320
		Launched reduce tasks=12
		Data-local map tasks=320
		Total time spent by all maps in occupied slots (ms)=2697866
		Total time spent by all reduces in occupied slots (ms)=1000818
		Total time spent by all map tasks (ms)=2697866
		Total time spent by all reduce tasks (ms)=1000818
		Total vcore-milliseconds taken by all map tasks=2697866
		Total vcore-milliseconds taken by all reduce tasks=1000818
		Total megabyte-milliseconds taken by all map tasks=2762614784
		Total megabyte-milliseconds taken by all reduce tasks=1024837632
	Map-Reduce Framework
		Map input records=107374182
		Map output records=107374182
		Map output bytes=10952166564
		Map output materialized bytes=4662963282
		Input split bytes=54080
		Combine input records=0
		Combine output records=0
		Reduce input groups=107374182
		Reduce shuffle bytes=4662963282
		Reduce input records=107374182
		Reduce output records=107374182
		Spilled Records=214748364
		Shuffled Maps =3840
		Failed Shuffles=0
		Merged Map outputs=3840
		GC time elapsed (ms)=44837
		CPU time spent (ms)=1624430
		Physical memory (bytes) snapshot=177513975808
		Virtual memory (bytes) snapshot=530669502464
		Total committed heap usage (bytes)=177572151296
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=10737418200
	File Output Format Counters 
		Bytes Written=10737418200
17/10/03 10:02:18 INFO terasort.TeraSort: done

real	4m29.921s
user	0m9.117s
sys	0m0.377s



```
