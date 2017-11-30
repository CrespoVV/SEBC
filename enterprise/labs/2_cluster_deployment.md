```{
  "timestamp" : "2017-11-30T16:54:20.200Z",
  "clusters" : [ {
    "name" : "BCTestCluster",
    "version" : "CDH5",
    "services" : [ {
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
        "name" : "zookeeper-SERVER-055c71fda2bec483832566222f4028c3",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "avcv42uo79aiisxkr3k7trjhz"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-514034475b89663abcd400126a2e61b0",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "170c3e3d-ee30-4782-8673 -8ff5aa7d9731"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9xbun14ilh8d83ogbn4kbvzio"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-b7db1dda2c2d626360bcea4ae5d74554",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "1d96b310-d3ec-4e54-9d2b-bdc01d0b499a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9v0m57g90bicl7gh0e84fz641"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
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
            "value" : "3"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1600"
          }, {
            "name" : "rm_io_weight",
            "value" : "800"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm,/data/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/data/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "6"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "15574"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "16061"
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
          "value" : "true"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "EPG7iOvzOijZSTC94VysL3swtbzqtQ"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-055c71fda2bec483832566222f4028c3",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5ix9csxrslpm61ylavtnhal1s"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-2fea9a9a9405a2b2a94593ed67306cff",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "baa36ac6-664b-43dd-8f4a-2cdd9b61030c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3x26qlpda2g0fyakh3q5vad0l"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-514034475b89663abcd400126a2e61b0",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "170c3e3d-ee30-4782-8673-8ff5aa7d9731"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2elo2cnakpxxhq5wbsnytps7m"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-bf98cc84a11cde20fe5a5d5f77e18528",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "e5a0be13-af7d-4169-a227-5d59c061fd27"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "22twwle7obhkq0d2p1gg92gfx"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-055c71fda2bec483832566222f4028c3",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "187"
          }, {
            "name" : "role_jceks_password",
            "value" : "f3lg1gzirfahpyj8jloxdcu0v"
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
            "value" : "/dfs/dn,/data/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "8588674252"
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
            "value" : "/data/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn,/data/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "Ph9H4bOAzq0GEOz2qq5l79PaZBTeQ8"
        }, {
          "name" : "dfs_namenode_acls_enabled",
          "value" : "true"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "J4Bbxt9sUo9yrpzVZ06KUWjsYnCTPW"
        }, {
          "name" : "hadoop_secure_web_ui",
          "value" : "true"
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos"
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true"
        }, {
          "name" : "hdfs_sentry_sync_enable",
          "value" : "true"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "u2PqLXRB3d3COao38v7GyA8uy8mkHc"
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
        "name" : "hdfs-BALANCER-055c71fda2bec483832566222f4028c3",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-2fea9a9a9405a2b2a94593ed67306cff",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "baa36ac6-664b-43dd-8f4a-2cdd9b61030c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9h7r96b00ndgk2q04vmiy03e7"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-514034475b89663abcd400126a2e61b0",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "170c3e3d-ee30-4782-8673-8ff5aa7d9731"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "325bmm4eavyx7za4g85c2dxww"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-bf98cc84a11cde20fe5a5d5f77e18528",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "e5a0be13-af7d-4169-a227-5d59c061fd27"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bky00pjcuvm5bj4hz61c37rq4"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-055c71fda2bec483832566222f4028c3",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8es3rwskn8swjr9jalh90ts6b"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-514034475b89663abcd400126a2e61b0",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "170c3e3d-ee30-4782-8673-8ff5aa7d9731"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cgxubwsl2iulxyjqs4z1d8z5e"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-bf98cc84a11cde20fe5a5d5f77e18528",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "e5a0be13-af7d-4169-a227-5d59c061fd27"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4y1eji7k992r922nelauxvdb4"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-055c71fda2bec483832566222f4028c3",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1n8pkn8k8yjmt1hfih8p1ok8u"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-2fea9a9a9405a2b2a94593ed67306cff",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "baa36ac6-664b-43dd-8f4a-2cdd9b61030c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6t1vnzu35u1nqc4jidtxzg4fn"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-514034475b89663abcd400126a2e61b0",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "170c3e3d-ee30-4782-8673-8ff5aa7d9731"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "en4nfso27zmnew53j609e18yv"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-055c71fda2bec483832566222f4028c3",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
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
            "value" : "189"
          }, {
            "name" : "role_jceks_password",
            "value" : "37q3vi7hfgls56d1ldhmuknbr"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-514034475b89663abcd400126a2e61b0",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "170c3e3d-ee30-4782-8673-8ff5aa7d9731"
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
            "value" : "220"
          }, {
            "name" : "role_jceks_password",
            "value" : "4gmd1aulxixw31jdg7a7xdosy"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_enable_db_notification",
            "value" : "true"
          }, {
            "name" : "hive_metastore_java_heapsize",
            "value" : "536870912"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false"
          }, {
            "name" : "hiveserver2_java_heapsize",
            "value" : "536870912"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "4715813273"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "793"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-49-16.ec2.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "MySQL.20"
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
        "name" : "hive-GATEWAY-055c71fda2bec483832566222f4028c3",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-2fea9a9a9405a2b2a94593ed67306cff",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "baa36ac6-664b-43dd-8f4a-2cdd9b61030c"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-514034475b89663abcd400126a2e61b0",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "170c3e3d-ee30-4782-8673-8ff5aa7d9731"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-b7db1dda2c2d626360bcea4ae5d74554",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1d96b310-d3ec-4e54-9d2b-bdc01d0b499a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-bf98cc84a11cde20fe5a5d5f77e18528",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e5a0be13-af7d-4169-a227-5d59c061fd27"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-bf98cc84a11cde20fe5a5d5f77e18528",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "e5a0be13-af7d-4169-a227-5d59c061fd27"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "41xzrhpt8bgya3fmdo4ucll0l"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-bf98cc84a11cde20fe5a5d5f77e18528",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "e5a0be13-af7d-4169-a227-5d59c061fd27"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "em5hc8fbe1s01egg9nx10h8v2"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-49-16.ec2.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "MySQL.20"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
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
        "name" : "oozie-OOZIE_SERVER-055c71fda2bec483832566222f4028c3",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "26fwj9un3furia8s39yluz0lx"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-49-16.ec2.internal"
        }, {
          "name" : "database_password",
          "value" : "MySQL.20"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-bf98cc84a11cde20fe5a5d5f77e18528"
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
        "name" : "hue-HUE_LOAD_BALANCER-2fea9a9a9405a2b2a94593ed67306cff",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "baa36ac6-664b-43dd-8f4a-2cdd9b61030c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b4if100dsft9kp9h345pnzgbq"
          } ]
        }
      }, {
        "name" : "hue-HUE_SERVER-2fea9a9a9405a2b2a94593ed67306cff",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "baa36ac6-664b-43dd-8f4a-2cdd9b61030c"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "18f088bd-3295-4b52-8e8e-4fafd3320655"
          }, {
            "name" : "role_jceks_password",
            "value" : "3pgzpaosxggzssztr2o9kegtm"
          }, {
            "name" : "secret_key",
            "value" : "caiByFzUAecWIo3hBZFU663DNzhKSO"
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-2fea9a9a9405a2b2a94593ed67306cff",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "baa36ac6-664b-43dd-8f4a-2cdd9b61030c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9nwgvxb3yacllv7i4zw61kmy5"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-172-31-49-16.ec2.internal"
        }, {
          "name" : "sentry_server_database_name",
          "value" : "sentrys"
        }, {
          "name" : "sentry_server_database_password",
          "value" : "MySQL.20"
        }, {
          "name" : "sentry_server_database_user",
          "value" : "sentrys"
        }, {
          "name" : "sentry_service_admin_group",
          "value" : "hive,impala,hue,solr,kafka,hdfs,crispindev"
        }, {
          "name" : "sentry_service_allow_connect",
          "value" : "hive,impala,hue,hdfs,solr,kafka,crispindev"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "sentry-GATEWAY-bf98cc84a11cde20fe5a5d5f77e18528",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "e5a0be13-af7d-4169-a227-5d59c061fd27"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-055c71fda2bec483832566222f4028c3",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1q1nukb8ei3ozfntognoonbaq"
          } ]
        }
      } ],
      "displayName" : "Sentry"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "f0de64db-86ae-46ba-bccf-9ca374b9b496",
    "ipAddress" : "172.31.49.75",
    "hostname" : "ip-172-31-49-75.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "1d96b310-d3ec-4e54-9d2b-bdc01d0b499a",
    "ipAddress" : "172.31.54.226",
    "hostname" : "ip-172-31-54-226.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "170c3e3d-ee30-4782-8673-8ff5aa7d9731",
    "ipAddress" : "172.31.56.149",
    "hostname" : "ip-172-31-56-149.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ {
        "name" : "memory_overcommit_threshold",
        "value" : "1"
      } ]
    }
  }, {
    "hostId" : "e5a0be13-af7d-4169-a227-5d59c061fd27",
    "ipAddress" : "172.31.59.57",
    "hostname" : "ip-172-31-59-57.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "baa36ac6-664b-43dd-8f4a-2cdd9b61030c",
    "ipAddress" : "172.31.61.22",
    "hostname" : "ip-172-31-61-22.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-055c71fda2bec483832566222f4028c3",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "48509583ebbaac0291abc8436bd8bb8380cef133e327948e679570726002ec8f",
    "pwSalt" : -3962572166457354735,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-2fea9a9a9405a2b2a94593ed67306cff",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "fb27f74486483f2e8b71316620fa272fd4b3dda31ecfbcbc0ffae3f8392cf545",
    "pwSalt" : -141546686036635500,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-b7db1dda2c2d626360bcea4ae5d74554",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "265414442ff7bca619c4d12d9133f88053d8ee6ecc6d0ba2c4a5af3e6e56b818",
    "pwSalt" : 5824544613032493387,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-055c71fda2bec483832566222f4028c3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b05546fbc725012ad21c634e22dafa28a0d6cc886f3578fc1003544a6e05c3e1",
    "pwSalt" : -8863841239319815216,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-b7db1dda2c2d626360bcea4ae5d74554",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "aa2d51e22e889e29ce3179826290877f5c9da913b3105d6e21198e6d81b39531",
    "pwSalt" : -7829902555880564561,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-055c71fda2bec483832566222f4028c3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "54b6ea04d459412300836a0902a9b459ba2e8be834e935b45c55934f5145d777",
    "pwSalt" : -1572769709641052331,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-b7db1dda2c2d626360bcea4ae5d74554",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "87520673716aa2a1327b4757e4a907f55945924d2afccfa253e1ba4f50289098",
    "pwSalt" : -2338007067567993643,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-055c71fda2bec483832566222f4028c3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b3d1344a9a661e756e4619436e029891da3054d48ab82be5978692a3f380560f",
    "pwSalt" : 4808264030965752796,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-b7db1dda2c2d626360bcea4ae5d74554",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c1412c3ccb8375879a7aefdbefb6526c518d7f1489670a5dbc5a76caa01cfd96",
    "pwSalt" : 5371218503549646457,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-055c71fda2bec483832566222f4028c3",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "88c419a28f44e31e269544a0f95aee2368e2ae459c91876002e20d70920e1acb",
    "pwSalt" : 2871455653641540973,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-b7db1dda2c2d626360bcea4ae5d74554",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "cefc63022d4f02665b14f1608d9521bd46c4fd65f6c16c060890da2837461a70",
    "pwSalt" : 717893120698997490,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "12abe9d9e613958a86a40dd1873c9ee6a95d6b9f525da55bc0a6e515350e12f6",
    "pwSalt" : -502951654379594660,
    "pwLogin" : true
  }, {
    "name" : "crispindev",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "86b7f76d7725ca1a85a5c2e109590734d8b17a41037bf74c7018470084e9d494",
    "pwSalt" : -6420264194259404955,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "c026da060f2cb2327f9d2f7cd524747c896a11bd62db450ea4f61cc3b503b0cb",
    "pwSalt" : 3710040533782439694,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.12.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170818-0807",
    "gitHash" : "9bdee611802535491d400e03c98ef694a2c77d0a",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-49-16.ec2.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "reportm"
        }, {
          "name" : "headlamp_database_password",
          "value" : "MySQL.20"
        }, {
          "name" : "headlamp_database_user",
          "value" : "reportm"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-b7db1dda2c2d626360bcea4ae5d74554",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "1d96b310-d3ec-4e54-9d2b-bdc01d0b499a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2c5ifgxpkxpyrqlffo1jhab7g"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-b7db1dda2c2d626360bcea4ae5d74554",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "1d96b310-d3ec-4e54-9d2b-bdc01d0b499a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cs1xp5eotw2bgidcfab5pxel0"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-b7db1dda2c2d626360bcea4ae5d74554",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "1d96b310-d3ec-4e54-9d2b-bdc01d0b499a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2ynser8jcj2cjiu66z8myuf6x"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-b7db1dda2c2d626360bcea4ae5d74554",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "1d96b310-d3ec-4e54-9d2b-bdc01d0b499a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4i81flautz6prcngbvcg0m91f"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-b7db1dda2c2d626360bcea4ae5d74554",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "1d96b310-d3ec-4e54-9d2b-bdc01d0b499a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "9nh2p8hibiibrxm4rizno9d1h"
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
      "value" : "10/22/2012 17:00"
    }, {
      "name" : "KDC_ADMIN_HOST",
      "value" : "ip-172-31-59-57.ec2.internal"
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAAA8AAEACVJJQ09ILkNPTQAMY2xvdWRlcmEtc2NtAAAAAVofDvQBABcAEHcm92QlJEO7a+EzhJXZwZMAAAAB"
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm@RICOH.COM"
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-59-57.ec2.internal"
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "arcfour-hmac"
    }, {
      "name" : "KRB_LIBDEFAULTS_SAFETY_VALVE",
      "value" : ""
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
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    }, {
      "name" : "SECURITY_REALM",
      "value" : "RICOH.COM"
    } ]
  }```
  
