FROM centos:centos7.9.2009
LABEL auto="zcy" qq="2858349172" version="1.0"
COPY CentOS7-Base-163.repo  /etc/yum.repos.d/ 
COPY java.sh /etc/profile.d/
RUN yum install -y vim-enhanced tcpdump net-tools pcre pcre-devel gcc- gcc+ openssl gcc make zlib-devel \
    && yum clean all \
    && rm -f /etc/localtime && ln -s ../usr/share/zone/Asia/Shanghai /etc/localtime \
    && mkdir -p /usr/local/java
ADD jdk-8u171-linux-x64.tar.gz /usr/local/java/
RUN ln -s  /usr/local/java/jdk1.8.0_171  /opt/javaLastVer
CMD ["/usr/bin/tail","-f","/etc/hosts"]
