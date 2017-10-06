```
##The command and output for hdfs dfs -ls /user

	[ec2-user@ip-172-31-15-216 ~]$ hdfs dfs -ls /user
	Found 7 items
	drwxr-xr-x   - haley  supergroup          0 2017-10-06 09:03 /user/haley
	drwxrwxrwx   - mapred hadoop              0 2017-10-06 08:58 /user/history
	drwxrwxr-t   - hive   hive                0 2017-10-06 08:59 /user/hive
	drwxrwxr-x   - hue    hue                 0 2017-10-06 09:00 /user/hue
	drwxrwxr-x   - oozie  oozie               0 2017-10-06 09:00 /user/oozie
	drwxr-xr-x   - saturn supergroup          0 2017-10-06 09:03 /user/saturn
	drwxr-x--x   - spark  spark               0 2017-10-06 08:59 /user/spark


##The command and output from the CM API call ../api/v14/hosts
	[ec2-user@ip-172-31-7-128 ~]$ curl -u admin:admin 'http://localhost:7180/api/v14/hosts'
	{
	  "items" : [ {
	    "hostId" : "5407c936-d4c5-44ca-a4ae-789f249ce6d6",
	    "ipAddress" : "172.31.10.49",
	    "hostname" : "ip-172-31-10-49.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/hostRedirect/5407c936-d4c5-44ca-a4ae-789f249ce6d6",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 31185788928
	  }, {
	    "hostId" : "b02437d7-31ba-446f-954b-c17b13773866",
	    "ipAddress" : "172.31.15.216",
	    "hostname" : "ip-172-31-15-216.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/hostRedirect/b02437d7-31ba-446f-954b-c17b13773866",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 31185788928
	  }, {
	    "hostId" : "711e697b-872e-4172-b4c2-2c491dc7a0d7",
	    "ipAddress" : "172.31.4.137",
	    "hostname" : "ip-172-31-4-137.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/hostRedirect/711e697b-872e-4172-b4c2-2c491dc7a0d7",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 31185788928
	  }, {
	    "hostId" : "4c052c13-5714-4e53-a4b6-457cbb0a7aad",
	    "ipAddress" : "172.31.5.32",
	    "hostname" : "ip-172-31-5-32.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/hostRedirect/4c052c13-5714-4e53-a4b6-457cbb0a7aad",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 31185788928
	  }, {
	    "hostId" : "51be2b48-48db-467d-8202-5aaec423c169",
	    "ipAddress" : "172.31.7.128",
	    "hostname" : "ip-172-31-7-128.us-west-2.compute.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/hostRedirect/51be2b48-48db-467d-8202-5aaec423c169",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 31185788928
	  } ]
	}

##The command and output from the CM API call ../api/v8/clusters/<githubName>/services

	[ec2-user@ip-172-31-7-128 ~]$ curl -u admin:admin 'http://localhost:7180/api/v8/clusters/darwinmartinezagnostic/services'
	{
	  "items" : [ {
	    "name" : "hive",
	    "type" : "HIVE",
	    "clusterRef" : {
	      "clusterName" : "cluster"
	    },
	    "serviceUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
	    "serviceState" : "STARTED",
	    "healthSummary" : "GOOD",
	    "healthChecks" : [ {
	      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
	      "summary" : "GOOD"
	    }, {
	      "name" : "HIVE_HIVESERVER2S_HEALTHY",
	      "summary" : "GOOD"
	    } ],
	    "configStalenessStatus" : "FRESH",
	    "clientConfigStalenessStatus" : "FRESH",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "displayName" : "Hive"
	  }, {
	    "name" : "zookeeper",
	    "type" : "ZOOKEEPER",
	    "clusterRef" : {
	      "clusterName" : "cluster"
	    },
	    "serviceUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/serviceRedirect/zookeeper",
	    "serviceState" : "STARTED",
	    "healthSummary" : "GOOD",
	    "healthChecks" : [ {
	      "name" : "ZOOKEEPER_CANARY_HEALTH",
	      "summary" : "GOOD"
	    }, {
	      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
	      "summary" : "GOOD"
	    } ],
	    "configStalenessStatus" : "FRESH",
	    "clientConfigStalenessStatus" : "FRESH",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "displayName" : "ZooKeeper"
	  }, {
	    "name" : "hue",
	    "type" : "HUE",
	    "clusterRef" : {
	      "clusterName" : "cluster"
	    },
	    "serviceUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/serviceRedirect/hue",
	    "serviceState" : "STARTED",
	    "healthSummary" : "GOOD",
	    "healthChecks" : [ {
	      "name" : "HUE_HUE_SERVERS_HEALTHY",
	      "summary" : "GOOD"
	    } ],
	    "configStalenessStatus" : "FRESH",
	    "clientConfigStalenessStatus" : "FRESH",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "displayName" : "Hue"
	  }, {
	    "name" : "oozie",
	    "type" : "OOZIE",
	    "clusterRef" : {
	      "clusterName" : "cluster"
	    },
	    "serviceUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/serviceRedirect/oozie",
	    "serviceState" : "STARTED",
	    "healthSummary" : "GOOD",
	    "healthChecks" : [ {
	      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
	      "summary" : "GOOD"
	    } ],
	    "configStalenessStatus" : "FRESH",
	    "clientConfigStalenessStatus" : "FRESH",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "displayName" : "Oozie"
	  }, {
	    "name" : "yarn",
	    "type" : "YARN",
	    "clusterRef" : {
	      "clusterName" : "cluster"
	    },
	    "serviceUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/serviceRedirect/yarn",
	    "serviceState" : "STARTED",
	    "healthSummary" : "GOOD",
	    "healthChecks" : [ {
	      "name" : "YARN_JOBHISTORY_HEALTH",
	      "summary" : "GOOD"
	    }, {
	      "name" : "YARN_NODE_MANAGERS_HEALTHY",
	      "summary" : "GOOD"
	    }, {
	      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
	      "summary" : "GOOD"
	    }, {
	      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
	      "summary" : "DISABLED"
	    } ],
	    "configStalenessStatus" : "FRESH",
	    "clientConfigStalenessStatus" : "FRESH",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "displayName" : "YARN (MR2 Included)"
	  }, {
	    "name" : "spark_on_yarn",
	    "type" : "SPARK_ON_YARN",
	    "clusterRef" : {
	      "clusterName" : "cluster"
	    },
	    "serviceUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/serviceRedirect/spark_on_yarn",
	    "serviceState" : "STARTED",
	    "healthSummary" : "GOOD",
	    "healthChecks" : [ ],
	    "configStalenessStatus" : "FRESH",
	    "clientConfigStalenessStatus" : "FRESH",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "displayName" : "Spark"
	  }, {
	    "name" : "hdfs",
	    "type" : "HDFS",
	    "clusterRef" : {
	      "clusterName" : "cluster"
	    },
	    "serviceUrl" : "http://ip-172-31-7-128.us-west-2.compute.internal:7180/cmf/serviceRedirect/hdfs",
	    "serviceState" : "STARTED",
	    "healthSummary" : "GOOD",
	    "healthChecks" : [ {
	      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
	      "summary" : "GOOD"
	    }, {
	      "name" : "HDFS_CANARY_HEALTH",
	      "summary" : "GOOD"
	    }, {
	      "name" : "HDFS_DATA_NODES_HEALTHY",
	      "summary" : "GOOD"
	    }, {
	      "name" : "HDFS_FREE_SPACE_REMAINING",
	      "summary" : "GOOD"
	    }, {
	      "name" : "HDFS_HA_NAMENODE_HEALTH",
	      "summary" : "GOOD"
	    }, {
	      "name" : "HDFS_MISSING_BLOCKS",
	      "summary" : "GOOD"
	    }, {
	      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
	      "summary" : "GOOD"
	    } ],
	    "configStalenessStatus" : "FRESH",
	    "clientConfigStalenessStatus" : "FRESH",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "displayName" : "HDFS"
	  } ]
	}

```
