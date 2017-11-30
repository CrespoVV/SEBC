HDFS Lab: Test HDFS throughput

 time hadoop jar hadoop-examples.jar teragen -D dfs.blocksize=33554432 -D mapreduce.job.maps=4 100000000 /user/crispin/terasort-input

 17/11/28 21:43:57 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-49-75.ec2.internal/172.31.49.75:8032
17/11/28 21:43:58 INFO terasort.TeraGen: Generating 100000000 using 4
17/11/28 21:43:58 INFO mapreduce.JobSubmitter: number of splits:4
17/11/28 21:43:58 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1511889688799_0009
17/11/28 21:43:58 INFO impl.YarnClientImpl: Submitted application application_1511889688799_0009
17/11/28 21:43:58 INFO mapreduce.Job: The url to track the job: http://ip-172-31-49-75.ec2.internal:8088/proxy/application_1511889688799_0009/
17/11/28 21:43:58 INFO mapreduce.Job: Running job: job_1511889688799_0009
17/11/28 21:44:05 INFO mapreduce.Job: Job job_1511889688799_0009 running in uber mode : false
17/11/28 21:44:05 INFO mapreduce.Job:  map 0% reduce 0%
17/11/28 21:44:23 INFO mapreduce.Job:  map 8% reduce 0%
17/11/28 21:44:24 INFO mapreduce.Job:  map 15% reduce 0%
17/11/28 21:44:29 INFO mapreduce.Job:  map 19% reduce 0%
17/11/28 21:44:30 INFO mapreduce.Job:  map 22% reduce 0%
17/11/28 21:44:35 INFO mapreduce.Job:  map 25% reduce 0%
17/11/28 21:44:36 INFO mapreduce.Job:  map 28% reduce 0%
17/11/28 21:44:41 INFO mapreduce.Job:  map 30% reduce 0%
17/11/28 21:44:42 INFO mapreduce.Job:  map 32% reduce 0%
17/11/28 21:44:47 INFO mapreduce.Job:  map 35% reduce 0%
17/11/28 21:44:53 INFO mapreduce.Job:  map 37% reduce 0%
17/11/28 21:44:59 INFO mapreduce.Job:  map 40% reduce 0%
17/11/28 21:45:06 INFO mapreduce.Job:  map 43% reduce 0%
17/11/28 21:45:12 INFO mapreduce.Job:  map 46% reduce 0%
17/11/28 21:45:18 INFO mapreduce.Job:  map 51% reduce 0%
17/11/28 21:45:24 INFO mapreduce.Job:  map 54% reduce 0%
17/11/28 21:45:29 INFO mapreduce.Job:  map 55% reduce 0%
17/11/28 21:45:30 INFO mapreduce.Job:  map 58% reduce 0%
17/11/28 21:45:35 INFO mapreduce.Job:  map 60% reduce 0%
17/11/28 21:45:36 INFO mapreduce.Job:  map 62% reduce 0%
17/11/28 21:45:41 INFO mapreduce.Job:  map 64% reduce 0%
17/11/28 21:45:42 INFO mapreduce.Job:  map 66% reduce 0%
17/11/28 21:45:47 INFO mapreduce.Job:  map 67% reduce 0%
17/11/28 21:45:48 INFO mapreduce.Job:  map 69% reduce 0%
17/11/28 21:45:53 INFO mapreduce.Job:  map 74% reduce 0%
17/11/28 21:46:00 INFO mapreduce.Job:  map 79% reduce 0%
17/11/28 21:46:06 INFO mapreduce.Job:  map 83% reduce 0%
17/11/28 21:46:12 INFO mapreduce.Job:  map 87% reduce 0%
17/11/28 21:46:18 INFO mapreduce.Job:  map 88% reduce 0%
17/11/28 21:46:24 INFO mapreduce.Job:  map 91% reduce 0%
17/11/28 21:46:29 INFO mapreduce.Job:  map 92% reduce 0%
17/11/28 21:46:30 INFO mapreduce.Job:  map 95% reduce 0%
17/11/28 21:46:35 INFO mapreduce.Job:  map 96% reduce 0%
17/11/28 21:46:36 INFO mapreduce.Job:  map 98% reduce 0%
17/11/28 21:46:37 INFO mapreduce.Job:  map 100% reduce 0%
17/11/28 21:46:37 INFO mapreduce.Job: Job job_1511889688799_0009 completed successfully
17/11/28 21:46:37 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=581168
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=600744
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=600744
                Total vcore-milliseconds taken by all map tasks=600744
                Total megabyte-milliseconds taken by all map tasks=615161856
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=974
                CPU time spent (ms)=138200
                Physical memory (bytes) snapshot=806350848
                Virtual memory (bytes) snapshot=6412005376
                Total committed heap usage (bytes)=1603796992
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    2m42.319s
user    0m5.519s
sys     0m0.325s

