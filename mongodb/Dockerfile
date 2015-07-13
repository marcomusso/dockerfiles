FROM centos:6
MAINTAINER Marco Musso <github@marcomusso.it>

RUN mkdir /data

#WARNING: The default /etc/mongod.conf configuration file supplied by the 3.0 series packages has bind_ip set to 127.0.0.1 by default.
#COPY mongodb-org-3.0.repo /etc/yum.repos.d/mongodb-org-3.0.repo 
COPY mongodb-org-2.6.repo /etc/yum.repos.d/mongodb-org-2.6.repo 

RUN yum install -y \
  mongodb-org-2.6.6 \
  mongodb-org-server-2.6.6 \
  mongodb-org-shell-2.6.6 \
  mongodb-org-mongos-2.6.6 \
  mongodb-org-tools-2.6.6

VOLUME /data

CMD mongod --logpath /data/mongod.log --httpinterface --rest

EXPOSE 27017 28017
