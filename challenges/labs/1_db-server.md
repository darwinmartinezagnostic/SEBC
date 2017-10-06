```
##A command and output that shows the hostname of your database server
	[ec2-user@ip-172-31-15-216 ~]$ hostname
	ip-172-31-15-216.us-west-2.compute.internal


##A command and output that reports the database server version
	[ec2-user@ip-172-31-15-216 ~]$ mysql --version
	mysql  Ver 14.14 Distrib 5.7.19, for Linux (x86_64) using  EditLine wrapper

##A command and output that lists all the databases in the server
	[ec2-user@ip-172-31-15-216 ~]$ mysql -uroot -pMyNewPass4! -e 'show databases;'
	mysql: [Warning] Using a password on the command line interface can be insecure.
	+--------------------+
	| Database           |
	+--------------------+
	| information_schema |
	| amon               |
	| hive               |
	| hue                |
	| mysql              |
	| oozie              |
	| performance_schema |
	| rman               |
	| scm                |
	| sys                |
	+--------------------+
	

```
