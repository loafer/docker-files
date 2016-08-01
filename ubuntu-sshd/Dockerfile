FROM ubuntu

MAINTAINER zhaojihui "zjh527@163.com"

# 换源
RUN echo "deb http://mirrors.163.com/ubuntu/ trusty main restricted universe multiverse"> /etc/apt/sources.list
RUN apt-get update

# 安装 openssh-server和openssh-client
RUN apt-get install -y openssh-server
RUN apt-get install -y openssh-client
RUN mkdir -p /var/run/sshd

# 允许root使用ssh登陆
RUN sed -i 's/PermitRootLogin without-password/#PermitRootLogin without-password/g' /etc/ssh/sshd_config
RUN sed -i '$a PermitRootLogin yes' /etc/ssh/sshd_config

#设置root密码
RUN echo "root:ecode"|chpasswd

# 开放端口
EXPOSE 22

# 启动sshd服务
#CMD ["/etc/init.d/ssh start"]
