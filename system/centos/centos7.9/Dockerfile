FROM centos:centos7.9.2009 
LABEL author="zcy" desc="test centos7.9  v1.1"  QQ="2858"
ENV dirname=zcy version=1.0
COPY CentOS7-Base-163.repo  /etc/yum.repos.d/ 
RUN yum install -y vim-enhanced tcpdump net-tools pcre pcre-devel gcc- gcc+ openssl gcc make zlib-devel \
    && yum clean all \
    && rm -f /etc/localtime && ln -s ../usr/share/zone/Asia/Shanghai /etc/localtime \
    && touch $dirname \
    && mkdir /data
ADD  index.html.tar.gz  /data
CMD ["/usr/bin/tail","-f","/etc/hosts"]

