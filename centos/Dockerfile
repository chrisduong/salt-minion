# Dockerfile for SaltStack  Minion

FROM ubuntu:14.04
MAINTAINER Chris Duong <chris.duong83@gmail.com>

# Install dependencies
RUN apt-get update -qq && \
  apt-get install -y curl 
RUN curl -L https://bootstrap.saltstack.com | sh -s -- -M -N -X git v2014.7.0 || true
# Clean up
RUN apt-get clean; \
  rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/*

# Volumes
VOLUME ['/etc/salt/minion.d']

# Add Run File
ADD run.sh /usr/local/bin/run.sh
RUN chmod +x /usr/local/bin/run.sh


CMD "/usr/local/bin/run.sh"