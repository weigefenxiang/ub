FROM ubuntu:20.04

LABEL maintainer=Eleven

MAINTAINER author "Eleven"

ENV DEBIAN_FRONTEND=noninteractive

WORKDIR /root/

ARG Requirement='python3.8 python3-pip wget unzip net-tools curl vim' 
# ARG Delment='wget unzip net-tools curl vim'

RUN	apt update && apt install -y $Requirement \
	&& ln -s /usr/bin/python3.8 /usr/bin/python

# RUN 	pystun3	
RUN 	rm -rf /var/lib/apt/lists/* && apt clean
	


RUN     sed -i s@/archive.ubuntu.com/@/mirrors.tuna.tsinghua.edu.cn/@g /etc/apt/sources.list \
	&& sed -i s@/security.ubuntu.com/@/mirrors.tuna.tsinghua.edu.cn/@g /etc/apt/sources.list

RUN apt update
