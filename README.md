# Hadoop
this is my hadoop demo

1.install jdk hadoop 
  go to website and download
2.install op
enssh
  apt-get install openssh-server

3.start openssh
  /etc/init.d/ssh start

4.configure three xml files : core-site.xml hdfs-site.xml mapred-site.xml. under the folder "etc/hadoop"
  core-site.xml:
  ```
  <configuration>
	<property>
		<name>fs.default.name</name>
		<value>hdfs://localhost:9000</value>
	</property>
	
</configuration>
  ```
  hdfs-site.xml
  ```
  <configuration>
	<property>
		<name>dfs.replication</name>
		<value>1</value>	
	</property>
</configuration>
  ```
 mapred-site.xml:
 ```
 <configuration>
	<property>
		<name>mapred.job.tracker</name>	
		<value>localhost:9001</value>
	</property>
</configuration>
 ```

5.change hdfs's root directory
core-site.xml:
  ```
  <configuration>
	<property>
		<name>fs.default.name</name>
		<value>hdfs://localhost:9000</value>
	</property>
	<property>
		<name>hadoop.tmp.dir</name>
		<value>/usr/ulib/disk1/workspace/Hadoop</value>	
	</property>
</configuration>
  ```

6.format above directory
  hadoop namenode -format

7.start hadoop
  start-dfs.sh
  start-yarn.sh
