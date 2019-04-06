FROM centos:latest
MAINTAINER Ian Merrick <MerrickI@Cardiff.ac.uk>

##############################################################
# Software:             -
# Software Version:     -
# Software Website:     -
# Description:          MongoDB-server on Centos7
##############################################################

RUN mkdir -p /data/db && \
    yum update -y && \ 
    yum install -y epel-release && \
    yum install -y \
                   mongodb \
                   mongodb-server && \
    yum clean all && \
    rm -rf /var/cache/yum 

COPY mongo_entrypoint.sh /usr/local/bin/mongo_entrypoint.sh

ENTRYPOINT ["/usr/local/bin/mongo_entrypoint.sh"]
