# Pull base image
FROM java:8u92-oracle

MAINTAINER zhaojihui "zjh527@163.com"

RUN mkdir /opt/flume
RUN wget -qO- http://mirrors.tuna.tsinghua.edu.cn/apache/flume/1.6.0/apache-flume-1.6.0-bin.tar.gz \
  | tar zxvf - -C /opt/flume --strip-components=1

ADD start-flume.sh /opt/flume/bin/start-flume
COPY flume-ng-plugins-1.0-SNAPSHOT.jar /opt/flume/lib/flume-ng-plugins-1.0-SNAPSHOT.jar
COPY elasticsearch-1.7.5.jar /opt/flume/lib/elasticsearch-1.7.5.jar
COPY lucene-core-4.10.4.jar /opt/flume/lib/lucene-core-4.10.4.jar

ENV PATH /opt/flume/bin:$PATH
CMD [ "start-flume" ]
