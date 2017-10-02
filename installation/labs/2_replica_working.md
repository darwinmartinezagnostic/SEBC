```

**INSTALACION DE MYSQL**
	[root@ip-172-31-12-99 ~]# wget http://dev.mysql.com/get/mysql57-community-release-el7-11.noarch.rpm
	--2017-10-02 14:13:39--  http://dev.mysql.com/get/mysql57-community-release-el7-11.noarch.rpm
	Resolviendo dev.mysql.com (dev.mysql.com)... 137.254.60.11
	Conectando con dev.mysql.com (dev.mysql.com)[137.254.60.11]:80... conectado.
	Petición HTTP enviada, esperando respuesta... 301 Moved Permanently
	Localización: https://dev.mysql.com/get/mysql57-community-release-el7-11.noarch.rpm [siguiendo]
	--2017-10-02 14:13:39--  https://dev.mysql.com/get/mysql57-community-release-el7-11.noarch.rpm
	Conectando con dev.mysql.com (dev.mysql.com)[137.254.60.11]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 302 Found
	Localización: https://repo.mysql.com//mysql57-community-release-el7-11.noarch.rpm [siguiendo]
	--2017-10-02 14:13:40--  https://repo.mysql.com//mysql57-community-release-el7-11.noarch.rpm
	Resolviendo repo.mysql.com (repo.mysql.com)... 23.48.156.204
	Conectando con repo.mysql.com (repo.mysql.com)[23.48.156.204]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 200 OK
	Longitud: 25680 (25K) [application/x-redhat-package-manager]
	Grabando a: “mysql57-community-release-el7-11.noarch.rpm”

	100%[======================================>] 25.680      --.-K/s   en 0,008s  

	2017-10-02 14:13:40 (3,14 MB/s) - “mysql57-community-release-el7-11.noarch.rpm” guardado [25680/25680]

	[root@ip-172-31-12-99 ~]# sudo rpm -Uvh mysql57-community-release-el7-11.noarch.rpm
	advertencia:mysql57-community-release-el7-11.noarch.rpm: EncabezadoV3 DSA/SHA1 Signature, ID de clave 5072e1f5: NOKEY
	Preparando...                         ################################# [100%]
	Actualizando / instalando...
	   1:mysql57-community-release-el7-11 ################################# [100%]
	[root@ip-172-31-12-99 ~]# sudo yum install -y mysql-community-server
	Complementos cargados:amazon-id, rhui-lb, search-disabled-repos
	mysql-connectors-community                               | 2.5 kB     00:00     
	mysql-tools-community                                    | 2.5 kB     00:00     
	mysql57-community                                        | 2.5 kB     00:00     
	(1/3): mysql-connectors-community/x86_64/primary_db        |  16 kB   00:00     
	(2/3): mysql-tools-community/x86_64/primary_db             |  35 kB   00:00     
	(3/3): mysql57-community/x86_64/primary_db                 | 116 kB   00:00     
	Resolviendo dependencias
	--> Ejecutando prueba de transacción
	---> Paquete mysql-community-server.x86_64 0:5.7.19-1.el7 debe ser instalado
	--> Procesando dependencias: mysql-community-common(x86-64) = 5.7.19-1.el7 para el paquete: mysql-community-server-5.7.19-1.el7.x86_64
	--> Procesando dependencias: mysql-community-client(x86-64) >= 5.7.9 para el paquete: mysql-community-server-5.7.19-1.el7.x86_64
	--> Procesando dependencias: perl(strict) para el paquete: mysql-community-server-5.7.19-1.el7.x86_64
	--> Procesando dependencias: perl(Getopt::Long) para el paquete: mysql-community-server-5.7.19-1.el7.x86_64
	--> Procesando dependencias: libaio.so.1(LIBAIO_0.4)(64bit) para el paquete: mysql-community-server-5.7.19-1.el7.x86_64
	--> Procesando dependencias: libaio.so.1(LIBAIO_0.1)(64bit) para el paquete: mysql-community-server-5.7.19-1.el7.x86_64
	--> Procesando dependencias: /usr/bin/perl para el paquete: mysql-community-server-5.7.19-1.el7.x86_64
	--> Procesando dependencias: libaio.so.1()(64bit) para el paquete: mysql-community-server-5.7.19-1.el7.x86_64
	--> Ejecutando prueba de transacción
	---> Paquete libaio.x86_64 0:0.3.109-13.el7 debe ser instalado
	---> Paquete mysql-community-client.x86_64 0:5.7.19-1.el7 debe ser instalado
	--> Procesando dependencias: mysql-community-libs(x86-64) >= 5.7.9 para el paquete: mysql-community-client-5.7.19-1.el7.x86_64
	---> Paquete mysql-community-common.x86_64 0:5.7.19-1.el7 debe ser instalado
	---> Paquete perl.x86_64 4:5.16.3-292.el7 debe ser instalado
	--> Procesando dependencias: perl-libs = 4:5.16.3-292.el7 para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Scalar::Util) >= 1.10 para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Socket) >= 1.3 para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Carp) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Cwd) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Exporter) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(File::Path) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(File::Spec) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(File::Spec::Functions) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(File::Spec::Unix) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(File::Temp) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Filter::Util::Call) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Pod::Simple::Search) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Pod::Simple::XHTML) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Scalar::Util) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Socket) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Storable) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Time::HiRes) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(Time::Local) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(constant) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(threads) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl(threads::shared) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl-libs para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: perl-macros para el paquete: 4:perl-5.16.3-292.el7.x86_64
	--> Procesando dependencias: libperl.so()(64bit) para el paquete: 4:perl-5.16.3-292.el7.x86_64
	---> Paquete perl-Getopt-Long.noarch 0:2.40-2.el7 debe ser instalado
	--> Procesando dependencias: perl(Pod::Usage) >= 1.14 para el paquete: perl-Getopt-Long-2.40-2.el7.noarch
	--> Procesando dependencias: perl(Text::ParseWords) para el paquete: perl-Getopt-Long-2.40-2.el7.noarch
	--> Ejecutando prueba de transacción
	---> Paquete mariadb-libs.x86_64 1:5.5.44-2.el7 debe ser obsoleto
	--> Procesando dependencias: libmysqlclient.so.18()(64bit) para el paquete: 2:postfix-2.10.1-6.el7.x86_64
	--> Procesando dependencias: libmysqlclient.so.18(libmysqlclient_18)(64bit) para el paquete: 2:postfix-2.10.1-6.el7.x86_64
	---> Paquete mysql-community-libs.x86_64 0:5.7.19-1.el7 debe ser obsoleto
	---> Paquete perl-Carp.noarch 0:1.26-244.el7 debe ser instalado
	---> Paquete perl-Exporter.noarch 0:5.68-3.el7 debe ser instalado
	---> Paquete perl-File-Path.noarch 0:2.09-2.el7 debe ser instalado
	---> Paquete perl-File-Temp.noarch 0:0.23.01-3.el7 debe ser instalado
	---> Paquete perl-Filter.x86_64 0:1.49-3.el7 debe ser instalado
	---> Paquete perl-PathTools.x86_64 0:3.40-5.el7 debe ser instalado
	---> Paquete perl-Pod-Simple.noarch 1:3.28-4.el7 debe ser instalado
	--> Procesando dependencias: perl(Pod::Escapes) >= 1.04 para el paquete: 1:perl-Pod-Simple-3.28-4.el7.noarch
	--> Procesando dependencias: perl(Encode) para el paquete: 1:perl-Pod-Simple-3.28-4.el7.noarch
	---> Paquete perl-Pod-Usage.noarch 0:1.63-3.el7 debe ser instalado
	--> Procesando dependencias: perl(Pod::Text) >= 3.15 para el paquete: perl-Pod-Usage-1.63-3.el7.noarch
	--> Procesando dependencias: perl-Pod-Perldoc para el paquete: perl-Pod-Usage-1.63-3.el7.noarch
	---> Paquete perl-Scalar-List-Utils.x86_64 0:1.27-248.el7 debe ser instalado
	---> Paquete perl-Socket.x86_64 0:2.010-4.el7 debe ser instalado
	---> Paquete perl-Storable.x86_64 0:2.45-3.el7 debe ser instalado
	---> Paquete perl-Text-ParseWords.noarch 0:3.29-4.el7 debe ser instalado
	---> Paquete perl-Time-HiRes.x86_64 4:1.9725-3.el7 debe ser instalado
	---> Paquete perl-Time-Local.noarch 0:1.2300-2.el7 debe ser instalado
	---> Paquete perl-constant.noarch 0:1.27-2.el7 debe ser instalado
	---> Paquete perl-libs.x86_64 4:5.16.3-292.el7 debe ser instalado
	---> Paquete perl-macros.x86_64 4:5.16.3-292.el7 debe ser instalado
	---> Paquete perl-threads.x86_64 0:1.87-4.el7 debe ser instalado
	---> Paquete perl-threads-shared.x86_64 0:1.43-6.el7 debe ser instalado
	--> Ejecutando prueba de transacción
	---> Paquete mysql-community-libs-compat.x86_64 0:5.7.19-1.el7 debe ser obsoleto
	---> Paquete perl-Encode.x86_64 0:2.51-7.el7 debe ser instalado
	---> Paquete perl-Pod-Escapes.noarch 1:1.04-292.el7 debe ser instalado
	---> Paquete perl-Pod-Perldoc.noarch 0:3.20-4.el7 debe ser instalado
	--> Procesando dependencias: perl(HTTP::Tiny) para el paquete: perl-Pod-Perldoc-3.20-4.el7.noarch
	--> Procesando dependencias: perl(parent) para el paquete: perl-Pod-Perldoc-3.20-4.el7.noarch
	---> Paquete perl-podlators.noarch 0:2.5.1-3.el7 debe ser instalado
	--> Ejecutando prueba de transacción
	---> Paquete perl-HTTP-Tiny.noarch 0:0.033-3.el7 debe ser instalado
	---> Paquete perl-parent.noarch 1:0.225-244.el7 debe ser instalado
	--> Resolución de dependencias finalizada

	Dependencias resueltas

	================================================================================
	 Package         Arquitectura
		                Versión          Repositorio                      Tamaño
	================================================================================
	Instalando:
	 mysql-community-libs
		         x86_64 5.7.19-1.el7     mysql57-community                2.1 M
	     reemplazando  mariadb-libs.x86_64 1:5.5.44-2.el7
	 mysql-community-libs-compat
		         x86_64 5.7.19-1.el7     mysql57-community                2.0 M
	     reemplazando  mariadb-libs.x86_64 1:5.5.44-2.el7
	 mysql-community-server
		         x86_64 5.7.19-1.el7     mysql57-community                164 M
	Instalando para las dependencias:
	 libaio          x86_64 0.3.109-13.el7   rhui-REGION-rhel-server-releases  24 k
	 mysql-community-client
		         x86_64 5.7.19-1.el7     mysql57-community                 24 M
	 mysql-community-common
		         x86_64 5.7.19-1.el7     mysql57-community                272 k
	 perl            x86_64 4:5.16.3-292.el7 rhui-REGION-rhel-server-releases 8.0 M
	 perl-Carp       noarch 1.26-244.el7     rhui-REGION-rhel-server-releases  19 k
	 perl-Encode     x86_64 2.51-7.el7       rhui-REGION-rhel-server-releases 1.5 M
	 perl-Exporter   noarch 5.68-3.el7       rhui-REGION-rhel-server-releases  28 k
	 perl-File-Path  noarch 2.09-2.el7       rhui-REGION-rhel-server-releases  27 k
	 perl-File-Temp  noarch 0.23.01-3.el7    rhui-REGION-rhel-server-releases  56 k
	 perl-Filter     x86_64 1.49-3.el7       rhui-REGION-rhel-server-releases  76 k
	 perl-Getopt-Long
		         noarch 2.40-2.el7       rhui-REGION-rhel-server-releases  56 k
	 perl-HTTP-Tiny  noarch 0.033-3.el7      rhui-REGION-rhel-server-releases  38 k
	 perl-PathTools  x86_64 3.40-5.el7       rhui-REGION-rhel-server-releases  83 k
	 perl-Pod-Escapes
		         noarch 1:1.04-292.el7   rhui-REGION-rhel-server-releases  51 k
	 perl-Pod-Perldoc
		         noarch 3.20-4.el7       rhui-REGION-rhel-server-releases  87 k
	 perl-Pod-Simple noarch 1:3.28-4.el7     rhui-REGION-rhel-server-releases 216 k
	 perl-Pod-Usage  noarch 1.63-3.el7       rhui-REGION-rhel-server-releases  27 k
	 perl-Scalar-List-Utils
		         x86_64 1.27-248.el7     rhui-REGION-rhel-server-releases  36 k
	 perl-Socket     x86_64 2.010-4.el7      rhui-REGION-rhel-server-releases  49 k
	 perl-Storable   x86_64 2.45-3.el7       rhui-REGION-rhel-server-releases  77 k
	 perl-Text-ParseWords
		         noarch 3.29-4.el7       rhui-REGION-rhel-server-releases  14 k
	 perl-Time-HiRes x86_64 4:1.9725-3.el7   rhui-REGION-rhel-server-releases  45 k
	 perl-Time-Local noarch 1.2300-2.el7     rhui-REGION-rhel-server-releases  24 k
	 perl-constant   noarch 1.27-2.el7       rhui-REGION-rhel-server-releases  19 k
	 perl-libs       x86_64 4:5.16.3-292.el7 rhui-REGION-rhel-server-releases 688 k
	 perl-macros     x86_64 4:5.16.3-292.el7 rhui-REGION-rhel-server-releases  43 k
	 perl-parent     noarch 1:0.225-244.el7  rhui-REGION-rhel-server-releases  12 k
	 perl-podlators  noarch 2.5.1-3.el7      rhui-REGION-rhel-server-releases 112 k
	 perl-threads    x86_64 1.87-4.el7       rhui-REGION-rhel-server-releases  49 k
	 perl-threads-shared
		         x86_64 1.43-6.el7       rhui-REGION-rhel-server-releases  39 k

	Resumen de la transacción
	================================================================================
	Instalar  3 Paquetes (+30 Paquetes dependientes)

	Tamaño total de la descarga: 203 M
	Downloading packages:
	advertencia:/var/cache/yum/x86_64/7Server/mysql57-community/packages/mysql-community-common-5.7.19-1.el7.x86_64.rpm: EncabezadoV3 DSA/SHA1 Signature, ID de clave 5072e1f5: NOKEY
	No se ha instalado la llave pública de mysql-community-common-5.7.19-1.el7.x86_64.rpm 
	(1/33): mysql-community-common-5.7.19-1.el7.x86_64.rpm     | 272 kB   00:00     
	(2/33): mysql-community-libs-5.7.19-1.el7.x86_64.rpm       | 2.1 MB   00:00     
	(3/33): mysql-community-libs-compat-5.7.19-1.el7.x86_64.rp | 2.0 MB   00:00     
	(4/33): libaio-0.3.109-13.el7.x86_64.rpm                   |  24 kB   00:00     
	(5/33): perl-Carp-1.26-244.el7.noarch.rpm                  |  19 kB   00:00     
	(6/33): perl-Encode-2.51-7.el7.x86_64.rpm                  | 1.5 MB   00:00     
	(7/33): perl-Exporter-5.68-3.el7.noarch.rpm                |  28 kB   00:00     
	(8/33): perl-File-Path-2.09-2.el7.noarch.rpm               |  27 kB   00:00     
	(9/33): perl-File-Temp-0.23.01-3.el7.noarch.rpm            |  56 kB   00:00     
	(10/33): perl-5.16.3-292.el7.x86_64.rpm                    | 8.0 MB   00:00     
	(11/33): mysql-community-client-5.7.19-1.el7.x86_64.rpm    |  24 MB   00:00     
	(12/33): perl-Filter-1.49-3.el7.x86_64.rpm                 |  76 kB   00:00     
	(13/33): perl-Getopt-Long-2.40-2.el7.noarch.rpm            |  56 kB   00:00     
	(14/33): perl-HTTP-Tiny-0.033-3.el7.noarch.rpm             |  38 kB   00:00     
	(15/33): perl-Pod-Escapes-1.04-292.el7.noarch.rpm          |  51 kB   00:00     
	(16/33): perl-Pod-Perldoc-3.20-4.el7.noarch.rpm            |  87 kB   00:00     
	(17/33): perl-Pod-Simple-3.28-4.el7.noarch.rpm             | 216 kB   00:00     
	(18/33): perl-Pod-Usage-1.63-3.el7.noarch.rpm              |  27 kB   00:00     
	(19/33): perl-Scalar-List-Utils-1.27-248.el7.x86_64.rpm    |  36 kB   00:00     
	(20/33): perl-PathTools-3.40-5.el7.x86_64.rpm              |  83 kB   00:00     
	(21/33): perl-Socket-2.010-4.el7.x86_64.rpm                |  49 kB   00:00     
	(22/33): perl-Storable-2.45-3.el7.x86_64.rpm               |  77 kB   00:00     
	(23/33): perl-Text-ParseWords-3.29-4.el7.noarch.rpm        |  14 kB   00:00     
	(24/33): perl-Time-Local-1.2300-2.el7.noarch.rpm           |  24 kB   00:00     
	(25/33): perl-Time-HiRes-1.9725-3.el7.x86_64.rpm           |  45 kB   00:00     
	(26/33): perl-constant-1.27-2.el7.noarch.rpm               |  19 kB   00:00     
	(27/33): perl-libs-5.16.3-292.el7.x86_64.rpm               | 688 kB   00:00     
	(28/33): perl-parent-0.225-244.el7.noarch.rpm              |  12 kB   00:00     
	(29/33): perl-macros-5.16.3-292.el7.x86_64.rpm             |  43 kB   00:00     
	(30/33): perl-podlators-2.5.1-3.el7.noarch.rpm             | 112 kB   00:00     
	(31/33): perl-threads-1.87-4.el7.x86_64.rpm                |  49 kB   00:00     
	(32/33): perl-threads-shared-1.43-6.el7.x86_64.rpm         |  39 kB   00:00     
	(33/33): mysql-community-server-5.7.19-1.el7.x86_64.rpm    | 164 MB   00:03     
	--------------------------------------------------------------------------------
	Total                                               59 MB/s | 203 MB  00:03     
	Obteniendo clave desde file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
	Importando llave GPG 0x5072E1F5:
	 Usuarioid  : "MySQL Release Engineering <mysql-build@oss.oracle.com>"
	 Huella       : a4a9 4068 76fc bd3c 4567 70c8 8c71 8d3b 5072 e1f5
	 Paquete    : mysql57-community-release-el7-11.noarch (installed)
	 Desde      : /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
	Running transaction check
	Running transaction test
	Transaction test succeeded
	Running transaction
	Advertencia: Las bases de datos (RPMDB) han sido modificadas por un elemento ajeno a yum.
	  Instalando    : mysql-community-common-5.7.19-1.el7.x86_64               1/34 
	  Instalando    : mysql-community-libs-5.7.19-1.el7.x86_64                 2/34 
	  Instalando    : mysql-community-client-5.7.19-1.el7.x86_64               3/34 
	  Instalando    : 1:perl-parent-0.225-244.el7.noarch                       4/34 
	  Instalando    : perl-HTTP-Tiny-0.033-3.el7.noarch                        5/34 
	  Instalando    : perl-podlators-2.5.1-3.el7.noarch                        6/34 
	  Instalando    : perl-Pod-Perldoc-3.20-4.el7.noarch                       7/34 
	  Instalando    : 1:perl-Pod-Escapes-1.04-292.el7.noarch                   8/34 
	  Instalando    : perl-Text-ParseWords-3.29-4.el7.noarch                   9/34 
	  Instalando    : perl-Encode-2.51-7.el7.x86_64                           10/34 
	  Instalando    : perl-Pod-Usage-1.63-3.el7.noarch                        11/34 
	  Instalando    : 4:perl-macros-5.16.3-292.el7.x86_64                     12/34 
	  Instalando    : 4:perl-libs-5.16.3-292.el7.x86_64                       13/34 
	  Instalando    : 4:perl-Time-HiRes-1.9725-3.el7.x86_64                   14/34 
	  Instalando    : perl-Exporter-5.68-3.el7.noarch                         15/34 
	  Instalando    : perl-constant-1.27-2.el7.noarch                         16/34 
	  Instalando    : perl-Time-Local-1.2300-2.el7.noarch                     17/34 
	  Instalando    : perl-Socket-2.010-4.el7.x86_64                          18/34 
	  Instalando    : perl-Carp-1.26-244.el7.noarch                           19/34 
	  Instalando    : perl-Storable-2.45-3.el7.x86_64                         20/34 
	  Instalando    : perl-PathTools-3.40-5.el7.x86_64                        21/34 
	  Instalando    : perl-Scalar-List-Utils-1.27-248.el7.x86_64              22/34 
	  Instalando    : perl-File-Temp-0.23.01-3.el7.noarch                     23/34 
	  Instalando    : perl-File-Path-2.09-2.el7.noarch                        24/34 
	  Instalando    : perl-threads-shared-1.43-6.el7.x86_64                   25/34 
	  Instalando    : perl-threads-1.87-4.el7.x86_64                          26/34 
	  Instalando    : perl-Filter-1.49-3.el7.x86_64                           27/34 
	  Instalando    : 1:perl-Pod-Simple-3.28-4.el7.noarch                     28/34 
	  Instalando    : perl-Getopt-Long-2.40-2.el7.noarch                      29/34 
	  Instalando    : 4:perl-5.16.3-292.el7.x86_64                            30/34 
	  Instalando    : libaio-0.3.109-13.el7.x86_64                            31/34 
	  Instalando    : mysql-community-server-5.7.19-1.el7.x86_64              32/34 
	  Instalando    : mysql-community-libs-compat-5.7.19-1.el7.x86_64         33/34 
	  Eliminando    : 1:mariadb-libs-5.5.44-2.el7.x86_64                      34/34 
	  Comprobando   : perl-HTTP-Tiny-0.033-3.el7.noarch                        1/34 
	  Comprobando   : mysql-community-client-5.7.19-1.el7.x86_64               2/34 
	  Comprobando   : mysql-community-libs-compat-5.7.19-1.el7.x86_64          3/34 
	  Comprobando   : perl-threads-shared-1.43-6.el7.x86_64                    4/34 
	  Comprobando   : 4:perl-Time-HiRes-1.9725-3.el7.x86_64                    5/34 
	  Comprobando   : perl-Exporter-5.68-3.el7.noarch                          6/34 
	  Comprobando   : perl-constant-1.27-2.el7.noarch                          7/34 
	  Comprobando   : perl-PathTools-3.40-5.el7.x86_64                         8/34 
	  Comprobando   : 4:perl-macros-5.16.3-292.el7.x86_64                      9/34 
	  Comprobando   : 1:perl-parent-0.225-244.el7.noarch                      10/34 
	  Comprobando   : 4:perl-5.16.3-292.el7.x86_64                            11/34 
	  Comprobando   : perl-File-Temp-0.23.01-3.el7.noarch                     12/34 
	  Comprobando   : mysql-community-libs-5.7.19-1.el7.x86_64                13/34 
	  Comprobando   : 1:perl-Pod-Simple-3.28-4.el7.noarch                     14/34 
	  Comprobando   : perl-Time-Local-1.2300-2.el7.noarch                     15/34 
	  Comprobando   : 4:perl-libs-5.16.3-292.el7.x86_64                       16/34 
	  Comprobando   : mysql-community-common-5.7.19-1.el7.x86_64              17/34 
	  Comprobando   : libaio-0.3.109-13.el7.x86_64                            18/34 
	  Comprobando   : perl-Socket-2.010-4.el7.x86_64                          19/34 
	  Comprobando   : perl-Carp-1.26-244.el7.noarch                           20/34 
	  Comprobando   : perl-Storable-2.45-3.el7.x86_64                         21/34 
	  Comprobando   : perl-Scalar-List-Utils-1.27-248.el7.x86_64              22/34 
	  Comprobando   : 1:perl-Pod-Escapes-1.04-292.el7.noarch                  23/34 
	  Comprobando   : perl-Pod-Usage-1.63-3.el7.noarch                        24/34 
	  Comprobando   : perl-Encode-2.51-7.el7.x86_64                           25/34 
	  Comprobando   : perl-podlators-2.5.1-3.el7.noarch                       26/34 
	  Comprobando   : perl-Getopt-Long-2.40-2.el7.noarch                      27/34 
	  Comprobando   : perl-File-Path-2.09-2.el7.noarch                        28/34 
	  Comprobando   : perl-threads-1.87-4.el7.x86_64                          29/34 
	  Comprobando   : perl-Filter-1.49-3.el7.x86_64                           30/34 
	  Comprobando   : perl-Pod-Perldoc-3.20-4.el7.noarch                      31/34 
	  Comprobando   : perl-Text-ParseWords-3.29-4.el7.noarch                  32/34 
	  Comprobando   : mysql-community-server-5.7.19-1.el7.x86_64              33/34 
	  Comprobando   : 1:mariadb-libs-5.5.44-2.el7.x86_64                      34/34 

	Instalado:
	  mysql-community-libs.x86_64 0:5.7.19-1.el7                                    
	  mysql-community-libs-compat.x86_64 0:5.7.19-1.el7                             
	  mysql-community-server.x86_64 0:5.7.19-1.el7                                  

	Dependencia(s) instalada(s):
	  libaio.x86_64 0:0.3.109-13.el7                                                
	  mysql-community-client.x86_64 0:5.7.19-1.el7                                  
	  mysql-community-common.x86_64 0:5.7.19-1.el7                                  
	  perl.x86_64 4:5.16.3-292.el7                                                  
	  perl-Carp.noarch 0:1.26-244.el7                                               
	  perl-Encode.x86_64 0:2.51-7.el7                                               
	  perl-Exporter.noarch 0:5.68-3.el7                                             
	  perl-File-Path.noarch 0:2.09-2.el7                                            
	  perl-File-Temp.noarch 0:0.23.01-3.el7                                         
	  perl-Filter.x86_64 0:1.49-3.el7                                               
	  perl-Getopt-Long.noarch 0:2.40-2.el7                                          
	  perl-HTTP-Tiny.noarch 0:0.033-3.el7                                           
	  perl-PathTools.x86_64 0:3.40-5.el7                                            
	  perl-Pod-Escapes.noarch 1:1.04-292.el7                                        
	  perl-Pod-Perldoc.noarch 0:3.20-4.el7                                          
	  perl-Pod-Simple.noarch 1:3.28-4.el7                                           
	  perl-Pod-Usage.noarch 0:1.63-3.el7                                            
	  perl-Scalar-List-Utils.x86_64 0:1.27-248.el7                                  
	  perl-Socket.x86_64 0:2.010-4.el7                                              
	  perl-Storable.x86_64 0:2.45-3.el7                                             
	  perl-Text-ParseWords.noarch 0:3.29-4.el7                                      
	  perl-Time-HiRes.x86_64 4:1.9725-3.el7                                         
	  perl-Time-Local.noarch 0:1.2300-2.el7                                         
	  perl-constant.noarch 0:1.27-2.el7                                             
	  perl-libs.x86_64 4:5.16.3-292.el7                                             
	  perl-macros.x86_64 4:5.16.3-292.el7                                           
	  perl-parent.noarch 1:0.225-244.el7                                            
	  perl-podlators.noarch 0:2.5.1-3.el7                                           
	  perl-threads.x86_64 0:1.87-4.el7                                              
	  perl-threads-shared.x86_64 0:1.43-6.el7                                       

	Sustituido(s):
	  mariadb-libs.x86_64 1:5.5.44-2.el7                                            

	¡Listo!

	**iniciando mysqld**
	[root@ip-172-31-12-99 ~]# sudo service mysqld start
	Redirecting to /bin/systemctl start  mysqld.service

	**obteniendo la clave temporal**
	[root@ip-172-31-12-99 ~]# grep 'temporary password' /var/log/mysqld.log
	2017-10-02T18:16:38.964834Z 1 [Note] A temporary password is generated for root@localhost: +M/fLeihe6,.

	**accediendo a mysql**
	[root@ip-172-31-12-99 ~]# mysql -uroot -p
	Enter password: 
	Welcome to the MySQL monitor.  Commands end with ; or \g.
	Your MySQL connection id is 3
	Server version: 5.7.19

	Copyright (c) 2000, 2017, Oracle and/or its affiliates. All rights reserved.

	Oracle is a registered trademark of Oracle Corporation and/or its
	affiliates. Other names may be trademarks of their respective
	owners.

	Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

	**cambiando el pass de root**
	mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY '********';
	Query OK, 0 rows affected (0,00 sec)

	**creando el usuario para la conexion desde otros nodos**
	mysql> CREATE USER 'bootcamp'@'%' IDENTIFIED BY '*******';
	Query OK, 0 rows affected (0,00 sec)

	mysql> GRANT ALL PRIVILEGES ON * . * TO 'bootcamp'@'%';
	Query OK, 0 rows affected (0,00 sec)


	**Configurando el conector de mysql**
	[root@ip-172-31-12-99 ~]# wget http://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.39.tar.gz
	--2017-10-02 14:36:01--  http://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.39.tar.gz
	Resolviendo dev.mysql.com (dev.mysql.com)... 137.254.60.11
	Conectando con dev.mysql.com (dev.mysql.com)[137.254.60.11]:80... conectado.
	Petición HTTP enviada, esperando respuesta... 301 Moved Permanently
	Localización: https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.39.tar.gz [siguiendo]
	--2017-10-02 14:36:01--  https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.39.tar.gz
	Conectando con dev.mysql.com (dev.mysql.com)[137.254.60.11]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 302 Found
	Localización: https://cdn.mysql.com//archives/mysql-connector-java-5.1/mysql-connector-java-5.1.39.tar.gz [siguiendo]
	--2017-10-02 14:36:01--  https://cdn.mysql.com//archives/mysql-connector-java-5.1/mysql-connector-java-5.1.39.tar.gz
	Resolviendo cdn.mysql.com (cdn.mysql.com)... 23.48.156.204
	Conectando con cdn.mysql.com (cdn.mysql.com)[23.48.156.204]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 200 OK
	Longitud: 3899019 (3,7M) [application/x-tar-gz]
	Grabando a: “mysql-connector-java-5.1.39.tar.gz”

	100%[======================================>] 3.899.019   --.-K/s   en 0,07s   

	2017-10-02 14:36:02 (50,0 MB/s) - “mysql-connector-java-5.1.39.tar.gz” guardado [3899019/3899019]

	[root@ip-172-31-12-99 ~]# tar zxvf mysql-connector-java-5.1.39.tar.gz
	mysql-connector-java-5.1.39/
	mysql-connector-java-5.1.39/docs/
	mysql-connector-java-5.1.39/src/
	mysql-connector-java-5.1.39/src/com/
	mysql-connector-java-5.1.39/src/com/mysql/
	mysql-connector-java-5.1.39/src/com/mysql/fabric/
	mysql-connector-java-5.1.39/src/com/mysql/fabric/hibernate/
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/
	mysql-connector-java-5.1.39/src/com/mysql/fabric/proto/
	mysql-connector-java-5.1.39/src/com/mysql/fabric/proto/xmlrpc/
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/exceptions/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/authentication/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/configs/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/integration/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/integration/c3p0/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/integration/jboss/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/interceptors/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jmx/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/log/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/profiler/
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/
	mysql-connector-java-5.1.39/src/demo/
	mysql-connector-java-5.1.39/src/demo/fabric/
	mysql-connector-java-5.1.39/src/demo/fabric/resources/
	mysql-connector-java-5.1.39/src/demo/fabric/resources/com/
	mysql-connector-java-5.1.39/src/demo/fabric/resources/com/mysql/
	mysql-connector-java-5.1.39/src/demo/fabric/resources/com/mysql/fabric/
	mysql-connector-java-5.1.39/src/demo/fabric/resources/com/mysql/fabric/demo/
	mysql-connector-java-5.1.39/src/doc/
	mysql-connector-java-5.1.39/src/doc/sources/
	mysql-connector-java-5.1.39/src/lib/
	mysql-connector-java-5.1.39/src/org/
	mysql-connector-java-5.1.39/src/org/gjt/
	mysql-connector-java-5.1.39/src/org/gjt/mm/
	mysql-connector-java-5.1.39/src/org/gjt/mm/mysql/
	mysql-connector-java-5.1.39/src/testsuite/
	mysql-connector-java-5.1.39/src/testsuite/fabric/
	mysql-connector-java-5.1.39/src/testsuite/fabric/jdbc/
	mysql-connector-java-5.1.39/src/testsuite/perf/
	mysql-connector-java-5.1.39/src/testsuite/regression/
	mysql-connector-java-5.1.39/src/testsuite/regression/jdbc4/
	mysql-connector-java-5.1.39/src/testsuite/regression/jdbc42/
	mysql-connector-java-5.1.39/src/testsuite/simple/
	mysql-connector-java-5.1.39/src/testsuite/simple/jdbc4/
	mysql-connector-java-5.1.39/src/testsuite/simple/jdbc42/
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/
	mysql-connector-java-5.1.39/CHANGES
	mysql-connector-java-5.1.39/COPYING
	mysql-connector-java-5.1.39/README
	mysql-connector-java-5.1.39/README.txt
	mysql-connector-java-5.1.39/build.xml
	mysql-connector-java-5.1.39/docs/README.txt
	mysql-connector-java-5.1.39/docs/connector-j.html
	mysql-connector-java-5.1.39/docs/connector-j.pdf
	mysql-connector-java-5.1.39/mysql-connector-java-5.1.39-bin.jar
	mysql-connector-java-5.1.39/src/com/mysql/fabric/FabricCommunicationException.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/FabricConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/FabricStateResponse.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/HashShardMapping.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/RangeShardMapping.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/Response.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/Server.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/ServerGroup.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/ServerMode.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/ServerRole.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/ShardIndex.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/ShardMapping.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/ShardMappingFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/ShardTable.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/ShardingType.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/hibernate/FabricMultiTenantConnectionProvider.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/ErrorReportingExceptionInterceptor.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/FabricMySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/FabricMySQLConnectionProperties.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/FabricMySQLConnectionProxy.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/FabricMySQLDataSource.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/FabricMySQLDriver.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/JDBC4FabricMySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/jdbc/JDBC4FabricMySQLConnectionProxy.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/proto/xmlrpc/AuthenticatedXmlRpcMethodCaller.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/proto/xmlrpc/DigestAuthentication.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/proto/xmlrpc/InternalXmlRpcMethodCaller.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/proto/xmlrpc/ResultSetParser.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/proto/xmlrpc/XmlRpcClient.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/proto/xmlrpc/XmlRpcMethodCaller.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/Client.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/Array.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/Data.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/Fault.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/Member.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/MethodCall.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/MethodResponse.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/Param.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/Params.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/ResponseParser.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/Struct.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/base/Value.java
	mysql-connector-java-5.1.39/src/com/mysql/fabric/xmlrpc/exceptions/MySQLFabricException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/AbandonedConnectionCleanupThread.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/AssertionFailedException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/AuthenticationPlugin.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/BalanceStrategy.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/BestResponseTimeBalanceStrategy.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Blob.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/BlobFromLocator.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Buffer.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/BufferRow.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ByteArrayRow.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/CacheAdapter.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/CacheAdapterFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/CachedResultSetMetaData.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/CallableStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/CharsetMapping.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Charsets.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Clob.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/CommunicationsException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/CompressedInputStream.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Connection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ConnectionFeatureNotAvailableException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ConnectionGroup.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ConnectionGroupManager.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ConnectionImpl.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ConnectionLifecycleInterceptor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ConnectionProperties.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ConnectionPropertiesImpl.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ConnectionPropertiesTransform.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Constants.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/DatabaseMetaData.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/DatabaseMetaDataUsingInfoSchema.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/DocsConnectionPropsHelper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Driver.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/EscapeProcessor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/EscapeProcessorResult.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/EscapeTokenizer.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ExceptionInterceptor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ExportControlled.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Extension.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/FailoverConnectionProxy.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Field.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/IterateBlock.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC42CallableStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC42Helper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC42PreparedStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC42ResultSet.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC42ServerPreparedStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC42UpdatableResultSet.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4CallableStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4ClientInfoProvider.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4ClientInfoProviderSP.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4CommentClientInfoProvider.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4Connection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4DatabaseMetaData.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4DatabaseMetaDataUsingInfoSchema.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4LoadBalancedMySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4MultiHostMySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4MySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4MysqlSQLXML.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4NClob.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4PreparedStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4PreparedStatementHelper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4ReplicationMySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4ResultSet.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4ServerPreparedStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/JDBC4UpdatableResultSet.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/LicenseConfiguration.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/LoadBalanceExceptionChecker.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/LoadBalancedAutoCommitInterceptor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/LoadBalancedConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/LoadBalancedConnectionProxy.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/LoadBalancedMySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/LocalizedErrorMessages.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Messages.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MiniAdmin.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MultiHostConnectionProxy.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MultiHostMySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MysqlDataTruncation.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MysqlDefs.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MysqlErrorNumbers.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MysqlIO.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MysqlParameterMetadata.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/MysqlSavepoint.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/NamedPipeSocketFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/NdbLoadBalanceExceptionChecker.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/NetworkResources.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/NoSubInterceptorWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/NonRegisteringDriver.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/NonRegisteringReplicationDriver.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/NotImplemented.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/NotUpdatable.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/OperationNotSupportedException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/OutputStreamWatcher.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/PacketTooBigException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ParameterBindings.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/PerConnectionLRUFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/PerVmServerConfigCacheFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/PingTarget.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/PreparedStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ProfilerEventHandlerFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/RandomBalanceStrategy.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ReflectiveStatementInterceptorAdapter.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ReplicationConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ReplicationConnectionGroup.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ReplicationConnectionGroupManager.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ReplicationConnectionProxy.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ReplicationDriver.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ReplicationMySQLConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ResultSetImpl.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ResultSetInternalMethods.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ResultSetMetaData.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ResultSetRow.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/RowData.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/RowDataCursor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/RowDataDynamic.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/RowDataStatic.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/SQLError.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Security.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/SequentialBalanceStrategy.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/ServerPreparedStatement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/SingleByteCharsetConverter.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/SocketFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/SocketMetadata.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/SocksProxySocketFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/StandardLoadBalanceExceptionChecker.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/StandardSocketFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Statement.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/StatementImpl.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/StatementInterceptor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/StatementInterceptorV2.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/StreamingNotifiable.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/StringUtils.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/TimeUtil.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/TimeZoneMapping.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/UpdatableResultSet.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Util.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/V1toV2StatementInterceptorAdapter.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/WatchableOutputStream.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/WatchableWriter.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/Wrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/WriterWatcher.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/authentication/MysqlClearPasswordPlugin.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/authentication/MysqlNativePasswordPlugin.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/authentication/MysqlOldPasswordPlugin.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/authentication/Sha256PasswordPlugin.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/configs/3-0-Compat.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/configs/5-0-Compat.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/configs/clusterBase.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/configs/coldFusion.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/configs/fullDebug.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/configs/maxPerformance.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/configs/solarisMaxPerformance.properties
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/DeadlockTimeoutRollbackMarker.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLDataException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLIntegrityConstraintViolationException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLInvalidAuthorizationSpecException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLNonTransientConnectionException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLNonTransientException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLQueryInterruptedException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLStatementCancelledException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLSyntaxErrorException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLTimeoutException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLTransactionRollbackException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLTransientConnectionException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/MySQLTransientException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/CommunicationsException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLDataException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLIntegrityConstraintViolationException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLInvalidAuthorizationSpecException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLNonTransientConnectionException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLNonTransientException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLQueryInterruptedException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLSyntaxErrorException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLTimeoutException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLTransactionRollbackException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLTransientConnectionException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/exceptions/jdbc4/MySQLTransientException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/integration/c3p0/MysqlConnectionTester.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/integration/jboss/ExtendedMysqlExceptionSorter.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/integration/jboss/MysqlValidConnectionChecker.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/interceptors/ResultSetScannerInterceptor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/interceptors/ServerStatusDiffInterceptor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/interceptors/SessionAssociationInterceptor.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/CallableStatementWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/ConnectionWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC42CallableStatementWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC42PreparedStatementWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC4CallableStatementWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC4ConnectionWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC4MysqlPooledConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC4MysqlXAConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC4PreparedStatementWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC4StatementWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/JDBC4SuspendableXAConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/MysqlConnectionPoolDataSource.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/MysqlDataSource.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/MysqlDataSourceFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/MysqlPooledConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/MysqlXAConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/MysqlXADataSource.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/MysqlXAException.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/MysqlXid.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/PreparedStatementWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/StatementWrapper.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/SuspendableXAConnection.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jdbc2/optional/WrapperBase.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jmx/LoadBalanceConnectionGroupManager.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jmx/LoadBalanceConnectionGroupManagerMBean.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jmx/ReplicationGroupManager.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/jmx/ReplicationGroupManagerMBean.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/log/Jdk14Logger.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/log/Log.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/log/LogFactory.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/log/LogUtils.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/log/NullLogger.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/log/Slf4JLogger.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/log/StandardLogger.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/profiler/LoggingProfilerEventHandler.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/profiler/ProfilerEvent.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/profiler/ProfilerEventHandler.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/Base64Decoder.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/BaseBugReport.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/ErrorMappingsDocGenerator.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/LRUCache.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/PropertiesDocGenerator.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/ReadAheadInputStream.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/ResultSetUtil.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/ServerController.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/TimezoneDump.java
	mysql-connector-java-5.1.39/src/com/mysql/jdbc/util/VersionFSHierarchyMaker.java
	mysql-connector-java-5.1.39/src/demo/fabric/Client1_Fabric.java
	mysql-connector-java-5.1.39/src/demo/fabric/Employee.java
	mysql-connector-java-5.1.39/src/demo/fabric/EmployeesDataSource.java
	mysql-connector-java-5.1.39/src/demo/fabric/EmployeesJdbc.java
	mysql-connector-java-5.1.39/src/demo/fabric/HibernateFabric.java
	mysql-connector-java-5.1.39/src/demo/fabric/resources/com/mysql/fabric/demo/employee.hbm.xml
	mysql-connector-java-5.1.39/src/doc/sources/pom.xml
	mysql-connector-java-5.1.39/src/lib/c3p0-0.9.1-pre6.jar
	mysql-connector-java-5.1.39/src/lib/c3p0-0.9.1-pre6.src.zip
	mysql-connector-java-5.1.39/src/lib/jboss-common-jdbc-wrapper-src.jar
	mysql-connector-java-5.1.39/src/lib/jboss-common-jdbc-wrapper.jar
	mysql-connector-java-5.1.39/src/lib/slf4j-api-1.6.1.jar
	mysql-connector-java-5.1.39/src/org/gjt/mm/mysql/Driver.java
	mysql-connector-java-5.1.39/src/testsuite/BaseStatementInterceptor.java
	mysql-connector-java-5.1.39/src/testsuite/BaseTestCase.java
	mysql-connector-java-5.1.39/src/testsuite/UnreliableSocketFactory.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/BaseFabricTestCase.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/SetupFabricTestsuite.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/TestAdminCommands.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/TestDumpCommands.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/TestResultSetParser.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/TestShardMapping.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/TestXmlRpcCore.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/jdbc/TestBasicConnection.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/jdbc/TestFabricMySQLConnectionSharding.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/jdbc/TestHABasics.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/jdbc/TestHashSharding.java
	mysql-connector-java-5.1.39/src/testsuite/fabric/jdbc/TestRegressions.java
	mysql-connector-java-5.1.39/src/testsuite/perf/BasePerfTest.java
	mysql-connector-java-5.1.39/src/testsuite/perf/LoadStorePerfTest.java
	mysql-connector-java-5.1.39/src/testsuite/perf/RetrievalPerfTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/BlobRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/CachedRowsetTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/CallableStatementRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/CharsetRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/ConnectionRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/DataSourceRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/EscapeProcessorRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/MetaDataRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/MicroPerformanceRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/NumbersRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/PooledConnectionRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/ResultSetRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/StatementRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/StressRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/StringRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/SubqueriesRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/SyntaxRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/UtilsRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/jdbc4/ConnectionRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/jdbc4/ExceptionSubclassesTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/jdbc4/MetaDataRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/jdbc4/StatementRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/regression/jdbc42/StatementRegressionTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/BlobTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/CallableStatementTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/CharsetTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/ConnectionTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/DataSourceTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/DateTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/EscapeProcessingTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/MetadataTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/MiniAdminTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/MultiHostConnectionTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/NumbersTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/ReadOnlyCallableStatementTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/ResultSetTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/SSLTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/ServerControllerTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/SimpleTransformer.java
	mysql-connector-java-5.1.39/src/testsuite/simple/SplitDBdotNameTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/StatementsTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/StringUtilsTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/TestBug57662Logger.java
	mysql-connector-java-5.1.39/src/testsuite/simple/TestLifecycleInterceptor.java
	mysql-connector-java-5.1.39/src/testsuite/simple/TransactionTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/TraversalTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/UpdatabilityTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/UtilsTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/XATest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/jdbc4/StatementsTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/jdbc42/ConnectionTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/jdbc42/ResultSetTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/jdbc42/StatementsTest.java
	mysql-connector-java-5.1.39/src/testsuite/simple/tb2-data.txt.gz
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/ca-cert.pem
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/ca-key.pem
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/mykey.pem
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/mykey.pub
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/server-cert.pem
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/server-key.pem
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/server-req.pem
	mysql-connector-java-5.1.39/src/testsuite/ssl-test-certs/test-cert-store

	**moviendo el conector para /usr/share/java**
	[root@ip-172-31-12-99 ~]# sudo mkdir -p /usr/share/java
	[root@ip-172-31-12-99 ~]# sudo cp mysql-connector-java-5.1.39/mysql-connector-java-5.1.39-bin.jar /usr/share/java/mysql-connector-java.jar

	**instalando java**
	[ec2-user@ip-172-31-12-99 ~]$ wget http://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.12/RPMS/x86_64/oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm
	--2017-10-02 15:00:10--  http://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.12/RPMS/x86_64/oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm
	Resolviendo archive.cloudera.com (archive.cloudera.com)... 151.101.52.167
	Conectando con archive.cloudera.com (archive.cloudera.com)[151.101.52.167]:80... conectado.
	Petición HTTP enviada, esperando respuesta... 200 OK
	Longitud: 142039186 (135M) [application/x-redhat-package-manager]
	Grabando a: “oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm”

	100%[======================================>] 142.039.186 43,1MB/s   en 3,1s   

	2017-10-02 15:00:13 (43,1 MB/s) - “oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm” guardado [142039186/142039186]

	[ec2-user@ip-172-31-12-99 ~]$ sudo rpm -ivh oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm
	advertencia:oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm: EncabezadoV4 DSA/SHA1 Signature, ID de clave e8f86acd: NOKEY
	Preparando...                         ################################# [100%]
	Actualizando / instalando...
	   1:oracle-j2sdk1.7-1.7.0+update67-1 ################################# [100%]

	**descargando e instalando cloudera manager**
	[ec2-user@ip-172-31-12-99 ~]$ wget https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/cloudera-manager.repo
	--2017-10-02 15:01:00--  https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/cloudera-manager.repo
	Resolviendo archive.cloudera.com (archive.cloudera.com)... 151.101.52.167
	Conectando con archive.cloudera.com (archive.cloudera.com)[151.101.52.167]:443... conectado.
	Petición HTTP enviada, esperando respuesta... 200 OK
	Longitud: 290
	Grabando a: “cloudera-manager.repo”

	100%[======================================>] 290         --.-K/s   en 0s      

	2017-10-02 15:01:00 (69,0 MB/s) - “cloudera-manager.repo” guardado [290/290]

	[ec2-user@ip-172-31-12-99 ~]$ ls
	cloudera-manager.repo  oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm
	[ec2-user@ip-172-31-12-99 ~]$ vi cloudera-manager.repo 
	[ec2-user@ip-172-31-12-99 ~]$ sudo mv cloudera-manager.repo /etc/yum.repos.d
	[ec2-user@ip-172-31-12-99 ~]$ sudo yum install -y cloudera-manager-daemons cloudera-manager-server
	Complementos cargados:amazon-id, rhui-lb, search-disabled-repos
	cloudera-manager                                           |  951 B  00:00:00     
	cloudera-manager/primary                                   | 4.3 kB  00:00:00     
	cloudera-manager                                                              7/7
	Resolviendo dependencias
	--> Ejecutando prueba de transacción
	---> Paquete cloudera-manager-daemons.x86_64 0:5.11.2-1.cm5112.p0.6.el7 debe ser instalado
	---> Paquete cloudera-manager-server.x86_64 0:5.11.2-1.cm5112.p0.6.el7 debe ser instalado
	--> Resolución de dependencias finalizada

	Dependencias resueltas

	==================================================================================
	 Package                  Arquitectura
		                         Versión                   Repositorio      Tamaño
	==================================================================================
	Instalando:
	 cloudera-manager-daemons x86_64 5.11.2-1.cm5112.p0.6.el7  cloudera-manager 651 M
	 cloudera-manager-server  x86_64 5.11.2-1.cm5112.p0.6.el7  cloudera-manager 8.5 k

	Resumen de la transacción
	==================================================================================
	Instalar  2 Paquetes

	Tamaño total de la descarga: 651 M
	Tamaño instalado: 826 M
	Downloading packages:
	advertencia:/var/cache/yum/x86_64/7Server/cloudera-manager/packages/cloudera-manager-server-5.11.2-1.cm5112.p0.6.el7.x86_64.rpm: EncabezadoV4 DSA/SHA1 Signature, ID de clave e8f86acd: NOKEY
	No se ha instalado la llave pública de cloudera-manager-server-5.11.2-1.cm5112.p0.6.el7.x86_64.rpm 
	(1/2): cloudera-manager-server-5.11.2-1.cm5112.p0.6.el7.x8 | 8.5 kB  00:00:00     
	(2/2): cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el7.x | 651 MB  00:00:13     
	----------------------------------------------------------------------------------
	Total                                                 48 MB/s | 651 MB  00:13     
	Obteniendo clave desde https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera
	Importando llave GPG 0xE8F86ACD:
	 Usuarioid  : "Yum Maintainer <webmaster@cloudera.com>"
	 Huella       : 5f14 d39e f068 1aca 6f04 4a43 f90c 0d8f e8f8 6acd
	 Desde      : https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/RPM-GPG-KEY-cloudera
	Running transaction check
	Running transaction test
	Transaction test succeeded
	Running transaction
	Advertencia: Las bases de datos (RPMDB) han sido modificadas por un elemento ajeno a yum.
	  Instalando    : cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el7.x86_64    1/2 
	  Instalando    : cloudera-manager-server-5.11.2-1.cm5112.p0.6.el7.x86_64     2/2 
	  Comprobando   : cloudera-manager-server-5.11.2-1.cm5112.p0.6.el7.x86_64     1/2 
	  Comprobando   : cloudera-manager-daemons-5.11.2-1.cm5112.p0.6.el7.x86_64    2/2 

	Instalado:
	  cloudera-manager-daemons.x86_64 0:5.11.2-1.cm5112.p0.6.el7                      
	  cloudera-manager-server.x86_64 0:5.11.2-1.cm5112.p0.6.el7                       

	¡Listo!
	[ec2-user@ip-172-31-12-99 ~]$ sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql scm bootcamp ********!
	JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
	Verifying that we can write to /etc/cloudera-scm-server
	Creating SCM configuration file in /etc/cloudera-scm-server
	Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
	Mon Oct 02 15:08:18 EDT 2017 WARN: Establishing SSL connection without server's identity verification is not recommended. According to MySQL 5.5.45+, 5.6.26+ and 5.7.6+ requirements SSL connection must be established by default if explicit option isn't set. For compliance with existing applications not using SSL the verifyServerCertificate property is set to 'false'. You need either to explicitly disable SSL by setting useSSL=false, or set useSSL=true and provide truststore for server certificate verification.
	[                          main] DbCommandExecutor              INFO  Successfully connected to database.
	All done, your SCM database is configured correctly!
	[ec2-user@ip-172-31-12-99 ~]$ sudo service cloudera-scm-server start
	Starting cloudera-scm-server (via systemctl):              [  OK  ]




```

