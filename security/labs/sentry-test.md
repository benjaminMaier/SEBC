### kinit

```
[centos@ip-10-0-0-178 ~]$ kinit benjaminMaier
Password for benjaminMaier@BENJAMINMAIER.SG:
```

### beeline

```
[centos@ip-10-0-0-178 ~]$ beeline
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-10-0-0-163.eu-west-1.compute.internal:10000/default;principal=hive/ip-10-0-0-163.eu-west-1.compute.internal@BENJAMINMAIER.SG
scan complete in 2ms
Connecting to jdbc:hive2://ip-10-0-0-163.eu-west-1.compute.internal:10000/default;principal=hive/ip-10-0-0-163.eu-west-1.compute.internal@BENJAMINMAIER.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-0-0-163.eu-west-1.compu>
```

### show tables in beeline

```
0: jdbc:hive2://ip-10-0-0-163.eu-west-1.compu> show tables;
INFO  : Compiling command(queryId=hive_20171019091414_23f737cf-3406-4516-bd01-7c2692ae417d): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019091414_23f737cf-3406-4516-bd01-7c2692ae417d); Time taken: 0.676 seconds
INFO  : Executing command(queryId=hive_20171019091414_23f737cf-3406-4516-bd01-7c2692ae417d): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019091414_23f737cf-3406-4516-bd01-7c2692ae417d); Time taken: 0.27 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.312 seconds)
0: jdbc:hive2://ip-10-0-0-163.eu-west-1.compu>
```



### tables for george

```
[centos@ip-10-0-0-178 ~]$ kinit george
Password for george@BENJAMINMAIER.SG:
[centos@ip-10-0-0-178 ~]$ beeline
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-10-0-0-163.eu-west-1.compute.internal:10000/default;principal=hive/ip-10-0-0-163.eu-west-1.compute.internal@BENJAMINMAIER.SG
scan complete in 1ms
Connecting to jdbc:hive2://ip-10-0-0-163.eu-west-1.compute.internal:10000/default;principal=hive/ip-10-0-0-163.eu-west-1.compute.internal@BENJAMINMAIER.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-0-0-163.eu-west-1.compu> show tables;
INFO  : Compiling command(queryId=hive_20171019092626_354731d0-3370-4ae3-922e-f108c461d1ad): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019092626_354731d0-3370-4ae3-922e-f108c461d1ad); Time taken: 0.063 seconds
INFO  : Executing command(queryId=hive_20171019092626_354731d0-3370-4ae3-922e-f108c461d1ad): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019092626_354731d0-3370-4ae3-922e-f108c461d1ad); Time taken: 0.123 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.28 seconds)
```


### tables for ferdinand

```
[centos@ip-10-0-0-178 ~]$ kinit ferdinand
Password for ferdinand@BENJAMINMAIER.SG:
[centos@ip-10-0-0-178 ~]$ beeline
Beeline version 1.1.0-cdh5.9.3 by Apache Hive
beeline> !connect jdbc:hive2://ip-10-0-0-163.eu-west-1.compute.internal:10000/default;principal=hive/ip-10-0-0-163.eu-west-1.compute.internal@BENJAMINMAIER.SG
scan complete in 2ms
Connecting to jdbc:hive2://ip-10-0-0-163.eu-west-1.compute.internal:10000/default;principal=hive/ip-10-0-0-163.eu-west-1.compute.internal@BENJAMINMAIER.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.3)
Driver: Hive JDBC (version 1.1.0-cdh5.9.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-10-0-0-163.eu-west-1.compu> show tables;
INFO  : Compiling command(queryId=hive_20171019092727_e0bb7306-5c29-4da6-afb4-5f79311b20ea): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019092727_e0bb7306-5c29-4da6-afb4-5f79311b20ea); Time taken: 0.063 seconds
INFO  : Executing command(queryId=hive_20171019092727_e0bb7306-5c29-4da6-afb4-5f79311b20ea): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019092727_e0bb7306-5c29-4da6-afb4-5f79311b20ea); Time taken: 0.141 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.295 seconds)
```