# Pull base image
FROM java:8

MAINTAINER zhaojihui "zjh527@163.com"

#Install ApacheDS
RUN cd /tmp && wget http://mirrors.cnnic.cn/apache//directory/apacheds/dist/2.0.0-M20/apacheds-2.0.0-M20.tar.gz
RUN cd /tmp && tar -xzf apacheds-2.0.0-M20.tar.gz && mv apacheds-2.0.0-M20 /opt/apacheds

EXPOSE  10389
EXPOSE  10636

ENTRYPOINT ["/opt/apacheds/bin/apacheds.sh"]
CMD ["start"]
