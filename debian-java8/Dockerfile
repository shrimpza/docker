#
# OpenJDK Java 8 JRE on Debian Dockerfile
#

# Pull base image.
FROM debian:sid

# Install Java.
RUN \
  apt-get update && \
  apt-get install -y openjdk-8-jre wget unzip && \
  rm -rf /var/lib/apt/lists/*

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64

# Define default command.
CMD ["bash"]
