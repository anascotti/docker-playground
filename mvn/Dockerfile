FROM java8u45_centos7

WORKDIR /opt

# install mvn
RUN wget "http://apache.mirrors.spacedump.net/maven/maven-3/3.3.9/binaries/apache-maven-3.3.9-bin.tar.gz"
RUN ["tar", "xzf", "apache-maven-3.3.9-bin.tar.gz"]

ENV M2_HOME=/opt/apache-maven-3.3.9
ENV M2=$M2_HOME/bin
ENV PATH=$M2:$PATH

ADD settings.xml /opt/apache-maven-3.3.9/conf/settings.xml

CMD [ "mvn", "--version" ]
