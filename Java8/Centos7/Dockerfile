FROM centos:7

MAINTAINER Kartik <kartik.punde.13@gmail.com>
USER root

#Package Installation
RUN yum update -y && \
    yum install -y openssh-server \
                   passwd \
                   bash-completion \
                   java-1.8.0-openjdk \
                   java-1.8.0-openjdk-devel --nogpgcheck \
                   bind-utils \
                   wget && \
    yum clean all

RUN echo "root" | passwd remote_user --stdin

ENV JAVA_HOME /usr/lib/jvm/java-1.8.0-openjdk/

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["bash"]
