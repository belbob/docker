FROM centos:centos7
MAINTAINER belbob <robert.keersse@gmail.com>
RUN yum -y update; yum clean all
RUN yum -y install wget epel-release; yum clean all
RUN cd /etc/yum.repos.d/ && wget http://download.opensuse.org/repositories/isv:ownCloud:community/CentOS_CentOS-7/isv:ownCloud:community.repo
RUN yum install -y owncloud php-pdo php-gd; yum clean all
EXPOSE 80
ENTRYPOINT ["/usr/sbin/httpd"]
CMD ["-D", "FOREGROUND"]
