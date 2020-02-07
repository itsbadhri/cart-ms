# Docker file for Cart Frontend. FROM should be the first uncommented line. Only ARG can preceed it
#ARG myenv
FROM centos:7
RUN yum -y update
ADD scripts /opt
RUN chmod +x /opt/*.sh
RUN /opt/packages.sh
ADD config /root
#RUN chmod +x /root/myenv.sh; source /root/myenv.sh $myenv
RUN chmod +x /root/myenv.sh; source /root/myenv.sh
#RUN yum -y install httpd php php-gd php-mysql
ADD code /var/www/html
CMD ["httpd", "-D", "FOREGROUND"]