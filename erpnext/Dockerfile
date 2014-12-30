FROM centos:centos7
MAINTAINER belbob <robert.keersse@gmail.com>
RUN yum -y swap -- remove fakesystemd -- install systemd systemd-libs
RUN yum update -y; yum clean all
RUN yum install -y epel-release; yum clean all
RUN yum install -y wget sudo python-pip; yum clean all
RUN sed -i s'/Defaults    requiretty/#Defaults    requiretty'/g /etc/sudoers
#RUN wget https://raw.githubusercontent.com/frappe/bench/master/install_scripts/setup_frappe.sh
ADD ./setup_frappe.sh /setup_frappe.sh
RUN sudo bash setup_frappe.sh --setup-production
EXPOSE 80
