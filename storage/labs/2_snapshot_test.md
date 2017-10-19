### Test HDFS Snapshots

### create precious directory and put zip file in 

```
[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -mkdir /precious
[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -chmod 777 /precious
[centos@ip-10-0-0-207 ~]$ hdfs dfs -put SEBC-master.zip /precious
[centos@ip-10-0-0-207 ~]$ hdfs dfs -ls /precious
Found 1 items
-rw-r--r--   3 centos supergroup     450893 2017-10-17 12:03 /precious/SEBC-master.zip
```
### Take a snapshot 

```
[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfsadmin -allowSnapshot /precious
Allowing snaphot on /precious succeeded

[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs lsSnapshottableDir
drwxrwxrwx 0 hdfs supergroup 0 2017-10-17 12:03 0 65536 /precious

[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -createSnapshot /precious sebc-hdfs-test
Created snapshot /precious/.snapshot/sebc-hdfs-test

[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -ls /precious/.snapshot
Found 1 items
drwxrwxrwx   - hdfs supergroup          0 2017-10-17 12:10 /precious/.snapshot/sebc-hdfs-test
```

### delete directory and zip file

```
[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -rm -R /precious
rm: Failed to move to trash: hdfs://ip-10-0-0-16.eu-west-1.compute.internal:8020/precious: The directory /precious cannot be deleted since /precious is snapshottable and already has snapshots
[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -rm  /precious/SEBC-master.zip
17/10/17 12:14:04 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-10-0-0-16.eu-west-1.compute.internal:8020/precious/SEBC-master.zip' to trash at: hdfs://ip-10-0-0-16.eu-west-1.compute.internal:8020/user/hdfs/.Trash/Current/precious/SEBC-master.zip
[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -ls  /precious/
[centos@ip-10-0-0-207 ~]$
```

### restore delete file

```
centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -ls /precious/.snapshot/sebc-hdfs-test
Found 1 items
-rw-r--r--   3 centos supergroup     450893 2017-10-17 12:03 /precious/.snapshot/sebc-hdfs-test/SEBC-master.zip

[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -cp /precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /precious/

[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -ls  /precious/
Found 1 items
-rw-r--r--   3 hdfs supergroup     450893 2017-10-17 12:15 /precious/SEBC-master.zip
```
