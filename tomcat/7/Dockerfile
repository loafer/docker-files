# Pull base image
FROM java:8

MAINTAINER zhaojihui "zjh527@163.com"

# Install Tomcat7
RUN cd /tmp && wget "http://apache.fayea.com/tomcat/tomcat-7/v7.0.64/bin/apache-tomcat-7.0.64.tar.gz"
RUN cd /tmp && tar -xf apache-tomcat-7.0.64.tar.gz
RUN mv /tmp/apache-tomcat-7.0.64 /opt/tomcat

ENV CATALINA_HOME /opt/tomcat

EXPOSE 8080

#CMD ["/opt/tomcat/bin/catalina.sh", "run"]
