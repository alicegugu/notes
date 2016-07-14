# Overview
![Components](http://spark.apache.org/docs/latest/img/cluster-overview.png)

## cluster manager types
* standalone - builtin with spark
* apache mesos
* hadoop yarn
[reference](http://hadoop.apache.org/docs/r2.6.4/hadoop-yarn/hadoop-yarn-site/YARN.html)


# Building
## compile


## make a distribution
export MAVEN_OPTS="-Xmx2g -XX:MaxPermSize=512M -XX:ReservedCodeCacheSize=512m"
./make-distribution.sh -Phadoop-2.6 -Pyarn -Dhadoop.version=2.6.0 -DskipTests -Phive -Phive-thriftserver

or

build/mvn -Pyarn -Phadoop-2.4 -Dhadoop.version=2.4.0 -DskipTests clean package
# Deploying

# Usage
run pyspark to open a spark interactive shell


## submiting applications
[guid](http://spark.apache.org/docs/latest/submitting-applications.html)

## Monitoring
[guid](http://spark.apache.org/docs/latest/monitoring.html)
* http://<driver-node>:4040

# Thrift server
## configuration

### metastore
Configuration of Hive is done by placing your hive-site.xml, core-site.xml (for security configuration), hdfs-site.xml (for HDFS configuration) file in conf/
