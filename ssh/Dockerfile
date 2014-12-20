FROM centos:centos7
MAINTAINER belbob <robert.keersse@gmail.com>
RUN yum -y update
RUN yum -y install openssh-server passwd
RUN yum clean all
RUN mkdir /var/run/sshd
RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key -N ''
RUN echo 'root:password' | chpasswd
EXPOSE 22
ENTRYPOINT ["/usr/sbin/sshd", "-D"]
