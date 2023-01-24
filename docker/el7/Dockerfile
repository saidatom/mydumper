# Using Debian's GCC image, pinned to latest LTS, scheduled to EOL on Jun'26.
FROM centos:7 as builder

ARG DEBIAN_FRONTEND=noninteractive

# Package 'lsb-release' is required by 'percona-release' package.
RUN \
  yum -y install epel-release && \
  yum -y install wget curl && \
  yum -y install cmake gcc-c++ git make glib2-devel zlib-devel pcre-devel openssl-devel libzstd-devel sudo 

RUN \
  yum -y install  https://repo.percona.com/yum/percona-release-latest.noarch.rpm

RUN \
  wget https://r.mariadb.com/downloads/mariadb_repo_setup -O /tmp/mariadb_repo_setup

