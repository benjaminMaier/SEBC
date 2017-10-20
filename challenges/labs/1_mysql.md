### hostname of mysql

```
[centos@ip-10-0-0-85 ~]$ hostname -f
ip-10-0-0-85.eu-west-1.compute.internal
```

### mysql version 

```
[centos@ip-10-0-0-85 ~]$ mysql --version
mysql  Ver 14.14 Distrib 5.5.58, for Linux (x86_64) using readline 5.1
``` 

### mysql databases 

```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
| test               |
+--------------------+
10 rows in set (0.00 sec)
```