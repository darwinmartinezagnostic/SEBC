```
**Check vm.swappiness on all your nodes**

[root@ip-172-31-12-99 ~]# cat /proc/sys/vm/swappiness
30
[root@ip-172-31-12-99 ~]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@ip-172-31-12-99 ~]# vi /etc/sysctl.conf
[root@ip-172-31-12-99 ~]# tail -2 /etc/sysctl.conf
####################
vm.swappiness=1

**Show the mount attributes of your volume(s)**
[root@ip-172-31-12-99 ~]# df -h
S.ficheros     Tamaño Usados  Disp Uso% Montado en
/dev/xvda2       120G   1,2G  119G   1% /
devtmpfs          15G      0   15G   0% /dev
tmpfs             15G      0   15G   0% /dev/shm
tmpfs             15G    17M   15G   1% /run
tmpfs             15G      0   15G   0% /sys/fs/cgroup
/dev/xvdc        118G    64M  112G   1% /disk02
/dev/xvdb        118G    61M  112G   1% /disk01
tmpfs            3,0G      0  3,0G   0% /run/user/1000


**If you have ext-based volumes, list the reserve space setting**
[root@ip-172-31-12-99 ~]# egrep "^/dev/*" /proc/mounts
/dev/xvda2 / xfs rw,relatime,attr2,inode64,noquota 0 0
/dev/xvdc /disk02 ext4 rw,relatime,data=ordered 0 0
/dev/xvdb /disk01 ext4 rw,relatime,data=ordered 0 0


**Disable transparent hugepage support**
[root@ip-172-31-12-99 ~]# cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never
[root@ip-172-31-12-99 ~]# echo never > /sys/kernel/mm/transparent_hugepage/enabled
[root@ip-172-31-12-99 ~]# cat /sys/kernel/mm/transparent_hugepage/enabled
always madvise [never]
[root@ip-172-31-12-99 ~]# cat /sys/kernel/mm/transparent_hugepage/defrag 
[always] madvise never
[root@ip-172-31-12-99 ~]# echo never > /sys/kernel/mm/transparent_hugepage/defrag 
[root@ip-172-31-12-99 ~]# cat /sys/kernel/mm/transparent_hugepage/defrag 
always madvise [never]

**List your network interface configuration**
[root@ip-172-31-12-99 ~]# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.12.99  netmask 255.255.240.0  broadcast 172.31.15.255
        inet6 fe80::8fe:55ff:fea1:55a  prefixlen 64  scopeid 0x20<link>
        ether 0a:fe:55:a1:05:5a  txqueuelen 1000  (Ethernet)
        RX packets 7256  bytes 706058 (689.5 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 5772  bytes 768657 (750.6 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 4  bytes 340 (340.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4  bytes 340 (340.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[root@ip-172-31-12-99 ~]# cat /etc/sysconfig/network-scripts/ifcfg-eth* | egrep "^DEVICE|BOOTPROTO|ONBOOT|NETMASK|NETWORK|IPADDR|PEERDNS"
DEVICE="eth0"
BOOTPROTO="dhcp"
ONBOOT="yes"
PEERDNS="yes"

**Show that forward and reverse host lookups are correctly resolved**
	[root@ip-172-31-12-99 ~]# getent hosts 172.31.4.254
	172.31.4.254    ip-172-31-4-254.us-west-2.compute.internal node2
	[root@ip-172-31-12-99 ~]# getent hosts node3
	172.31.3.136    ip-172-31-3-136.us-west-2.compute.internal node3

	**instalando nslookup**
	[root@ip-172-31-12-99 ~]# sudo yum install bind-utils
	Complementos cargados:amazon-id, rhui-lb, search-disabled-repos
	Resolviendo dependencias
	--> Ejecutando prueba de transacción
	---> Paquete bind-utils.x86_64 32:9.9.4-51.el7 debe ser instalado
	--> Procesando dependencias: bind-libs = 32:9.9.4-51.el7 para el paquete: 32:bind-utils-9.9.4-51.el7.x86_64
	--> Procesando dependencias: libGeoIP.so.1()(64bit) para el paquete: 32:bind-utils-9.9.4-51.el7.x86_64
	--> Procesando dependencias: libbind9.so.90()(64bit) para el paquete: 32:bind-utils-9.9.4-51.el7.x86_64
	--> Procesando dependencias: libdns.so.100()(64bit) para el paquete: 32:bind-utils-9.9.4-51.el7.x86_64
	--> Procesando dependencias: libisc.so.95()(64bit) para el paquete: 32:bind-utils-9.9.4-51.el7.x86_64
	--> Procesando dependencias: libisccc.so.90()(64bit) para el paquete: 32:bind-utils-9.9.4-51.el7.x86_64
	--> Procesando dependencias: libisccfg.so.90()(64bit) para el paquete: 32:bind-utils-9.9.4-51.el7.x86_64
	--> Procesando dependencias: liblwres.so.90()(64bit) para el paquete: 32:bind-utils-9.9.4-51.el7.x86_64
	--> Ejecutando prueba de transacción
	---> Paquete GeoIP.x86_64 0:1.5.0-11.el7 debe ser instalado
	---> Paquete bind-libs.x86_64 32:9.9.4-51.el7 debe ser instalado
	--> Procesando dependencias: bind-license = 32:9.9.4-51.el7 para el paquete: 32:bind-libs-9.9.4-51.el7.x86_64
	--> Ejecutando prueba de transacción
	---> Paquete bind-license.noarch 32:9.9.4-29.el7 debe ser actualizado
	--> Procesando dependencias: bind-license = 32:9.9.4-29.el7 para el paquete: 32:bind-libs-lite-9.9.4-29.el7.x86_64
	---> Paquete bind-license.noarch 32:9.9.4-51.el7 debe ser una actualización
	--> Ejecutando prueba de transacción
	---> Paquete bind-libs-lite.x86_64 32:9.9.4-29.el7 debe ser actualizado
	---> Paquete bind-libs-lite.x86_64 32:9.9.4-51.el7 debe ser una actualización
	--> Resolución de dependencias finalizada

	Dependencias resueltas

	================================================================================
	 Package        Arquitectura
		               Versión           Repositorio                      Tamaño
	================================================================================
	Instalando:
	 bind-utils     x86_64 32:9.9.4-51.el7   rhui-REGION-rhel-server-releases 203 k
	Instalando para las dependencias:
	 GeoIP          x86_64 1.5.0-11.el7      rhui-REGION-rhel-server-releases 1.1 M
	 bind-libs      x86_64 32:9.9.4-51.el7   rhui-REGION-rhel-server-releases 1.0 M
	Actualizando para las dependencias:
	 bind-libs-lite x86_64 32:9.9.4-51.el7   rhui-REGION-rhel-server-releases 732 k
	 bind-license   noarch 32:9.9.4-51.el7   rhui-REGION-rhel-server-releases  84 k

	Resumen de la transacción
	================================================================================
	Instalar    1 Paquete  (+2 Paquetes dependientes)
	Actualizar             ( 2 Paquetes dependientes)

	Tamaño total de la descarga: 3.0 M
	Is this ok [y/d/N]: y
	Downloading packages:
	Delta RPMs disabled because /usr/bin/applydeltarpm not installed.
	(1/5): bind-license-9.9.4-51.el7.noarch.rpm                |  84 kB   00:00     
	(2/5): bind-libs-9.9.4-51.el7.x86_64.rpm                   | 1.0 MB   00:00     
	(3/5): GeoIP-1.5.0-11.el7.x86_64.rpm                       | 1.1 MB   00:00     
	(4/5): bind-libs-lite-9.9.4-51.el7.x86_64.rpm              | 732 kB   00:00     
	(5/5): bind-utils-9.9.4-51.el7.x86_64.rpm                  | 203 kB   00:00     
	--------------------------------------------------------------------------------
	Total                                              5.0 MB/s | 3.0 MB  00:00     
	Running transaction check
	Running transaction test
	Transaction test succeeded
	Running transaction
	  Instalando    : GeoIP-1.5.0-11.el7.x86_64                                 1/7 
	  Actualizando  : 32:bind-license-9.9.4-51.el7.noarch                       2/7 
	  Instalando    : 32:bind-libs-9.9.4-51.el7.x86_64                          3/7 
	  Instalando    : 32:bind-utils-9.9.4-51.el7.x86_64                         4/7 
	  Actualizando  : 32:bind-libs-lite-9.9.4-51.el7.x86_64                     5/7 
	  Limpieza      : 32:bind-libs-lite-9.9.4-29.el7.x86_64                     6/7 
	  Limpieza      : 32:bind-license-9.9.4-29.el7.noarch                       7/7 
	  Comprobando   : 32:bind-libs-lite-9.9.4-51.el7.x86_64                     1/7 
	  Comprobando   : 32:bind-utils-9.9.4-51.el7.x86_64                         2/7 
	  Comprobando   : 32:bind-license-9.9.4-51.el7.noarch                       3/7 
	  Comprobando   : GeoIP-1.5.0-11.el7.x86_64                                 4/7 
	  Comprobando   : 32:bind-libs-9.9.4-51.el7.x86_64                          5/7 
	  Comprobando   : 32:bind-license-9.9.4-29.el7.noarch                       6/7 
	  Comprobando   : 32:bind-libs-lite-9.9.4-29.el7.x86_64                     7/7 

	Instalado:
	  bind-utils.x86_64 32:9.9.4-51.el7                                             

	Dependencia(s) instalada(s):
	  GeoIP.x86_64 0:1.5.0-11.el7          bind-libs.x86_64 32:9.9.4-51.el7         

	Dependencia(s) actualizada(s):
	  bind-libs-lite.x86_64 32:9.9.4-51.el7   bind-license.noarch 32:9.9.4-51.el7  

	¡Listo!

	**Verificando nslookup**
	[root@ip-172-31-12-99 ~]# nslookup ip-172-31-3-136.us-west-2.compute.internal
	Server:		172.31.0.2
	Address:	172.31.0.2#53

	Non-authoritative answer:
	Name:	ip-172-31-3-136.us-west-2.compute.internal
	Address: 172.31.3.136


	**Install nscd package**
	[root@ip-172-31-12-99 ~]# yum install nscd
	Complementos cargados:amazon-id, rhui-lb, search-disabled-repos
	Resolviendo dependencias
	--> Ejecutando prueba de transacción
	---> Paquete nscd.x86_64 0:2.17-196.el7 debe ser instalado
	--> Procesando dependencias: glibc = 2.17-196.el7 para el paquete: nscd-2.17-196.el7.x86_64
	--> Ejecutando prueba de transacción
	---> Paquete glibc.x86_64 0:2.17-105.el7 debe ser actualizado
	--> Procesando dependencias: glibc = 2.17-105.el7 para el paquete: glibc-common-2.17-105.el7.x86_64
	---> Paquete glibc.x86_64 0:2.17-196.el7 debe ser una actualización
	--> Ejecutando prueba de transacción
	---> Paquete glibc-common.x86_64 0:2.17-105.el7 debe ser actualizado
	---> Paquete glibc-common.x86_64 0:2.17-196.el7 debe ser una actualización
	--> Resolución de dependencias finalizada

	Dependencias resueltas

	================================================================================
	 Package       Arquitectura
		               Versión          Repositorio                       Tamaño
	================================================================================
	Instalando:
	 nscd          x86_64  2.17-196.el7     rhui-REGION-rhel-server-releases  273 k
	Actualizando para las dependencias:
	 glibc         x86_64  2.17-196.el7     rhui-REGION-rhel-server-releases  3.6 M
	 glibc-common  x86_64  2.17-196.el7     rhui-REGION-rhel-server-releases   11 M

	Resumen de la transacción
	================================================================================
	Instalar    1 Paquete
	Actualizar             ( 2 Paquetes dependientes)

	Tamaño total de la descarga: 15 M
	Is this ok [y/d/N]: y
	Downloading packages:
	Delta RPMs disabled because /usr/bin/applydeltarpm not installed.
	(1/3): glibc-common-2.17-196.el7.x86_64.rpm                |  11 MB   00:00     
	(2/3): nscd-2.17-196.el7.x86_64.rpm                        | 273 kB   00:00     
	(3/3): glibc-2.17-196.el7.x86_64.rpm                       | 3.6 MB   00:00     
	--------------------------------------------------------------------------------
	Total                                               29 MB/s |  15 MB  00:00     
	Running transaction check
	Running transaction test
	Transaction test succeeded
	Running transaction
	  Actualizando  : glibc-2.17-196.el7.x86_64                                 1/5 
	warning: /etc/nsswitch.conf created as /etc/nsswitch.conf.rpmnew
	  Actualizando  : glibc-common-2.17-196.el7.x86_64                          2/5 
	  Instalando    : nscd-2.17-196.el7.x86_64                                  3/5 
	  Limpieza      : glibc-2.17-105.el7.x86_64                                 4/5 
	  Limpieza      : glibc-common-2.17-105.el7.x86_64                          5/5 
	  Comprobando   : glibc-common-2.17-196.el7.x86_64                          1/5 
	  Comprobando   : nscd-2.17-196.el7.x86_64                                  2/5 
	  Comprobando   : glibc-2.17-196.el7.x86_64                                 3/5 
	  Comprobando   : glibc-2.17-105.el7.x86_64                                 4/5 
	  Comprobando   : glibc-common-2.17-105.el7.x86_64                          5/5 

	Instalado:
	  nscd.x86_64 0:2.17-196.el7                                                    

	Dependencia(s) actualizada(s):
	  glibc.x86_64 0:2.17-196.el7         glibc-common.x86_64 0:2.17-196.el7        

	¡Listo!


	**Install ntp package**
	[root@ip-172-31-12-99 ~]# yum install ntp
	Complementos cargados:amazon-id, rhui-lb, search-disabled-repos
	Resolviendo dependencias
	--> Ejecutando prueba de transacción
	---> Paquete ntp.x86_64 0:4.2.6p5-25.el7_3.2 debe ser instalado
	--> Procesando dependencias: ntpdate = 4.2.6p5-25.el7_3.2 para el paquete: ntp-4.2.6p5-25.el7_3.2.x86_64
	--> Procesando dependencias: libopts.so.25()(64bit) para el paquete: ntp-4.2.6p5-25.el7_3.2.x86_64
	--> Ejecutando prueba de transacción
	---> Paquete autogen-libopts.x86_64 0:5.18-5.el7 debe ser instalado
	---> Paquete ntpdate.x86_64 0:4.2.6p5-25.el7_3.2 debe ser instalado
	--> Resolución de dependencias finalizada

	Dependencias resueltas

	================================================================================
	 Package       Arquitectura
		              Versión            Repositorio                      Tamaño
	================================================================================
	Instalando:
	 ntp           x86_64 4.2.6p5-25.el7_3.2 rhui-REGION-rhel-server-releases 547 k
	Instalando para las dependencias:
	 autogen-libopts
		       x86_64 5.18-5.el7         rhui-REGION-rhel-server-releases  66 k
	 ntpdate       x86_64 4.2.6p5-25.el7_3.2 rhui-REGION-rhel-server-releases  86 k

	Resumen de la transacción
	================================================================================
	Instalar  1 Paquete (+2 Paquetes dependientes)

	Tamaño total de la descarga: 699 k
	Tamaño instalado: 1.6 M
	Is this ok [y/d/N]: y
	Downloading packages:
	(1/3): ntp-4.2.6p5-25.el7_3.2.x86_64.rpm                   | 547 kB   00:00     
	(2/3): autogen-libopts-5.18-5.el7.x86_64.rpm               |  66 kB   00:00     
	(3/3): ntpdate-4.2.6p5-25.el7_3.2.x86_64.rpm               |  86 kB   00:00     
	--------------------------------------------------------------------------------
	Total                                              1.3 MB/s | 699 kB  00:00     
	Running transaction check
	Running transaction test
	Transaction test succeeded
	Running transaction
	  Instalando    : ntpdate-4.2.6p5-25.el7_3.2.x86_64                         1/3 
	  Instalando    : autogen-libopts-5.18-5.el7.x86_64                         2/3 
	  Instalando    : ntp-4.2.6p5-25.el7_3.2.x86_64                             3/3 
	  Comprobando   : autogen-libopts-5.18-5.el7.x86_64                         1/3 
	  Comprobando   : ntp-4.2.6p5-25.el7_3.2.x86_64                             2/3 
	  Comprobando   : ntpdate-4.2.6p5-25.el7_3.2.x86_64                         3/3 

	Instalado:
	  ntp.x86_64 0:4.2.6p5-25.el7_3.2                                               

	Dependencia(s) instalada(s):
	  autogen-libopts.x86_64 0:5.18-5.el7    ntpdate.x86_64 0:4.2.6p5-25.el7_3.2   

	¡Listo!


**Show the nscd service is running**
	
[root@ip-172-31-12-99 ~]# service nscd status
Redirecting to /bin/systemctl status  nscd.service
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: inactive (dead)
[root@ip-172-31-12-99 ~]# service nscd start
Redirecting to /bin/systemctl start  nscd.service
[root@ip-172-31-12-99 ~]# service nscd status
Redirecting to /bin/systemctl status  nscd.service
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since lun 2017-10-02 13:39:27 EDT; 5s ago
  Process: 9735 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9736 (nscd)
   CGroup: /system.slice/nscd.service
           └─9736 /usr/sbin/nscd

oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 m...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 m...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 m...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 m...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 m...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 m...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 m...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 d...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal nscd[9736]: 9736 s...
oct 02 13:39:27 ip-172-31-12-99.us-west-2.compute.internal systemd[1]: Starte...
Hint: Some lines were ellipsized, use -l to show in full.


**Show the ntpd service is running**
[root@ip-172-31-12-99 ~]# service ntpd status
Redirecting to /bin/systemctl status  ntpd.service
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: inactive (dead)
[root@ip-172-31-12-99 ~]# service ntpd start
Redirecting to /bin/systemctl start  ntpd.service
[root@ip-172-31-12-99 ~]# service ntpd status
Redirecting to /bin/systemctl status  ntpd.service
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since lun 2017-10-02 13:45:24 EDT; 1min 23s ago
  Process: 9854 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 9855 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─9855 /usr/sbin/ntpd -u ntp:ntp -g

oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: Listen...
oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: Listen...
oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: Listen...
oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: Listen...
oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: Listen...
oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal systemd[1]: Starte...
oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: 0.0.0....
oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: 0.0.0....
oct 02 13:45:24 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: 0.0.0....
oct 02 13:45:32 ip-172-31-12-99.us-west-2.compute.internal ntpd[9855]: 0.0.0....
Hint: Some lines were ellipsized, use -l to show in full.

```








