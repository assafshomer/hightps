FROM nimmis/java
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get -y update
RUN apt-get -y --force-yes install python-software-properties
RUN apt-get -y --force-yes install software-properties-common
RUN add-apt-repository ppa:webupd8team/java
RUN apt-get -y update
RUN apt-get install -y --force-yes git maven
RUN echo debconf shared/accepted-oracle-license-v1-1 select true | \
  sudo debconf-set-selections
RUN echo debconf shared/accepted-oracle-license-v1-1 seen true | \
  sudo debconf-set-selections  
RUN apt-get install -y --force-yes oracle-java8-installer 
RUN apt-get install -y --force-yes oracle-java8-unlimited-jce-policy protobuf-compiler procmail