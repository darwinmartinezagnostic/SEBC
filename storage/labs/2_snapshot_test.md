```

**Create a precious directory in HDFS; copy the ZIP course file into it.**
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ hdfs dfs -mkdir precious
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ hdfs dfs -put SEBC-master-students.zip precious/
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ hdfs dfs -ls /user/darwinmartinezagnostic/precious
Found 1 items
-rw-r--r--   3 darwinmartinezagnostic supergroup     474831 2017-10-03 10:20 /user/darwinmartinezagnostic/precious/SEBC-master-students.zip


**Enable snapshots for precious**
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ sudo -u hdfs hdfs dfsadmin -allowSnapshot /user/darwinmartinezagnostic/precious
Allowing snaphot on /user/darwinmartinezagnostic/precious succeeded

**Create a snapshot called sebc-hdfs-test**
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ sudo -u hdfs hdfs dfs -createSnapshot /user/darwinmartinezagnostic/precious sebc-hdfs-test
Created snapshot /user/darwinmartinezagnostic/precious/.snapshot/sebc-hdfs-test

**Delete the directory**
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ hdfs dfs -rm -R /user/darwinmartinezagnostic/precious
rm: Failed to move to trash: hdfs://ip-172-31-1-176.us-west-2.compute.internal:8020/user/darwinmartinezagnostic/precious: The directory /user/darwinmartinezagnostic/precious cannot be deleted since /user/darwinmartinezagnostic/precious is snapshottable and already has snapshots

**Delete the ZIP file**
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ hdfs dfs -ls /user/darwinmartinezagnostic/precious
Found 1 items
-rw-r--r--   3 darwinmartinezagnostic supergroup     474831 2017-10-03 10:20 /user/darwinmartinezagnostic/precious/SEBC-master-students.zip
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ hdfs dfs -rm /user/darwinmartinezagnostic/precious/SEBC-master-students.zip
17/10/03 10:44:03 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-1-176.us-west-2.compute.internal:8020/user/darwinmartinezagnostic/precious/SEBC-master-students.zip' to trash at: hdfs://ip-172-31-1-176.us-west-2.compute.internal:8020/user/darwinmartinezagnostic/.Trash/Current/user/darwinmartinezagnostic/precious/SEBC-master-students.zip
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ hdfs dfs -ls /user/darwinmartinezagnostic/precious

**Restore the deleted file**
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ sudo -u hdfs hdfs dfs -cp /user/darwinmartinezagnostic/precious/.snapshot/sebc-hdfs-test/SEBC-master-students.zip /user/darwinmartinezagnostic/precious
[darwinmartinezagnostic@ip-172-31-1-176 ~]$ hdfs dfs -ls /user/darwinmartinezagnostic/precious
Found 1 items
-rw-r--r--   3 hdfs supergroup     474831 2017-10-03 10:50 /user/darwinmartinezagnostic/precious/SEBC-master-students.zip
[darwinmartinezagnostic@ip-172-31-1-176 ~]$


 

```
