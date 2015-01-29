FROM fedora:latest
MAINTAINER robert <robert@belbob.thuis>
RUN yum update -y
RUN yum install -y cockpit
EXPOSE 9090
ENTRYPOINT ["/usr/libexec/cockpit-ws"]
CMD ["-D", "FOREGROUND"]