time hadoop jar hadoop-examples.jar terasort /user/crispin-dev/terasort-input /user/crispin-dev/terasort-output

17/11/28 21:50:35 INFO terasort.TeraSort: starting
17/11/28 21:50:36 INFO input.FileInputFormat: Total input paths to process : 4
Spent 214ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 221ms
Sampling 10 splits of 300
Making 12 from 100000 sampled records
Computing parititions took 624ms
Spent 847ms computing partitions.
17/11/28 21:50:37 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-49-75.ec2.internal/172.31.49.75:8032
17/11/28 21:50:37 INFO mapreduce.JobSubmitter: number of splits:300
17/11/28 21:50:38 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1511889688799_0010
17/11/28 21:50:38 INFO impl.YarnClientImpl: Submitted application application_1511889688799_0010
17/11/28 21:50:38 INFO mapreduce.Job: The url to track the job: http://ip-172-31-49-75.ec2.internal:8088/proxy/application_1511889688799_0010/
17/11/28 21:50:38 INFO mapreduce.Job: Running job: job_1511889688799_0010
17/11/28 21:50:44 INFO mapreduce.Job: Job job_1511889688799_0010 running in uber mode : false
17/11/28 21:50:44 INFO mapreduce.Job:  map 0% reduce 0%
17/11/28 21:50:57 INFO mapreduce.Job:  map 1% reduce 0%
17/11/28 21:50:58 INFO mapreduce.Job:  map 3% reduce 0%
17/11/28 21:50:59 INFO mapreduce.Job:  map 6% reduce 0%
17/11/28 21:51:00 INFO mapreduce.Job:  map 7% reduce 0%
17/11/28 21:51:01 INFO mapreduce.Job:  map 8% reduce 0%
17/11/28 21:51:09 INFO mapreduce.Job:  map 9% reduce 0%
17/11/28 21:51:10 INFO mapreduce.Job:  map 10% reduce 0%
17/11/28 21:51:12 INFO mapreduce.Job:  map 11% reduce 0%
17/11/28 21:51:13 INFO mapreduce.Job:  map 14% reduce 0%
17/11/28 21:51:14 INFO mapreduce.Job:  map 15% reduce 0%
17/11/28 21:51:19 INFO mapreduce.Job:  map 16% reduce 0%
17/11/28 21:51:21 INFO mapreduce.Job:  map 17% reduce 0%
17/11/28 21:51:22 INFO mapreduce.Job:  map 18% reduce 0%
17/11/28 21:51:25 INFO mapreduce.Job:  map 19% reduce 0%
17/11/28 21:51:26 INFO mapreduce.Job:  map 21% reduce 0%
17/11/28 21:51:27 INFO mapreduce.Job:  map 23% reduce 0%
17/11/28 21:51:30 INFO mapreduce.Job:  map 24% reduce 0%
17/11/28 21:51:32 INFO mapreduce.Job:  map 25% reduce 0%
17/11/28 21:51:38 INFO mapreduce.Job:  map 27% reduce 0%
17/11/28 21:51:39 INFO mapreduce.Job:  map 28% reduce 0%
17/11/28 21:51:40 INFO mapreduce.Job:  map 30% reduce 0%
17/11/28 21:51:41 INFO mapreduce.Job:  map 31% reduce 0%
17/11/28 21:51:43 INFO mapreduce.Job:  map 32% reduce 0%
17/11/28 21:51:45 INFO mapreduce.Job:  map 33% reduce 0%
17/11/28 21:51:51 INFO mapreduce.Job:  map 35% reduce 0%
17/11/28 21:51:53 INFO mapreduce.Job:  map 36% reduce 0%
17/11/28 21:51:54 INFO mapreduce.Job:  map 37% reduce 0%
17/11/28 21:51:55 INFO mapreduce.Job:  map 39% reduce 0%
17/11/28 21:51:56 INFO mapreduce.Job:  map 41% reduce 0%
17/11/28 21:52:03 INFO mapreduce.Job:  map 42% reduce 0%
17/11/28 21:52:04 INFO mapreduce.Job:  map 43% reduce 0%
17/11/28 21:52:06 INFO mapreduce.Job:  map 45% reduce 0%
17/11/28 21:52:07 INFO mapreduce.Job:  map 46% reduce 0%
17/11/28 21:52:08 INFO mapreduce.Job:  map 47% reduce 0%
17/11/28 21:52:09 INFO mapreduce.Job:  map 48% reduce 0%
17/11/28 21:52:12 INFO mapreduce.Job:  map 49% reduce 0%
17/11/28 21:52:15 INFO mapreduce.Job:  map 50% reduce 0%
17/11/28 21:52:16 INFO mapreduce.Job:  map 51% reduce 0%
17/11/28 21:52:18 INFO mapreduce.Job:  map 52% reduce 0%
17/11/28 21:52:19 INFO mapreduce.Job:  map 54% reduce 0%
17/11/28 21:52:22 INFO mapreduce.Job:  map 56% reduce 0%
17/11/28 21:52:26 INFO mapreduce.Job:  map 57% reduce 0%
17/11/28 21:52:28 INFO mapreduce.Job:  map 59% reduce 0%
17/11/28 21:52:30 INFO mapreduce.Job:  map 60% reduce 0%
17/11/28 21:52:32 INFO mapreduce.Job:  map 61% reduce 0%
17/11/28 21:52:33 INFO mapreduce.Job:  map 62% reduce 0%
17/11/28 21:52:36 INFO mapreduce.Job:  map 64% reduce 0%
17/11/28 21:52:38 INFO mapreduce.Job:  map 65% reduce 0%
17/11/28 21:52:40 INFO mapreduce.Job:  map 66% reduce 0%
17/11/28 21:52:41 INFO mapreduce.Job:  map 67% reduce 0%
17/11/28 21:52:43 INFO mapreduce.Job:  map 68% reduce 0%
17/11/28 21:52:44 INFO mapreduce.Job:  map 69% reduce 0%
17/11/28 21:52:46 INFO mapreduce.Job:  map 70% reduce 0%
17/11/28 21:52:48 INFO mapreduce.Job:  map 71% reduce 0%
17/11/28 21:52:49 INFO mapreduce.Job:  map 72% reduce 0%
17/11/28 21:52:51 INFO mapreduce.Job:  map 73% reduce 0%
17/11/28 21:52:53 INFO mapreduce.Job:  map 75% reduce 0%
17/11/28 21:52:55 INFO mapreduce.Job:  map 76% reduce 0%
17/11/28 21:52:57 INFO mapreduce.Job:  map 77% reduce 0%
17/11/28 21:52:59 INFO mapreduce.Job:  map 78% reduce 0%
17/11/28 21:53:01 INFO mapreduce.Job:  map 79% reduce 0%
17/11/28 21:53:02 INFO mapreduce.Job:  map 80% reduce 0%
17/11/28 21:53:03 INFO mapreduce.Job:  map 81% reduce 0%
17/11/28 21:53:06 INFO mapreduce.Job:  map 83% reduce 0%
17/11/28 21:53:09 INFO mapreduce.Job:  map 84% reduce 0%
17/11/28 21:53:10 INFO mapreduce.Job:  map 85% reduce 0%
17/11/28 21:53:11 INFO mapreduce.Job:  map 86% reduce 0%
17/11/28 21:53:13 INFO mapreduce.Job:  map 87% reduce 0%
17/11/28 21:53:16 INFO mapreduce.Job:  map 88% reduce 0%
17/11/28 21:53:19 INFO mapreduce.Job:  map 89% reduce 0%
17/11/28 21:53:23 INFO mapreduce.Job:  map 89% reduce 2%
17/11/28 21:53:24 INFO mapreduce.Job:  map 90% reduce 2%
17/11/28 21:53:25 INFO mapreduce.Job:  map 90% reduce 5%
17/11/28 21:53:26 INFO mapreduce.Job:  map 91% reduce 13%
17/11/28 21:53:28 INFO mapreduce.Job:  map 91% reduce 15%
17/11/28 21:53:29 INFO mapreduce.Job:  map 92% reduce 18%
17/11/28 21:53:30 INFO mapreduce.Job:  map 92% reduce 23%
17/11/28 21:53:31 INFO mapreduce.Job:  map 93% reduce 28%
17/11/28 21:53:32 INFO mapreduce.Job:  map 94% reduce 28%
17/11/28 21:53:36 INFO mapreduce.Job:  map 94% reduce 29%
17/11/28 21:53:38 INFO mapreduce.Job:  map 95% reduce 29%
17/11/28 21:53:39 INFO mapreduce.Job:  map 96% reduce 29%
17/11/28 21:53:40 INFO mapreduce.Job:  map 97% reduce 29%
17/11/28 21:53:41 INFO mapreduce.Job:  map 98% reduce 29%
17/11/28 21:53:43 INFO mapreduce.Job:  map 98% reduce 30%
17/11/28 21:53:44 INFO mapreduce.Job:  map 99% reduce 30%
17/11/28 21:53:45 INFO mapreduce.Job:  map 100% reduce 30%
17/11/28 21:53:46 INFO mapreduce.Job:  map 100% reduce 31%
17/11/28 21:53:47 INFO mapreduce.Job:  map 100% reduce 34%
17/11/28 21:53:48 INFO mapreduce.Job:  map 100% reduce 37%
17/11/28 21:53:49 INFO mapreduce.Job:  map 100% reduce 48%
17/11/28 21:53:50 INFO mapreduce.Job:  map 100% reduce 57%
17/11/28 21:53:52 INFO mapreduce.Job:  map 100% reduce 60%
17/11/28 21:53:53 INFO mapreduce.Job:  map 100% reduce 65%
17/11/28 21:53:54 INFO mapreduce.Job:  map 100% reduce 67%
17/11/28 21:53:55 INFO mapreduce.Job:  map 100% reduce 71%
17/11/28 21:53:56 INFO mapreduce.Job:  map 100% reduce 76%
17/11/28 21:53:58 INFO mapreduce.Job:  map 100% reduce 84%
17/11/28 21:53:59 INFO mapreduce.Job:  map 100% reduce 86%
17/11/28 21:54:00 INFO mapreduce.Job:  map 100% reduce 87%
17/11/28 21:54:01 INFO mapreduce.Job:  map 100% reduce 90%
17/11/28 21:54:02 INFO mapreduce.Job:  map 100% reduce 93%
17/11/28 21:54:04 INFO mapreduce.Job:  map 100% reduce 95%
17/11/28 21:54:05 INFO mapreduce.Job:  map 100% reduce 99%
17/11/28 21:54:06 INFO mapreduce.Job:  map 100% reduce 100%
17/11/28 21:54:08 INFO mapreduce.Job: Job job_1511889688799_0010 completed successfully
17/11/28 21:54:09 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=4441031776
                FILE: Number of bytes written=8829886591
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000045000
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=936
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=24
        Job Counters
                Launched map tasks=300
                Launched reduce tasks=12
                Data-local map tasks=300
                Total time spent by all maps in occupied slots (ms)=3279506
                Total time spent by all reduces in occupied slots (ms)=612461
                Total time spent by all map tasks (ms)=3279506
                Total time spent by all reduce tasks (ms)=612461
                Total vcore-milliseconds taken by all map tasks=3279506
                Total vcore-milliseconds taken by all reduce tasks=612461
                Total megabyte-milliseconds taken by all map tasks=3358214144
                Total megabyte-milliseconds taken by all reduce tasks=627160064
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4342967363
                Input split bytes=45000
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4342967363
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =3600
                Failed Shuffles=0
                Merged Map outputs=3600
                GC time elapsed (ms)=47304
                CPU time spent (ms)=1630130
                Physical memory (bytes) snapshot=165741957120
                Virtual memory (bytes) snapshot=499940999168
                Total committed heap usage (bytes)=169209757696
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
17/11/28 21:54:09 INFO terasort.TeraSort: done

real    3m34.698s
user    0m8.518s
sys     0m0.386s
