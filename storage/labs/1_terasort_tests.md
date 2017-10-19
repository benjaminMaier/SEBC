### Add user on Linux

```
[centos@ip-10-0-0-207 ~]$ sudo useradd benjaminMaier
[centos@ip-10-0-0-207 ~]$ sudo passwd benjaminMaier
```

### create user directory

```
[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -mkdir /user/benjaminMaier
[centos@ip-10-0-0-207 ~]$ sudo -u hdfs hdfs dfs -chown benjaminMaier:benjaminMaier /user/benjaminMaier
```

### run teragen with 4 mappers and 32MB blocksize

```
[benjaminMaier@ip-10-0-0-207 centos]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.blocksize=33554432  107374182 /user/benjaminMaier/teragen_output
17/10/17 11:49:31 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-16.eu-west-1.compute.internal/10.0.0.16:8032
17/10/17 11:49:31 INFO terasort.TeraSort: Generating 107374182 using 4
17/10/17 11:49:31 INFO mapreduce.JobSubmitter: number of splits:4
17/10/17 11:49:31 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/10/17 11:49:32 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508231975125_0004
17/10/17 11:49:32 INFO impl.YarnClientImpl: Submitted application application_1508231975125_0004
17/10/17 11:49:32 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-16.eu-west-1.compute.internal:8088/proxy/application_1508231975125_0004/
17/10/17 11:49:32 INFO mapreduce.Job: Running job: job_1508231975125_0004
17/10/17 11:49:37 INFO mapreduce.Job: Job job_1508231975125_0004 running in uber mode : false
17/10/17 11:49:37 INFO mapreduce.Job:  map 0% reduce 0%
17/10/17 11:49:48 INFO mapreduce.Job:  map 13% reduce 0%
17/10/17 11:49:51 INFO mapreduce.Job:  map 17% reduce 0%
17/10/17 11:49:54 INFO mapreduce.Job:  map 22% reduce 0%
17/10/17 11:49:57 INFO mapreduce.Job:  map 25% reduce 0%
17/10/17 11:50:00 INFO mapreduce.Job:  map 32% reduce 0%
17/10/17 11:50:04 INFO mapreduce.Job:  map 35% reduce 0%
17/10/17 11:50:07 INFO mapreduce.Job:  map 40% reduce 0%
17/10/17 11:50:10 INFO mapreduce.Job:  map 44% reduce 0%
17/10/17 11:50:13 INFO mapreduce.Job:  map 47% reduce 0%
17/10/17 11:50:16 INFO mapreduce.Job:  map 52% reduce 0%
17/10/17 11:50:19 INFO mapreduce.Job:  map 57% reduce 0%
17/10/17 11:50:22 INFO mapreduce.Job:  map 58% reduce 0%
17/10/17 11:50:25 INFO mapreduce.Job:  map 61% reduce 0%
17/10/17 11:50:28 INFO mapreduce.Job:  map 66% reduce 0%
17/10/17 11:50:31 INFO mapreduce.Job:  map 71% reduce 0%
17/10/17 11:50:34 INFO mapreduce.Job:  map 76% reduce 0%
17/10/17 11:50:37 INFO mapreduce.Job:  map 78% reduce 0%
17/10/17 11:50:40 INFO mapreduce.Job:  map 84% reduce 0%
17/10/17 11:50:43 INFO mapreduce.Job:  map 88% reduce 0%
17/10/17 11:50:46 INFO mapreduce.Job:  map 91% reduce 0%
17/10/17 11:50:49 INFO mapreduce.Job:  map 95% reduce 0%
17/10/17 11:50:52 INFO mapreduce.Job:  map 98% reduce 0%
17/10/17 11:50:55 INFO mapreduce.Job:  map 100% reduce 0%
17/10/17 11:50:55 INFO mapreduce.Job: Job job_1508231975125_0004 completed successfully
17/10/17 11:50:55 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=492762
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10737418200
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=292788
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=292788
                Total vcore-seconds taken by all map tasks=292788
                Total megabyte-seconds taken by all map tasks=299814912
        Map-Reduce Framework
                Map input records=107374182
                Map output records=107374182
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1439
                CPU time spent (ms)=175630
                Physical memory (bytes) snapshot=824770560
                Virtual memory (bytes) snapshot=6301696000
                Total committed heap usage (bytes)=982515712
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=230593859918397906
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10737418200

real    1m26.590s
user    0m5.648s
sys     0m0.246s
```

