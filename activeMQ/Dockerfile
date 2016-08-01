# Pull base image
FROM java:8

MAINTAINER zhaojihui "zjh527@163.com"

#install activeMQ
RUN cd /tmp && wget http://mirrors.hust.edu.cn/apache/activemq/5.13.0/apache-activemq-5.13.0-bin.tar.gz
RUN cd /tmp && tar -xzf apache-activemq-5.13.0-bin.tar.gz && mv apache-activemq-5.13.0 /opt/activemq

EXPOSE 8161
EXPOSE 61616

ENTRYPOINT ["/opt/activemq/bin/activemq"]
CMD ["console"]
