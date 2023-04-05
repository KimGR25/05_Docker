FROM centos:7

RUN yum -y update && yum install -y vsftpd && yum clean all
COPY vsftpd.conf.centos7.template /etc/vsftpd/vsftpd.conf

VOLUME /var/ftp/pub
COPY welcometomyftpserver.txt /var/ftp/pub/welcometomyftpserver.txt

EXPOSE 21 20

ENTRYPOINT /usr/sbin/vsftpd
