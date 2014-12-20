FROM centos:centos6
MAINTAINER belbob <robert.keersse@gmail.com>
RUN yum update -y
RUN yum install -y wget sudo systemd
#RUN setenforce 0
#RUN sed -i s'/SELINUX=enforcing/SELINUX=disabled'/g /etc/sysconfig/selinux
RUN sed -i s'/Defaults    requiretty/#Defaults    requiretty'/g /etc/sudoers
RUN wget https://raw.githubusercontent.com/frappe/bench/master/install_scripts/setup_frappe.sh
RUN sudo bash setup_frappe.sh --setup-production
EXPOSE 80
