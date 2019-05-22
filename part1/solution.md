
## 1)
```
sudo useradd training 
sudo passwd training 
sudo groupadd skcc
sudo usermod -a -G skcc training
```

## 2) 
```
IP정보 조회 :  ip addr
호스트명 조회 : hostname
ip-172-31-2-76.ap-northeast-2.compute.internal
ip-172-31-11-108.ap-northeast-2.compute.internal
ip-172-31-5-178.ap-northeast-2.compute.internal
ip-172-31-2-186.ap-northeast-2.compute.internal
ip-172-31-14-114.ap-northeast-2.compute.internal
```


## 3)리눅스 릴리즈 정보
```
[centos@ip-172-31-2-76 ~]$ cat /etc/*release*
CentOS Linux release 7.6.1810 (Core)
Derived from Red Hat Enterprise Linux 7.6 (Source)
NAME="CentOS Linux"
VERSION="7 (Core)"
ID="centos"
ID_LIKE="rhel fedora"
VERSION_ID="7"
PRETTY_NAME="CentOS Linux 7 (Core)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:centos:centos:7"
HOME_URL="https://www.centos.org/"
BUG_REPORT_URL="https://bugs.centos.org/"

CENTOS_MANTISBT_PROJECT="CentOS-7"
CENTOS_MANTISBT_PROJECT_VERSION="7"
REDHAT_SUPPORT_PRODUCT="centos"
REDHAT_SUPPORT_PRODUCT_VERSION="7"

CentOS Linux release 7.6.1810 (Core)
CentOS Linux release 7.6.1810 (Core)
cpe:/o:centos:centos:7
```

## 4)마스터 노드의 파일 시스템 정보 조회
```
[centos@ip-172-31-2-76 ~]$ df
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/nvme0n1p1 104846316 1156260 103690056   2% /
devtmpfs         7872836       0   7872836   0% /dev
tmpfs            7895692       0   7895692   0% /dev/shm
tmpfs            7895692   16736   7878956   1% /run
tmpfs            7895692       0   7895692   0% /sys/fs/cgroup
tmpfs            1579140       0   1579140   0% /run/user/1000
```

