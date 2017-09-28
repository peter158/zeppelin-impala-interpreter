# zeppelin-impala-interpreter
Impala interpreter for Apache Zeppelin.


#Build
Requirement: Zeppelin must be in your local repo.

```
mvn clean package  or  mvn clean package -DskipTests
```

#Download
If you cannot build the jar, you can download it in the [release page](https://github.com/peter158/zeppelin-impala-interpreter/releases)

#Deployment

```
1, Update $ZEPPELIN_HOME/conf/zeppeln-site.xml

<property>
  <name>zeppelin.interpreters</name>
  <value>...,org.apache.zeppelin.impala.ImpalaInterpreter</value>
</property>

2, Create $ZEPPELIN_HOME/interpreter/impala
3, Copy interpreter jar in $ZEPPELIN_HOME/interpreter/impala

```
#Configuration
###Properties
| Property        | Value    | 
| --------   | -----:   |
| default.driver        | org.apache.hive.jdbc.HiveDriver      | 
| default.url       | jdbc:hive2://localhost:21050/      | 
| default.user        | impalaUser      | 
| default. password        | impalaPassword      | 

###Dependencies
| Artifact        | Exclude    | 
| --------   | -----:   |
| org.apache.hive:hive-jdbc:0.14.0	|  | 
| org.apache.hadoop:hadoop-common:2.6.0       |       | 
| jline:jline:2.14       |       | 


#How to use
In Zeppelin, use %impala in a paragraph. After that,you can type the same impala sql code ,For more information, please consult:[https://www.w3cschool.cn/impala/impala_query_language_basics.html](https://www.w3cschool.cn/impala/impala_query_language_basics.html)
#Examples
Configuration
![]()