FROM debian:jessie

MAINTAINER shrimpza

# Install Java.
RUN apt-get update && apt-get -y install wget openjdk-7-jre-headless
RUN \
  wget -O /tmp/sflowtrend.deb http://www.inmon.com/products/sFlowTrend/downloads/sFlowTrend-linux-6_2.deb && \
  dpkg -i /tmp/sflowtrend.deb && \
  rm -f /tmp/sflowtrend
RUN rm -rf /var/lib/apt/lists/*

# Define default command.
CMD ["/usr/local/bin/sflowtrend-server", "run"]
