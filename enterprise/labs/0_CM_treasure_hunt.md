´´´

1. What is ubertask optimization?

	La optimizacion de ubertask es un metodo que se utiliza para que tareas con un tamaño especifico se ejecuten secuencialmente dentro de una misma JVM. El tamaño de estas tareas se define en mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces y mapreduce.job.ubertask.maxbytes.


2. Where in CM is the Kerberos Security Realm value displayed?
	Administracion --> Ajustes --> Kerberos --> default_realm


3. Which CDH service(s) host a property for enabling Kerberos authentication?
	HDFS YARN ZOOKEEPER

4. How do you upgrade the CM agents?
	a) Log in to the Cloudera Manager Admin Console.
	b) Upgrade hosts using one of the following methods:
	- Cloudera Manager installs Agent software
	1- Select Yes, I would like to upgrade the Cloudera Manager Agent packages now and click Continue.
	2- Select the release of the Cloudera Manager Agent to install. Normally, this is the Matched Release for this Cloudera Manager Server. However, if you used a custom repository (instead of archive.cloudera.com) for the Cloudera Manager server, select Custom Repository and provide the required information. The custom repository allows you to use an alternative location, but that location must contain the matched Agent version.
	3- Click Continue. The JDK Installation Options page displays.
	* Leave Install Oracle Java SE Development Kit (JDK) checked to allow Cloudera Manager to install the JDK on each cluster host, or uncheck if you plan to install it yourself.
	* If local laws permit you to deploy unlimited strength encryption, and you are running a secure cluster, check the Install Java Unlimited Strength Encryption Policy Files checkbox.
	Click Continue.
	4) Specify credentials and initiate Agent installation:
	* Select root or enter the username for an account that has password-less sudo permission.
	* Select an authentication method:
	- If you choose password authentication, enter and confirm the password.
	- If you choose public-key authentication, provide a passphrase and path to the required key files.
	* You can specify an alternate SSH port. The default value is 22.
	* You can specify the maximum number of host installations to run at once. The default value is 10.
	5) Click Continue. The Cloudera Manager Agent packages and optionally the JDK are installed.


5. Give the tsquery statement used to chart Hue's CPU utilization?
	select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName="hue"


6. Name all the roles that make up the Hive service
	Hive Metastore Server
	HiveServer2 


7. What steps must be completed before integrating Cloudera Manager with Kerberos?
	1. Instalar los paquetes de kerberos server en un nodo
		yum -y install krb5-server krb5-libs krb5-auth-dialog krb5-workstation
	2. Instalar los paquetes de kerberos client en el resto de los nodos
		yum -y install krb5-workstation krb5-libs krb5-auth-dialog
	3. Modificar el archivo /var/kerberos/krb5kdc/kdc.conf en el server
		3.1 Se cambia el valor de Realm Name
		3.2 Opcionalmente se pueden agregar parametros como:
			max_life = 1d y max_renewable_life = 7d
	4. Modificar el archivo /etc/krb5.conf en todos los nodos
		4.1 Se cambia el valor de default_realm (debe corresponder con el Realm Name del archivo anterior)
		4.2 Se determina el tipo de encriptamiento que se aplicara en los atributos default_tgs_enctypes y default_tkt_enctypes
		4.3 En la etiqueta [realms] se ajusta el kdc y el admin_server
	5. Se crea la BD usando el kdb5_util utility en el server.
		/usr/sbin/kdb5_util create -s
	6. Se agregan los usuarios que seran usados en CM 
		kadmin.local: addprinc cloudera-scm@EXAMPLE.COM
	7. Se agrega el usuario creado anteriormente al archivo /var/kerberos/krb5kdc/kadm5.acl 
		cloudera-scm@EXAMPLE.COM admilc
	8. Se agregan los roles a la bd
		kadmin.local:  addpol admin
		kadmin.local:  addpol users
		kadmin.local:  addpol hosts
	9. Se inician los servicios de kerberos
		service krb5kdc start
		service kadmin start
´´´
