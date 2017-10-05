´´´
[ec2-user@ip-172-31-12-99 ~]$ curl -u darwinmartinezagnostic:cloudera 'http://localhost:7180/api/v2/cm/deployment'
{
  "timestamp" : "2017-10-05T14:15:00.319Z",
  "clusters" : [ {
    "name" : "darwinmartinezagnostic",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "2979004416"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "297900441"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false"
          }, {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2979004416"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "1645766246"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "276"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-12-99.us-west-2.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "MyNewPass4!"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "bootcamp"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "sentry_service",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-389e83cd26a8c808524e29a49651d1f5",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e18iutescptc0ivllb1gakvnz"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cufslg679oezmy0bkt5inubc4"
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-389e83cd26a8c808524e29a49651d1f5",
        "type" : "WEBHCAT",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_webhcat_secret_key",
            "value" : "IJfBahPmriA4ngqOfFAr14v4r7NOC4"
          }, {
            "name" : "role_jceks_password",
            "value" : "8rog7oueggtk1x7396tpe3i8y"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6grxhb0e5cmz983fvxtn397nd"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-389e83cd26a8c808524e29a49651d1f5",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e1za48mzwsqqgeyvvfr3mcrzl"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-c0de723634551dae237250012b46c469",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6nfzire9vkrpzw3fhypj62br5"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HUE_SERVER",
          "items" : [ {
            "name" : "hue_http_port",
            "value" : "1888"
          } ]
        } ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-12-99.us-west-2.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "MyNewPass4!"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "bootcamp"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-389e83cd26a8c808524e29a49651d1f5"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "sentry_service",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-c0de723634551dae237250012b46c469",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9axgpr2xt8m4t9uu1rfolxudf"
          }, {
            "name" : "secret_key",
            "value" : "wzRGmD2y9v0wVXVELxA57SkUjVbkPS"
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-c0de723634551dae237250012b46c469",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5lc80lo8rxrrebrdbc3zgn1oi"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-12-99.us-west-2.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "MyNewPass4!"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "bootcamp"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-c0de723634551dae237250012b46c469",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9uyob3oy6xlo2ittrcjsjaisv"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "12"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm,/disk01/yarn/nm,/disk02/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/disk01/yarn/container-logs,/disk02/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "8093"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "13373"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "6"
          } ]
        } ],
        "items" : [ {
          "name" : "hadoop_secure_web_ui",
          "value" : "true"
        }, {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "LT7pjV0Y1UpqmTJI2Rfu2B4OtdXhdx"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-c0de723634551dae237250012b46c469",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cvmf06vkvd5i1wflhqoemmujp"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "72o62dcxmqfig29eplp2ard5l"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-389e83cd26a8c808524e29a49651d1f5",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9capl9jx9stcvu3n1nb24ly0b"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-c0de723634551dae237250012b46c469",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3mz9kfo5tqgfj0cwthxtgyt5t"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "72"
          }, {
            "name" : "role_jceks_password",
            "value" : "50p1xacd02r4n2j9dgstedsan"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/disk01/dfs/dn,/disk02/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700"
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1"
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400"
          }, {
            "name" : "rm_io_weight",
            "value" : "200"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/disk01/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn,/disk01/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_bind_wildcard",
            "value" : "true"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "2979004416"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "2979004416"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "7DUa3GkFcFe8Xkg9sCXwUcjzvj5H1N"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "MAkoAgm53JxMiZGyhuR3uDswTiox3h"
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos"
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "9UOEGOp7XrWt6GhCrY2zVKHkKg4ke8"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-389e83cd26a8c808524e29a49651d1f5",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "97fr11wmfufsf99m7qsgrm2qy"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-389e83cd26a8c808524e29a49651d1f5",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e0g381drd89nncjtb3v5rji31"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-c0de723634551dae237250012b46c469",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7qfah3b7cuf6ahqgelrbox70z"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2hj23dhf1p92w8m5uh0uknep6"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-c0de723634551dae237250012b46c469",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "emdeuscktmhcylajfc4zyzz3z"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-389e83cd26a8c808524e29a49651d1f5",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c39av3y45cg4m73epwmal5ubs"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ec7ozhu6zgu1ncrb4whddawpd"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-389e83cd26a8c808524e29a49651d1f5",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3n7ih2edgnvxxsqm9y66hk5ly"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-c0de723634551dae237250012b46c469",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9qnmczlfx2j3bbp2g07u4its0"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-1a15892b5b81be0dd9c534b513ceea09",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "79"
          }, {
            "name" : "role_jceks_password",
            "value" : "11xc4hky6av2o74o382z4pgaf"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-c0de723634551dae237250012b46c469",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "74"
          }, {
            "name" : "role_jceks_password",
            "value" : "54ohlrprenopv7gerx1dmlwg4"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SENTRY_SERVER",
          "items" : [ {
            "name" : "sentry_server_java_heapsize",
            "value" : "268435456"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-172-31-12-99.us-west-2.compute.internal"
        }, {
          "name" : "sentry_server_database_password",
          "value" : "MyNewPass4!"
        }, {
          "name" : "sentry_server_database_user",
          "value" : "bootcamp"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "sentry-GATEWAY-952bd6de47234e38278e5d53a2781f6c",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "99a1b769-90a7-4c7e-9bec-40389b855e48"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-389e83cd26a8c808524e29a49651d1f5",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9eyi4xgvjvdih55kzfy87v2m1"
          } ]
        }
      } ],
      "displayName" : "Sentry"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "f2406e7e-58fa-40ce-aa08-7ecc4f09eae8",
    "ipAddress" : "172.31.1.176",
    "hostname" : "ip-172-31-1-176.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "99a1b769-90a7-4c7e-9bec-40389b855e48",
    "ipAddress" : "172.31.12.99",
    "hostname" : "ip-172-31-12-99.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "58d98ee3-01b7-412c-83cf-83e5cc60837a",
    "ipAddress" : "172.31.3.136",
    "hostname" : "ip-172-31-3-136.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "b7bb7b67-5633-4250-9956-24f661ebeff7",
    "ipAddress" : "172.31.4.254",
    "hostname" : "ip-172-31-4-254.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-952bd6de47234e38278e5d53a2781f6c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e1ee48d3a7de9ba70444a566313e75dbc3aeacc83c3d77d462c15bb1dd3ccf06",
    "pwSalt" : 5381545334877423473,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-952bd6de47234e38278e5d53a2781f6c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "449a83514f8d8b886411084010f71c7265b1bf0b0dba2601da7087f9070f19df",
    "pwSalt" : 7809707301160455688,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-952bd6de47234e38278e5d53a2781f6c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "d62be4d96b1ae1768b46beb89656df5f4c3f9256cc2e675335f6b53109bcbe1b",
    "pwSalt" : 586528699725771887,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-952bd6de47234e38278e5d53a2781f6c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "94a5dc5d9000a45c05cdefcea4a06cebd23fa0616ef358a98fda8bcab7aac8c5",
    "pwSalt" : -4188303827819563805,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-952bd6de47234e38278e5d53a2781f6c",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "452be2d6e430be8ee0200de4fe22ce2066217671d0e7e6de74444ea7ba8e4677",
    "pwSalt" : 5044673970017146218,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "73bfcfeacce57a3ee1b246fb4958f7967be490088a55fc47dcb32b77773d1d3c",
    "pwSalt" : 954057635363044763,
    "pwLogin" : true
  }, {
    "name" : "darwinmartinezagnostic",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "ed971716df5f1972cc6b9dcb9367f2f82f8101a5d1eaffb77d04d7cf416551a6",
    "pwSalt" : -4999210929688502413,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "7d818de7844f9bd709f3cf7c809c0fe6e2e0edcb24b6728d855254fef402cb93",
    "pwSalt" : 5281265292691112530,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.11.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170811-0014",
    "gitHash" : "3c3ea33a12076fb83a8f11c4452c52fac685d01b",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-172-31-12-99.us-west-2.compute.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "MyNewPass4!"
        }, {
          "name" : "firehose_database_user",
          "value" : "bootcamp"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        }, {
          "name" : "firehose_storage_dir",
          "value" : "/var/log/cloudera-host-monitor"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-12-99.us-west-2.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "MyNewPass4!"
        }, {
          "name" : "headlamp_database_user",
          "value" : "bootcamp"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        }, {
          "name" : "firehose_storage_dir",
          "value" : "/var/log/cloudera-service-monitor"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-952bd6de47234e38278e5d53a2781f6c",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "99a1b769-90a7-4c7e-9bec-40389b855e48"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "67e814y3mf367ujwu3trgrq4f"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-952bd6de47234e38278e5d53a2781f6c",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "99a1b769-90a7-4c7e-9bec-40389b855e48"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6rgdq1hmci8nk4vzc1b3n4bjq"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-952bd6de47234e38278e5d53a2781f6c",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "99a1b769-90a7-4c7e-9bec-40389b855e48"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "25e6buhxebd8p2qom4vsmuq7x"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-952bd6de47234e38278e5d53a2781f6c",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "99a1b769-90a7-4c7e-9bec-40389b855e48"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8xn6xhagxd0grkgh8oigrq2b5"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-952bd6de47234e38278e5d53a2781f6c",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "99a1b769-90a7-4c7e-9bec-40389b855e48"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4vlqeyz7d4xa6bf84t88g52lm"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-952bd6de47234e38278e5d53a2781f6c",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "99a1b769-90a7-4c7e-9bec-40389b855e48"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a2ci24ehb2p1mou3z4t0fjj7m"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false"
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 12:20"
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAAA/AAEADEFHTk9TVElDLkNPTQAMY2xvdWRlcmEtc2NtAAAAAVnU9nEBABcAEKUSfLUQzd3KNFMiY1n2RTQAAAAB"
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm@AGNOSTIC.COM"
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-12-99.us-west-2.compute.internal"
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "arcfour-hmac"
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true"
    }, {
      "name" : "MAX_RENEW_LIFE",
      "value" : "604800"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    }, {
      "name" : "SECURITY_REALM",
      "value" : "AGNOSTIC.COM"
    } ]
  }
}

´´´
