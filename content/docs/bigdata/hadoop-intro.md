# Understanding Hadoop 

Hadoop - is a set of technologies.. used to store and process huge amounts of data..

Hadoop is not a database.. its an alternative file system with a processing library..

Libraries:
MapReduce 1&2, Hive, Pig

RDBMS Limits:
- Scalability
- Speed
- Queryability, sophisticated processing

Database Choices:
- File systems
	-HDFS (Hadoop distributed file system)

- Databases
	-NoSQL(key/value, columnstore, doc db(mongo db), etc)
	- RDBMS (MySql, Sql Server, Oracle)
		

* When implementing Hadoop then Hadoop is an addition to your RDBMS..

Hadoop & HBase:

 - Hadoop uses alternative file system(HDFS)
 - HBase is a NoSQL database (wide columnstore)
	- wide columnstore = customerid having name. value attributes for customer related info.	

CAP Theory:
 - Consistency
	- Transactions
 - Availability
	- Up-time
 - Partioning
	- Scalability 
 
* Hadoop fits in Scalability
	- commodity(old/bad) hardware for data storage
	
* Flexibility (availability)
	- Commodity hardware for distributed processing
	
What kind of data for Hadoop?

- LOB(line of business)
		- usually transactional and not a good fit..
- Behavioral data
		
		
* Hadoop is a suplement to the existing relational database.. its not a replacement for RDBMS ..


What is Hadoop?
	- 2 Components plus projects
		- Open source data storage: HDFS
		- Processing API: MapReduce
		- Other projects/libraries: HBase, Hive, Pig etc.
		
Hadoop Distributions
	- Apache Hadoop (Open Source)
	- Cloudera, MapR, Hortonworks(Commercial)
	- AWS, Windows Azure HDInsight (Cloud)
		- here aws uses open source hadoop
	
Why use Hadoop?
 - Cheaper (scales to petabytes or more)
 - Faster (parallel data processing)
 - Better (suited for particular types of 'Big data')

Hadoop Business Problems: (Use-cases)
 - Risk modeling
 - Customer churn analysis
 - Recommendation engine
 - Ad targeting
 - Transactional analysis
 - Threat analysis
 - Search quality

Hadoop users: FB, Yahoo, Amazon, eBay, American airlines, NYT, IBM


Hadoop Vs HBase: (Core & Core)
 - file system has larger files..
 - each information will be in 3 times
 - HDFS by default is 64MB or 128MB (these r called chunks)
 - MapReduce is developed in Java.

 
HBase (Wide column):
ID		Data
1		Name="Tamilan", Location="Chennai" 
2		Name="Maran", Car="Honda"
3		Location="Blore", Car="Toyota", Color="CherryRed"

HBase/Hive are not part of Hadoop core.. 


Hadoop Developer
Hadoop Administrator
Hadoop Architect

Understanding JVM:
 - Hadoop processes run in separate JVMs
 - JVMs dont share state
 - JVM processes differ between Hadoop 1.0 and 2.0
 
Hadoop File Systems
 - HDFS (Hadoop distributed file system)
 - 2 modes of implementation
	- Distributed(3 copies) or pseudo-distributed(for testing - will be implemented in single node on single machine)
 - Regular file system 
 - Regular file system (Hadoop can be run in rfs)
	- Standalone mode
	 
Files and JVMS
 - Single node (for all hadoop processes)
	- Local file system
	- Single JVM
	
 - Pseudo-distributed
	- Uses HDFS
	- JVM daemons run processes
	




Core Libraries:
- Map Reduce v2 / YARN - Yet Another Resource Negociator
- HBase for wide column store
- Hive to query HBase
- Pig scripting for ETL
- Mahout library - for machine learning and predictive analytics
- Oozie - for workflow or coordination of jobs.
- Zookeeper - for coordination of groups of jobs
- Sqoop - for data exchange in between other systems (RDBMS like Sql server)
- Flume - is a log collector - coz hadoop jobs produce a large amount of log info abt job process
- Ambari - provisioning, managing and maintaining hadoop clusters


Commercial Distribution - Cloudera Hadoop:



