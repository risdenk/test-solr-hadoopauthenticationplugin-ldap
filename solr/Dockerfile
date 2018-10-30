FROM solr:alpine

RUN rm -rf /opt/solr/server/solr-webapp/webapp/WEB-INF/lib/hadoop-*.jar

ENV HADOOP_VERSION=2.9.1
ADD --chown=solr http://central.maven.org/maven2/org/apache/hadoop/hadoop-hdfs/${HADOOP_VERSION}/hadoop-hdfs-${HADOOP_VERSION}.jar /opt/solr/server/solr-webapp/webapp/WEB-INF/lib/hadoop-hdfs-${HADOOP_VERSION}.jar
ADD --chown=solr http://central.maven.org/maven2/org/apache/hadoop/hadoop-auth/${HADOOP_VERSION}/hadoop-auth-${HADOOP_VERSION}.jar /opt/solr/server/solr-webapp/webapp/WEB-INF/lib/hadoop-auth-${HADOOP_VERSION}.jar
ADD --chown=solr http://central.maven.org/maven2/org/apache/hadoop/hadoop-annotations/${HADOOP_VERSION}/hadoop-annotations-${HADOOP_VERSION}.jar /opt/solr/server/solr-webapp/webapp/WEB-INF/lib/hadoop-annotations-${HADOOP_VERSION}.jar
ADD --chown=solr http://central.maven.org/maven2/org/apache/hadoop/hadoop-common/${HADOOP_VERSION}/hadoop-common-${HADOOP_VERSION}.jar /opt/solr/server/solr-webapp/webapp/WEB-INF/lib/hadoop-common-${HADOOP_VERSION}.jar

COPY --chown=solr security.json /opt/security.json

