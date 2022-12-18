FROM ubuntu:20.04

LABEL maintainer=Eleven

MAINTAINER author "Eleven"

ENV DEBIAN_FRONTEND=noninteractive

WORKDIR /root/

ADD .vimrc /root/.vimrc

ARG Requirement='python3.8 python3-pip unzip vim wget net-tools curl iputils-ping traceroute' 
# ARG Delment='wget unzip net-tools curl vim'

RUN	apt update && apt install -y $Requirement \
	&& ln -s /usr/bin/python3.8 /usr/bin/python

# RUN 	pystun3	
RUN 	rm -rf /var/lib/apt/lists/* && apt clean

RUN     sed -i s@/archive.ubuntu.com/@/mirrors.tuna.tsinghua.edu.cn/@g /etc/apt/sources.list \
	&& sed -i s@/security.ubuntu.com/@/mirrors.tuna.tsinghua.edu.cn/@g /etc/apt/sources.list

RUN	echo "alias myip=\"echo 'Direct ip' ;curl -s cip.cc | sed '4,100d' ; echo ''; echo 'Proxy ip' ; curl -s icanhazip.com; echo ''; echo 'ipv6 addr' ; curl -s 6.ipw.cn ; echo ''\"" >> /etc/bash.bashrc

RUN apt update
