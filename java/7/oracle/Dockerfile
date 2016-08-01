# Pull base image
FROM devbase

MAINTAINER zhaojihui "zjh527@163.com"

# update source
#RUN echo "deb http://mirrors.163.com/ubuntu/ trusty main restricted universe multiverse"> /etc/apt/sources.list
#RUN apt-get update && apt-get install software-properties-common -y
#RUN add-apt-repository ppa:webupd8team/java
#RUN apt-get update && apt-get -y upgrade

# automatically accept oracle license
#RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
#RUN apt-get install oracle-java7-installer -y
#RUN rm -rf /var/lib/apt/lists/*


#Install JDK7
#ADD jdk-7u80-linux-x64.tar.gz /tmp/jdk1.7.0_80
#RUN mkdir -p /usr/lib/jvm
#RUN mv /tmp/jdk1.7.0_80/jdk1.7.0_80/ /usr/lib/jvm/java-7-oracle/
#RUN cd tmp && rm -rf jdk1.7.0_80

#Set Oracle JDK7 as default Java
RUN update-alternatives --install /usr/bin/java java /usr/lib/jvm/java-7-oracle/bin/java 300
RUN update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/java-7-oracle/bin/javac 300

ENV JAVA_HOME /usr/lib/jvm/java-7-oracle/
