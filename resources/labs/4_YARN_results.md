```

***slowest***
	### Parametros ######################
	# Data size = 51200000 byte
	# Mapper containers = 3
	# Reducer containers = 3
	# Container memory = 2048
	# MAP_MB = 1638
	# RED_MB = 1638
	# Directorio teragen = tg-10GB-3-3-2048
	# Directorio terasort = ts-10GB-3-3-2048
	#####################################

	## ejecutando teragen ##

	real	1m26.825s
	user	0m5.167s
	sys	0m0.252s

	## ejecutando terasort ##

	real	2m18.625s
	user	0m7.235s
	sys	0m0.341s

	## Eliminando los directorios creados ##
	Deleted tg-10GB-3-3-2048
	Deleted ts-10GB-3-3-2048


***fastest***

	### Parametros ######################
	# Data size = 51200000 byte
	# Mapper containers = 7
	# Reducer containers = 7
	# Container memory = 2048
	# MAP_MB = 1638
	# RED_MB = 1638
	# Directorio teragen = tg-10GB-7-7-2048
	# Directorio terasort = ts-10GB-7-7-2048
	#####################################

	## ejecutando teragen ##

	real	1m16.009s
	user	0m5.276s
	sys	0m0.259s

	## ejecutando terasort ##

	real	1m33.895s
	user	0m7.278s
	sys	0m0.273s

	## Eliminando los directorios creados ##
	Deleted tg-10GB-7-7-2048
	Deleted ts-10GB-7-7-2048

```


