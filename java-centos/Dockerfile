FROM centos:7

RUN yes | yum -y install wget

WORKDIR /opt

RUN wget --no-cookies --no-check-certificate --header \
    "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" \
    "http://download.oracle.com/otn-pub/java/jdk/8u45-b14/jdk-8u45-linux-x64.tar.gz"
RUN ["tar", "xzf", "jdk-8u45-linux-x64.tar.gz"]
RUN alternatives --install /usr/bin/java java /opt/jdk1.8.0_45/bin/java 1

ENV JAVA_HOME="/opt/jdk1.8.0_45"
ENV PATH=$PATH:$JAVA_HOME/bin

# ENTRYPOINT [ "java" ]
CMD [ "java", "-version" ]