## 5)yum repolist enabled
```
[centos@ip-172-31-2-76 ~]$ yum repolist all
Loaded plugins: fastestmirror
Determining fastest mirrors
epel/x86_64/metalink                                     | 7.5 kB     00:00
 * base: mirror.kakao.com
 * epel: d2lzkl7pfhq30w.cloudfront.net
 * extras: mirror.kakao.com
 * updates: mirror.kakao.com
base                                                     | 3.6 kB     00:00
cloudera-manager                                         |  951 B     00:00
epel                                                     | 4.7 kB     00:00
extras                                                   | 3.4 kB     00:00
updates                                                  | 3.4 kB     00:00
(1/2): epel/x86_64/updateinfo                              | 998 kB   00:00
(2/2): epel/x86_64/primary_db                              | 6.7 MB   00:00
cloudera-manager/primary                                   | 4.3 kB   00:00
cloudera-manager                                                            7/7
repo id                       repo name                          status
C7.0.1406-base/x86_64         CentOS-7.0.1406 - Base             disabled
C7.0.1406-centosplus/x86_64   CentOS-7.0.1406 - CentOSPlus       disabled
C7.0.1406-extras/x86_64       CentOS-7.0.1406 - Extras           disabled
C7.0.1406-fasttrack/x86_64    CentOS-7.0.1406 - Fasttrack        disabled
C7.0.1406-updates/x86_64      CentOS-7.0.1406 - Updates          disabled
C7.1.1503-base/x86_64         CentOS-7.1.1503 - Base             disabled
C7.1.1503-centosplus/x86_64   CentOS-7.1.1503 - CentOSPlus       disabled
C7.1.1503-extras/x86_64       CentOS-7.1.1503 - Extras           disabled
C7.1.1503-fasttrack/x86_64    CentOS-7.1.1503 - Fasttrack        disabled
C7.1.1503-updates/x86_64      CentOS-7.1.1503 - Updates          disabled
C7.2.1511-base/x86_64         CentOS-7.2.1511 - Base             disabled
C7.2.1511-centosplus/x86_64   CentOS-7.2.1511 - CentOSPlus       disabled
C7.2.1511-extras/x86_64       CentOS-7.2.1511 - Extras           disabled
C7.2.1511-fasttrack/x86_64    CentOS-7.2.1511 - Fasttrack        disabled
C7.2.1511-updates/x86_64      CentOS-7.2.1511 - Updates          disabled
C7.3.1611-base/x86_64         CentOS-7.3.1611 - Base             disabled
C7.3.1611-centosplus/x86_64   CentOS-7.3.1611 - CentOSPlus       disabled
C7.3.1611-extras/x86_64       CentOS-7.3.1611 - Extras           disabled
C7.3.1611-fasttrack/x86_64    CentOS-7.3.1611 - Fasttrack        disabled
C7.3.1611-updates/x86_64      CentOS-7.3.1611 - Updates          disabled
C7.4.1708-base/x86_64         CentOS-7.4.1708 - Base             disabled
C7.4.1708-centosplus/x86_64   CentOS-7.4.1708 - CentOSPlus       disabled
C7.4.1708-extras/x86_64       CentOS-7.4.1708 - Extras           disabled
C7.4.1708-fasttrack/x86_64    CentOS-7.4.1708 - Fasttrack        disabled
C7.4.1708-updates/x86_64      CentOS-7.4.1708 - Updates          disabled
C7.5.1804-base/x86_64         CentOS-7.5.1804 - Base             disabled
C7.5.1804-centosplus/x86_64   CentOS-7.5.1804 - CentOSPlus       disabled
C7.5.1804-extras/x86_64       CentOS-7.5.1804 - Extras           disabled
C7.5.1804-fasttrack/x86_64    CentOS-7.5.1804 - Fasttrack        disabled
C7.5.1804-updates/x86_64      CentOS-7.5.1804 - Updates          disabled
base/7/x86_64                 CentOS-7 - Base                    enabled: 10,019
base-debuginfo/x86_64         CentOS-7 - Debuginfo               disabled
base-source/7                 CentOS-7 - Base Sources            disabled
c7-media                      CentOS-7 - Media                   disabled
centosplus/7/x86_64           CentOS-7 - Plus                    disabled
centosplus-source/7           CentOS-7 - Plus Sources            disabled
cloudera-manager              Cloudera Manager                   enabled:      7
cr/7/x86_64                   CentOS-7 - cr                      disabled
*epel/x86_64                  Extra Packages for Enterprise Linu enabled: 13,194
epel-debuginfo/x86_64         Extra Packages for Enterprise Linu disabled
epel-source/x86_64            Extra Packages for Enterprise Linu disabled
epel-testing/x86_64           Extra Packages for Enterprise Linu disabled
epel-testing-debuginfo/x86_64 Extra Packages for Enterprise Linu disabled
epel-testing-source/x86_64    Extra Packages for Enterprise Linu disabled
extras/7/x86_64               CentOS-7 - Extras                  enabled:    413
extras-source/7               CentOS-7 - Extras Sources          disabled
fasttrack/7/x86_64            CentOS-7 - fasttrack               disabled
updates/7/x86_64              CentOS-7 - Updates                 enabled:  1,945
updates-source/7              CentOS-7 - Updates Sources         disabled
repolist: 25,578
```

## 6) training user info
```
[centos@ip-172-31-2-76 ~]$ cat /etc/passwd
training:x:1001:1001::/home/training:/bin/bash
```

## 7) skcc group info
```
[centos@ip-172-31-2-76 ~]$ cat /etc/group
skcc:x:1002:training
```

## 8)
```
[centos@ip-172-31-2-76 ~]$ getent group skcc
skcc:x:1002:training
```

## 9) 
```
[centos@ip-172-31-2-76 ~]$ getent passwd training
training:x:1001:1001::/home/training:/bin/bash
```

## b. Install a Mysql server
## 1)
```
[centos@ip-172-31-2-76 mysql-connector-java-5.1.46]$ hostname
nd1.team5.com
```

## 2)
```
[training@nd1 mysql-connector-java-5.1.46]$ mysql --version
mysql  Ver 15.1 Distrib 5.5.60-MariaDB, for Linux (x86_64) using readline 5.1
```

## 3)
```
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| hue                |
| metastore          |
| mysql              |
| nav                |
| navms              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
12 rows in set (0.00 sec)
```



