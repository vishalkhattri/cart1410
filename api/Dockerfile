# This is docker file for api layer cart MS
FROM centos:7
MAINTAINER khattri09@gmail.com
RUN yum -y update
ADD scripts /opt/
RUN chmod 755 /opt/*
RUN /opt/installpackage.sh
ADD config/ /etc/httpd/conf/
ADD code /apps/apache
ENV BACKENDLB=test 
EXPOSE 80
CMD ["/opt/startapache.sh"]