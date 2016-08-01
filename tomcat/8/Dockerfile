# Pull base image
FROM java:8

MAINTAINER zhaojihui "zjh527@163.com"

# Install Tomcat8
RUN cd /tmp && wget "http://apache.fayea.com/tomcat/tomcat-8/v8.0.26/bin/apache-tomcat-8.0.26.tar.gz"
RUN cd /tmp && tar -xf apache-tomcat-8.0.26.tar.gz
RUN mv /tmp/apache-tomcat-8.0.26 /opt/tomcat

ENV CATALINA_HOME /opt/tomcat

EXPOSE 8080

CMD ["/opt/tomcat/bin/catalina.sh", "run"]
