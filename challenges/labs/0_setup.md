```
## Cloud Provider

	My cloud provider is "AWS"

##List your instances by IP address and DNS name

	[ec2-user@ip-172-31-15-216 ~]$ ssh node1 uname -n
	ip-172-31-15-216.us-west-2.compute.internal
	[ec2-user@ip-172-31-15-216 ~]$ ssh node2 uname -n
	ip-172-31-7-128.us-west-2.compute.internal
	[ec2-user@ip-172-31-15-216 ~]$ ssh node3 uname -n
	ip-172-31-10-49.us-west-2.compute.internal
	[ec2-user@ip-172-31-15-216 ~]$ ssh node4 uname -n
	ip-172-31-5-32.us-west-2.compute.internal
	[ec2-user@ip-172-31-15-216 ~]$ ssh node5 uname -n
	ip-172-31-4-137.us-west-2.compute.internal
	[ec2-user@ip-172-31-15-216 ~]$ 



##List the Linux release you are using
	[ec2-user@ip-172-31-15-216 ~]$ cat /etc/redhat-release
	Red Hat Enterprise Linux Server release 7.2 (Maipo)

##List the file system capacity for the first node
	[ec2-user@ip-172-31-15-216 ~]$ ssh node1 df -h
	S.ficheros     Tamaño Usados  Disp Uso% Montado en
	/dev/xvda2       120G   1,2G  119G   1% /
	devtmpfs          15G      0   15G   0% /dev
	tmpfs             15G      0   15G   0% /dev/shm
	tmpfs             15G    17M   15G   1% /run
	tmpfs             15G      0   15G   0% /sys/fs/cgroup
	/dev/xvdc        118G    61M  112G   1% /disk02
	/dev/xvdb        118G    61M  112G   1% /disk01
	tmpfs            3,0G      0  3,0G   0% /run/user/0
	tmpfs            3,0G      0  3,0G   0% /run/user/1000


##List the command and output for yum repolist enabled
	[ec2-user@ip-172-31-15-216 ~]$ yum repolist enabled
	Complementos cargados:amazon-id, rhui-lb, search-disabled-repos
	Repo rhui-REGION-client-config-server-7 forced skip_if_unavailable=True due to: /etc/pki/rhui/cdn.redhat.com-chain.crt
	Repo rhui-REGION-client-config-server-7 forced skip_if_unavailable=True due to: /etc/pki/rhui/product/rhui-client-config-server-7.crt
	Repo rhui-REGION-client-config-server-7 forced skip_if_unavailable=True due to: /etc/pki/rhui/rhui-client-config-server-7.key
	Repo rhui-REGION-rhel-server-releases forced skip_if_unavailable=True due to: /etc/pki/rhui/cdn.redhat.com-chain.crt
	Repo rhui-REGION-rhel-server-releases forced skip_if_unavailable=True due to: /etc/pki/rhui/product/content-rhel7.crt
	Repo rhui-REGION-rhel-server-releases forced skip_if_unavailable=True due to: /etc/pki/rhui/content-rhel7.key
	Repo rhui-REGION-rhel-server-rh-common forced skip_if_unavailable=True due to: /etc/pki/rhui/cdn.redhat.com-chain.crt
	Repo rhui-REGION-rhel-server-rh-common forced skip_if_unavailable=True due to: /etc/pki/rhui/product/content-rhel7.crt
	Repo rhui-REGION-rhel-server-rh-common forced skip_if_unavailable=True due to: /etc/pki/rhui/content-rhel7.key
	Could not contact CDS load balancer rhui2-cds01.us-west-2.aws.ce.redhat.com, trying others.


	Could not contact any CDS load balancers: rhui2-cds01.us-west-2.aws.ce.redhat.com, rhui2-cds02.us-west-2.aws.ce.redhat.com.


##List the /etc/passwd entries for saturn and haley
	[ec2-user@ip-172-31-15-216 ~]$ cat /etc/passwd |grep -E "haley|saturn"
	saturn:x:2800:2800::/home/saturn:/bin/bash
	haley:x:2900:2900::/home/haley:/bin/bash


##List the /etc/group entries for comets and planets
	[ec2-user@ip-172-31-15-216 ~]$ cat /etc/group |grep -E "comets|planets"
	comets:x:2901:haley
	planets:x:2902:saturn

```
