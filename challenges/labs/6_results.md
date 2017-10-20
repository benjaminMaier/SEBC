```
1: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> show tables;
INFO  : Compiling command(queryId=hive_20171020102626_f9dc7893-8709-4492-ab71-1d3c4f89f791): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171020102626_f9dc7893-8709-4492-ab71-1d3c4f89f791); Time taken: 0.056 seconds
INFO  : Executing command(queryId=hive_20171020102626_f9dc7893-8709-4492-ab71-1d3c4f89f791): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171020102626_f9dc7893-8709-4492-ab71-1d3c4f89f791); Time taken: 0.116 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.196 seconds)
```


```
0: jdbc:hive2://ip-10-0-0-166.eu-west-1.compu> show tables;
INFO  : Compiling command(queryId=hive_20171020102929_6b92dbb9-1383-4bbe-a862-74dfa9648b5b): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171020102929_6b92dbb9-1383-4bbe-a862-74dfa9648b5b); Time taken: 0.048 seconds
INFO  : Executing command(queryId=hive_20171020102929_6b92dbb9-1383-4bbe-a862-74dfa9648b5b): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171020102929_6b92dbb9-1383-4bbe-a862-74dfa9648b5b); Time taken: 0.128 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
| sample_08  |
+------------+--+
2 rows selected (0.266 seconds)
```