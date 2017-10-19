### TASK 2: Inspect the derived/default values. Adjust as necessary

Worker vcores	20 <br />
Worker spindles	12 <br />
Worker RAM	128 <br />
Workload factor	1 <br />
Worker nodes	10 <br />

Adjusted parameters:
<ul>
<li>OS	Meomory of 8GB because most operating systems use 4-8GB minimum. </li>
<li>OS vcores of 1 is enough for the operating systems </li>
<li>yarn.scheduler.maximum-allocation-vcores=1 because Cloudera recommends on their tuning guide sheet in Step6 </li>
<li>yarn.scheduler.maximum-allocation-mb=4096 MB because Cloudera recommends for 8192 MB however those cluster RAM is twice higher than our cluster (242688 MB vs. 119808 MB).
Therefore yarn.scheduler.maximum-allocation-mb have to be minimized to the half. </li>
<li>yarn.scheduler.increment-allocation-mb =512 MB because Cloudera recommends on their tuning guide sheet in Step6 </li>
<li>yarn.app.mapreduce.am.resource.mb=1024 MB because Cloudera recommends on their tuning guide sheet in Step7. 1 MB is to low RAM for the application master </li>

<li>mapreduce.map.java.opts.max.heap=1024 due to have a close value to mapreduce.map.memory.mb to prevent wasting of memory </li>
<li>mapreduce.reduce.java.opts.max.heap=1024 due to have a close value to mapreduce.reduce.memory.mb to prevent wasting of memory </li>
<li>yarn.app.mapreduce.am.resource.command-opts=1024 due to have a close value to yarn.app.mapreduce.am.resource.mb to prevent wasting of memory </li>

<li>-D mapreduce.map.memory.mb=1024 set it to the same value as in the Task Container Settings </li>
<li>-D mapreduce.reduce.memory.mb=1024 set it to the same value as in the Task Container Settings </li>
<li>-D mapreduce.map.java.opts.max.heap=1024 set it to the same value as in the Task Container Settings </li>
<li>-D mapreduce.reduce.java.opts.max.heap=1024 set it to the same value as in the Task Container Settings </li>
</ul>
 
 
### TASK 3: What criteria affects workload factor? What does a value of 1, 2, or 4 signify?


Expected number of concurrent threads per core.  Use 1 stands for CPU intensive tasks and 4 stands for standard I/O bound tasks. Value 2 stands for more CPU tasks but also I/O bound tasks are appearing in this cluster.



