FROM docker.io/debian:jessie
MAINTAINER Claudio Borges <cbsfilho@gmail.com>
RUN sed -i 's/$/ contrib non-free/g' /etc/apt/sources.list
RUN echo "deb http://deb.debian.org/debian jessie-backports main contrib non-free" > /etc/apt/sources.list.d/backports.list
RUN apt-get update
RUN apt-get install -y ftp git-core dialog dh-make build-essential \
devscripts wget autotools-dev dh-systemd libluajit-5.1-dev \
libexpat-dev libgd2-dev libgeoip-dev libmhash-dev \
libpam0g-dev libpcre3-dev libperl-dev libssl-dev libxslt1-dev \
libmaxminddb-dev libmaxminddb0
WORKDIR /root
RUN git clone https://github.com/but3k4/nginx-package.git