### terasort 

```
[benjaminMaier@ip-10-0-0-207 centos]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/benjaminMaier/teragen_output /user/benjaminMaier/terasort_output
17/10/17 11:52:38 INFO terasort.TeraSort: starting
17/10/17 11:52:40 INFO input.FileInputFormat: Total input paths to process : 4
Spent 244ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 251ms
Sampling 10 splits of 320
Making 8 from 100000 sampled records
Computing parititions took 811ms
Spent 1064ms computing partitions.
17/10/17 11:52:41 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-16.eu-west-1.compute.internal/10.0.0.16:8032
17/10/17 11:52:41 INFO mapreduce.JobSubmitter: number of splits:320
17/10/17 11:52:41 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508231975125_0005
17/10/17 11:52:42 INFO impl.YarnClientImpl: Submitted application application_1508231975125_0005
17/10/17 11:52:42 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-16.eu-west-1.compute.internal:8088/proxy/application_1508231975125_0005/
17/10/17 11:52:42 INFO mapreduce.Job: Running job: job_1508231975125_0005
17/10/17 11:52:48 INFO mapreduce.Job: Job job_1508231975125_0005 running in uber mode : false
17/10/17 11:52:48 INFO mapreduce.Job:  map 0% reduce 0%
17/10/17 11:52:58 INFO mapreduce.Job:  map 2% reduce 0%
17/10/17 11:52:59 INFO mapreduce.Job:  map 3% reduce 0%
17/10/17 11:53:01 INFO mapreduce.Job:  map 4% reduce 0%
17/10/17 11:53:08 INFO mapreduce.Job:  map 5% reduce 0%
17/10/17 11:53:09 INFO mapreduce.Job:  map 6% reduce 0%
17/10/17 11:53:10 INFO mapreduce.Job:  map 7% reduce 0%
17/10/17 11:53:14 INFO mapreduce.Job:  map 8% reduce 0%
17/10/17 11:53:18 INFO mapreduce.Job:  map 10% reduce 0%
17/10/17 11:53:19 INFO mapreduce.Job:  map 11% reduce 0%
17/10/17 11:53:27 INFO mapreduce.Job:  map 13% reduce 0%
17/10/17 11:53:29 INFO mapreduce.Job:  map 15% reduce 0%
17/10/17 11:53:37 INFO mapreduce.Job:  map 16% reduce 0%
17/10/17 11:53:39 INFO mapreduce.Job:  map 18% reduce 0%
17/10/17 11:53:41 INFO mapreduce.Job:  map 19% reduce 0%
17/10/17 11:53:46 INFO mapreduce.Job:  map 20% reduce 0%
17/10/17 11:53:48 INFO mapreduce.Job:  map 21% reduce 0%
17/10/17 11:53:49 INFO mapreduce.Job:  map 22% reduce 0%
17/10/17 11:53:52 INFO mapreduce.Job:  map 23% reduce 0%
17/10/17 11:53:56 INFO mapreduce.Job:  map 24% reduce 0%
17/10/17 11:53:57 INFO mapreduce.Job:  map 25% reduce 0%
17/10/17 11:53:59 INFO mapreduce.Job:  map 26% reduce 0%
17/10/17 11:54:04 INFO mapreduce.Job:  map 27% reduce 0%
17/10/17 11:54:05 INFO mapreduce.Job:  map 28% reduce 0%
17/10/17 11:54:06 INFO mapreduce.Job:  map 29% reduce 0%
17/10/17 11:54:07 INFO mapreduce.Job:  map 30% reduce 0%
17/10/17 11:54:14 INFO mapreduce.Job:  map 31% reduce 0%
17/10/17 11:54:15 INFO mapreduce.Job:  map 32% reduce 0%
17/10/17 11:54:16 INFO mapreduce.Job:  map 33% reduce 0%
17/10/17 11:54:17 INFO mapreduce.Job:  map 34% reduce 0%
17/10/17 11:54:24 INFO mapreduce.Job:  map 35% reduce 0%
17/10/17 11:54:25 INFO mapreduce.Job:  map 36% reduce 0%
17/10/17 11:54:26 INFO mapreduce.Job:  map 37% reduce 0%
17/10/17 11:54:28 INFO mapreduce.Job:  map 38% reduce 0%
17/10/17 11:54:33 INFO mapreduce.Job:  map 39% reduce 0%
17/10/17 11:54:34 INFO mapreduce.Job:  map 40% reduce 0%
17/10/17 11:54:35 INFO mapreduce.Job:  map 41% reduce 0%
17/10/17 11:54:37 INFO mapreduce.Job:  map 42% reduce 0%
17/10/17 11:54:41 INFO mapreduce.Job:  map 43% reduce 0%
17/10/17 11:54:43 INFO mapreduce.Job:  map 44% reduce 0%
17/10/17 11:54:45 INFO mapreduce.Job:  map 45% reduce 0%
17/10/17 11:54:50 INFO mapreduce.Job:  map 46% reduce 0%
17/10/17 11:54:52 INFO mapreduce.Job:  map 47% reduce 0%
17/10/17 11:54:53 INFO mapreduce.Job:  map 48% reduce 0%
17/10/17 11:54:54 INFO mapreduce.Job:  map 49% reduce 0%
17/10/17 11:55:00 INFO mapreduce.Job:  map 50% reduce 0%
17/10/17 11:55:01 INFO mapreduce.Job:  map 51% reduce 0%
17/10/17 11:55:02 INFO mapreduce.Job:  map 52% reduce 0%
17/10/17 11:55:04 INFO mapreduce.Job:  map 53% reduce 0%
17/10/17 11:55:10 INFO mapreduce.Job:  map 55% reduce 0%
17/10/17 11:55:11 INFO mapreduce.Job:  map 56% reduce 0%
17/10/17 11:55:13 INFO mapreduce.Job:  map 57% reduce 0%
17/10/17 11:55:20 INFO mapreduce.Job:  map 58% reduce 0%
17/10/17 11:55:21 INFO mapreduce.Job:  map 60% reduce 0%
17/10/17 11:55:23 INFO mapreduce.Job:  map 61% reduce 0%
17/10/17 11:55:28 INFO mapreduce.Job:  map 62% reduce 0%
17/10/17 11:55:30 INFO mapreduce.Job:  map 63% reduce 0%
17/10/17 11:55:31 INFO mapreduce.Job:  map 64% reduce 0%
17/10/17 11:55:35 INFO mapreduce.Job:  map 65% reduce 0%
17/10/17 11:55:38 INFO mapreduce.Job:  map 66% reduce 0%
17/10/17 11:55:39 INFO mapreduce.Job:  map 67% reduce 0%
17/10/17 11:55:41 INFO mapreduce.Job:  map 68% reduce 0%
17/10/17 11:55:46 INFO mapreduce.Job:  map 69% reduce 0%
17/10/17 11:55:48 INFO mapreduce.Job:  map 70% reduce 0%
17/10/17 11:55:50 INFO mapreduce.Job:  map 71% reduce 0%
17/10/17 11:55:51 INFO mapreduce.Job:  map 72% reduce 0%
17/10/17 11:55:53 INFO mapreduce.Job:  map 73% reduce 0%
17/10/17 11:55:58 INFO mapreduce.Job:  map 74% reduce 0%
17/10/17 11:55:59 INFO mapreduce.Job:  map 75% reduce 0%
17/10/17 11:56:00 INFO mapreduce.Job:  map 76% reduce 0%
17/10/17 11:56:02 INFO mapreduce.Job:  map 77% reduce 0%
17/10/17 11:56:08 INFO mapreduce.Job:  map 78% reduce 0%
17/10/17 11:56:09 INFO mapreduce.Job:  map 79% reduce 0%
17/10/17 11:56:11 INFO mapreduce.Job:  map 80% reduce 0%
17/10/17 11:56:14 INFO mapreduce.Job:  map 81% reduce 0%
17/10/17 11:56:17 INFO mapreduce.Job:  map 82% reduce 0%
17/10/17 11:56:18 INFO mapreduce.Job:  map 83% reduce 0%
17/10/17 11:56:20 INFO mapreduce.Job:  map 84% reduce 0%
17/10/17 11:56:24 INFO mapreduce.Job:  map 84% reduce 2%
17/10/17 11:56:26 INFO mapreduce.Job:  map 84% reduce 3%
17/10/17 11:56:27 INFO mapreduce.Job:  map 84% reduce 4%
17/10/17 11:56:28 INFO mapreduce.Job:  map 85% reduce 6%
17/10/17 11:56:29 INFO mapreduce.Job:  map 85% reduce 9%
17/10/17 11:56:30 INFO mapreduce.Job:  map 85% reduce 12%
17/10/17 11:56:31 INFO mapreduce.Job:  map 85% reduce 13%
17/10/17 11:56:33 INFO mapreduce.Job:  map 86% reduce 13%
17/10/17 11:56:34 INFO mapreduce.Job:  map 86% reduce 16%
17/10/17 11:56:35 INFO mapreduce.Job:  map 86% reduce 18%
17/10/17 11:56:36 INFO mapreduce.Job:  map 86% reduce 20%
17/10/17 11:56:38 INFO mapreduce.Job:  map 87% reduce 20%
17/10/17 11:56:40 INFO mapreduce.Job:  map 87% reduce 23%
17/10/17 11:56:41 INFO mapreduce.Job:  map 87% reduce 24%
17/10/17 11:56:42 INFO mapreduce.Job:  map 87% reduce 25%
17/10/17 11:56:44 INFO mapreduce.Job:  map 88% reduce 25%
17/10/17 11:56:46 INFO mapreduce.Job:  map 89% reduce 26%
17/10/17 11:56:52 INFO mapreduce.Job:  map 90% reduce 26%
17/10/17 11:56:53 INFO mapreduce.Job:  map 91% reduce 26%
17/10/17 11:56:58 INFO mapreduce.Job:  map 91% reduce 27%
17/10/17 11:56:59 INFO mapreduce.Job:  map 92% reduce 27%
17/10/17 11:57:00 INFO mapreduce.Job:  map 93% reduce 27%
17/10/17 11:57:06 INFO mapreduce.Job:  map 94% reduce 27%
17/10/17 11:57:10 INFO mapreduce.Job:  map 95% reduce 27%
17/10/17 11:57:11 INFO mapreduce.Job:  map 95% reduce 28%
17/10/17 11:57:14 INFO mapreduce.Job:  map 96% reduce 28%
17/10/17 11:57:17 INFO mapreduce.Job:  map 97% reduce 28%
17/10/17 11:57:21 INFO mapreduce.Job:  map 98% reduce 28%
17/10/17 11:57:24 INFO mapreduce.Job:  map 98% reduce 29%
17/10/17 11:57:27 INFO mapreduce.Job:  map 99% reduce 29%
17/10/17 11:57:29 INFO mapreduce.Job:  map 100% reduce 29%
17/10/17 11:57:31 INFO mapreduce.Job:  map 100% reduce 32%
17/10/17 11:57:32 INFO mapreduce.Job:  map 100% reduce 37%
17/10/17 11:57:33 INFO mapreduce.Job:  map 100% reduce 39%
17/10/17 11:57:34 INFO mapreduce.Job:  map 100% reduce 54%
17/10/17 11:57:35 INFO mapreduce.Job:  map 100% reduce 59%
17/10/17 11:57:36 INFO mapreduce.Job:  map 100% reduce 60%
17/10/17 11:57:37 INFO mapreduce.Job:  map 100% reduce 63%
17/10/17 11:57:38 INFO mapreduce.Job:  map 100% reduce 65%
17/10/17 11:57:40 INFO mapreduce.Job:  map 100% reduce 69%
17/10/17 11:57:41 INFO mapreduce.Job:  map 100% reduce 70%
17/10/17 11:57:42 INFO mapreduce.Job:  map 100% reduce 71%
17/10/17 11:57:43 INFO mapreduce.Job:  map 100% reduce 75%
17/10/17 11:57:44 INFO mapreduce.Job:  map 100% reduce 76%
17/10/17 11:57:45 INFO mapreduce.Job:  map 100% reduce 77%
17/10/17 11:57:46 INFO mapreduce.Job:  map 100% reduce 83%
17/10/17 11:57:47 INFO mapreduce.Job:  map 100% reduce 84%
17/10/17 11:57:48 INFO mapreduce.Job:  map 100% reduce 85%
17/10/17 11:57:49 INFO mapreduce.Job:  map 100% reduce 87%
17/10/17 11:57:50 INFO mapreduce.Job:  map 100% reduce 89%
17/10/17 11:57:52 INFO mapreduce.Job:  map 100% reduce 92%
17/10/17 11:57:53 INFO mapreduce.Job:  map 100% reduce 93%
17/10/17 11:57:55 INFO mapreduce.Job:  map 100% reduce 94%
17/10/17 11:57:56 INFO mapreduce.Job:  map 100% reduce 95%
17/10/17 11:57:58 INFO mapreduce.Job:  map 100% reduce 97%
17/10/17 11:57:59 INFO mapreduce.Job:  map 100% reduce 98%
17/10/17 11:58:00 INFO mapreduce.Job:  map 100% reduce 99%
17/10/17 11:58:02 INFO mapreduce.Job:  map 100% reduce 100%
17/10/17 11:58:02 INFO mapreduce.Job: Job job_1508231975125_0005 completed successfully
17/10/17 11:58:02 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4773863905
                FILE: Number of bytes written=9477639658
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10737470360
                HDFS: Number of bytes written=10737418200
                HDFS: Number of read operations=984
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=320
                Launched reduce tasks=8
                Data-local map tasks=320
                Total time spent by all maps in occupied slots (ms)=2750915
                Total time spent by all reduces in occupied slots (ms)=724840
                Total time spent by all map tasks (ms)=2750915
                Total time spent by all reduce tasks (ms)=724840
                Total vcore-seconds taken by all map tasks=2750915
                Total vcore-seconds taken by all reduce tasks=724840
                Total megabyte-seconds taken by all map tasks=2816936960
                Total megabyte-seconds taken by all reduce tasks=742236160
        Map-Reduce Framework
                Map input records=107374182
                Map output records=107374182
                Map output bytes=10952166564
                Map output materialized bytes=4662863455
                Input split bytes=52160
                Combine input records=0
                Combine output records=0
                Reduce input groups=107374182
                Reduce shuffle bytes=4662863455
                Reduce input records=107374182
                Reduce output records=107374182
                Spilled Records=214748364
                Shuffled Maps =2560
                Failed Shuffles=0
                Merged Map outputs=2560
                GC time elapsed (ms)=40083
                CPU time spent (ms)=1548090
                Physical memory (bytes) snapshot=162528534528
                Virtual memory (bytes) snapshot=517015363584
                Total committed heap usage (bytes)=184464441344
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10737418200
        File Output Format Counters
                Bytes Written=10737418200
17/10/17 11:58:02 INFO terasort.TeraSort: done

real    5m25.008s
user    0m9.207s
sys     0m0.352s
```