## 2. create table
```
## a.MariaDB [(none)]> create database test;
Query OK, 1 row affected (0.01 sec)
Database changed
MariaDB [test]> CREATE TABLE `authors` (
    ->   `id` int(11) NOT NULL AUTO_INCREMENT,
    ->   `first_name` varchar(50) COLLATE utf8_unicode_ci NOT NULL,
    ->   `last_name` varchar(50) COLLATE utf8_unicode_ci NOT NULL,
    ->   `email` varchar(100) COLLATE utf8_unicode_ci NOT NULL,
    ->   `birthdate` date NOT NULL,
    ->   `added` timestamp NOT NULL DEFAULT current_timestamp(),
    ->   PRIMARY KEY (`id`),
    ->   UNIQUE KEY `email` (`email`)
    -> ) ENGINE=InnoDB AUTO_INCREMENT=10001 DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;
Query OK, 0 rows affected (0.00 sec)

MariaDB [test]> show tables;
+----------------+
| Tables_in_test |
+----------------+
| authors        |
| posts          |
+----------------+
2 rows in set (0.00 sec)
```


## b. 

## c.
```
MariaDB [(none)]> GRANT ALL ON *.* TO 'training'@'%' IDENTIFIED BY 'training';
Query OK, 0 rows affected (0.00 sec)

MariaDB [(none)]> FLUSH PRIVILEGES;
Query OK, 0 rows affected (0.00 sec)
```
![photo.PNG](https://github.com/rlalfo11/bigdata_final/blob/master/CM_Manager.PNG?raw=true)

## 3.
## a. 
```
[training@nd1 centos]$ sqoop import --connect jdbc:mysql://nd1.team5.com/test --username training --password training --table posts --target-dir /test/posts_import
Warning: /opt/cloudera/parcels/CDH-5.15.2-1.cdh5.15.2.p0.3/bin/../lib/sqoop/../accumulo does not exist! Accumulo imports will fail.
Please set $ACCUMULO_HOME to the root of your Accumulo installation.
19/05/22 15:21:27 INFO sqoop.Sqoop: Running Sqoop version: 1.4.6-cdh5.15.2
19/05/22 15:21:27 WARN tool.BaseSqoopTool: Setting your password on the command-line is insecure. Consider using -P instead.
19/05/22 15:21:27 INFO manager.MySQLManager: Preparing to use a MySQL streaming resultset.
19/05/22 15:21:27 INFO tool.CodeGenTool: Beginning code generation
19/05/22 15:21:28 INFO manager.SqlManager: Executing SQL statement: SELECT t.* FROM `posts` AS t LIMIT 1
19/05/22 15:21:28 INFO manager.SqlManager: Executing SQL statement: SELECT t.* FROM `posts` AS t LIMIT 1
19/05/22 15:21:28 INFO orm.CompilationManager: HADOOP_MAPRED_HOME is /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce
Note: /tmp/sqoop-training/compile/d69cc6bc4e2cc0ac05c577ac5ba58628/posts.java uses or overrides a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
19/05/22 15:21:29 ERROR orm.CompilationManager: Could not make directory: /home/centos/.
19/05/22 15:21:29 INFO orm.CompilationManager: Writing jar file: /tmp/sqoop-training/compile/d69cc6bc4e2cc0ac05c577ac5ba58628/posts.jar
19/05/22 15:21:29 WARN manager.MySQLManager: It looks like you are importing from mysql.
19/05/22 15:21:29 WARN manager.MySQLManager: This transfer can be faster! Use the --direct
19/05/22 15:21:29 WARN manager.MySQLManager: option to exercise a MySQL-specific fast path.
19/05/22 15:21:29 INFO manager.MySQLManager: Setting zero DATETIME behavior to convertToNull (mysql)
19/05/22 15:21:29 INFO mapreduce.ImportJobBase: Beginning import of posts
19/05/22 15:21:29 INFO Configuration.deprecation: mapred.jar is deprecated. Instead, use mapreduce.job.jar
19/05/22 15:21:30 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
19/05/22 15:21:30 INFO client.RMProxy: Connecting to ResourceManager at nd1.team5.com/172.31.2.76:8032
19/05/22 15:21:31 INFO db.DBInputFormat: Using read commited transaction isolation
19/05/22 15:21:31 INFO db.DataDrivenDBInputFormat: BoundingValsQuery: SELECT MIN(`id`), MAX(`id`) FROM `posts`
19/05/22 15:21:31 INFO db.IntegerSplitter: Split size: 11; Num splits: 4 from: 1 to: 46
19/05/22 15:21:31 INFO mapreduce.JobSubmitter: number of splits:4
19/05/22 15:21:31 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1558504385866_0002
19/05/22 15:21:31 INFO impl.YarnClientImpl: Submitted application application_1558504385866_0002
19/05/22 15:21:31 INFO mapreduce.Job: The url to track the job: http://nd1.team5.com:8088/proxy/application_1558504385866_0002/
19/05/22 15:21:31 INFO mapreduce.Job: Running job: job_1558504385866_0002
19/05/22 15:21:37 INFO mapreduce.Job: Job job_1558504385866_0002 running in uber mode : false
19/05/22 15:21:37 INFO mapreduce.Job:  map 0% reduce 0%
19/05/22 15:21:43 INFO mapreduce.Job:  map 100% reduce 0%
19/05/22 15:21:43 INFO mapreduce.Job: Job job_1558504385866_0002 completed successfully
19/05/22 15:21:43 INFO mapreduce.Job: Counters: 30
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=701636
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=400
                HDFS: Number of bytes written=11037
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=15439
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=15439
                Total vcore-milliseconds taken by all map tasks=15439
                Total megabyte-milliseconds taken by all map tasks=15809536
        Map-Reduce Framework
                Map input records=29
                Map output records=29
                Input split bytes=400
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=208
                CPU time spent (ms)=2740
                Physical memory (bytes) snapshot=904192000
                Virtual memory (bytes) snapshot=6355845120
                Total committed heap usage (bytes)=1222639616
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=11037
19/05/22 15:21:43 INFO mapreduce.ImportJobBase: Transferred 10.7783 KB in 13.7491 seconds (802.7433 bytes/sec)
19/05/22 15:21:43 INFO mapreduce.ImportJobBase: Retrieved 29 records.
```

```
mysql -> hive
[training@nd1 centos]$ sqoop import --connect jdbc:mysql://nd1.team5.com/test --username training --password training --table authors --target-dir /test/authors_import_direct --hive-import --create-hive-table --hive-table default.authors
Warning: /opt/cloudera/parcels/CDH-5.15.2-1.cdh5.15.2.p0.3/bin/../lib/sqoop/../accumulo does not exist! Accumulo imports will fail.
Please set $ACCUMULO_HOME to the root of your Accumulo installation.
19/05/22 15:43:50 INFO sqoop.Sqoop: Running Sqoop version: 1.4.6-cdh5.15.2
19/05/22 15:43:50 WARN tool.BaseSqoopTool: Setting your password on the command-line is insecure. Consider using -P instead.
19/05/22 15:43:50 INFO tool.BaseSqoopTool: Using Hive-specific delimiters for output. You can override
19/05/22 15:43:50 INFO tool.BaseSqoopTool: delimiters with --fields-terminated-by, etc.
19/05/22 15:43:50 INFO manager.MySQLManager: Preparing to use a MySQL streaming resultset.
19/05/22 15:43:50 INFO tool.CodeGenTool: Beginning code generation
19/05/22 15:43:51 INFO manager.SqlManager: Executing SQL statement: SELECT t.* FROM `authors` AS t LIMIT 1
19/05/22 15:43:51 INFO manager.SqlManager: Executing SQL statement: SELECT t.* FROM `authors` AS t LIMIT 1
19/05/22 15:43:51 INFO orm.CompilationManager: HADOOP_MAPRED_HOME is /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce
Note: /tmp/sqoop-training/compile/08436c81bd05578e84c9bf25ca8f4be3/authors.java uses or overrides a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
19/05/22 15:43:52 ERROR orm.CompilationManager: Could not make directory: /home/centos/.
19/05/22 15:43:52 INFO orm.CompilationManager: Writing jar file: /tmp/sqoop-training/compile/08436c81bd05578e84c9bf25ca8f4be3/authors.jar
19/05/22 15:43:52 WARN manager.MySQLManager: It looks like you are importing from mysql.
19/05/22 15:43:52 WARN manager.MySQLManager: This transfer can be faster! Use the --direct
19/05/22 15:43:52 WARN manager.MySQLManager: option to exercise a MySQL-specific fast path.
19/05/22 15:43:52 INFO manager.MySQLManager: Setting zero DATETIME behavior to convertToNull (mysql)
19/05/22 15:43:52 INFO mapreduce.ImportJobBase: Beginning import of authors
19/05/22 15:43:52 INFO Configuration.deprecation: mapred.jar is deprecated. Instead, use mapreduce.job.jar
19/05/22 15:43:52 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
19/05/22 15:43:52 INFO client.RMProxy: Connecting to ResourceManager at nd1.team5.com/172.31.2.76:8032
19/05/22 15:43:54 INFO db.DBInputFormat: Using read commited transaction isolation
19/05/22 15:43:54 INFO db.DataDrivenDBInputFormat: BoundingValsQuery: SELECT MIN(`id`), MAX(`id`) FROM `authors`
19/05/22 15:43:54 INFO db.IntegerSplitter: Split size: 11; Num splits: 4 from: 1 to: 47
19/05/22 15:43:54 INFO mapreduce.JobSubmitter: number of splits:4
19/05/22 15:43:54 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1558504385866_0004
19/05/22 15:43:54 INFO impl.YarnClientImpl: Submitted application application_1558504385866_0004
19/05/22 15:43:54 INFO mapreduce.Job: The url to track the job: http://nd1.team5.com:8088/proxy/application_1558504385866_0004/
19/05/22 15:43:54 INFO mapreduce.Job: Running job: job_1558504385866_0004
19/05/22 15:43:59 INFO mapreduce.Job: Job job_1558504385866_0004 running in uber mode : false
19/05/22 15:43:59 INFO mapreduce.Job:  map 0% reduce 0%
19/05/22 15:44:05 INFO mapreduce.Job:  map 100% reduce 0%
19/05/22 15:44:05 INFO mapreduce.Job: Job job_1558504385866_0004 completed successfully
19/05/22 15:44:06 INFO mapreduce.Job: Counters: 30
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=702416
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=400
                HDFS: Number of bytes written=3547
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=14828
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=14828
                Total vcore-milliseconds taken by all map tasks=14828
                Total megabyte-milliseconds taken by all map tasks=15183872
        Map-Reduce Framework
                Map input records=47
                Map output records=47
                Input split bytes=400
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=188
                CPU time spent (ms)=2880
                Physical memory (bytes) snapshot=945840128
                Virtual memory (bytes) snapshot=6360301568
                Total committed heap usage (bytes)=1222639616
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=3547
19/05/22 15:44:06 INFO mapreduce.ImportJobBase: Transferred 3.4639 KB in 13.1729 seconds (269.2646 bytes/sec)
19/05/22 15:44:06 INFO mapreduce.ImportJobBase: Retrieved 47 records.
19/05/22 15:44:06 INFO manager.SqlManager: Executing SQL statement: SELECT t.* FROM `authors` AS t LIMIT 1
19/05/22 15:44:06 WARN hive.TableDefWriter: Column birthdate had to be cast to a less precise type in Hive
19/05/22 15:44:06 WARN hive.TableDefWriter: Column added had to be cast to a less precise type in Hive
19/05/22 15:44:06 INFO hive.HiveImport: Loading uploaded data into Hive

Logging initialized using configuration in jar:file:/opt/cloudera/parcels/CDH-5.15.2-1.cdh5.15.2.p0.3/jars/hive-common-1.1.0-cdh5.15.2.jar!/hive-log4j.properties
OK
Time taken: 2.345 seconds
Loading data to table default.authors
Table default.authors stats: [numFiles=4, totalSize=3547]
OK
Time taken: 0.247 seconds
```


```
[training@nd1 centos]$ sqoop import --connect jdbc:mysql://nd1.team5.com/test --username training --password training --table posts --target-dir /test/posts_import_direct --hive-import --create-hive-table --hive-table default.posts
Warning: /opt/cloudera/parcels/CDH-5.15.2-1.cdh5.15.2.p0.3/bin/../lib/sqoop/../accumulo does not exist! Accumulo imports will fail.
Please set $ACCUMULO_HOME to the root of your Accumulo installation.
19/05/22 15:45:41 INFO sqoop.Sqoop: Running Sqoop version: 1.4.6-cdh5.15.2
19/05/22 15:45:41 WARN tool.BaseSqoopTool: Setting your password on the command-line is insecure. Consider using -P instead.
19/05/22 15:45:41 INFO tool.BaseSqoopTool: Using Hive-specific delimiters for output. You can override
19/05/22 15:45:41 INFO tool.BaseSqoopTool: delimiters with --fields-terminated-by, etc.
19/05/22 15:45:41 INFO manager.MySQLManager: Preparing to use a MySQL streaming resultset.
19/05/22 15:45:41 INFO tool.CodeGenTool: Beginning code generation
19/05/22 15:45:41 INFO manager.SqlManager: Executing SQL statement: SELECT t.* FROM `posts` AS t LIMIT 1
19/05/22 15:45:41 INFO manager.SqlManager: Executing SQL statement: SELECT t.* FROM `posts` AS t LIMIT 1
19/05/22 15:45:41 INFO orm.CompilationManager: HADOOP_MAPRED_HOME is /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce
Note: /tmp/sqoop-training/compile/6513445fd9d48d1af969360c34d10b16/posts.java uses or overrides a deprecated API.
Note: Recompile with -Xlint:deprecation for details.
19/05/22 15:45:42 ERROR orm.CompilationManager: Could not make directory: /home/centos/.
19/05/22 15:45:42 INFO orm.CompilationManager: Writing jar file: /tmp/sqoop-training/compile/6513445fd9d48d1af969360c34d10b16/posts.jar
19/05/22 15:45:42 WARN manager.MySQLManager: It looks like you are importing from mysql.
19/05/22 15:45:42 WARN manager.MySQLManager: This transfer can be faster! Use the --direct
19/05/22 15:45:42 WARN manager.MySQLManager: option to exercise a MySQL-specific fast path.
19/05/22 15:45:42 INFO manager.MySQLManager: Setting zero DATETIME behavior to convertToNull (mysql)
19/05/22 15:45:42 INFO mapreduce.ImportJobBase: Beginning import of posts
19/05/22 15:45:42 INFO Configuration.deprecation: mapred.jar is deprecated. Instead, use mapreduce.job.jar
19/05/22 15:45:43 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
19/05/22 15:45:43 INFO client.RMProxy: Connecting to ResourceManager at nd1.team5.com/172.31.2.76:8032
19/05/22 15:45:44 INFO db.DBInputFormat: Using read commited transaction isolation
19/05/22 15:45:44 INFO db.DataDrivenDBInputFormat: BoundingValsQuery: SELECT MIN(`id`), MAX(`id`) FROM `posts`
19/05/22 15:45:44 INFO db.IntegerSplitter: Split size: 11; Num splits: 4 from: 1 to: 46
19/05/22 15:45:44 INFO mapreduce.JobSubmitter: number of splits:4
19/05/22 15:45:44 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1558504385866_0005
19/05/22 15:45:44 INFO impl.YarnClientImpl: Submitted application application_1558504385866_0005
19/05/22 15:45:44 INFO mapreduce.Job: The url to track the job: http://nd1.team5.com:8088/proxy/application_1558504385866_0005/
19/05/22 15:45:44 INFO mapreduce.Job: Running job: job_1558504385866_0005
19/05/22 15:45:49 INFO mapreduce.Job: Job job_1558504385866_0005 running in uber mode : false
19/05/22 15:45:49 INFO mapreduce.Job:  map 0% reduce 0%
19/05/22 15:45:55 INFO mapreduce.Job:  map 100% reduce 0%
19/05/22 15:45:57 INFO mapreduce.Job: Job job_1558504385866_0005 completed successfully
19/05/22 15:45:57 INFO mapreduce.Job: Counters: 30
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=702352
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=400
                HDFS: Number of bytes written=11037
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=15982
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=15982
                Total vcore-milliseconds taken by all map tasks=15982
                Total megabyte-milliseconds taken by all map tasks=16365568
        Map-Reduce Framework
                Map input records=29
                Map output records=29
                Input split bytes=400
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=191
                CPU time spent (ms)=2680
                Physical memory (bytes) snapshot=905666560
                Virtual memory (bytes) snapshot=6348140544
                Total committed heap usage (bytes)=1222639616
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=11037
19/05/22 15:45:57 INFO mapreduce.ImportJobBase: Transferred 10.7783 KB in 13.6672 seconds (807.5519 bytes/sec)
19/05/22 15:45:57 INFO mapreduce.ImportJobBase: Retrieved 29 records.
19/05/22 15:45:57 INFO manager.SqlManager: Executing SQL statement: SELECT t.* FROM `posts` AS t LIMIT 1
19/05/22 15:45:57 WARN hive.TableDefWriter: Column date had to be cast to a less precise type in Hive
19/05/22 15:45:57 INFO hive.HiveImport: Loading uploaded data into Hive
Logging initialized using configuration in jar:file:/opt/cloudera/parcels/CDH-5.15.2-1.cdh5.15.2.p0.3/jars/hive-common-1.1.0-cdh5.15.2.jar!/hive-log4j.properties
OK
Time taken: 2.404 seconds
Loading data to table default.posts
Table default.posts stats: [numFiles=4, totalSize=11037]
OK
Time taken: 0.238 seconds
```
