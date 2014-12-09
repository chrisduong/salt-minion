# Dockerfile for SaltStack  Minion

FROM centos:centos7
MAINTAINER Chris Duong <chris.duong83@gmail.com>

# Install dependencies
RUN yum clean all; \
      yum install curl -y 
RUN curl -L https://bootstrap.saltstack.com | sh -s -- -M -N -X git v2014.7.0 || true

# Volumes
VOLUME ['/etc/salt/minion.d']

# Add Run File
ADD run.sh /usr/local/bin/run.sh
RUN chmod +x /usr/local/bin/run.sh


CMD "/usr/local/bin/run.sh"