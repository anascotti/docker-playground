FROM centos:7
ENV TERM dumb

ADD MariaDB.repo /etc/yum.repos.d/MariaDB.repo
RUN yum -y install MariaDB-server
RUN echo "[mysqld]" >> /etc/my.cnf
RUN echo "bind-address=0.0.0.0" >> /etc/my.cnf

EXPOSE 3306
CMD ["mysqld_safe"]