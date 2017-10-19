```	
[centos@ip-10-0-0-207 ~]$ curl -u benjaminMaier:cloudera http://ec2-54-171-173-68.eu-west-1.compute.amazonaws.com:7180/api/v2/cm/deployment
{
  "timestamp" : "2017-10-18T08:48:05.196Z",
  "clusters" : [ {
    "name" : "benjaminMaier",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "593494016"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "593494016"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "3433247539"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "577"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-10-0-0-207.eu-west-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-0c003a4b09864fa6f92f2dc7c6c60104",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-043a9d0791642f49a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-161a08b95e39a3cb78617eaff96fa2c0",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0e29603cc06aa3a3c"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-1e9bb1a67d46df4123e8c9aee0568baa",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-07a6c93e118fcec3a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-59a986a97ec1df89979cce653427e699",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-01256409bea327f34"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "11breg9qlpl5anwy9124l3rp6"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5axyzzym9rdwgbzllu8q4nkav"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "593494016"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-161a08b95e39a3cb78617eaff96fa2c0",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0e29603cc06aa3a3c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "79w1f9lq1fmk64y8ltbgnmh1s"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-59a986a97ec1df89979cce653427e699",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-01256409bea327f34"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a2edn9vil29dwnfzoybz2ew8r"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "20vg4xj39ipibofyvu23mlvt9"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-10-0-0-207.eu-west-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "hue_password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-eed78ce7f37975d446c0bee09d3ac848"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9r37tqcs88nh3eqgs6rmi8g3i"
          }, {
            "name" : "secret_key",
            "value" : "JwgS2LgWM6VAFk5nMjRYPZzDhVVUHK"
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
            "value" : "ip-10-0-0-207.eu-west-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie_password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "593494016"
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
        "name" : "oozie-OOZIE_SERVER-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "755prhro1boegwn6pv30dfv93"
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
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "593494016"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm,/data0/yarn/nm,/mnt/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/data0/yarn/container-logs,/mnt/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "4939"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "593494016"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "4939"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "Kc3LCmWj8ivnB0QfIGfwPICjFixGdt"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b6ixu09ebcggqw95x4jfmwd29"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-0c003a4b09864fa6f92f2dc7c6c60104",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-043a9d0791642f49a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "12q193kaqksxk8uzasrvh2oi9"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-161a08b95e39a3cb78617eaff96fa2c0",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0e29603cc06aa3a3c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "jaipp2w3otewy8gap1ag1jti"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1e9bb1a67d46df4123e8c9aee0568baa",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-07a6c93e118fcec3a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "51crxaklqmtledsfmrlfvzsnx"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-59a986a97ec1df89979cce653427e699",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-01256409bea327f34"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "vngtfnnuer5cmbgdjxw1m5ru"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "53"
          }, {
            "name" : "role_jceks_password",
            "value" : "2d2l0wjtcqbj84qkn6q2lt7q5"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "593494016"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn,/data0/dfs/dn,/mnt/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "4293264998"
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
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
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn,/data0/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "593494016"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "593494016"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "cRAfn9HNeDnYjmk9mfammyoADHJvI0"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "zOCmkRwdQTnPqRMzH7OC1My5JjF3SV"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "2Fhs87Fda5AfCepk8BgQrPLZYwA019"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-0c003a4b09864fa6f92f2dc7c6c60104",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-043a9d0791642f49a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bi10ep5j90moeqrso0w0529pk"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-161a08b95e39a3cb78617eaff96fa2c0",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0e29603cc06aa3a3c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aghxe3s893xqlhfwyt37xmecl"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-1e9bb1a67d46df4123e8c9aee0568baa",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-07a6c93e118fcec3a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3bc8d7lwii088wy8mt7one1tb"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-59a986a97ec1df89979cce653427e699",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-01256409bea327f34"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1tlan0qf8qox100nokf1qh8wv"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-161a08b95e39a3cb78617eaff96fa2c0",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0e29603cc06aa3a3c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "zsg2ydeoytg2y32icko7b08e"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dp46fmro2j9ba2c9ng4vml5nb"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3d91a350mnk78d3v4di50c8kg"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-0c003a4b09864fa6f92f2dc7c6c60104",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-043a9d0791642f49a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8e38bzyy1ylxhx475k1w83idb"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-161a08b95e39a3cb78617eaff96fa2c0",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0e29603cc06aa3a3c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bnvmlei8k5bsfkoqgcap8l2nu"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-59a986a97ec1df89979cce653427e699",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-01256409bea327f34"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2kifp2z5vqf2qbmsidkrfu05p"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-161a08b95e39a3cb78617eaff96fa2c0",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0e29603cc06aa3a3c"
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
            "value" : "62"
          }, {
            "name" : "role_jceks_password",
            "value" : "shln4rwjkcdqz2vk0n9mp273"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-eed78ce7f37975d446c0bee09d3ac848",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-038e6e0dbdeab8b77"
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
            "value" : "55"
          }, {
            "name" : "role_jceks_password",
            "value" : "62w99qz7zuqby25iks9pn4oh"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-038e6e0dbdeab8b77",
    "ipAddress" : "10.0.0.16",
    "hostname" : "ip-10-0-0-16.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0e29603cc06aa3a3c",
    "ipAddress" : "10.0.0.207",
    "hostname" : "ip-10-0-0-207.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-01256409bea327f34",
    "ipAddress" : "10.0.0.250",
    "hostname" : "ip-10-0-0-250.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-043a9d0791642f49a",
    "ipAddress" : "10.0.0.54",
    "hostname" : "ip-10-0-0-54.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-07a6c93e118fcec3a",
    "ipAddress" : "10.0.0.60",
    "hostname" : "ip-10-0-0-60.eu-west-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__95969c7a-a9a9-48d5-8597-0577d4bec479",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "0859766d214ad1ff57289256329d2946071a6ac580d7375731fc253351b492dc",
    "pwSalt" : -2367153219920439892,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-eed78ce7f37975d446c0bee09d3ac848",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "29239d21998516c54a1a1a1f94270ecdb874974558c6d9211017b4e43405ba26",
    "pwSalt" : -4346957646272132578,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-eed78ce7f37975d446c0bee09d3ac848",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "de22235f27ce20a5ca3dc472010d639856df94b052402d802f4a4d0b4f0563d7",
    "pwSalt" : -5742187994050422490,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-eed78ce7f37975d446c0bee09d3ac848",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "d029531cd2b917199280d4ef6df21319f0dc96fae0c70f4377d83e64e0e478ec",
    "pwSalt" : 545615147991039973,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-eed78ce7f37975d446c0bee09d3ac848",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "066b6be588493389c82474a66c0bc685cb9c9810532123caa590a4c142a54cde",
    "pwSalt" : 1018590755538363778,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "173cf5379a795477f2047943fd7eb041c69f27a02a1ffff37f858aad24ced2d4",
    "pwSalt" : 6128999628864359093,
    "pwLogin" : true
  }, {
    "name" : "benjaminMaier",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "5ccc5b069bbfed742641b05064f367734246ad03a36dcf32f48889dc6ee35d66",
    "pwSalt" : 2663809368848288785,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "3e1af0a70c25d97bcce3a247e8b1b61d612b0123f7186b47f02039271b44624e",
    "pwSalt" : 1098327204530564767,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1014",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "593494016"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "593494016"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-10-0-0-207.eu-west-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "593494016"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "593494016"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "805306368"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-eed78ce7f37975d446c0bee09d3ac848",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-038e6e0dbdeab8b77"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "94zxwgg4jn9ykuueetb48req1"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-eed78ce7f37975d446c0bee09d3ac848",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-038e6e0dbdeab8b77"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "eyaztgpfpoq38zq6ji0lod474"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-eed78ce7f37975d446c0bee09d3ac848",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-038e6e0dbdeab8b77"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dmt9rba4t91ysx0ufs9uzyjky"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-eed78ce7f37975d446c0bee09d3ac848",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-038e6e0dbdeab8b77"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2mk717ydlnv79becdjzxtho99"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-eed78ce7f37975d446c0bee09d3ac848",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-038e6e0dbdeab8b77"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dj6ti4osrlcymn353alf6afke"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 2:30"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
```