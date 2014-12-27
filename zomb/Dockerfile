#
# ZOMB
#

# Pull base image.
FROM debian:java8

MAINTAINER shrimpza

# Install requirements
RUN \
  mkdir /opt/zomb && \
  wget -O /tmp/zomb.zip https://drone.io/github.com/shrimpza/zomb/files/dist/zomb.zip && \
  unzip /tmp/zomb.zip -d /opt/zomb/

VOLUME ["/var/zomb/apps"]

# Define working directory.
WORKDIR /opt/zomb

# API Ports
EXPOSE 8080 8081

# Define default command.
ENTRYPOINT ["java","-jar","/opt/zomb/zomb.jar","8080","8081","/var/zomb/apps"]

