### pi as siwicki

```
[siwicki@ip-10-0-0-188 java]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 10 10
Number of Maps  = 10
Samples per Map = 10
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
17/10/20 10:09:27 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-166.eu-west-1.compute.internal/10.0.0.166:8032
17/10/20 10:09:27 INFO hdfs.DFSClient: Created token for siwicki: HDFS_DELEGATION_TOKEN owner=siwicki@BENJAMINMAIER.CO.UK, renewer=yarn, realUser=, issueDate=1508494167950, maxDate=1509098967950, sequenceNumber=10, masterKeyId=2 on 10.0.0.166:8020
17/10/20 10:09:27 INFO security.TokenCache: Got dt for hdfs://ip-10-0-0-166.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.166:8020, Ident: (token for siwicki: HDFS_DELEGATION_TOKEN owner=siwicki@BENJAMINMAIER.CO.UK, renewer=yarn, realUser=, issueDate=1508494167950, maxDate=1509098967950, sequenceNumber=10, masterKeyId=2)
17/10/20 10:09:28 INFO input.FileInputFormat: Total input paths to process : 10
17/10/20 10:09:28 INFO mapreduce.JobSubmitter: number of splits:10
17/10/20 10:09:28 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508492657672_0010
17/10/20 10:09:28 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.166:8020, Ident: (token for siwicki: HDFS_DELEGATION_TOKEN owner=siwicki@BENJAMINMAIER.CO.UK, renewer=yarn, realUser=, issueDate=1508494167950, maxDate=1509098967950, sequenceNumber=10, masterKeyId=2)
17/10/20 10:09:28 INFO impl.YarnClientImpl: Submitted application application_1508492657672_0010
17/10/20 10:09:28 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-166.eu-west-1.compute.internal:8088/proxy/application_1508492657672_0010/
17/10/20 10:09:28 INFO mapreduce.Job: Running job: job_1508492657672_0010
17/10/20 10:09:35 INFO mapreduce.Job: Job job_1508492657672_0010 running in uber mode : false
17/10/20 10:09:35 INFO mapreduce.Job:  map 0% reduce 0%
17/10/20 10:09:42 INFO mapreduce.Job:  map 20% reduce 0%
17/10/20 10:09:45 INFO mapreduce.Job:  map 40% reduce 0%
17/10/20 10:09:47 INFO mapreduce.Job:  map 90% reduce 0%
17/10/20 10:09:48 INFO mapreduce.Job:  map 100% reduce 0%
17/10/20 10:09:52 INFO mapreduce.Job:  map 100% reduce 100%
17/10/20 10:09:53 INFO mapreduce.Job: Job job_1508492657672_0010 completed successfully
17/10/20 10:09:53 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=83
                FILE: Number of bytes written=1376987
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=2980
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=10
                Total time spent by all maps in occupied slots (ms)=77114
                Total time spent by all reduces in occupied slots (ms)=2688
                Total time spent by all map tasks (ms)=77114
                Total time spent by all reduce tasks (ms)=2688
                Total vcore-seconds taken by all map tasks=77114
                Total vcore-seconds taken by all reduce tasks=2688
                Total megabyte-seconds taken by all map tasks=78964736
                Total megabyte-seconds taken by all reduce tasks=2752512
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=339
                Input split bytes=1800
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=339
                Reduce input records=20
                Reduce output records=0
                Spilled Records=40
                Shuffled Maps =10
                Failed Shuffles=0
                Merged Map outputs=10
                GC time elapsed (ms)=1074
                CPU time spent (ms)=6970
                Physical memory (bytes) snapshot=4778721280
                Virtual memory (bytes) snapshot=30708494336
                Total committed heap usage (bytes)=4798283776
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1180
        File Output Format Counters
                Bytes Written=97
Job Finished in 25.758 seconds
Estimated value of Pi is 3.20000000000000000000
```
