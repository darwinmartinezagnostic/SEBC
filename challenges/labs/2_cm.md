```
##List the command and output
	[ec2-user@ip-172-31-7-128 ~]$ ls /etc/yum.repos.d
	mysql-community.repo         redhat-rhui-client-config.repo
	mysql-community-source.repo  redhat-rhui.repo
	redhat.repo                  rhui-load-balancers.conf

##Connect Cloudera Manager Server to its database
	[ec2-user@ip-172-31-7-128 ~]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql -h node1 scm bootcamp MyNewPass4!
	JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
	Verifying that we can write to /etc/cloudera-scm-server
	Creating SCM configuration file in /etc/cloudera-scm-server
	Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
	Fri Oct 06 08:22:23 EDT 2017 WARN: Establishing SSL connection without server's identity verification is not recommended. According to MySQL 5.5.45+, 5.6.26+ and 5.7.6+ requirements SSL connection must be established by default if explicit option isn't set. For compliance with existing applications not using SSL the verifyServerCertificate property is set to 'false'. You need either to explicitly disable SSL by setting useSSL=false, or set useSSL=true and provide truststore for server certificate verification.
	[                          main] DbCommandExecutor              INFO  Successfully connected to database.
	All done, your SCM database is configured correctly!




```
