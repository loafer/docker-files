# Pull base image
FROM ubuntu

MAINTAINER zhaojihui "zjh527@163.com"

# install wget
RUN apt-get install -y wget

# change sources
RUN cd /etc/apt && mv sources.list sources.list.bak && wget http://mirrors.163.com/.help/sources.list.trusty
RUN cd /etc/apt && mv sources.list.trusty sources.list
RUN apt-get update

# install gcc
RUN apt-get install build-essential -y && rm -rf /var/lib/apt/lists/*
