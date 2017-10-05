´´´
**Report the latest available version of the API**

[ec2-user@ip-172-31-12-99 ~]$ curl -u darwinmartinezagnostic:cloudera 'http://localhost:7180/api/version'
v17

**Report the CM version**

	[ec2-user@ip-172-31-12-99 ~]$ curl -u darwinmartinezagnostic:cloudera 'http://localhost:7180/api/v1/clusters'
	{
	  "items" : [ {
	    "name" : "darwinmartinezagnostic",
	    "version" : "CDH5"
	  } ]
	}


**List all CM users**

	[ec2-user@ip-172-31-12-99 ~]$ curl -u darwinmartinezagnostic:cloudera 'http://lcalhost:7180/api/v1/users'
	{
	  "items" : [ {
	    "name" : "admin",
	    "roles" : [ "ROLE_LIMITED" ]
	  }, {
	    "name" : "darwinmartinezagnostic",
	    "roles" : [ "ROLE_ADMIN" ]
	  }, {
	    "name" : "minotaur",
	    "roles" : [ "ROLE_CONFIGURATOR" ]
	  } ]
	}

**Report the database server in use by CM**

	[ec2-user@ip-172-31-12-99 ~]$ curl -u darwinmartinezagnostic:cloudera 'http://lcalhost:7180/api/v17/cm/scmDbInfo'
	{
	  "scmDbType" : "MYSQL",
	  "embeddedDbUsed" : false
	}



´´´
