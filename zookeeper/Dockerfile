# Pull base image
FROM java:8

MAINTAINER zhaojihui "zjh527@163.com"

#install zookeeper
RUN cd /tmp && wget http://apache.dataguru.cn/zookeeper/zookeeper-3.4.6/zookeeper-3.4.6.tar.gz
RUN cd /tmp && tar -xzf zookeeper-3.4.6.tar.gz && mv zookeeper-3.4.6 /opt/zookeeper
RUN cp /opt/zookeeper/conf/zoo_sample.cfg /opt/zookeeper/conf/zoo.cfg

EXPOSE 2181

ENTRYPOINT ["/opt/zookeeper/bin/zkServer.sh"]
CMD ["start-foreground"]
