# Dockerfile for Salt Master
Inspired from soon/salt-minion
There are two tags for Ubuntu Trusty (ubuntu-14.04) and CentOS 7 (Centos7)

# Installation
Following https://github.com/saltstack/salt-bootstrap/tree/v2014.10.30

# Configuring Salt Minion
Default LOG_LEVEL is "error", you can change to "info" for more verbose

## Connecting Salt Minion to Salt Master
``
docker run -d --name salt_minion_01 -e LOG_LEVEL=info --link saltmaster1:salt chrisduong/salt-minion:ubuntu-14.04
``

``
# Notes
At the moment, -N option does not work as expected as we installed from git.
Create Minion conf volume: /etc/salt/minion.d