Different versions of Cloudera: 
 - Cloudera Enterprice
 - Cloudera Express
 - Cloudera Live (Live demo: http://demo.gethue.com/home )

Another verdor: hortonworks.com
	- have distributions for unix & windows

Another one: mapr.com

---------------------

Cloudera Demo:
	- Hue is the interface for hadoop cluster in cloudera..
	- Under query editor..
		- Job Designer = MapReduce
		- 
----------------------

Cloud hosted Hadoop:
- Hadoop with AWS (Amazon EMR - Elastic mapreduce) (setup and configurations are different)
- Hadoop with Azure  (New > Data services > HDInight > Hadoop

* Setting up hadoop is quite complecated..

Setting up Hadoop:
- Hadoop binaries(apache hadoop) or vendor distribution
- Hadoop version
- Location (preferably the hadoop cluster on cloud)
	- Local install (free but takes a long time)
	- Local VM (must install virtualization software)
	- Cloud (costs money to test!)

Setting Up Hadoop Data Storage
- Local
	- File system (single distribution)
	- HDFS (pseudo or distributed)
- Cloud
	- Cloud files (S3, BLOG)
	- HDFS

Setting Up Hadoop Libraries
- MapReduce
	- version 1.0 or 2.0
- Other libraries
- Developer Tools

Cloudera Hadoop Virtual Machine
- OS + virtualization software
- Hadoop virtual machine for that type of VM
- Cloudera tools and samples
- Cloudera Hadoop VM is an enterprice edition for development. if we need to deploy then we need to pay the fee.
- Install developer tools

Note: CDH5 and Cloudera Manager 5 - To enable Cloudera Manager we need 8GB ram and 2 virtual CPU cores


Hadoop Local install:
 - Download from apache.hadoop.com
 - extract and run the downloads..
 - cd conf/
 - vi core-site.xml
 - vi hdfs-site.xml
 - vi mapred-site.xml
 - vi hadoop-env.sh
 - cat masters
 - cat slaves
 - bin/hadoop namenode -format
 - bin/start-all.sh
 - jps
	

Hadoop architectural components:
	- HDFS
	- MapReduce

Demons: 
-NameNode		- Storage 
- DataNode, 		- Storage
- SecondaryNameNode, 	- Storage
- Jps
- JobTracker, 		- Processing
- TaskTracker, 		- Processing
			



- JobTracker, TaskTracker are responsible for running MapReduce tasks and jobs.

- MapReduce programs are written in Java.
- Hadoop allows to use other languages via streaming..

- Hadoop sends the mapreduce jobs across the data nodes and the data analysis is done across the data nodes and the final results returned back to master node. 

- Namenode communicates with Datanodes
- JobTracker communicates the job/process with TaskTracker




* Computation(program) is processor bound.

Structured
Unstructured (FB: vids, pics, texts, audio)
Semi-structured (log files)

Big Data - definition is given by IBM







Adding Core Libraries:

 - HBase
	- Allows SQL like queries which generates MapReduce jobs

 - Hive 
	- SQL-like query, create batch (MapReduce) jobs

 - Pig
	- ETL-like scripting language (for data manupulation like stripping, trimming, joining)

 - Impala
	- SQL-like query(in-memory querying), interactive process (no batch process)


Adding Other Libraries:

 - Mahout
	- Machine learning algorithms, predictive analytics, data mining

 - Spark
	- Resilient distributed data sets (in-memory streaming)

 - Storm
	- complex event processing (in-memory streaming)


MapReduce Programming Languages

 - Hadoop IDEs
	- Eclipse (Java)
	- Sublime (python)
	- RStudio (R Language)


- Hadoop 2.0 
	- JobTracker & TaskTracker are replaced by Yarn ResourceManager and Yarn Nodemanager


What is MapReduce?
 - Programming paradigm
 - Designed to solve one problem
 - Created by Google (purpose: how to index or get meaning out of all the information that is available on the internet.
 - Bringing computation to data location rather bringing data to compute.
 - Two parts (Map, Reduce)

The Map part of MapReduce:
 - Execute the Map() function on data.
 - Execute on each node.
 - Output<key, value> pairs on each node

The Reduce part of MapReduce:
 - Execute the Reduce() function on data
 - Execute on some node
 - Aggregate sets of <key, value> pairs on some nodes
 - Output a combined list



MapReduce 1.0
 - Distributed, scalable, cheap
 - Storage
	HDFS - triple replicated
	Commodity hardware
 - Processing
	Parallel via Map(local) and Reduce(aggregated)

Codng Steps
 - Create a class
 - Create a static Map class
 - Create a static Reduce class
 - Create a main function
	- Create a job
	- Job calls the Map and Reduce classes



* In MapReduce, its a single type of input in, run your mapper, get your key-value pairs out, run your reducer, get your combined list, and then go on to the next one. 

Hello World for MapReduce
 - "Word count"
 - Takes some text as input
 - Produces a list of words and counts them


Key aspects of MapReduce
 - It's an API, or set of libraries
	
	Job - unit of MapReduce work / instance
	Map task - runs on each node
	Reduce task - runs on some nodes
	Source data - HDFS or other location

MapReduce Deamons nad Service
 - JVMs or services - isolated processes (no state share)
	Job Tracker - one (controller and scheduler)
	Task Tracker - one per cluster (monitors tasks)
- Job configurations
	Specify input/output locations for job instances
	Job clients submit jobs for execution




MapReduce Coding Patterns
	- Standard - usually written in Java
	- Hadoop Streaming - Java base
		Other language for mapper/reducer logic
	- Hadoop Pipes - uses C++

Running First MapReduce Job
	- Word count == "Hello World!"
	- IDEs and runners
	- Eclipse and Hadoop SDKs
	- File system or HDFS

MapReduce Job Output
 - Success
 - Series of text files
 - Immutable if stored on HDFS
 - Each run needs a new file name
 - Usually appends run time to file name for uniqueness

MapReduce Job Status and Logs
 - Monitoring job run status
 - Local websites to view logs
 - Logs
 - Troubleshooting failed job runs
 - Error logs





Exploring Cloudera distribution Hue user interface.. 

Ways to Run MapReduce Jobs:
 	- Configure JobConf options
	- From the development environment (IDE)
	- From a GUI (Hue / HDInsight console)
	- From the command line 
		hadoop jar filename.jar input output

Job Execution optimizations
	
Methods to write MapReduce Jobs
	- Standard - usually writte in Java
	- Streaming
	- Pipes
	- Abstraction libraries
		Hive, Pig, etc. (higher-level language)



Better MapReduce: Optimizations

	- Optimize before the job runs
	- Optimize onload of the data
	- Optimize the map phase of the job
	- Optimize the shuffle phase of the job
	- Optimize the reduce phase of the job
	- Optimize after the job completes

---

## Hive:
 
- is useful for query like requirements.. like sum, average, coun etc..
- is not much suitable for data cleansing(like parsing, stripping, processing etc)..

![Hive Sql](../../images/hive.png "Hive Sql")
