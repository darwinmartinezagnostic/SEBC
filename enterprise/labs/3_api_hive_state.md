´´´

	[ec2-user@ip-172-31-12-99 ~]$ curl -X POST -u darwinmartinezagnostic:cloudera 'http://localhost:7180/api/v1/clusters/darwinmartinezagnostic/services/hive/commands/stop'
	{
	  "id" : 1357,
	  "name" : "Stop",
	  "startTime" : "2017-10-05T14:23:19.740Z",
	  "active" : true,
	  "serviceRef" : {
	    "clusterName" : "cluster",
	    "serviceName" : "hive"
	  }
	}

	[ec2-user@ip-172-31-12-99 ~]$ curl -u darwinmartinezagnostic:cloudera 'http://lcalhost:7180/api/v1/clusters/darwinmartinezagnostic/services/hive'
	{
	  "name" : "hive",
	  "type" : "HIVE",
	  "clusterRef" : {
	    "clusterName" : "cluster"
	  },
	  "serviceUrl" : "http://ip-172-31-12-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
	  "serviceState" : "STOPPED",
	  "healthSummary" : "DISABLED",
	  "healthChecks" : [ {
	    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
	    "summary" : "DISABLED"
	  }, {
	    "name" : "HIVE_HIVESERVER2S_HEALTHY",
	    "summary" : "DISABLED"
	  }, {
	    "name" : "HIVE_WEBHCATS_HEALTHY",
	    "summary" : "DISABLED"
	  } ],
	  "configStale" : false
	}

	[ec2-user@ip-172-31-12-99 ~]$ curl -X POST -u darwinmartinezagnostic:cloudera 'http://localhost:7180/api/v1/clusters/darwinmartinezagnostic/services/hive/commands/start'
	{
	  "id" : 1365,
	  "name" : "Start",
	  "startTime" : "2017-10-05T14:27:29.398Z",
	  "active" : true,
	  "serviceRef" : {
	    "clusterName" : "cluster",
	    "serviceName" : "hive"
	  }
	}

	[ec2-user@ip-172-31-12-99 ~]$ curl u darwinmartinezagnostic:cloudera 'http://localhost:7180/api/v1/clusters/darwinmartinezagnostic/services/hive'{
	  "name" : "hive",
	  "type" : "HIVE",
	  "clusterRef" : {
	    "clusterName" : "cluster"
	  },
	  "serviceUrl" : "http://ip-172-31-12-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
	  "serviceState" : "STARTED",
	  "healthSummary" : "DISABLED",
	  "healthChecks" : [ {
	    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
	    "summary" : "DISABLED"
	  }, {
	    "name" : "HIVE_HIVESERVER2S_HEALTHY",
	    "summary" : "DISABLED"
	  }, {
	    "name" : "HIVE_WEBHCATS_HEALTHY",
	    "summary" : "DISABLED"
	  } ],
	  "configStale" : false
	}

´´´
