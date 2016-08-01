# Pull base image
FROM ubuntu:14.04.4

MAINTAINER zhaojihui "zjh527@163.com"

ARG JRE_MAJOR='8'
ARG JRE_UPDATE='92'
ARG JRE_BUILD='14'

RUN \
  sed -i 's/archive.ubuntu.com/mirrors.aliyun.com/g' /etc/apt/sources.list && \
  apt-get update && \
  apt-get install -y wget && \
  wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/"$JRE_MAJOR"u"$JRE_UPDATE"-b"$JRE_BUILD"/jre-"$JRE_MAJOR"u"$JRE_UPDATE"-linux-x64.tar.gz && \
  mkdir -p /usr/lib/jvm/java-8-oracle && \
  tar -C /usr/lib/jvm/java-8-oracle --strip-components=1 -xvf *linux-x64.tar.gz && \
  update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/java-8-oracle/bin/java" 1 && \
  rm -rf /var/lib/apt/lists/* && \
  rm *linux-x64.tar.gz


ENV JAVA_HOME /usr/lib/jvm/java-8-oracle
